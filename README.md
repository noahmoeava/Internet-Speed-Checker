<h1>Internet Speed Checker</h1>

<h2>Description</h2>
This code uses the speedtest module to check the internet speed of a device. First, the speedtest module is imported and an instance of the Speedtest class is created. Then, the best server to test the speed is chosen by calling the get_best_server() method. The download and upload speeds are tested using the download() and upload() methods and the results are stored in variables. The speeds are then converted to Mbps for readability and the results are printed using the print() function.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Python</b> 

<h2>Environments Used </h2>

- <b>Windows 11</b>

<h2>Program Walkthrough:</h2>

<b>Step 1: Import the necessary modules.</b>

```python
import speedtest
```
<b>Step 2: Create an instance of the Speedtest class.</b>

```python
st = speedtest.Speedtest()
```

<b>Step 3: Choose the closest server to test the speed.</b>

```python
st.get_best_server()
```
<b>Step 4: Test the download speed.</b>

```python
download_speed = st.download()
```
<b>Step 5: Test the upload speed.</b>

```python
upload_speed = st.upload()
```
<b>Step 6: Convert the speeds to a readable format.</b>

```python
download_speed_mbps = download_speed / 10**6
upload_speed_mbps = upload_speed / 10**6
```
<b>Step 7: Print the results.</b>

```python
print("Download speed: {:.2f} Mbps".format(download_speed_mbps))
print("Upload speed: {:.2f} Mbps".format(upload_speed_mbps))
```

<b> The final result should look like this:</b>
```python
import speedtest

st = speedtest.Speedtest()
st.get_best_server()
download_speed = st.download()
upload_speed = st.upload()
download_speed_mbps = download_speed / 10**6
upload_speed_mbps = upload_speed / 10**6

print("Download speed: {:.2f} Mbps".format(download_speed_mbps))
print("Upload speed: {:.2f} Mbps".format(upload_speed_mbps))
```
