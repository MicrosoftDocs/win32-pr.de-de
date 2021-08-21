---
title: Bereitstellen von Dateidaten
description: Beschreibt, wie ein Anbieter Platzhalterinformationen und Dateidaten liefert.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/01/2018
ms.topic: article
ms.openlocfilehash: 4f0da65095e908ec3211bb23be654ee9e0e2853c093bb36e8a92701c24106ff4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792394"
---
# <a name="providing-file-data"></a>Bereitstellen von Dateidaten

Wenn ein Anbieter zum ersten Mal einen Virtualisierungsstamm erstellt, ist er auf dem lokalen System leer. Das heißt, dass noch keins der Elemente im Hintergrunddatenspeicher auf dem Datenträger zwischengespeichert wurde. Wenn Elemente geöffnet werden, fordert ProjFS Informationen vom Anbieter an, damit Platzhalter für diese Elemente im lokalen Dateisystem erstellt werden können.  Wenn auf Elementinhalte zugegriffen wird, fordert ProjFS diese Inhalte vom Anbieter an.  Das Ergebnis ist, dass virtualisierte Dateien und Verzeichnisse aus Sicht des Benutzers den normalen Dateien und Verzeichnissen ähneln, die sich bereits im lokalen Dateisystem befinden.

## <a name="placeholder-creation"></a>Platzhaltererstellung

Wenn eine Anwendung versucht, ein Handle für eine virtualisierte Datei zu öffnen, ruft ProjFS den **[PRJ_GET_PLACEHOLDER_INFO_CB-Rückruf](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb)** für jedes Element des Pfads auf, das noch nicht auf dem Datenträger vorhanden ist.  Wenn eine Anwendung beispielsweise versucht, zu öffnen, aber nur der Pfad auf dem Datenträger vorhanden ist, erhält der Anbieter einen Rückruf für `C:\virtRoot\dir1\dir2\file.txt` `C:\virtRoot\dir1` , dann für `C:\virtRoot\dir1\dir2` `C:\virtRoot\dir1\dir2\file.txt` .

Wenn ProjFS den PRJ_GET_PLACEHOLDER_INFO_CB-Rückruf des Anbieters aufruft, führt der Anbieter die folgenden Aktionen aus: 

1. Der Anbieter bestimmt, ob der angeforderte Name in seinem Hintergrundspeicher vorhanden ist.  Der Anbieter sollte **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** als Vergleichsroutine verwenden, um zu ermitteln, ob der angeforderte Name im Hintergrundspeicher vorhanden ist.  Wenn dies nicht der Wert ist, gibt der Anbieter HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND) aus dem Rückruf zurück.

1. Wenn der angeforderte Name im Hintergrundspeicher vorhanden ist, füllt der Anbieter eine [PRJ_PLACEHOLDER_INFO-Struktur](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_info) mit den Dateisystemmetadaten des Elements auf und ruft **[PrjWritePlaceholderInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** auf, um die Daten an ProjFS zu senden.  ProjFS verwendet diese Informationen, um einen Platzhalter im lokalen Dateisystem für das Element zu erstellen.

    > ProjFS verwendet alle FILE_ATTRIBUTE, die der Anbieter im **FileBasicInfo.FileAttributes-Member** von PRJ_PLACEHOLDER_INFO außer FILE_ATTRIBUTE_DIRECTORY; Sie wird den richtigen Wert für FILE_ATTRIBUTE_DIRECTORY im **FileBasicInfo.FileAttributes-Element** entsprechend dem angegebenen Wert des **FileBasicInfo.IsDirectory-Members** festlegen.

    > Wenn der Unterstützungsspeicher symbolische Verknüpfungen unterstützt, muss der Anbieter **[PrjWritePlaceholderInfo2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2)** verwenden, um die Platzhalterdaten an ProjFS zu senden.  **PrjWritePlaceholderInfo2** unterstützt eine zusätzliche Puffereingabe, mit der der Anbieter angeben kann, dass der Platzhalter eine symbolische Verknüpfung ist und was sein Ziel ist.  Andernfalls verhält es sich wie oben für **PrjWritePlaceholderInfo beschrieben.**  Im folgenden Beispiel wird veranschaulicht, wie **PrjWritePlaceholderInfo2** verwendet wird, um Unterstützung für symbolische Verknüpfungen zu bieten.
    >
    > Beachten **Sie, dass PrjWritePlaceholderInfo2** ab Windows 10 Version 2004 unterstützt wird.  Ein Anbieter sollte auf das Vorhandensein von **PrjWritePlaceholderInfo2** prüfen, z. B. mithilfe von **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.

```C++
HRESULT
MyGetPlaceholderInfoCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData
    )
{
    // MyGetItemInfo is a routine the provider might implement to get
    // information from its backing store for a given file path.  The first
    // parameter is an _In_ parameter that supplies the name to look for.
    // If the item exists the routine provides the file information in the
    // remaining parameters, all of which are annotated _Out_:
    // * 2nd parameter: the name as it appears in the backing store
    // * 3rd-9th parameters: basic file info
    // * 10th parameter: if the item is a symbolic link, a pointer to a 
    //   NULL-terminated string identifying the link's target
    //
    // Note that the routine returns the name that is in the backing
    // store.  This is because the input file path may not be in the same
    // case as what is in the backing store.  The provider should create
    // the placeholder with the name it has in the backing store.
    //
    // Note also that this example does not provide anything beyond basic
    // file information and a possible symbolic link target.
    HRESULT hr;
    WCHAR* backingStoreName = NULL;
    WCHAR* symlinkTarget = NULL;
    PRJ_PLACEHOLDER_INFO placeholderInfo = {};
    hr = MyGetItemInfo(callbackData->FilePathName,
                       &backingStoreName,
                       &placeholderInfo.FileBasicInfo.IsDirectory,
                       &placeholderInfo.FileBasicInfo.FileSize,
                       &placeholderInfo.FileBasicInfo.CreationTime,
                       &placeholderInfo.FileBasicInfo.LastAccessTime,
                       &placeholderInfo.FileBasicInfo.LastWriteTime,
                       &placeholderInfo.FileBasicInfo.ChangeTime,
                       &placeholderInfo.FileBasicInfo.FileAttributes,
                       &symlinkTarget);

    if (FAILED(hr))
    {
        // If callbackData->FilePathName doesn't exist in our backing store then
        // MyGetItemInfo should HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND).
        // If this is some other error, e.g. E_OUTOFMEMORY because MyGetItemInfo
        // couldn't allocate space for backingStoreName, we return that.
        return hr;
    }

    // If the file path is for a symbolic link, pass that in with the placeholder info.
    if (symlinkTarget != NULL)
    {
        PRJ_EXTENDED_INFO extraInfo = {};

        extraInfo.InfoType = PRJ_EXT_INFO_SYMLINK;
        extraInfo.Symlink.TargetName = symlinkTarget;

        // If this returns an error we'll want to return that error from the callback.
        hr = PrjWritePlaceholderInfo2(callbackData->NamespaceVirtualizationContext,
                                      backingStoreName,
                                      &placeholderInfo,
                                      sizeof(placeholderInfo),
                                      &extraInfo);
    }
    else
    {
        // If this returns an error we'll want to return that error from the callback.
        hr = PrjWritePlaceholderInfo(callbackData->NamespaceVirtualizationContext,
                                     backingStoreName,
                                     &placeholderInfo,
                                     sizeof(placeholderInfo));
    }

    free(backingStoreName);

    if (symlinkTarget != NULL)
    {
        free(symlinkTarget);
    }

    return hr;
}
```

## <a name="providing-file-contents"></a>Bereitstellen von Dateiinhalten

Wenn ProjFS sicherstellen muss, dass eine virtualisierte Datei Daten enthält, z. B. wenn eine Anwendung versucht, aus der Datei zu lesen, ruft ProjFS den **[PRJ_GET_FILE_DATA_CB-Rückruf](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** für dieses Element auf, um an die Bereitstellung des Dateiinhalts durch den Anbieter zu fragen.  Der Anbieter ruft die Daten der Datei aus seinem Hintergrundspeicher ab und verwendet **[PrjWriteFileData,](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata)** um die Daten an das lokale Dateisystem zu senden.

> Wenn ProjFS diesen Rückruf aufruft, gibt das **FilePathName-Element** des _callbackData-Parameters_ den Namen an, den die Datei beim Erstellen des Platzhalters hatte.  Das heißt, wenn die Datei seit dem Erstellen des Platzhalters umbenannt wurde, gibt der Rückruf den ursprünglichen Namen (vor dem Umbenennen) und nicht den aktuellen Namen (nach dem Umbenennen) an.  Bei Bedarf kann der Anbieter den **VersionInfo-Member** des _callbackData-Parameters_ verwenden, um zu bestimmen, welche Dateidaten angefordert werden.
>
> Weitere Informationen dazu, wie das **VersionInfo-Element** von PRJ_CALLBACK_DATA verwendet [](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info) werden kann, finden Sie in der Dokumentation zu PRJ_PLACEHOLDER_VERSION_INFO und im Thema Behandeln von [Ansichtsänderungen.](handling-view-changes.md)

Der Anbieter darf den im **PRJ_GET_FILE_DATA_CB-Rückruf** angeforderten Datenbereich in mehrere Aufrufe von **PrjWriteFileData** aufteilen, die jeweils einen Teil des angeforderten Bereichs angeben.  Der Anbieter muss jedoch den gesamten angeforderten Bereich vor abschluss des Rückrufs zur Verfügung stellen.  Wenn der Rückruf beispielsweise 10 MB Daten von _byteOffset_ 0 für die Länge  10.485.760 an fordert, kann der Anbieter die Daten in 10 Aufrufen von **PrjWriteFileData** angeben, die jeweils 1 MB senden.

Der Anbieter kann auch mehr als den angeforderten Bereich bis zur Länge der Datei zur Verfügung stellen.  Der Bereich, den der Anbieter zur Verfügung stellt, muss den angeforderten Bereich abdecken.  Wenn der Rückruf z. B. 1 MB daten von _byteOffset_ 4096 für die Länge  1.052.672 an fordert und die Datei eine Gesamtgröße von 10 MB hat, kann der Anbieter auswählen, dass ab Offset 0 2 MB Daten zurückgeben.

### <a name="buffer-alignment-considerations"></a>Überlegungen zur Pufferausrichtung

ProjFS verwendet [die](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) FILE_OBJECT des Aufrufers, der die Daten zum Schreiben der Daten in das lokale Dateisystem benötigt.  ProjFS kann jedoch nicht steuern, ob FILE_OBJECT für gepufferte oder ungepufferte E/A geöffnet wurde.  Wenn der FILE_OBJECT für ungepufferte E/A geöffnet wurde, müssen Lese- und Schreibvorgänge in die Datei bestimmte Ausrichtungsanforderungen erfüllen.  Der Anbieter kann diese Ausrichtungsanforderungen durch zwei Dinge erfüllen:

1. Verwenden **[Sie PrjAllocateAlignedBuffer,](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer)** um den Puffer zu zuordnen, um den Pufferparameter von **PrjWriteFileData** _zu_ übergeben.
1. Stellen Sie sicher, dass die Parameter _byteOffset_ und _length_ von **PrjWriteFileData** ganzzahlige Vielfache der Ausrichtungsanforderung des Speichergeräts sind (beachten Sie, dass der _length-Parameter_ diese Anforderung nicht erfüllen muss, wenn _byteOffset_ length gleich dem Ende der Datei  +   ist).  Der Anbieter kann **[prjGetVirtualizationInstanceInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo)** verwenden, um die Ausrichtungsanforderung des Speichergeräts abzurufen.

ProjFS überlässt es dem Anbieter, die richtige Ausrichtung zu berechnen.  Dies liegt daran, dass der Anbieter bei der Verarbeitung eines **PRJ_GET_FILE_DATA_CB-Rückrufs** die angeforderten Daten über mehrere **PrjWriteFileData-Aufrufe** hinweg zurückgeben kann, die jeweils einen Teil der insgesamt angeforderten Daten zurückgeben, bevor der Rückruf abgeschlossen wird.

> Wenn der Anbieter einen einzelnen Aufruf von **PrjWriteFileData** verwendet, um entweder die gesamte Datei zu schreiben, d. h. von _byteOffset_ = 0 bis _length_ = Größe der Datei, oder um den genauen Bereich zurück zu geben, der im **PRJ_GET_FILE_DATA_CB-Rückruf** angefordert wird, muss der Anbieter keine Ausrichtungsberechnungen durchführen.  Es muss jedoch weiterhin **PrjAllocateAlignedBuffer**  verwenden, um sicherzustellen, dass der Puffer die Ausrichtungsanforderungen des Speichergeräts erfüllt.

Weitere Informationen zu [gepufferten](/windows/desktop/FileIO/file-buffering) und nicht gepufferten E/A-Daten finden Sie im Thema Dateipufferung.

```C++
//  BlockAlignTruncate(): Aligns P on the previous V boundary (V must be != 0).
#define BlockAlignTruncate(P,V) ((P) & (0-((UINT64)(V))))

// This sample illustrates both returning the entire requested range in a
// single call to PrjWriteFileData(), and splitting it up into smaller 
// units.  Note that the provider must return all the requested data before
// completing the PRJ_GET_FILE_DATA_CB callback with S_OK.
HRESULT
MyGetFileDataCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData,
    _In_ UINT64 byteOffset,
    _In_ UINT32 length
    )
{
    HRESULT hr;

    // For the purposes of this sample our provider has a 1 MB limit to how
    // much data it can return at once (perhaps its backing store imposes such
    // a limit).
    UINT64 writeStartOffset;
    UINT32 writeLength;
    if (length <= 1024*1024)
    {
        // The range requested in the callback is less than 1MB, so we can return
        // the data in a single call, without doing any alignment calculations.
        writeStartOffset = byteOffset;
        writeLength = length;
    }
    else
    {
        // The range requested is more than 1MB.  Retrieve the device alignment
        // and calculate a transfer size that conforms to the device alignment and
        // is <= 1MB.
        PRJ_VIRTUALIZATION_INSTANCE_INFO instanceInfo;
        UINT32 infoSize = sizeof(instanceInfo);
        hr = PrjGetVirtualizationInstanceInfo(callbackData->NamespaceVirtualizationContext,
                                              &infoSize,
                                              &instanceInfo);

        if (FAILED(hr))
        {
            return hr;
        }

        // The first transfer will start at the beginning of the requested range,
        // which is guaranteed to have the correct alignment.
        writeStartOffset = byteOffset;

        // Ensure our transfer size is aligned to the device alignment, and is
        // no larger than 1 MB (note this assumes the device alignment is less
        // than 1 MB).
        UINT64 writeEndOffset = BlockAlignTruncate(writeStartOffset + 1024*1024,
                                                   instanceInfo->WriteAlignment);
        assert(writeEndOffset > 0);
        assert(writeEndOffset > writeStartOffset);

        writeLength = writeEndOffset - writeStartOffset;
    }

    // Allocate a buffer that adheres to the needed memory alignment.
    void* writeBuffer = NULL;
    writeBuffer = PrjAllocateAlignedBuffer(callbackData->NamespaceVirtualizationContext,
                                           writeLength);

    if (writeBuffer == NULL)
    {
        return E_OUTOFMEMORY;
    }

    do
    {
        // MyGetFileDataFromStore is a routine the provider might implement to copy
        // data for the specified file from the provider's backing store to a
        // buffer.  The routine finds the file located at callbackData->FilePathName
        // and copies writeLength bytes of its data, starting at writeStartOffset,
        // to the buffer pointed to by writeBuffer.
        hr = MyGetFileDataFromStore(callbackData->FilePathName,
                                    writeStartOffset,
                                    writeLength,
                                    writeBuffer);

        if (FAILED(hr))
        {
            PrjFreeAlignedBuffer(writeBuffer);
            return hr;
        }

        // Write the data to the file in the local file system.
        hr = PrjWriteFileData(callbackData->NamespaceVirtualizationContext,
                              callbackData->DataStreamId,
                              writeBuffer,
                              writeStartOffset,
                              writeLength);

        if (FAILED(hr))
        {
            PrjFreeAlignedBuffer(writeBuffer);
            return hr;
        }

        // The length parameter to the callback is guaranteed to be either
        // correctly aligned or to result in a write to the end of the file.
        length -= writeLength;
        if (length < writeLength)
        {
            writeLength = length;
        }
    }
    while (writeLength > 0);

    PrjFreeAlignedBuffer(writeBuffer);
    return hr;
}
```