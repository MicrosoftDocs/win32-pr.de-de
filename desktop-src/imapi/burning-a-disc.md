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
# <a name="burning-a-disc-image"></a>Brennen eines Festplatten Bilds

Das Mastering (Brennen eines Datenträgers) mithilfe von IMAPI besteht aus den folgenden Schritten:

1.  Erstellen Sie ein Dateisystem Image, das die Verzeichnisse und Dateien zum Schreiben der Festplatte enthält.
2.  [Richten Sie einen Disc Recorder ein](#set-up-a-disc-recorder) , um mit dem optischen Gerät zu kommunizieren.
3.  [Erstellen Sie einen Datenschreiber](#create-a-data-writer-and-write-the-burn-image) , und brennen Sie das Abbild auf die Festplatte

Ein Beispiel für das Brennen eines Festplatten Abbilds finden Sie unter [VBScript-Beispiel](#vbscript-example).

## <a name="construct-a-burn-image"></a>Erstellen eines Verbrauchs Abbilds

Ein Burn-Image ist ein Datenstrom, der auf optische Medien geschrieben werden kann. Das Burn-Image für die Formate "ISO9660", "Joliet" und "UDF" besteht aus einem Dateisystem einzelner Dateien und Verzeichnisse. Das **cfilesystemmage** -Objekt ist das Dateisystem Objekt, das die Dateien und Verzeichnisse enthält, die auf dem optischen Medium platziert werden sollen. Die [**ifilesystemmage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) -Schnittstelle ermöglicht den Zugriff auf das Dateisystem Objekt und die Einstellungen.

Nachdem Sie das Dateisystem Objekt erstellt haben, rufen Sie die [**ifilesystemmage:: featefileitem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) -Methode und die [**ifilesystemmage:: | atedirectoryitem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) -Methode auf, um die Datei-bzw. Verzeichnisobjekte zu erstellen. Die Datei-und Verzeichnisobjekte können verwendet werden, um bestimmte Details zur Datei und zum Verzeichnis bereitzustellen. Mit den Ereignishandlermethoden, die für [**ifilesystemmage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) verfügbar sind, kann die aktuelle Datei identifiziert werden, die dem Dateisystem Abbild hinzugefügt wird, die Anzahl der bereits kopierten Sektoren und die Gesamtzahl der zu kopierenden Sektoren.

Optional kann ein Start Abbild mit der [**ifilesystemmage::p UT \_ bootimageoptions**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions) -Eigenschaft an das Dateisystem angefügt werden. Ein Beispiel finden Sie unter [Hinzufügen eines Start Abbilds](adding-a-boot-image.md).

Rufen Sie zum Schluss [**ifilesystemimage:: errateresultimage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) auf, um einen Datenstrom zu erstellen, und bieten Sie Zugriff über [**ifilesystemimageresult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult). Der neue Datenstrom kann dann direkt der [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) -Methode bereitgestellt oder zur späteren Verwendung in einer Datei gespeichert werden.

## <a name="set-up-a-disc-recorder"></a>Einrichten eines Disk Recorder

Das **MsftDiscMaster2** -Objekt stellt eine Enumeration der optischen Geräte auf dem System bereit. Die [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) -Schnittstelle ermöglicht den Zugriff auf die resultierende Geräteenumeration. Durchlaufen Sie die Enumerationen, um nach einem entsprechenden Aufzeichnungsgerät zu suchen. Das **MsftDiscMaster2** -Objekt bietet auch Ereignis Benachrichtigungen, wenn optische Geräte einem Computer hinzugefügt oder daraus gelöscht werden.

Nachdem Sie einen optischen Recorder gefunden und seine ID abgerufen haben, erstellen Sie ein **MsftDiscRecorder2** -Objekt, und initialisieren Sie den Recorder mithilfe der Geräte-ID. Die [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) -Schnittstelle bietet Zugriff auf das Recorder-Objekt sowie einige grundlegende Geräteinformationen wie Hersteller-ID, Produkt-ID, Produkt Revision und Methoden, um die Medien zu auswerfen und die Leiste zu schließen.

## <a name="create-a-data-writer-and-write-the-burn-image"></a>Erstellen eines Daten Writers und Schreiben des Verbrauchs Abbilds

Das **MsftDiscFormat2Data** -Objekt stellt die Schreibmethode, die Eigenschaften über die Schreibfunktion und die medienspezifischen Eigenschaften bereit. Die [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) -Schnittstelle bietet Zugriff auf das **MsftDiscFormat2Data** -Objekt.

Der Disk Recorder verknüpft mithilfe der [**IDiscFormat2Data::p UT \_ Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) -Eigenschaft mit dem Format Schreiber. Nachdem der Recorder an das Format-Writer gebunden wurde, können Sie Abfragen bezüglich der Medien ausführen und Schreib spezifische Eigenschaften aktualisieren, bevor Sie das Ergebnisbild mithilfe der [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) -Methode auf die Festplatte schreiben.

Andere von IMAPI bereitgestellte Schnittstellen zum Schreiben von Formaten funktionieren ähnlich. zusätzliche Schnittstellen zum Schreiben von Formaten umfassen Folgendes:

-   [**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase) löscht erneut beschreibbare optische Medien.
-   [**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd) schreibt ein RAW-Image in optische Medien.
-   [**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce) schreibt Audiospuren in optische Medien.

> [!Note]  
> Es ist möglich, dass bei einem Verbrennungsvorgang (d. h. beim Abmelden des Benutzers oder beim Aussetzen des Systems) ein Strom Status Übergang stattfindet. Dies führt zu einer Unterbrechung des Verbrauchs und möglichen Datenverlusten. Informationen zur Programmierung finden Sie unter verhindern der Abmeldung [oder aussetzen während eines Burn](preventing-logoff-or-suspend-during-a-burn.md)-Vorgangs.

 

## <a name="vbscript-example"></a>VBScript-Beispiel

In diesem Skript Beispiel wird gezeigt, wie die IMAPI-Objekte zum Brennen von optischen Medien verwendet werden. genauer gesagt, schreiben Sie ein Verzeichnis auf eine leere CD. Der Code enthält keine Fehlerüberprüfung, und es wird Folgendes vorausgesetzt:

-   Auf dem System ist ein kompatibles CD-Gerät installiert.
-   Das Geräte Datenträger ist das zweite Laufwerk des Systems.
-   Ein kompatibles Laufwerk wird auf dem Festplattengerät eingefügt.
-   Die Festplatte ist leer.
-   Dateien, die auf den Datenträger geschrieben werden sollen, befinden sich in "g: \\ burndir".

Diesem Skript können zusätzliche Funktionen hinzugefügt werden, wie z. b. Fehlerüberprüfung, Geräte-und Medienkompatibilität, Ereignis Benachrichtigung und die Berechnung des freien Speicherplatzes auf der Festplatte.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von IMAPI](using-imapi.md)
</dt> <dt>

[**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase)
</dt> <dt>

[**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd)
</dt> <dt>

[**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce)
</dt> <dt>

[**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2)
</dt> <dt>

[**Ifilesystemimage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> <dt>

[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> </dl>

 

 