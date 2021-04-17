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
# <a name="creating-a-multisession-disc"></a>Erstellen einer Multi-Session-CD

Die [Image-Mastering-API](about-imapi.md) (IMAPI) unterstützt das Hinzufügen und Entfernen von Dateien zu den folgenden mehr sitzungsdatenträger:

-   CD-R/CD-RW
-   Single-Layer DVD + r/DVD-r
-   Dual-Layer-DVD + R
-   BD-R
-   DVD-RW/DVD + RW (**nur Windows 7**)
-   DVD-RAM (**nur Windows 7**)
-   BD-RE (**nur Windows 7**)

Die Erstellung einer mehr sitzenden CD mithilfe von IMAPI besteht aus den folgenden Schritten. Jeder dieser dokumentierten Schritte enthält den relevanten Teil des kompletten Visual Basic Skript Beispiels, das im letzten Abschnitt bereitgestellt wurde.

## <a name="initializing-the-disc-recorder"></a>Der Disc Recorder wird initialisiert.

Vor der Geräte Initialisierung stellt das **MsftDiscMaster2** -Objekt eine Enumeration der optischen Geräte auf dem System bereit. Die [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) -Schnittstelle ermöglicht den Zugriff auf diese Geräte Enumeration, um den Speicherort des entsprechenden Aufzeichnungs Geräts zu vereinfachen. Das **MsftDiscMaster2** -Objekt stellt auch Ereignis Benachrichtigungen bereit, wenn optische Geräte einem Computer hinzugefügt oder daraus entfernt werden.

Nachdem Sie einen optischen Recorder gefunden und die ihm zugewiesene ID abgerufen haben, erstellen Sie ein neues **MsftDiscMaster2** -Objekt, und initialisieren Sie den Recorder mithilfe der spezifischen Geräte-ID.

Die [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) -Schnittstelle ermöglicht den Zugriff auf grundlegende Geräteinformationen, z. b. Hersteller-ID, Produkt-ID, Produkt Revision sowie Methoden zum Auswerfen von Medien oder Schließen der Info Leiste.

> [!Note]  
> Die im folgenden Beispiel deklarierten zusätzlichen Konstanten und Dimensionen werden später in dem gesamten Beispielskript im letzten Abschnitt dieses Dokuments verwendet. Diese Elemente sind für die Initialisierung eines Disk Recorder nicht erforderlich.

 


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



## <a name="creating-a-data-writer"></a>Erstellen eines Daten Writers

Das _ *MsftDiscFormat2Data**-Objekt stellt die Schreibmethode, deren Eigenschaften und die medienspezifischen Eigenschaften bereit. Die [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) -Schnittstelle ermöglicht den Zugriff auf dieses Objekt.

Der Disk Recorder bindet mithilfe der [**IDiscFormat2Data::p UT \_ Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) -Eigenschaft an den Format Schreiber. Nachdem die Aufzeichnung an den Format Schreiber gebunden ist, können Medien-und Schreib spezifische Eigenschaften Abfragen ausgeführt werden, bevor das Ergebnisbild mithilfe der [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) -Methode auf die Festplatte geschrieben wird.

> [!Note]  
> Die im Beispielcode unten angegebene Zeichenfolge für den Client Namen sollte entsprechend für die jeweilige Anwendung angepasst werden.

 


```VB
    ' Create a DiscFormat2Data object and set the recorder
    Dim DataWriter
    Set DataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    DataWriter.Recorder = Recorder
    DataWriter.ClientName = "IMAPIv2 TEST"
```



## <a name="creating-the-file-system-object"></a>Erstellen des Datei System Objekts

Damit eine neue Sitzung aufgezeichnet werden kann, muss zuerst ein Burn-Image generiert werden. Ein Burn-Image für die Formate " **ISO9660**", " **Joliet** " und " **UDF** " besteht aus Dateisystemen einzelner Dateien und Verzeichnisse. Das **msftfilesystemmage** -Objekt ist das Dateisystem Objekt, das die Dateien und Verzeichnisse enthält, die auf dem optischen Medium platziert werden sollen. Die [**ifilesystemmage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) -Schnittstelle ermöglicht den Zugriff auf das Dateisystem Objekt und die Einstellungen.


```VB
    ' Create a new file system image object
    Dim FSI
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
```



## <a name="importing-a-file-system"></a>Importieren eines Dateisystems

Bevor Sie fortfahren, stellen Sie sicher, dass die Festplatte nicht leer ist, indem Sie die Eigenschaft [**IDiscFormat2:: get \_ mediaheuristicallyblank**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-get_mediaheuristicallyblank) überprüfen.

Nachdem das **msftfilesystemmage** -Objekt erstellt wurde, sollte die [**ifilesystemmage::p UT \_ multisessioninterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) -Eigenschaft initialisiert werden, bevor entweder die [**ifilesystemmage:: ImportFile**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) System-oder die [**ifilesystemmage:: importspecificfile**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) System-Methode aufgerufen wird, um das Dateisystem aus der letzten aufgezeichneten Sitzung zu importieren. Diese Methoden füllen automatisch das **msftfilesystemimage** -Objekt mit Informationen auf, in denen die zuvor aufgezeichneten Dateien und Verzeichnisse beschrieben werden.

> [!Note]  
> Die [**ifilesystemimage::p UT \_ multisessioninterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) -Eigenschaft wird in der Regel mit den Multisession-Schnittstellen initialisiert, die vom Datenschreiber über die [**IDiscFormat2Data:: get \_ multisessioninterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces) -Eigenschaft bereitgestellt werden.

 

Der Versuch, die **ifilesystemimage::p UT \_ multisessioninterfaces** -Eigenschaft festzulegen, schlägt fehl, wenn IMAPI die mehrfach Sitzung für die aktuell eingefügten Medien nicht unterstützt, oder die Medien können aus einem anderen Grund nicht angefügt werden (z. b. weil Sie geschlossen wurde).

Wenn die vorherige brennen-Sitzung mehr als einen Dateisystemtyp enthielt, werden von der [**ifilesystemage:: ImportFile**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) System-Methode Informationen aus dem vorhandenen Dateisystemtyp importiert. Im Beispiel in diesem Thema ist UDF beispielsweise das importierte Dateisystem. Durch die Verwendung der [**ifilesystemage:: importspecificfile**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) System-Methode kann jedoch die spezifische Auswahl des Dateisystems importiert werden.

> [!Note]  
> Mithilfe der [**ifilesystemmage:: identifyfilesystemsondisk**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-identifyfilesystemsondisc) -Methode kann festgelegt werden, welche Dateisysteme auf der Festplatte verfügbar sind.

 


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



## <a name="adding-or-removing-files-to-the-file-system"></a>Hinzufügen oder Entfernen von Dateien im Datei System

Nachdem Sie das Dateisystem Objekt erstellt und das Dateisystem aus der vorherigen Sitzung importiert haben, rufen Sie die Methoden [**ifilesystemmage:: featefileitem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) und [**ifilesystemmage:: featedirectoryitem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) auf, um neue Datei-bzw. Verzeichnisobjekte zu erstellen. Die Datei-und Verzeichnisobjekte stellen bestimmte Details zu den Dateien und Verzeichnissen bereit. Alternativ kann die [**IFsiDirectoryItem:: AddTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree) -Methode eines Verzeichnis Objekts, das über die [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) -Schnittstelle dargestellt wird, zum Hinzufügen vorhandener Dateien und Verzeichnisse von einem anderen Speichergerät (d. h. einer Festplatte) verwendet werden.

Die für [**ifilesystemage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) verfügbare Ereignishandler-Aktualisierungs Methode identifiziert die aktuelle Datei, die dem Dateisystem Abbild hinzugefügt wird, die Anzahl der bereits kopierten Sektoren und die Gesamtzahl der zu kopierenden Sektoren.

Um vorhandene Dateien und Verzeichnisse aus dem Dateisystem zu entfernen, verwenden Sie die [**IFsiDirectoryItem:: Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) -Methode und die [**IFsiDirectoryItem:: removetree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) -Methode der Verzeichnisobjekte, die über die [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) -Schnittstelle dargestellt werden. Die [**ifilesystemmage:: get \_ root**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_root) -Eigenschaft wird verwendet, um einen Zeiger auf das Stammverzeichnis des Dateisystems und die **ifsidirector yitem** -Schnittstelle zu erhalten, um die Verzeichnisstruktur zu durchlaufen.

> [!Note]  
> Dateien und Verzeichnisse, die über die [**IFsiDirectoryItem:: Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) -und [**IFsiDirectoryItem:: removetree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) -Methode entfernt werden, werden nicht physisch von der Festplatte entfernt, und die gelöschten Informationen können von der erweiterten Software problemlos wieder hergestellt werden.

 


```VB
    ' Add the directory and its contents to the file system 
    WScript.Echo "Adding " & Path & " directory to the disc..."
    FSI.Root.AddTree Path, false
```



## <a name="constructing-a-file-system-image"></a>Erstellen eines Datei System Abbilds

Der letzte Schritt besteht darin, [**ifilesystemimage:: errateresultimage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) aufzurufen, um einen Datenstream für das Burn-Image zu erstellen und über die [**ifilesystemimageresult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult) -Schnittstelle darauf zuzugreifen. Dieser Datenstrom kann entweder direkt für die [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) -Methode bereitgestellt oder zur späteren Verwendung in einer Datei gespeichert werden.


```VB
    ' Create an image from the file system image object
    Dim Result
    Set Result = FSI.CreateResultImage()
    Stream = Result.ImageStream
```



## <a name="example-summary"></a>Beispiel Zusammenfassung

Im folgenden Visual Basic Skript Beispiel wird gezeigt, wie Sie IMAPI-Objekte zum Erstellen von mehr sitzungsdisks verwenden. Im Beispiel wird eine neue Sitzung erstellt und der Festplatte ein Verzeichnis hinzugefügt. Der Einfachheit halber führt der Code keine umfassende Fehlerüberprüfung aus, und es wird Folgendes vorausgesetzt:

-   Auf dem System ist ein kompatibles CD-Gerät installiert.
-   Das Geräte Datenträger ist das erste Laufwerk des Systems.
-   Ein kompatibles Laufwerk wird auf dem Festplattengerät eingefügt.
-   Dateien, die der Festplatte hinzugefügt werden sollen, befinden sich in "g: \\ burndir".

Dem Skript können zusätzliche Funktionen hinzugefügt werden, z. b. umfangreiche Fehlerüberprüfung, Geräte-und Medienkompatibilität, Ereignis Benachrichtigung und Berechnung des freien Speicherplatzes auf der Festplatte.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von IMAPI](using-imapi.md)
</dt> <dt>

[_ *IStream**](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> <dt>

[**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[**Ifilesystemimage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> </dl>

 

 
