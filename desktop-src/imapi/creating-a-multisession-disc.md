---
title: Erstellen einer Multi-Session-CD
ms.assetid: 327304c4-fdb9-47c6-9b19-49100b933590
description: Weitere Informationen finden Sie unter Erstellen eines mehrteiligen Sitzungs Datenträgers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2db17b8a16f46797fc0f6de2bf94850e3b3039bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485435"
---
# <a name="creating-a-multisession-disc"></a><span data-ttu-id="1b983-103">Erstellen einer Multi-Session-CD</span><span class="sxs-lookup"><span data-stu-id="1b983-103">Creating a Multisession Disc</span></span>

<span data-ttu-id="1b983-104">Die [Image-Mastering-API](about-imapi.md) (IMAPI) unterstützt das Hinzufügen und Entfernen von Dateien zu den folgenden mehr sitzungsdatenträger:</span><span class="sxs-lookup"><span data-stu-id="1b983-104">The [Image Mastering API](about-imapi.md) (IMAPI) supports the addition and removal of files to, or from, the following multisession disc types:</span></span>

-   <span data-ttu-id="1b983-105">CD-R/CD-RW</span><span class="sxs-lookup"><span data-stu-id="1b983-105">CD-R/CD-RW</span></span>
-   <span data-ttu-id="1b983-106">Single-Layer DVD + r/DVD-r</span><span class="sxs-lookup"><span data-stu-id="1b983-106">Single-Layer DVD+R/DVD-R</span></span>
-   <span data-ttu-id="1b983-107">Dual-Layer-DVD + R</span><span class="sxs-lookup"><span data-stu-id="1b983-107">DVD+R Dual Layer</span></span>
-   <span data-ttu-id="1b983-108">BD-R</span><span class="sxs-lookup"><span data-stu-id="1b983-108">BD-R</span></span>
-   <span data-ttu-id="1b983-109">DVD-RW/DVD + RW (**nur Windows 7**)</span><span class="sxs-lookup"><span data-stu-id="1b983-109">DVD-RW/DVD+RW (**Windows 7 Only**)</span></span>
-   <span data-ttu-id="1b983-110">DVD-RAM (**nur Windows 7**)</span><span class="sxs-lookup"><span data-stu-id="1b983-110">DVD-RAM (**Windows 7 Only**)</span></span>
-   <span data-ttu-id="1b983-111">BD-RE (**nur Windows 7**)</span><span class="sxs-lookup"><span data-stu-id="1b983-111">BD-RE (**Windows 7 Only**)</span></span>

<span data-ttu-id="1b983-112">Die Erstellung einer mehr sitzenden CD mithilfe von IMAPI besteht aus den folgenden Schritten.</span><span class="sxs-lookup"><span data-stu-id="1b983-112">Creation of a multisession disc using IMAPI consists of the following steps.</span></span> <span data-ttu-id="1b983-113">Jeder dieser dokumentierten Schritte enthält den relevanten Teil des kompletten Visual Basic Skript Beispiels, das im letzten Abschnitt bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1b983-113">Each of these documented steps contains the relevant portion of the complete Visual Basic script example provided in the final section.</span></span>

## <a name="initializing-the-disc-recorder"></a><span data-ttu-id="1b983-114">Der Disc Recorder wird initialisiert.</span><span class="sxs-lookup"><span data-stu-id="1b983-114">Initializing the Disc Recorder</span></span>

<span data-ttu-id="1b983-115">Vor der Geräte Initialisierung stellt das **MsftDiscMaster2** -Objekt eine Enumeration der optischen Geräte auf dem System bereit.</span><span class="sxs-lookup"><span data-stu-id="1b983-115">Prior to device initialization, the **MsftDiscMaster2** object provides an enumeration of the optical devices on the system.</span></span> <span data-ttu-id="1b983-116">Die [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) -Schnittstelle ermöglicht den Zugriff auf diese Geräte Enumeration, um den Speicherort des entsprechenden Aufzeichnungs Geräts zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="1b983-116">The [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) interface provides access to this device enumeration to facilitate the location of the appropriate recording device.</span></span> <span data-ttu-id="1b983-117">Das **MsftDiscMaster2** -Objekt stellt auch Ereignis Benachrichtigungen bereit, wenn optische Geräte einem Computer hinzugefügt oder daraus entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="1b983-117">The **MsftDiscMaster2** object also provides event notifications when optical devices are added to or removed from a machine.</span></span>

<span data-ttu-id="1b983-118">Nachdem Sie einen optischen Recorder gefunden und die ihm zugewiesene ID abgerufen haben, erstellen Sie ein neues **MsftDiscMaster2** -Objekt, und initialisieren Sie den Recorder mithilfe der spezifischen Geräte-ID.</span><span class="sxs-lookup"><span data-stu-id="1b983-118">After locating an optical recorder and retrieving the ID assigned to it, create a new **MsftDiscMaster2** object and initialize the recorder using the specific device ID.</span></span>

<span data-ttu-id="1b983-119">Die [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) -Schnittstelle ermöglicht den Zugriff auf grundlegende Geräteinformationen, z. b. Hersteller-ID, Produkt-ID, Produkt Revision sowie Methoden zum Auswerfen von Medien oder Schließen der Info Leiste.</span><span class="sxs-lookup"><span data-stu-id="1b983-119">The [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) interface provides access to basic device information such as vendor ID, product ID, product revision, as well as the methods to eject media or close the tray.</span></span>

> [!Note]  
> <span data-ttu-id="1b983-120">Die im folgenden Beispiel deklarierten zusätzlichen Konstanten und Dimensionen werden später in dem gesamten Beispielskript im letzten Abschnitt dieses Dokuments verwendet.</span><span class="sxs-lookup"><span data-stu-id="1b983-120">The additional constants and dimensions declared in the following sample are used later in the complete sample script located in the final section of this document.</span></span> <span data-ttu-id="1b983-121">Diese Elemente sind für die Initialisierung eines Disk Recorder nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1b983-121">These elements are not required for the act of initializing a disc recorder.</span></span>

 


```VB
' **_ CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to add
    Dim Stream               ' Data stream for burning device
    
    Index = 0                ' First drive on the system
    Path = "G:\BurnDir"      ' Files to add to the disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim DiscMaster
    Set DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder2 object for the specified burning device.
    Dim UniqueId
    set Recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    UniqueId = DiscMaster.Item(Index)
    Recorder.InitializeDiscRecorder(UniqueId)
```



## <a name="creating-a-data-writer"></a><span data-ttu-id="1b983-122">Erstellen eines Daten Writers</span><span class="sxs-lookup"><span data-stu-id="1b983-122">Creating a Data Writer</span></span>

<span data-ttu-id="1b983-123">Das _ \*MsftDiscFormat2Data\*\*-Objekt stellt die Schreibmethode, deren Eigenschaften und die medienspezifischen Eigenschaften bereit.</span><span class="sxs-lookup"><span data-stu-id="1b983-123">The _ *MsftDiscFormat2Data*\* object provides the writing method, its properties, as well as the media-specific properties.</span></span> <span data-ttu-id="1b983-124">Die [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) -Schnittstelle ermöglicht den Zugriff auf dieses Objekt.</span><span class="sxs-lookup"><span data-stu-id="1b983-124">The [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) interface provides access to this object.</span></span>

<span data-ttu-id="1b983-125">Der Disk Recorder bindet mithilfe der [**IDiscFormat2Data::p UT \_ Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) -Eigenschaft an den Format Schreiber.</span><span class="sxs-lookup"><span data-stu-id="1b983-125">The disc recorder binds to the format writer using the [**IDiscFormat2Data::put\_Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) property.</span></span> <span data-ttu-id="1b983-126">Nachdem die Aufzeichnung an den Format Schreiber gebunden ist, können Medien-und Schreib spezifische Eigenschaften Abfragen ausgeführt werden, bevor das Ergebnisbild mithilfe der [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) -Methode auf die Festplatte geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="1b983-126">After the recorder is bound to the format writer, media and write-specific property queries can be performed prior to writing the result image to disc using the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method.</span></span>

> [!Note]  
> <span data-ttu-id="1b983-127">Die im Beispielcode unten angegebene Zeichenfolge für den Client Namen sollte entsprechend für die jeweilige Anwendung angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="1b983-127">The client name string specified in the sample code below should be adjusted as appropriate for the specific application.</span></span>

 


```VB
    ' Create a DiscFormat2Data object and set the recorder
    Dim DataWriter
    Set DataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    DataWriter.Recorder = Recorder
    DataWriter.ClientName = "IMAPIv2 TEST"
```



## <a name="creating-the-file-system-object"></a><span data-ttu-id="1b983-128">Erstellen des Datei System Objekts</span><span class="sxs-lookup"><span data-stu-id="1b983-128">Creating the File System Object</span></span>

<span data-ttu-id="1b983-129">Damit eine neue Sitzung aufgezeichnet werden kann, muss zuerst ein Burn-Image generiert werden.</span><span class="sxs-lookup"><span data-stu-id="1b983-129">In order to record a new session, a burn image must be generated for it first.</span></span> <span data-ttu-id="1b983-130">Ein Burn-Image für die Formate " **ISO9660**", " **Joliet** " und " **UDF** " besteht aus Dateisystemen einzelner Dateien und Verzeichnisse.</span><span class="sxs-lookup"><span data-stu-id="1b983-130">A burn image for **ISO9660**, **Joliet** and **UDF** formats consist of file systems of individual files and directories.</span></span> <span data-ttu-id="1b983-131">Das **msftfilesystemmage** -Objekt ist das Dateisystem Objekt, das die Dateien und Verzeichnisse enthält, die auf dem optischen Medium platziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1b983-131">The **MsftFileSystemImage** object is the file system object that contains the files and directories to be placed on the optical media.</span></span> <span data-ttu-id="1b983-132">Die [**ifilesystemmage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) -Schnittstelle ermöglicht den Zugriff auf das Dateisystem Objekt und die Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="1b983-132">The [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) interface provides access to the file system object and settings.</span></span>


```VB
    ' Create a new file system image object
    Dim FSI
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
```



## <a name="importing-a-file-system"></a><span data-ttu-id="1b983-133">Importieren eines Dateisystems</span><span class="sxs-lookup"><span data-stu-id="1b983-133">Importing a File System</span></span>

<span data-ttu-id="1b983-134">Bevor Sie fortfahren, stellen Sie sicher, dass die Festplatte nicht leer ist, indem Sie die Eigenschaft [**IDiscFormat2:: get \_ mediaheuristicallyblank**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-get_mediaheuristicallyblank) überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1b983-134">Before proceeding, ensure that the disc is not blank by checking the [**IDiscFormat2::get\_MediaHeuristicallyBlank**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-get_mediaheuristicallyblank) property.</span></span>

<span data-ttu-id="1b983-135">Nachdem das **msftfilesystemmage** -Objekt erstellt wurde, sollte die [**ifilesystemmage::p UT \_ multisessioninterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) -Eigenschaft initialisiert werden, bevor entweder die [**ifilesystemmage:: ImportFile**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) System-oder die [**ifilesystemmage:: importspecificfile**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) System-Methode aufgerufen wird, um das Dateisystem aus der letzten aufgezeichneten Sitzung zu importieren.</span><span class="sxs-lookup"><span data-stu-id="1b983-135">After creating the **MsftFileSystemImage** object, the [**IFileSystemImage::put\_MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) property should be initialized prior to a call to either the [**IFileSystemImage::ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) or [**IFileSystemImage::ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) method to import the file system from the last recorded session.</span></span> <span data-ttu-id="1b983-136">Diese Methoden füllen automatisch das **msftfilesystemimage** -Objekt mit Informationen auf, in denen die zuvor aufgezeichneten Dateien und Verzeichnisse beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1b983-136">These methods will automatically populate the **MsftFileSystemImage** object with information describing the previously recorded files and directories.</span></span>

> [!Note]  
> <span data-ttu-id="1b983-137">Die [**ifilesystemimage::p UT \_ multisessioninterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) -Eigenschaft wird in der Regel mit den Multisession-Schnittstellen initialisiert, die vom Datenschreiber über die [**IDiscFormat2Data:: get \_ multisessioninterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces) -Eigenschaft bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1b983-137">The [**IFileSystemImage::put\_MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) property is typically initialized with the multisession interfaces provided by the data writer via the [**IDiscFormat2Data::get\_MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces) property.</span></span>

 

<span data-ttu-id="1b983-138">Der Versuch, die **ifilesystemimage::p UT \_ multisessioninterfaces** -Eigenschaft festzulegen, schlägt fehl, wenn IMAPI die mehrfach Sitzung für die aktuell eingefügten Medien nicht unterstützt, oder die Medien können aus einem anderen Grund nicht angefügt werden (z. b. weil Sie geschlossen wurde).</span><span class="sxs-lookup"><span data-stu-id="1b983-138">Attempts to set the **IFileSystemImage::put\_MultisessionInterfaces** property will fail if IMAPI does not support multisession for the currently inserted media or the media cannot be appended for some other reason (e.g. because it is closed).</span></span>

<span data-ttu-id="1b983-139">Wenn die vorherige brennen-Sitzung mehr als einen Dateisystemtyp enthielt, werden von der [**ifilesystemage:: ImportFile**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) System-Methode Informationen aus dem vorhandenen Dateisystemtyp importiert.</span><span class="sxs-lookup"><span data-stu-id="1b983-139">If the previous burn session contained more than one file system type, the [**IFileSystemImage::ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) method will import information from the most advanced file system type present.</span></span> <span data-ttu-id="1b983-140">Im Beispiel in diesem Thema ist UDF beispielsweise das importierte Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="1b983-140">For example, in the example provided in this topic, UDF is the imported file system.</span></span> <span data-ttu-id="1b983-141">Durch die Verwendung der [**ifilesystemage:: importspecificfile**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) System-Methode kann jedoch die spezifische Auswahl des Dateisystems importiert werden.</span><span class="sxs-lookup"><span data-stu-id="1b983-141">However, use of the [**IFileSystemImage::ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) method allows the specific selection of the file system to import.</span></span>

> [!Note]  
> <span data-ttu-id="1b983-142">Mithilfe der [**ifilesystemmage:: identifyfilesystemsondisk**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-identifyfilesystemsondisc) -Methode kann festgelegt werden, welche Dateisysteme auf der Festplatte verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="1b983-142">The [**IFileSystemImage::IdentifyFileSystemsOnDisc**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-identifyfilesystemsondisc) method can be used to determine which file systems are available on the disc.</span></span>

 


```VB
    ' Import the last session, if the disc is not empty, or initialize
    ' the file system, if the disc is empty
    If Not DataWriter.MediaHeuristicallyBlank _
    Then
        On Error Resume Next
        FSI.MultisessionInterfaces = DataWriter.MultisessionInterfaces
        If Err.Number <> 0 _
        Then
            WScript.Echo "Multisession is not supported for this disc"
            Main = 1
            Exit Function
        End If
        On Error Goto 0

        WScript.Echo "Importing data from the previous session..."
        FSI.ImportFileSystem()
    Else 
        FSI.ChooseImageDefaults(Recorder)
    End If
```



## <a name="adding-or-removing-files-to-the-file-system"></a><span data-ttu-id="1b983-143">Hinzufügen oder Entfernen von Dateien im Datei System</span><span class="sxs-lookup"><span data-stu-id="1b983-143">Adding or Removing Files to the File System</span></span>

<span data-ttu-id="1b983-144">Nachdem Sie das Dateisystem Objekt erstellt und das Dateisystem aus der vorherigen Sitzung importiert haben, rufen Sie die Methoden [**ifilesystemmage:: featefileitem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) und [**ifilesystemmage:: featedirectoryitem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) auf, um neue Datei-bzw. Verzeichnisobjekte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1b983-144">After creating the file system object and importing the file system from the previous session, call the [**IFileSystemImage::CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) and [**IFileSystemImage::CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) methods to create new file and directory objects, respectively.</span></span> <span data-ttu-id="1b983-145">Die Datei-und Verzeichnisobjekte stellen bestimmte Details zu den Dateien und Verzeichnissen bereit.</span><span class="sxs-lookup"><span data-stu-id="1b983-145">The file and directory objects provide specific details about the files and directories.</span></span> <span data-ttu-id="1b983-146">Alternativ kann die [**IFsiDirectoryItem:: AddTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree) -Methode eines Verzeichnis Objekts, das über die [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) -Schnittstelle dargestellt wird, zum Hinzufügen vorhandener Dateien und Verzeichnisse von einem anderen Speichergerät (d. h. einer Festplatte) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b983-146">Alternatively, the [**IFsiDirectoryItem::AddTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree) method of a directory object, represented via the [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) interface, can be used to add existing files and directories from another storage device (i.e. a hard drive).</span></span>

<span data-ttu-id="1b983-147">Die für [**ifilesystemage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) verfügbare Ereignishandler-Aktualisierungs Methode identifiziert die aktuelle Datei, die dem Dateisystem Abbild hinzugefügt wird, die Anzahl der bereits kopierten Sektoren und die Gesamtzahl der zu kopierenden Sektoren.</span><span class="sxs-lookup"><span data-stu-id="1b983-147">The event handler update method available for [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) identifies the current file being added to the file system image, the number of sectors already copied, and the total number of sectors to be copied.</span></span>

<span data-ttu-id="1b983-148">Um vorhandene Dateien und Verzeichnisse aus dem Dateisystem zu entfernen, verwenden Sie die [**IFsiDirectoryItem:: Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) -Methode und die [**IFsiDirectoryItem:: removetree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) -Methode der Verzeichnisobjekte, die über die [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) -Schnittstelle dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1b983-148">To remove existing files and directories from the file system, use the [**IFsiDirectoryItem::Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) and [**IFsiDirectoryItem::RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) methods of the directory objects represented via the [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) interface.</span></span> <span data-ttu-id="1b983-149">Die [**ifilesystemmage:: get \_ root**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_root) -Eigenschaft wird verwendet, um einen Zeiger auf das Stammverzeichnis des Dateisystems und die **ifsidirector yitem** -Schnittstelle zu erhalten, um die Verzeichnisstruktur zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="1b983-149">The [**IFileSystemImage::get\_Root**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_root) property is used to get a pointer to the root directory of the file system and the **IFsiDirectoryItem** interface to traverse through the directory tree.</span></span>

> [!Note]  
> <span data-ttu-id="1b983-150">Dateien und Verzeichnisse, die über die [**IFsiDirectoryItem:: Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) -und [**IFsiDirectoryItem:: removetree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) -Methode entfernt werden, werden nicht physisch von der Festplatte entfernt, und die gelöschten Informationen können von der erweiterten Software problemlos wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1b983-150">Files and directories removed via the [**IFsiDirectoryItem::Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) and [**IFsiDirectoryItem::RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) methods are not physically removed from the disc, and advanced software can easily recover the deleted information.</span></span>

 


```VB
    ' Add the directory and its contents to the file system 
    WScript.Echo "Adding " & Path & " directory to the disc..."
    FSI.Root.AddTree Path, false
```



## <a name="constructing-a-file-system-image"></a><span data-ttu-id="1b983-151">Erstellen eines Datei System Abbilds</span><span class="sxs-lookup"><span data-stu-id="1b983-151">Constructing a File System Image</span></span>

<span data-ttu-id="1b983-152">Der letzte Schritt besteht darin, [**ifilesystemimage:: errateresultimage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) aufzurufen, um einen Datenstream für das Burn-Image zu erstellen und über die [**ifilesystemimageresult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult) -Schnittstelle darauf zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="1b983-152">The final step is to call [**IFileSystemImage::CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) to create a data stream for the burn image and provide access to it through the [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult) interface.</span></span> <span data-ttu-id="1b983-153">Dieser Datenstrom kann entweder direkt für die [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) -Methode bereitgestellt oder zur späteren Verwendung in einer Datei gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="1b983-153">This data stream can either be provided directly to the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method or be saved to a file for later use.</span></span>


```VB
    ' Create an image from the file system image object
    Dim Result
    Set Result = FSI.CreateResultImage()
    Stream = Result.ImageStream
```



## <a name="example-summary"></a><span data-ttu-id="1b983-154">Beispiel Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="1b983-154">Example Summary</span></span>

<span data-ttu-id="1b983-155">Im folgenden Visual Basic Skript Beispiel wird gezeigt, wie Sie IMAPI-Objekte zum Erstellen von mehr sitzungsdisks verwenden.</span><span class="sxs-lookup"><span data-stu-id="1b983-155">The following Visual Basic script example shows how to use IMAPI objects to create multisession discs.</span></span> <span data-ttu-id="1b983-156">Im Beispiel wird eine neue Sitzung erstellt und der Festplatte ein Verzeichnis hinzugefügt. Der Einfachheit halber führt der Code keine umfassende Fehlerüberprüfung aus, und es wird Folgendes vorausgesetzt:</span><span class="sxs-lookup"><span data-stu-id="1b983-156">The example creates a new session and adds a directory to the disc. For the sake of simplicity, the code does not perform extensive error checking, and assumes the following:</span></span>

-   <span data-ttu-id="1b983-157">Auf dem System ist ein kompatibles CD-Gerät installiert.</span><span class="sxs-lookup"><span data-stu-id="1b983-157">A compatible disc device is installed on the system.</span></span>
-   <span data-ttu-id="1b983-158">Das Geräte Datenträger ist das erste Laufwerk des Systems.</span><span class="sxs-lookup"><span data-stu-id="1b983-158">The disc device is the first drive on the system.</span></span>
-   <span data-ttu-id="1b983-159">Ein kompatibles Laufwerk wird auf dem Festplattengerät eingefügt.</span><span class="sxs-lookup"><span data-stu-id="1b983-159">A compatible disc is inserted in the disc device.</span></span>
-   <span data-ttu-id="1b983-160">Dateien, die der Festplatte hinzugefügt werden sollen, befinden sich in "g: \\ burndir".</span><span class="sxs-lookup"><span data-stu-id="1b983-160">Files to add to the disc are located in "g:\\burndir".</span></span>

<span data-ttu-id="1b983-161">Dem Skript können zusätzliche Funktionen hinzugefügt werden, z. b. umfangreiche Fehlerüberprüfung, Geräte-und Medienkompatibilität, Ereignis Benachrichtigung und Berechnung des freien Speicherplatzes auf der Festplatte.</span><span class="sxs-lookup"><span data-stu-id="1b983-161">Additional functionality such as extensive error checking, device and media compatibility, event notification, and calculation of free space on the disc can be added to the script.</span></span>


```VB
' This script adds data files from a single directory tree to a
' disc (a new session is added, if the disc already contains data)

' Copyright (C) Microsoft. All rights reserved.

Option Explicit

' **_ CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to add
    Dim Stream               ' Data stream for burning device
    
    Index = 0                ' First drive on the system
    Path = "G:\BurnDir"      ' Files to add to the disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim DiscMaster
    Set DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder2 object for the specified burning device.
    Dim UniqueId
    set Recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    UniqueId = DiscMaster.Item(Index)
    Recorder.InitializeDiscRecorder(UniqueId)

    ' Create a DiscFormat2Data object and set the recorder
    Dim DataWriter
    Set DataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    DataWriter.Recorder = Recorder
    DataWriter.ClientName = "IMAPIv2 TEST"

    ' Create a new file system image object
    Dim FSI
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")

    ' Import the last session, if the disc is not empty, or initialize
    ' the file system, if the disc is empty
    If Not DataWriter.MediaHeuristicallyBlank _
    Then
        On Error Resume Next
        FSI.MultisessionInterfaces = DataWriter.MultisessionInterfaces
        If Err.Number <> 0 _
        Then
            WScript.Echo "Multisession is not supported for this disc"
            Main = 1
            Exit Function
        End If
        On Error Goto 0

        WScript.Echo "Importing data from the previous session..."
        FSI.ImportFileSystem()
    Else 
        FSI.ChooseImageDefaults(Recorder)
    End If

    ' Add the directory and its contents to the file system 
    WScript.Echo "Adding " & Path & " directory to the disc..."
    FSI.Root.AddTree Path, false

    ' Create an image from the file system image object
    Dim Result
    Set Result = FSI.CreateResultImage()
    Stream = Result.ImageStream
    
    ' Write stream to disc using the specified recorder
    WScript.Echo "Writing content to the disc..."
    DataWriter.Write(Stream)

    WScript.Echo "Finished writing content."
    Main = 0
End Function

```



## <a name="related-topics"></a><span data-ttu-id="1b983-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1b983-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b983-163">Verwenden von IMAPI</span><span class="sxs-lookup"><span data-stu-id="1b983-163">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="1b983-164">_ *IStream*\*</span><span class="sxs-lookup"><span data-stu-id="1b983-164">_ *IStream*\*</span></span>](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> <dt>

[<span data-ttu-id="1b983-165">**IDiscMaster2**</span><span class="sxs-lookup"><span data-stu-id="1b983-165">**IDiscMaster2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[<span data-ttu-id="1b983-166">**IDiscFormat2Data**</span><span class="sxs-lookup"><span data-stu-id="1b983-166">**IDiscFormat2Data**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[<span data-ttu-id="1b983-167">**Ifilesystemimage**</span><span class="sxs-lookup"><span data-stu-id="1b983-167">**IFileSystemImage**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> </dl>

 

 
