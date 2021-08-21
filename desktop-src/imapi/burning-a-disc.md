---
title: Verwerfen eines Datenträgerbilds
description: Das Mastering (Verwerfen eines Datenträgers) mithilfe der IMAPI besteht aus den folgenden Schritten Erstellen eines Dateisystemimages, das die Verzeichnisse und Dateien zum Schreiben von Datenträgern enthält. Richten Sie einen Datenträgerrecorder für die Kommunikation mit dem optischen Gerät ein. Erstellen Sie einen Datenwriter, und verwerten Sie das Image auf einen Datenträger.
ms.assetid: f2eee14e-695d-4678-b3c1-b521ab4d4a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 237a4aa73b6820b75b4a9a1ed03baeeb87ac093bfc549cb9cc0ed947077515dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758910"
---
# <a name="burning-a-disc-image"></a>Verwerfen eines Datenträgerbilds

Das Mastering (Bearbeiten eines Datenträgers) mithilfe von IMAPI besteht aus den folgenden Schritten:

1.  Erstellen Sie ein Dateisystemimage, das die Verzeichnisse und Dateien zum Schreiben von Datenträgern enthält.
2.  [Richten Sie einen Datenträgerrecorder](#set-up-a-disc-recorder) für die Kommunikation mit dem optischen Gerät ein.
3.  [Erstellen Sie einen Datenwriter,](#create-a-data-writer-and-write-the-burn-image) und verwerten Sie das Image auf einen Datenträger.

Ein Beispiel, in dem ein Datenträgerbild verätzt wird, finden Sie unter [VBScript-Beispiel.](#vbscript-example)

## <a name="construct-a-burn-image"></a>Erstellen eines Burn-Images

Ein Burn-Image ist ein Datenstrom, der bereit ist, auf optische Medien geschrieben zu werden. Das Burn-Image für die Formate ISO9660, Joliet und UDF besteht aus einem Dateisystem einzelner Dateien und Verzeichnisse. Das **CFileSystemImage-Objekt** ist das Dateisystemobjekt, das die Dateien und Verzeichnisse enthält, die auf den optischen Medien gespeichert werden sollen. Die [**IFileSystemImage-Schnittstelle**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) ermöglicht den Zugriff auf das Dateisystemobjekt und die Einstellungen.

Rufen Sie nach dem Erstellen des Dateisystemobjekts die Methoden [**IFileSystemImage::CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) und [**IFileSystemImage::CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) auf, um die Datei- bzw. Verzeichnisobjekte zu erstellen. Die Datei- und Verzeichnisobjekte können verwendet werden, um spezifische Details zur Datei und zum Verzeichnis bereitzustellen. Die für [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) verfügbaren Ereignishandlermethoden können die aktuelle Datei, die dem Dateisystemimage hinzugefügt wird, die Anzahl der bereits kopierten Sektoren und die Gesamtzahl der zu kopierenden Sektoren identifizieren.

Optional kann ein Startimage mithilfe der Eigenschaft [**IFileSystemImage::p ut \_ BootImageOptions**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions) an das Dateisystem angefügt werden. Ein Beispiel finden Sie unter [Hinzufügen eines Startabbilds.](adding-a-boot-image.md)

Rufen Sie abschließend [**IFileSystemImage::CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) auf, um einen Datenstrom zu erstellen, und ermöglicht den Zugriff über [**IFileSystemImageResult.**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult) Der neue Datenstrom kann dann direkt für die [**IDiscFormat2Data::Write-Methode**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) bereitgestellt oder zur späteren Verwendung in einer Datei gespeichert werden.

## <a name="set-up-a-disc-recorder"></a>Einrichten eines Datenträgeraufzeichnungsgeräts

Das **MsftDiscMaster2-Objekt** stellt eine Enumeration der optischen Geräte auf dem System bereit. Die [**IDiscMaster2-Schnittstelle**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) bietet Zugriff auf die resultierende Geräteenumeration. Durchlaufen Sie die Enumerationen, um ein geeignetes Aufzeichnungsgerät zu finden. Das **MsftDiscMaster2-Objekt** stellt auch Ereignisbenachrichtigungen bereit, wenn einem Computer optische Geräte hinzugefügt oder daraus gelöscht werden.

Nachdem Sie einen optischen Aufzeichnungsgerät gefunden und seine ID abgerufen haben, erstellen Sie ein **MsftDiscRecorder2-Objekt,** und initialisieren Sie den Aufzeichnungsdatenträger mithilfe der Geräte-ID. Die [**IDiscRecorder2-Schnittstelle**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) bietet Zugriff auf das Aufzeichnungsobjekt sowie einige grundlegende Geräteinformationen wie Anbieter-ID, Produkt-ID, Produktrevision und Methoden zum Auswerfen der Medien und Schließen der Taskleiste.

## <a name="create-a-data-writer-and-write-the-burn-image"></a>Erstellen eines Datenwriters und Schreiben des Burn-Images

Das **MsftDiscFormat2Data-Objekt** stellt die Schreibmethode, die Eigenschaften der Schreibfunktion und medienspezifische Eigenschaften bereit. Die [**IDiscFormat2Data-Schnittstelle**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) bietet Zugriff auf das **MsftDiscFormat2Data-Objekt.**

Die Datenträgeraufzeichnung ist mithilfe der [**IDiscFormat2Data::p ut \_ Recorder-Eigenschaft**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) mit dem Formatwriter verknüpft. Nachdem die Aufzeichnung an den Formatwriter gebunden wurde, können Sie Abfragen zu den Medien ausführen und schreibspezifische Eigenschaften aktualisieren, bevor Sie das Ergebnisbild mit der [**IDiscFormat2Data::Write-Methode**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) auf einen Datenträger schreiben.

Andere Formatschreibschnittstellen, die von DER IMAPI bereitgestellt werden, funktionieren ähnlich. Zusätzliche Schnittstellen zum Schreiben von Formaten:

-   [**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase) löscht umschreibbare optische Medien.
-   [**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd) schreibt ein Rohbild in optische Medien.
-   [**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce) schreibt Audiospuren in optische Medien.

> [!Note]  
> Es ist möglich, dass ein Energiezustandsübergang während eines Burn-Vorgangs (d. h. Abmeldung des Benutzers oder Systemunterbrechung) stattfindet, was zu einer Unterbrechung des Verbrandungsprozesses und einem möglichen Datenverlust führt. Überlegungen zur Programmierung finden Sie unter [Verhindern von Abmeldung oder Anhalten während eines Brandes.](preventing-logoff-or-suspend-during-a-burn.md)

 

## <a name="vbscript-example"></a>VBScript-Beispiel

Dieses Skriptbeispiel zeigt, wie Sie die IMAPI-Objekte verwenden, um optische Medien zu verdrehen. Schreiben Sie genauer gesagt ein Verzeichnis auf einen leeren Datenträger. Der Code enthält keine Fehlerüberprüfung und geht von Folgendem aus:

-   Auf dem System ist ein kompatibles Datenträgergerät installiert.
-   Das Datenträgergerät ist das zweite Laufwerk im System.
-   Ein kompatibler Datenträger wird in das Datenträgergerät eingefügt.
-   Der Datenträger ist leer.
-   Dateien, die auf den Datenträger geschrieben werden sollen, befinden sich in "g: \\ burndir".

Diesem Skript können zusätzliche Funktionen wie Fehlerüberprüfung, Geräte- und Medienkompatibilität, Ereignisbenachrichtigung und Berechnung des freien Speicherplatzes auf dem Datenträger hinzugefügt werden.


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

[**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> <dt>

[**Istream**](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> </dl>

 

 