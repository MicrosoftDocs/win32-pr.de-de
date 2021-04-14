---
title: Bereitstellen von Dateidaten
description: Beschreibt, wie ein Anbieter Platzhalter Informationen und Datei Daten bereitstellt.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/01/2018
ms.topic: article
ms.openlocfilehash: 341a0f1c477b605b2a437edf311c380910744ac0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390688"
---
# <a name="providing-file-data"></a>Bereitstellen von Dateidaten

Wenn ein Anbieter erstmalig einen virtualisierungsstamm erstellt, ist er auf dem lokalen System leer. Das heißt, keines der Elemente im Sicherungsdaten Speicher wurde noch auf dem Datenträger zwischengespeichert. Wenn Elemente geöffnet werden, fordert projfs Informationen vom Anbieter an, damit Platzhalter für diese Elemente im lokalen Dateisystem erstellt werden können.  Beim Zugriff auf den Element Inhalt fordert projfs diese Inhalte vom Anbieter an.  Das Ergebnis ist, dass virtualisierte Dateien und Verzeichnisse aus Sicht des Benutzers ähnlich wie normale Dateien und Verzeichnisse angezeigt werden, die sich bereits im lokalen Dateisystem befinden.

## <a name="placeholder-creation"></a>Platzhalter Erstellung

Wenn eine Anwendung versucht, ein Handle für eine virtualisierte Datei zu öffnen, ruft projfs den **[PRJ_GET_PLACEHOLDER_INFO_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb)** Rückruf für jedes Element des Pfads auf, der noch nicht auf dem Datenträger vorhanden ist.  Wenn z. b. versucht wird, eine Anwendung zu öffnen `C:\virtRoot\dir1\dir2\file.txt` , aber nur der Pfad auf dem Daten `C:\virtRoot\dir1` Träger vorhanden ist, empfängt der Anbieter einen Rückruf für `C:\virtRoot\dir1\dir2` und dann für `C:\virtRoot\dir1\dir2\file.txt` .

Wenn projfs den **PRJ_GET_PLACEHOLDER_INFO_CB** Rückruf des Anbieters aufruft, führt der Anbieter die folgenden Aktionen aus:

1. Der Anbieter bestimmt, ob der angeforderte Name im Sicherungs Speicher vorhanden ist.  Der Anbieter sollte **[prjdatamecompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** als Vergleichs Routine beim Durchsuchen des Sicherungs Speicher verwenden, um zu bestimmen, ob der angeforderte Name im Sicherungs Speicher vorhanden ist.  Wenn dies nicht der Fall ist, gibt der Anbieter HRESULT_FROM_WIN32 (ERROR_FILE_NOT_FOUND) aus dem Rückruf zurück.

1. Wenn der angeforderte Name im Sicherungs Speicher vorhanden ist, füllt der Anbieter eine [PRJ_PLACEHOLDER_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_info) Struktur mit den Dateisystem Metadaten des Elements auf und ruft **[prjschreiteplaceholderinfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** auf, um die Daten an projfs zu senden.  Diese Informationen werden von projfs verwendet, um einen Platzhalter im lokalen Dateisystem für das Element zu erstellen.

    > Projfs verwendet alle FILE_ATTRIBUTE Flags, die der Anbieter im **filebasicinfo. fileattributmember** von PRJ_PLACEHOLDER_INFO mit Ausnahme von FILE_ATTRIBUTE_DIRECTORY enthält. Er legt den korrekten Wert für FILE_ATTRIBUTE_DIRECTORY im **filebasicinfo. fileattributmember** gemäß dem angegebenen Wert des Elements **filebasicinfo. IsDirectory** fest.

    > Wenn der Sicherungs Speicher symbolische Verknüpfungen unterstützt, muss der Anbieter **[PrjWritePlaceholderInfo2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2)** verwenden, um die Platzhalter Daten an projfs zu senden.  **PrjWritePlaceholderInfo2** unterstützt eine zusätzliche Puffer Eingabe, die es dem Anbieter ermöglicht, anzugeben, dass der Platzhalter eine symbolische Verknüpfung und das Ziel ist.  Andernfalls verhält es sich wie oben beschrieben für **prjschreiteplaceholderinfo**.  Im folgenden Beispiel wird veranschaulicht, wie **PrjWritePlaceholderInfo2** verwendet wird, um symbolische Verknüpfungen zu unterstützen.
    >
    > Beachten Sie, dass **PrjWritePlaceholderInfo2** ab Windows 10, Version 2004, unterstützt wird.  Ein Anbieter sollte überprüfen, ob PrjWritePlaceholderInfo2 vorhanden ist, z. . mithilfe von **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.

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

Wenn projfs sicherstellen muss, dass eine virtualisierte Datei Daten enthält, z. b. Wenn eine Anwendung versucht, aus der Datei zu lesen, ruft projfs den **[PRJ_GET_FILE_DATA_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** Rückruf für dieses Element auf, um anzufordern, dass der Anbieter den Inhalt der Datei bereitstellt.  Der Anbieter Ruft die Daten der Datei aus dem Sicherungs Speicher ab und verwendet **[prjschreitefiledata](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata)** , um die Daten an das lokale Dateisystem zu senden.

> Wenn dieser Rückruf von projfs aufgerufen wird, gibt das **FilePathName** -Element des _callBackData_ -Parameters den Namen an, den die Datei bei der Erstellung des Platzhalters enthielt.  Das heißt, wenn die Datei umbenannt wurde, seit der Platzhalter erstellt wurde, stellt der Rückruf den ursprünglichen Namen (vor dem Umbenennen) und nicht den aktuellen Namen (nach dem Umbenennen) bereit.  Bei Bedarf kann der Anbieter den **VERSIONINFO** -Member des _callBackData_ -Parameters verwenden, um zu bestimmen, welche Datei Daten angefordert werden.
>
> Weitere Informationen zur Verwendung des **VERSIONINFO** -Members von PRJ_CALLBACK_DATA finden Sie in der Dokumentation zu [PRJ_PLACEHOLDER_VERSION_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info) und im Thema [Bearbeiten von Änderungs Änderungen](handling-view-changes.md) .

Der Anbieter darf den Bereich der im **PRJ_GET_FILE_DATA_CB** Rückruf angeforderten Daten in mehrere Aufrufe von **prjschreitefiledata** aufteilen, die jeweils einen Teil des angeforderten Bereichs bereitstellen.  Der Anbieter muss jedoch den gesamten angeforderten Bereich angeben, bevor der Rückruf abgeschlossen wird.  Wenn der Rückruf z. b. 10 MB von _Byteoffset_ 0 für die _Länge_ 10.485.760 anfordert, kann der Anbieter die Daten in 10 Aufrufen an **prjschreitefiledata** bereitstellen, die jeweils 1 MB senden.

Der Anbieter kann auch mehr als den angeforderten Bereich angeben, bis zur Länge der Datei.  Der Bereich, den der Anbieter bereitstellt, muss den angeforderten Bereich abdecken.  Wenn der Rückruf z. b. 1 MB Daten von _Byteoffset_ 4096 für die _Länge_ 1.052.672 anfordert und die Datei eine Gesamtgröße von 10 MB hat, kann der Anbieter die Rückgabe von 2 MB Daten ab dem Offset 0 auswählen.

### <a name="buffer-alignment-considerations"></a>Überlegungen zur Puffer Ausrichtung

Projfs verwendet die [FILE_OBJECT](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) des Aufrufers, der die Daten zum Schreiben der Daten in das lokale Dateisystem benötigt.  Projfs kann jedoch nicht steuern, ob diese FILE_OBJECT für gepufferte oder nicht gepufferte e/a-Vorgänge geöffnet wurde.  Wenn die FILE_OBJECT für nicht gepufferte e/a-Vorgänge geöffnet wurde, müssen Lese-und Schreibvorgänge in die Datei bestimmte Ausrichtungs Anforderungen einhalten.  Der Anbieter kann diese Ausrichtungs Anforderungen durch zwei Dinge erfüllen:

1. Verwenden Sie **[prjallocatealignedbuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer)** , um den Puffer zuzuweisen, der in den _Puffer_ Parameter **prjschreitefiledata** übergeben werden soll.
1. Stellen Sie sicher, dass die Parameter " _Byteoffset_ " und " _length_ " von " **prjschreitefiledata** " ein ganzzahliges Vielfache der Ausrichtungs Anforderung des Speichergeräts sind (Beachten Sie, dass der _length_ -Parameter diese Anforderung nicht erfüllen muss, wenn die _Byteoffset_-  +  _Länge_ gleich dem Dateiende ist).  Der Anbieter kann **[prjgetvirtualizationinstanceinfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo)** verwenden, um die Ausrichtungs Anforderung des Speichergeräts abzurufen.

Projfs verlässt den Anbieter, um die richtige Ausrichtung zu berechnen.  Dies liegt daran, dass bei der Verarbeitung eines **PRJ_GET_FILE_DATA_CB** Rückrufs der Anbieter die angeforderten Daten möglicherweise über mehrere **prjwrite tefiledata** -Aufrufe zurückgibt, die jeweils einen Teil der gesamten angeforderten Daten zurückgeben, bevor Sie den Rückruf abschließen.

> Wenn der Anbieter einen einzelnen Befehl an **prjschreitefiledata** verwenden soll, um entweder die gesamte Datei zu schreiben, d. h. von _Byteoffset_ = 0 bis _length_ = Größe der Datei, oder wenn der genaue Bereich zurückgegeben werden soll, der im **PRJ_GET_FILE_DATA_CB** Rückruf angefordert wurde, muss der Anbieter keine Ausrichtungs Berechnungen durchführen.  Es muss jedoch weiterhin **prjzuzucatealignedbuffer** verwendet werden, um sicherzustellen, dass der _Puffer_ den Ausrichtungs Anforderungen des Speichergeräts entspricht.

Weitere Informationen zu gepufferten und nicht gepufferten e/a-Vorgängen finden Sie im Thema [Datei Pufferung](/windows/desktop/FileIO/file-buffering) .

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