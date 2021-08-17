---
title: Lebenszyklus von Virtualisierungsinstanzen
description: Übersicht über den Lebenszyklus einer ProjFS-Virtualisierungsinstanz.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/17/2018
ms.topic: article
ms.openlocfilehash: bbaaf5eca5481f3959e3e5afeb36a8cf6b264c939e8eb2cc9d84ba501d3c8530
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792384"
---
# <a name="virtualization-instance-lifecycle"></a>Lebenszyklus von Virtualisierungsinstanzen

Die Anbieteranwendung verwaltet eine oder mehrere Virtualisierungsinstanzen.  Jede Virtualisierungsinstanz durchläuft vier Phasen ihres Lebenszyklus:

1. Erstellung
2. Start
3. Typ
4. Herunterfahren

Beachten Sie, dass der Anbieter nach dem Herunterfahren einer Virtualisierungsinstanz diese nicht neu erstellen muss, um sie wiederzuverwenden.  Es kann einfach neu gestartet werden.

> **Hinweis:** In diesem Abschnitt werden Beispiele für ProjFS-APIs gezeigt.  Jedes Beispiel soll die grundlegende API-Nutzung veranschaulichen.  Eine Dokumentation der optionen, die in diesen Beispielen nicht verwendet werden, finden Sie in der [Referenz zur ProjFS-API.](/windows/desktop/api/_projfs)

## <a name="creating-a-virtualization-root"></a>Erstellen eines Virtualisierungsstamms

Bevor ein Anbieter die Virtualisierungsinstanz starten kann, die Elemente in das lokale Dateisystem projectt, muss er den Virtualisierungsstamm erstellen.  Der Virtualisierungsstamm ist das Verzeichnis, in dem der Anbieter eine Struktur von Verzeichnissen und Dateien probiert.

Um einen Virtualisierungsstamm zu erstellen, muss der Anbieter:

1. Erstellen Sie ein Verzeichnis, das als Virtualisierungsstamm dient.

    Der Anbieter erstellt ein Verzeichnis, das als Virtualisierungsstamm verwendet wird, z. B. **[CreateDirectory:](/windows/desktop/api/fileapi/nf-fileapi-createdirectoryw)**

    ```C++
    HRESULT hr;
    const wchar_t* rootName = LR"(C:\virtRoot)";
    if (!CreateDirectoryW(rootName, nullptr))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        wprintf(L"Failed to create virtualization root (0x%08x)\n", hr);
        return;
    }
    ```

1. Erstellen Sie eine Virtualisierungsinstanz-ID.

    Jede Virtualisierungsinstanz verfügt über eine eindeutige ID, die als _Virtualisierungsinstanz-ID bezeichnet wird._  Das System verwendet diesen Wert, um zu identifizieren, welcher Virtualisierungsinstanz sein Inhalt zugeordnet ist.

    ```C++
    GUID instanceId;
    hr = CoCreateGuid(&instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to create instance ID (0x%08x)\n", hr);
        return;
    }
    ```

1. Markieren Sie das neue Verzeichnis als Virtualisierungsstamm.

    Der Anbieter ruft **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** auf, um das neue Verzeichnis als Virtualisierungsstamm zu markieren und der Virtualisierungsinstanz zu zuweisen.

    ```C++
    hr = PrjMarkDirectoryAsPlaceholder(rootName,
                                       nullptr,
                                       nullptr,
                                       &instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to mark virtualization root (0x%08x)\n", hr);
        return;
    }
    ```

Der Anbieter muss den Virtualisierungsstamm nur einmal für jede Virtualisierungsinstanz erstellen.  Nachdem ein Stamm erstellt wurde, kann die zugehörige Instanz wiederholt gestartet und beendet werden, ohne den Stamm neu zu erstellen.

## <a name="starting-a-virtualization-instance"></a>Starten einer Virtualisierungsinstanz

Nachdem der Virtualisierungsstamm erstellt wurde, muss der Anbieter die Virtualisierungsinstanz starten.  Dies signalisiert ProjFS, dass der Anbieter bereit ist, Rückrufe zu empfangen und Daten zur Verfügung zu stellen.

Um die Virtualisierungsinstanz zu starten, muss der Anbieter:

1. Richten Sie die Rückruftabelle ein.

    ProjFS kommuniziert mit dem Anbieter durch Aufrufen von Rückrufroutinen, die vom Anbieter implementiert werden.  Der Anbieter füllt eine [PRJ_CALLBACKS](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callbacks) Struktur mit Zeigern auf seine Rückrufroutinen auf.

    ```C++
    PRJ_CALLBACKS callbackTable;

    // Supply required callbacks.
    callbackTable.StartDirectoryEnumerationCallback = MyStartEnumCallback;
    callbackTable.EndDirectoryEnumerationCallback = MyEndEnumCallback;
    callbackTable.GetDirectoryEnumerationCallback = MyGetEnumCallback;
    callbackTable.GetPlaceholderInfoCallback = MyGetPlaceholderInfoCallback;
    callbackTable.GetFileDataCallback = MyGetFileDataCallback;

    // The rest of the callbacks are optional.
    callbackTable.QueryFileNameCallback = nullptr;
    callbackTable.NotificationCallback = nullptr;
    callbackTable.CancelCommandCallback = nullptr;
    ```

1. Starten Sie die -Instanz.

    Der Anbieter ruft **[PrjStartVirtualizing auf,](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)** um die Virtualisierungsinstanz zu starten.

    ```C++
    PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT instanceHandle;
    hr = PrjStartVirtualizing(rootName,
                              &callbackTable,
                              nullptr,
                              nullptr,
                              &instanceHandle);
    if (FAILED(hr))
    {
        wprintf(L"Failed to start the virtualization instance (0x%08x)\n", hr);
        return;
    }
    ```
    **Der instanceHandle-Parameter von PrjStartVirtualizing** gibt ein Handle an die Virtualisierungsinstanz zurück.   Der Anbieter verwendet dieses Handle beim Aufrufen anderer ProjFS-APIs.

## <a name="virtualization-instance-runtime"></a>Virtualisierungsinstanzlaufzeit

Sobald der Aufruf von **PrjStartVirtualizing** zurückgegeben wird, ruft ProjFS die Rückrufroutinen des Anbieters als Reaktion auf Dateisystemvorgänge in der Virtualisierungsinstanz auf.  Informationen dazu, wie der Anbieter verschiedene Dateisystemvorgänge verarbeiten kann, finden Sie in den folgenden Abschnitten:

* [Auflisten von Dateien und Verzeichnissen](enumerating-files-and-directories.md)
* [Bereitstellen von Dateidaten](providing-file-data.md)
* [Dateisystem-Vorgangsbenachrichtigungen](file-system-operation-notifications.md)
* [Behandeln von Ansichtsänderungen](handling-view-changes.md)

## <a name="shutting-down-a-virtualization-instance"></a>Herunterfahren einer Virtualisierungsinstanz

Um ProjFS zu signalisieren, dass der Anbieter den Empfang von Rückrufen und die Bereitstellung von Daten beenden möchte, muss der Anbieter die Virtualisierungsinstanz beenden.  Hierzu ruft der Anbieter **[PrjStopVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing)** auf und über gibt das Handle an die Virtualisierungsinstanz weiter, die er vom Aufruf von **PrjStartVirtualizing erhalten hat.**

```C++
PrjStopVirtualizing(instanceHandle);
```

Beachten Sie, dass ProjFS die Rückrufroutinen des Anbieters weiterhin aufrufen kann, bis dieser Aufruf zurückgegeben wird.