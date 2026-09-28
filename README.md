# Digital-power-factor-meter
# Digital Power Factor Meter

print("==============================")
print("     DIGITAL POWER FACTOR METER")
print("==============================")

voltage = float(input("Enter voltage (V): "))
current = float(input("Enter current (A): "))
real_power = float(input("Enter real power (W): "))

# Calculate apparent power
apparent_power = voltage * current

# Calculate power factor
if apparent_power > 0:
    power_factor = real_power / apparent_power
else:
    power_factor = 0

print("\n------------------------------")
print("Apparent Power:", round(apparent_power, 2), "VA")
print("Power Factor :", round(power_factor, 2))
print("------------------------------")

if power_factor >= 0.95:
    print("🟢 GOOD POWER FACTOR")
elif power_factor >= 0.80:
    print("🟡 ACCEPTABLE POWER FACTOR")
else:
    print("🔴 LOW POWER FACTOR")
