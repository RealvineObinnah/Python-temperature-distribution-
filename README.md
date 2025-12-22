# Python-temperature-distribution-
The code to add inputs to the program to solve engineering problems pertaining temperature distribution across a plain wall

# Program to collect thermal inputs from user

print("=== Thermal Input Collector ===")

# Ask for inputs
thickness = float(input("Enter thickness of wall (x) in m : "))
initial_time = float(input("Enter initial time (t0) in secs : "))
final_time = float(input("Enter final time (t) in secs : "))
thermal_diffusivity = float(input("Enter thermal diffusivity (α) in m^2 / secs : "))
initial_temperature = float(input("Enter initial temperature (Ti) in ⁰C : "))
final_temperature = float(input("Enter final temperature (Tf) in ⁰C : "))
fourier_number = float(input("Enter Fourier number (Fo): "))

# Display the collected inputs
print("\n=== INPUT SUMMARY ===")
print(f"Thickness of wall (x): {thickness} m")
print(f"Initial time (t0): {initial_time} secs")
print(f"Final time (t): {final_time} secs") 
print(f"Thermal diffusivity (α): {thermal_diffusivity} m^2 / secs")
print(f"Initial temperature (Ti): {initial_temperature} ⁰C")
print(f"Final temperature (Tf): {final_temperature} ⁰C")
print(f"Fourier number (Fo): {fourier_number}"),

# Calculate change in thickness
delta_x = thickness / 5

# Calculate change in time (Δt)
delta_t = (fourier_number * (delta_x ** 2)) / thermal_diffusivity

print(f"Change in thickness (Δx = x/5): {delta_x} m")

# Display calculated change in time
print(f"\nCalculated change in time (Δt) = Fo * (Δx²) / α : {delta_t} s")

time_in_hours = delta_t / 60 /60

print(f"Time in hours : {time_in_hours} hr")
