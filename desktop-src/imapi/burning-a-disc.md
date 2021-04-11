---
title: Brennen eines Festplatten Bilds
description: 'Das Mastering (Brennen eines Datenträgers) mithilfe von IMAPI besteht aus den folgenden Schritten: Erstellen eines Dateisystem Images, das die Verzeichnisse und Dateien zum Schreiben von Datenträgern enthält. Richten Sie einen Disc Recorder ein, um mit dem optischen Gerät zu kommunizieren. Erstellen Sie einen Datenschreiber, und brennen Sie das Abbild auf die Festplatte'
ms.assetid: f2eee14e-695d-4678-b3c1-b521ab4d4a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e3086f728ca0b0826a001d26841edcfe07c6a1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314924"
---
# <a name="burning-a-disc-image"></a><span data-ttu-id="43ed5-103">Brennen eines Festplatten Bilds</span><span class="sxs-lookup"><span data-stu-id="43ed5-103">Burning a Disc Image</span></span>

<span data-ttu-id="43ed5-104">Das Mastering (Brennen eines Datenträgers) mithilfe von IMAPI besteht aus den folgenden Schritten:</span><span class="sxs-lookup"><span data-stu-id="43ed5-104">Mastering (burning a disc) using IMAPI consists of the following steps:</span></span>

1.  <span data-ttu-id="43ed5-105">Erstellen Sie ein Dateisystem Image, das die Verzeichnisse und Dateien zum Schreiben der Festplatte enthält.</span><span class="sxs-lookup"><span data-stu-id="43ed5-105">Construct a file system image that contains the directories and files to write disc.</span></span>
2.  <span data-ttu-id="43ed5-106">[Richten Sie einen Disc Recorder ein](#set-up-a-disc-recorder) , um mit dem optischen Gerät zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="43ed5-106">[Set up a disc recorder](#set-up-a-disc-recorder) to communicate with the optical device.</span></span>
3.  <span data-ttu-id="43ed5-107">[Erstellen Sie einen Datenschreiber](#create-a-data-writer-and-write-the-burn-image) , und brennen Sie das Abbild auf die Festplatte</span><span class="sxs-lookup"><span data-stu-id="43ed5-107">[Create a data writer](#create-a-data-writer-and-write-the-burn-image) and burn the image to disc.</span></span>

<span data-ttu-id="43ed5-108">Ein Beispiel für das Brennen eines Festplatten Abbilds finden Sie unter [VBScript-Beispiel](#vbscript-example).</span><span class="sxs-lookup"><span data-stu-id="43ed5-108">For an example that burns a disc image, see [VBScript example](#vbscript-example).</span></span>

## <a name="construct-a-burn-image"></a><span data-ttu-id="43ed5-109">Erstellen eines Verbrauchs Abbilds</span><span class="sxs-lookup"><span data-stu-id="43ed5-109">Construct a burn image</span></span>

<span data-ttu-id="43ed5-110">Ein Burn-Image ist ein Datenstrom, der auf optische Medien geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="43ed5-110">A burn image is a data stream that is ready to be written to optical media.</span></span> <span data-ttu-id="43ed5-111">Das Burn-Image für die Formate "ISO9660", "Joliet" und "UDF" besteht aus einem Dateisystem einzelner Dateien und Verzeichnisse.</span><span class="sxs-lookup"><span data-stu-id="43ed5-111">The burn image for ISO9660, Joliet and UDF formats consists of a file system of individual files and directories.</span></span> <span data-ttu-id="43ed5-112">Das **cfilesystemmage** -Objekt ist das Dateisystem Objekt, das die Dateien und Verzeichnisse enthält, die auf dem optischen Medium platziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="43ed5-112">The **CFileSystemImage** object is the file system object that holds the files and directories to place on the optical media.</span></span> <span data-ttu-id="43ed5-113">Die [**ifilesystemmage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) -Schnittstelle ermöglicht den Zugriff auf das Dateisystem Objekt und die Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="43ed5-113">The [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) interface provides access to the file system object and settings.</span></span>

<span data-ttu-id="43ed5-114">Nachdem Sie das Dateisystem Objekt erstellt haben, rufen Sie die [**ifilesystemmage:: featefileitem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) -Methode und die [**ifilesystemmage:: | atedirectoryitem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) -Methode auf, um die Datei-bzw. Verzeichnisobjekte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="43ed5-114">After creating the file system object, call the [**IFileSystemImage::CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) and [**IFileSystemImage::CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) methods to create the file and directory objects, respectively.</span></span> <span data-ttu-id="43ed5-115">Die Datei-und Verzeichnisobjekte können verwendet werden, um bestimmte Details zur Datei und zum Verzeichnis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="43ed5-115">The file and directory objects can be used to provide specific details about the file and directory.</span></span> <span data-ttu-id="43ed5-116">Mit den Ereignishandlermethoden, die für [**ifilesystemmage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) verfügbar sind, kann die aktuelle Datei identifiziert werden, die dem Dateisystem Abbild hinzugefügt wird, die Anzahl der bereits kopierten Sektoren und die Gesamtzahl der zu kopierenden Sektoren.</span><span class="sxs-lookup"><span data-stu-id="43ed5-116">The event handler methods available for [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) can identify the current file being added to the file system image, the number of sectors already copied, and the total number of sectors to be copied.</span></span>

<span data-ttu-id="43ed5-117">Optional kann ein Start Abbild mit der [**ifilesystemmage::p UT \_ bootimageoptions**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions) -Eigenschaft an das Dateisystem angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="43ed5-117">Optionally, a boot image can be attached to the file system using the [**IFileSystemImage::put\_BootImageOptions**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions) property.</span></span> <span data-ttu-id="43ed5-118">Ein Beispiel finden Sie unter [Hinzufügen eines Start Abbilds](adding-a-boot-image.md).</span><span class="sxs-lookup"><span data-stu-id="43ed5-118">For an example, see [Adding a Boot Image](adding-a-boot-image.md).</span></span>

<span data-ttu-id="43ed5-119">Rufen Sie zum Schluss [**ifilesystemimage:: errateresultimage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) auf, um einen Datenstrom zu erstellen, und bieten Sie Zugriff über [**ifilesystemimageresult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult).</span><span class="sxs-lookup"><span data-stu-id="43ed5-119">Finally, call [**IFileSystemImage::CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) to create a data stream and provides access through [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult).</span></span> <span data-ttu-id="43ed5-120">Der neue Datenstrom kann dann direkt der [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) -Methode bereitgestellt oder zur späteren Verwendung in einer Datei gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="43ed5-120">The new data stream can then be provided directly to the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method or be saved to a file for later use.</span></span>

## <a name="set-up-a-disc-recorder"></a><span data-ttu-id="43ed5-121">Einrichten eines Disk Recorder</span><span class="sxs-lookup"><span data-stu-id="43ed5-121">Set up a disc recorder</span></span>

<span data-ttu-id="43ed5-122">Das **MsftDiscMaster2** -Objekt stellt eine Enumeration der optischen Geräte auf dem System bereit.</span><span class="sxs-lookup"><span data-stu-id="43ed5-122">The **MsftDiscMaster2** object provides an enumeration of the optical devices on the system.</span></span> <span data-ttu-id="43ed5-123">Die [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) -Schnittstelle ermöglicht den Zugriff auf die resultierende Geräteenumeration.</span><span class="sxs-lookup"><span data-stu-id="43ed5-123">The [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) interface provides access to the resultant device enumeration.</span></span> <span data-ttu-id="43ed5-124">Durchlaufen Sie die Enumerationen, um nach einem entsprechenden Aufzeichnungsgerät zu suchen.</span><span class="sxs-lookup"><span data-stu-id="43ed5-124">Traverse the enumerations to locate an appropriate recording device.</span></span> <span data-ttu-id="43ed5-125">Das **MsftDiscMaster2** -Objekt bietet auch Ereignis Benachrichtigungen, wenn optische Geräte einem Computer hinzugefügt oder daraus gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="43ed5-125">The **MsftDiscMaster2** object also provides event notifications when optical devices are added to or deleted from a computer.</span></span>

<span data-ttu-id="43ed5-126">Nachdem Sie einen optischen Recorder gefunden und seine ID abgerufen haben, erstellen Sie ein **MsftDiscRecorder2** -Objekt, und initialisieren Sie den Recorder mithilfe der Geräte-ID.</span><span class="sxs-lookup"><span data-stu-id="43ed5-126">After finding an optical recorder and retrieving its ID, create an **MsftDiscRecorder2** object and initialize the recorder using the device ID.</span></span> <span data-ttu-id="43ed5-127">Die [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) -Schnittstelle bietet Zugriff auf das Recorder-Objekt sowie einige grundlegende Geräteinformationen wie Hersteller-ID, Produkt-ID, Produkt Revision und Methoden, um die Medien zu auswerfen und die Leiste zu schließen.</span><span class="sxs-lookup"><span data-stu-id="43ed5-127">The [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) interface provides access to the recorder object as well as some basic device information such as vendor ID, product ID, product revision, and methods to eject the media and close the tray.</span></span>

## <a name="create-a-data-writer-and-write-the-burn-image"></a><span data-ttu-id="43ed5-128">Erstellen eines Daten Writers und Schreiben des Verbrauchs Abbilds</span><span class="sxs-lookup"><span data-stu-id="43ed5-128">Create a data writer and write the burn image</span></span>

<span data-ttu-id="43ed5-129">Das **MsftDiscFormat2Data** -Objekt stellt die Schreibmethode, die Eigenschaften über die Schreibfunktion und die medienspezifischen Eigenschaften bereit.</span><span class="sxs-lookup"><span data-stu-id="43ed5-129">The **MsftDiscFormat2Data** object provides the writing method, the properties about the write function and media-specific properties.</span></span> <span data-ttu-id="43ed5-130">Die [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) -Schnittstelle bietet Zugriff auf das **MsftDiscFormat2Data** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="43ed5-130">The [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) interface provides access to the **MsftDiscFormat2Data** object.</span></span>

<span data-ttu-id="43ed5-131">Der Disk Recorder verknüpft mithilfe der [**IDiscFormat2Data::p UT \_ Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) -Eigenschaft mit dem Format Schreiber.</span><span class="sxs-lookup"><span data-stu-id="43ed5-131">The disc recorder links to the format writer using the [**IDiscFormat2Data::put\_Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) property.</span></span> <span data-ttu-id="43ed5-132">Nachdem der Recorder an das Format-Writer gebunden wurde, können Sie Abfragen bezüglich der Medien ausführen und Schreib spezifische Eigenschaften aktualisieren, bevor Sie das Ergebnisbild mithilfe der [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) -Methode auf die Festplatte schreiben.</span><span class="sxs-lookup"><span data-stu-id="43ed5-132">After the recorder is bound to the format writer, you can perform queries regarding the media and update write-specific properties before writing the result image to disc using the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method.</span></span>

<span data-ttu-id="43ed5-133">Andere von IMAPI bereitgestellte Schnittstellen zum Schreiben von Formaten funktionieren ähnlich. zusätzliche Schnittstellen zum Schreiben von Formaten umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="43ed5-133">Other format writing interfaces provided by IMAPI work similarly; additional format writing interfaces include:</span></span>

-   <span data-ttu-id="43ed5-134">[**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase) löscht erneut beschreibbare optische Medien.</span><span class="sxs-lookup"><span data-stu-id="43ed5-134">[**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase) erases rewritable optical media.</span></span>
-   <span data-ttu-id="43ed5-135">[**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd) schreibt ein RAW-Image in optische Medien.</span><span class="sxs-lookup"><span data-stu-id="43ed5-135">[**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd) writes a raw image to optical media.</span></span>
-   <span data-ttu-id="43ed5-136">[**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce) schreibt Audiospuren in optische Medien.</span><span class="sxs-lookup"><span data-stu-id="43ed5-136">[**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce) writes audio tracks to optical media.</span></span>

> [!Note]  
> <span data-ttu-id="43ed5-137">Es ist möglich, dass bei einem Verbrennungsvorgang (d. h. beim Abmelden des Benutzers oder beim Aussetzen des Systems) ein Strom Status Übergang stattfindet. Dies führt zu einer Unterbrechung des Verbrauchs und möglichen Datenverlusten.</span><span class="sxs-lookup"><span data-stu-id="43ed5-137">It is possible for a power state transition to take place during a burn operation (i.e. user log-off or system suspend) which leads to the interruption of the burn process and possible data loss.</span></span> <span data-ttu-id="43ed5-138">Informationen zur Programmierung finden Sie unter verhindern der Abmeldung [oder aussetzen während eines Burn](preventing-logoff-or-suspend-during-a-burn.md)-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="43ed5-138">For programming considerations, see [Preventing Logoff or Suspend During a Burn](preventing-logoff-or-suspend-during-a-burn.md).</span></span>

 

## <a name="vbscript-example"></a><span data-ttu-id="43ed5-139">VBScript-Beispiel</span><span class="sxs-lookup"><span data-stu-id="43ed5-139">VBScript example</span></span>

<span data-ttu-id="43ed5-140">In diesem Skript Beispiel wird gezeigt, wie die IMAPI-Objekte zum Brennen von optischen Medien verwendet werden. genauer gesagt, schreiben Sie ein Verzeichnis auf eine leere CD. Der Code enthält keine Fehlerüberprüfung, und es wird Folgendes vorausgesetzt:</span><span class="sxs-lookup"><span data-stu-id="43ed5-140">This script example shows how to use the IMAPI objects to burn optical media; more specifically, write a directory to a blank disc. The code contains no error checking, and assumes the following:</span></span>

-   <span data-ttu-id="43ed5-141">Auf dem System ist ein kompatibles CD-Gerät installiert.</span><span class="sxs-lookup"><span data-stu-id="43ed5-141">A compatible disc device is installed on the system.</span></span>
-   <span data-ttu-id="43ed5-142">Das Geräte Datenträger ist das zweite Laufwerk des Systems.</span><span class="sxs-lookup"><span data-stu-id="43ed5-142">The disc device is the second drive on the system.</span></span>
-   <span data-ttu-id="43ed5-143">Ein kompatibles Laufwerk wird auf dem Festplattengerät eingefügt.</span><span class="sxs-lookup"><span data-stu-id="43ed5-143">A compatible disc is inserted in the disc device.</span></span>
-   <span data-ttu-id="43ed5-144">Die Festplatte ist leer.</span><span class="sxs-lookup"><span data-stu-id="43ed5-144">The disc is blank.</span></span>
-   <span data-ttu-id="43ed5-145">Dateien, die auf den Datenträger geschrieben werden sollen, befinden sich in "g: \\ burndir".</span><span class="sxs-lookup"><span data-stu-id="43ed5-145">Files to write to disc are located in "g:\\burndir".</span></span>

<span data-ttu-id="43ed5-146">Diesem Skript können zusätzliche Funktionen hinzugefügt werden, wie z. b. Fehlerüberprüfung, Geräte-und Medienkompatibilität, Ereignis Benachrichtigung und die Berechnung des freien Speicherplatzes auf der Festplatte.</span><span class="sxs-lookup"><span data-stu-id="43ed5-146">Additional functionality such as error checking, device and media compatibility, event notification, and calculating free space on the disc can be added to this script.</span></span>


```VB
' This script burns data files to disc in a single session 
' using files from a single directory tree.
 
' Copyright (C) Microsoft Corp. 2006

Option Explicit

' *** CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to burn
    Dim Stream               ' Data stream for burning device
    
    Index = 1                ' Second drive on the system
    Path = "g:\BurnDir"      ' Files to transfer to disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim g_DiscMaster
    Set g_DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder object for the specified burning device.
    Dim uniqueId
    set recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    uniqueId = g_DiscMaster.Item(index)
    recorder.InitializeDiscRecorder( uniqueId )

    ' Create an image stream for a specified directory.
    Dim FSI                  ' Disc file system
    Dim Dir                  ' Root directory of the disc file system
    Dim dataWriter    
        
    ' Create a new file system image and retrieve root directory
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
    Set Dir = FSI.Root

    'Create the new disc format and set the recorder
    Set dataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    dataWriter.recorder = Recorder
    dataWriter.ClientName = "IMAPIv2 TEST"

    FSI.ChooseImageDefaults(recorder)
        
    ' Add the directory and its contents to the file system 
    Dir.AddTree Path, false
        
    ' Create an image from the file system
    Dim result
    Set result = FSI.CreateResultImage()
    Stream = result.ImageStream
    
    ' Write stream to disc using the specified recorder.
    WScript.Echo "Writing content to disc..."
    dataWriter.write(Stream)

    WScript.Echo "----- Finished writing content -----"
    Main = 0
End Function

```



## <a name="related-topics"></a><span data-ttu-id="43ed5-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="43ed5-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43ed5-148">Verwenden von IMAPI</span><span class="sxs-lookup"><span data-stu-id="43ed5-148">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="43ed5-149">**IDiscFormat2Data**</span><span class="sxs-lookup"><span data-stu-id="43ed5-149">**IDiscFormat2Data**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[<span data-ttu-id="43ed5-150">**IDiscFormat2Erase**</span><span class="sxs-lookup"><span data-stu-id="43ed5-150">**IDiscFormat2Erase**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase)
</dt> <dt>

[<span data-ttu-id="43ed5-151">**IDiscFormat2RawCD**</span><span class="sxs-lookup"><span data-stu-id="43ed5-151">**IDiscFormat2RawCD**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd)
</dt> <dt>

[<span data-ttu-id="43ed5-152">**IDiscFormat2TrackAtOnce**</span><span class="sxs-lookup"><span data-stu-id="43ed5-152">**IDiscFormat2TrackAtOnce**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce)
</dt> <dt>

[<span data-ttu-id="43ed5-153">**IDiscMaster2**</span><span class="sxs-lookup"><span data-stu-id="43ed5-153">**IDiscMaster2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[<span data-ttu-id="43ed5-154">**IDiscRecorder2**</span><span class="sxs-lookup"><span data-stu-id="43ed5-154">**IDiscRecorder2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2)
</dt> <dt>

[<span data-ttu-id="43ed5-155">**Ifilesystemimage**</span><span class="sxs-lookup"><span data-stu-id="43ed5-155">**IFileSystemImage**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> <dt>

[<span data-ttu-id="43ed5-156">**IStream**</span><span class="sxs-lookup"><span data-stu-id="43ed5-156">**IStream**</span></span>](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> </dl>

 

 