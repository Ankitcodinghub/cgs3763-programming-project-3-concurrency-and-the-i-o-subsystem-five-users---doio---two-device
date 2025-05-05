# cgs3763-programming-project-3-concurrency-and-the-i-o-subsystem-five-users---doio---two-device
**TO GET THIS SOLUTION VISIT:** [CGS3763: Programming project #3 (Concurrency and the I/O subsystem) (Five Users – DOIO – Two Device ](https://www.ankitcodinghub.com/product/cgs3763-programming-project-3-concurrency-and-the-i-o-subsystem-five-users-doio-two-device-driver-two-disk/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;9278&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CGS3763: Programming project #3 (Concurrency and the I\/O subsystem)  (Five Users - DOIO – Two Device driver – Two Disk)&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
1.- In this assignment you will &nbsp;implement a simulation of the interaction of user programs with the OS to execute an I/O operation on two different devices.

<strong>User programs:</strong>

User programs will communicate with DOIO (OS) to request an I/O operation. (This will simulate a system call)

User programs will give to DOIO three parameters: User id, device number (dev is a random number in the range 1 and 2 that represents device one or device two) and an address (addr is a random number in the range 1 and 200.) (addr is an integer that represents a track number in the hard drive).

User programs will pass the parameters to DOIO through three buffers of size one each (bufid, bufdev, and bufaddr).

Once the parameters are stored in the buffers, user programs executes a P(request served) operation to wait for the completion of the I/O operation. You will need a semaphore array Request served[5].

There will be five users running concurrently and each will execute 5 I/O operations.

<strong>DOIO:</strong>

DOIO will collect and id, device(dev), &nbsp;and address(addr) from bufid, bufdev, and bufaddr to assemble the IORB.

DOIO will check on device number to decide which one of the two devices will get the IORB.

Once the device has been selected, DOIO will store the IORB (id and addr) into the two buffers that represent the IORQ (iorqid and iorqaddr) of the selected device. Notice that you need separate buffers (one for each device).

<strong>&nbsp;</strong>

<strong>&nbsp;</strong>

<strong>Device drivers (1 and 2): </strong>

Device drivers will collect an IORB (pair id and addr) from iorqid and iorqaddr and then &nbsp;initiates the physical I/O operation on the hard drive it controls and wait for the I/O operation to be completed: P(operation complete).

The device driver initiate the physical I/O operation by storing addr into a buffer of length one. The buffer name is “pio” (physical I/O).

When the I/O operation completes a signal is received, the driver will identify the user that issued the I/O request using the id, and will signal the semaphore “request served” associated to the user.

&nbsp;

<strong>Disk (1 and 2):</strong>

The disk processes simulates the access to a track in the hard drive.

The Disk process gets the addr from pio &nbsp;&nbsp;and stores it in a variable called “seek” and iterates in a dummy loop from 1 to “seek”.

Once out of the loop, disk will execute a V on the semaphore “operation complete”

<ol>
<li>Define all semaphores that you need according to the number of buffers used.</li>
<li>Each user will make 5 system calls to initiate I/O operations</li>
<li>DOIO will create 25 IORB</li>
<li>The sum of the I/O operations executed by drivers must add up 25. You will need a shared variable to control the total number of I/O operations because it is not known before hand the numbers of I/O operations initiated by each drive..</li>
</ol>
<strong>&nbsp;</strong>

<strong>Project Direction </strong>

You will write the program C– based on the <strong>BACI</strong> interpreter that you used in programming project 1.

&nbsp;

&nbsp;

<strong>Test your solution</strong>

&nbsp;

You must run and test your solution and &nbsp;&nbsp;comment on the results emitted.

<strong>&nbsp;</strong>
