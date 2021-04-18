---
title: Offloaded-Datenübertragungen
description: Offloaded-Datenübertragungen
ms.assetid: 91EBE6D6-2DA7-48DA-AEB7-3FAFCA8341F5
keywords:
- ODX
- Auslagerung kopieren
- Auslagerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1057ed27347fefc7ebc6a171eb7273da4341b024
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "106337473"
---
# <a name="offloaded-data-transfers"></a><span data-ttu-id="49c91-106">Offloaded-Datenübertragungen</span><span class="sxs-lookup"><span data-stu-id="49c91-106">Offloaded data transfers</span></span>

## <a name="platforms"></a><span data-ttu-id="49c91-107">Plattformen</span><span class="sxs-lookup"><span data-stu-id="49c91-107">Platforms</span></span>

<span data-ttu-id="49c91-108">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="49c91-108">**Clients** – Windows 8</span></span>  
<span data-ttu-id="49c91-109">**Server** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="49c91-109">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="49c91-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49c91-110">Description</span></span>

<span data-ttu-id="49c91-111">Um die Verschiebung der Speicherdaten voranzutreiben, hat Microsoft eine neue Datenübertragungstechnologie – offloaded Data Transfer (ODX) entwickelt.</span><span class="sxs-lookup"><span data-stu-id="49c91-111">To advance the storage data movement, Microsoft has developed a new data transfer technology – offloaded data transfer (ODX).</span></span> <span data-ttu-id="49c91-112">Anstelle von gepufferten Lese-und gepufferten Schreibvorgängen startet Windows ODX den Kopiervorgang mit einer Auslagerungs Überprüfung und ruft ein Token ab, das die Daten aus dem Speichergerät darstellt. Anschließend wird ein Auslagerungs Schreibbefehl mit dem Token verwendet, um die Daten Verschiebung vom Quell Datenträger zum Ziel Datenträger anzufordern.</span><span class="sxs-lookup"><span data-stu-id="49c91-112">Instead of using buffered read and buffered write operations, Windows ODX starts the copy operation with an offload read and retrieves a token representing the data from the storage device, then uses an offload write command with the token to request data movement from the source disk to the destination disk.</span></span> <span data-ttu-id="49c91-113">Der Kopier-Manager der Speichergeräte führt die Daten Verschiebung gemäß dem Token aus.</span><span class="sxs-lookup"><span data-stu-id="49c91-113">The copy manager of the storage devices performs the data movement according to the token.</span></span> <span data-ttu-id="49c91-114">In Windows 8 können der IT-Manager und der Speicher Administrator die Windows ODX-Funktion verwenden, um mit dem Speichergerät zu interagieren, um große Dateien oder Daten über das Hochgeschwindigkeitsspeicher Netzwerk zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="49c91-114">In the Windows 8, the IT manager and storage administrator are able to use the Windows ODX feature to interact with the storage device to move large files or data through the high-speed storage network.</span></span> <span data-ttu-id="49c91-115">Windows ODX reduziert den Netzwerk Datenverkehr für Client Server und die CPU-Zeit Auslastung bei großen Datenübertragungen erheblich, da sich alle Daten Verschiebungen im Back-End-Speicher Netzwerk befinden.</span><span class="sxs-lookup"><span data-stu-id="49c91-115">Windows ODX will significantly reduce client-server network traffic and CPU time usage during large data transfers because all the data movement is at the backend storage network.</span></span> <span data-ttu-id="49c91-116">ODX kann bei der Bereitstellung virtueller Maschinen, bei der umfangreichen Datenmigration und bei der Unterstützung von mehrstufigen Speichergeräten verwendet werden. Zudem können die Kosten der physischen Hardware Bereitstellung durch die ODX-und Thin Bereitstellung-Speicher Features gesenkt werden.</span><span class="sxs-lookup"><span data-stu-id="49c91-116">ODX can be used in virtual machine deployment, massive data migration, and tiered storage device support, and can lower the cost of physical hardware deployment through the ODX and thin provisioning storage features.</span></span>

> [!Note]  
> <span data-ttu-id="49c91-117">Diese Funktion kann nur auf Speichergeräten mit der Implementierung der SPC4-und SBC3-Spezifikation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49c91-117">This feature will only work on storage devices with SPC4 and SBC3 specification implementation.</span></span>

 

## <a name="functional-details"></a><span data-ttu-id="49c91-118">Funktions Details</span><span class="sxs-lookup"><span data-stu-id="49c91-118">Functional details</span></span>

-   <span data-ttu-id="49c91-119">Das Windows ODX-Feature ist in die Kopier-Engine des Windows-Betriebssystems eingebettet. während der Speicherenumeration fragt Windows die ODX-Funktion des Speichergeräts ab.</span><span class="sxs-lookup"><span data-stu-id="49c91-119">The Windows ODX feature is embedded in the copy engine of the Windows operating system; during storage enumeration, Windows will query the ODX capability of the storage device</span></span>
-   <span data-ttu-id="49c91-120">Kopieren des Quell Speichergeräts und Kopieren des Zielspeicher Geräts sollten unter dem gleichen Kopier-Manager für die Unterstützung der Kopier Auslagerung verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="49c91-120">Copy source storage device and copy destination storage device should be managed under the same copy manager for copy offload support</span></span>
-   <span data-ttu-id="49c91-121">Wenn ein Kopiervorgang fehlschlägt, muss der Kopier-Manager des Speichergeräts die richtigen zusätzlichen Sense-Daten für die Fehlerbehandlung der APP zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="49c91-121">If a copy offload operation fails, the storage device’s copy manager must return the proper additional sense data for the apps’ error handling</span></span>
-   <span data-ttu-id="49c91-122">Das Windows-Kopiermodul greift auf den herkömmlichen Kopiervorgang zurück, wenn der Kopiervorgang nicht ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="49c91-122">The Windows copy engine will fall back to the traditional copy operation if the copy offload operation fails</span></span>

## <a name="using-odx"></a><span data-ttu-id="49c91-123">Verwenden von ODX</span><span class="sxs-lookup"><span data-stu-id="49c91-123">Using ODX</span></span>

-   <span data-ttu-id="49c91-124">Die Datenübertragungs-app muss sicherstellen, dass sowohl Quell-als auch Kopier Ziel-LUN ODX-fähig sind, bevor die ODX-API-Routinen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="49c91-124">The data transfer app must ensure both copy source LUN and copy destination LUN are ODX capable before calling the ODX API routines</span></span>
-   <span data-ttu-id="49c91-125">In Windows-Explorer können Benutzer "Drag" oder "Kopieren und Einfügen" verwenden, um die Kopier Auslagerung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="49c91-125">In Windows explorer, users could use “drag” or “copy and paste” to perform copy offload</span></span>
-   <span data-ttu-id="49c91-126">Wenn die Quell-LUN und die Ziel-LUN mit dem Dateisystem bereitgestellt werden, muss die app nur FSCTL \_ Offload \_ Lesen und FSCTL \_ Offload- \_ Schreibvorgänge für die Datenübertragung von der Quell-LUN an die Ziel-LUN ausführen.</span><span class="sxs-lookup"><span data-stu-id="49c91-126">When the source LUN and destination LUN are mounted with the file system, the app must only call FSCTL\_Offload\_Read and FSCTL\_Offload\_Write to perform data transfer from the source LUN to the destination LUN</span></span>
-   <span data-ttu-id="49c91-127">Wenn ein Kopiervorgang fehlschlägt, muss der Kopier-Manager des Speichergeräts die richtigen zusätzlichen Sense-Daten für die Fehlerbehandlung von apps zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="49c91-127">If a copy offload operation fails, the storage device’s copy manager must return the proper additional sense data for apps’ error handling</span></span>
-   <span data-ttu-id="49c91-128">Wenn die LUN der Quell-oder Ziel-LUN nicht mit dem Dateisystem bereitgestellt und gesperrt ist, muss die APP IOCTL \_ Storage- \_ \_ Daten \_ Satz \_ Attribute mit devicedsmaction \_ offloadread oder devicedsmaction \_ offloadwrite-Aktion zum Ausführen der Kopier Auslagerung abrufen.</span><span class="sxs-lookup"><span data-stu-id="49c91-128">When the source LUN or destination LUN is not mounted with the file system and locked, the app must call IOCTL\_STORAGE\_MANAGE\_DATA\_SET\_ATTRIBUTES with DeviceDsmAction\_OffloadRead or DeviceDsmAction\_OffloadWrite action to perform copy offload</span></span>
-   <span data-ttu-id="49c91-129">Speicher Verwaltungs-Apps können eine SCSI- \_ Pass- \_ through-API verwenden, um offloaded-Datenübertragungen auszuführen, wenn sowohl die Quell-als auch die Ziel-LUNs nicht in einem Dateisystem eingebunden</span><span class="sxs-lookup"><span data-stu-id="49c91-129">Storage management apps may use SCSI\_PASS\_THROUGH API to perform offloaded data transfers when both source and destination LUNs are not mounted with any file system and locked</span></span>

## <a name="tests"></a><span data-ttu-id="49c91-130">Tests</span><span class="sxs-lookup"><span data-stu-id="49c91-130">Tests</span></span>

-   <span data-ttu-id="49c91-131">Überprüfen Sie die Windows ODX-Zertifizierung des Speicherarrays, um eine robuste Benutzer Leistung sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="49c91-131">To ensure a robust user experience, verify the Windows ODX certification of the storage array</span></span>
-   <span data-ttu-id="49c91-132">Das Speichergerät muss die Zertifizierungsanforderungen für Windows offloaded Data Transfers (verwendet als Logo) erfüllen, um die ODX-Funktion zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="49c91-132">The storage device must comply with Windows Offloaded Data Transfers certification (used to be Logo) requirements to support ODX feature</span></span>
-   <span data-ttu-id="49c91-133">Verwenden Sie das Hardware zertifizierungskit für Windows offloaded Data Transfers, um die Unterstützung von ODX-Features für die Speichergeräte</span><span class="sxs-lookup"><span data-stu-id="49c91-133">Use the Windows Offloaded Data Transfers Hardware Certification Kit to verify the ODX feature support of the storage devices</span></span>

## <a name="resources"></a><span data-ttu-id="49c91-134">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="49c91-134">Resources</span></span>

-   <span data-ttu-id="49c91-135">T10 xcopy Lite spec (11-059r8)</span><span class="sxs-lookup"><span data-stu-id="49c91-135">T10 XCOPY Lite Spec (11-059r8)</span></span>
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf)
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf)
-   [<span data-ttu-id="49c91-136">Hardware-Dashboard-Dienste</span><span class="sxs-lookup"><span data-stu-id="49c91-136">Hardware Dashboard Services</span></span>](/windows-hardware/drivers/dashboard/)
-   [<span data-ttu-id="49c91-137">SCSI- \_ Durchlauf \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="49c91-137">SCSI\_PASS\_THROUGH Structure</span></span>](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_scsi_pass_through)

 

 