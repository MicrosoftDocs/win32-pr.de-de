---
title: Lebenszyklus der virtualisierungsinstanz
description: Übersicht über den Lebenszyklus einer projfs-virtualisierungsinstanz.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/17/2018
ms.topic: article
ms.openlocfilehash: 567eff1f7b8acf330dba7c652e2e12b724072b9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516853"
---
# <a name="virtualization-instance-lifecycle"></a>Lebenszyklus der virtualisierungsinstanz

Die Anbieter Anwendung verwaltet mindestens eine virtualisierungsinstanz.  Jede virtualisierungsinstanz durchläuft vier Phasen in Ihrem Lebenszyklus:

1. Erstellung
2. Start
3. Typ
4. Shutdown

Beachten Sie, dass der Anbieter nach dem Herunterfahren einer virtualisierungsinstanz ihn nicht erneut erstellen muss, um ihn wiederzuverwenden.  Sie kann einfach erneut gestartet werden.

> **Hinweis**: in diesem Abschnitt werden Beispiele für projfs-APIs gezeigt.  Jedes Beispiel dient zur Veranschaulichung der grundlegenden API-Verwendung.  Eine Dokumentation der in diesen Beispielen nicht verwendeten Optionen finden Sie in der [projfs-API-Referenz](/windows/desktop/api/_projfs).

## <a name="creating-a-virtualization-root"></a>Erstellen eines virtualisierungsstamms

Bevor ein Anbieter die virtualisierungsinstanz starten kann, mit der Elemente in das lokale Dateisystem integriert werden, muss der virtualisierungsstamm erstellt werden.  Der virtualisierungsstamm ist das Verzeichnis, in dem der Anbieter eine Struktur von Verzeichnissen und Dateien projiziert.

Zum Erstellen eines virtualisierungsstamms muss der Anbieter folgende Aktionen ausführen:

1. Erstellen Sie ein Verzeichnis, das als virtualisierungsstamm fungiert.

    Der Anbieter erstellt ein Verzeichnis, das als virtualisierungsstamm verwendet werden soll, z. b. " **[kreatedirectory](/windows/desktop/api/fileapi/nf-fileapi-createdirectoryw)**":

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

1. Erstellen Sie eine Instanz-ID der Virtualisierung.

    Jede virtualisierungsinstanz verfügt über eine eindeutige ID, die als _virtualisierungsinstanz-ID_ bezeichnet wird.  Das System verwendet diesen Wert, um zu ermitteln, welcher virtualisierungsinstanz der Inhalt zugeordnet ist.

    ```C++
    GUID instanceId;
    hr = CoCreateGuid(&instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to create instance ID (0x%08x)\n", hr);
        return;
    }
    ```

1. Markieren Sie das neue Verzeichnis als virtualisierungsstamm.

    Der Anbieter ruft **[prjmarkdirectoryasplachalter](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** auf, um das neue Verzeichnis als virtualisierungsstamm zu markieren und es der virtualisierungsinstanz zuzuweisen.

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

Der Anbieter muss für jede virtualisierungsinstanz nur einmal den virtualisierungsstamm erstellen.  Nachdem ein Stamm erstellt wurde, kann die zugehörige Instanz wiederholt gestartet und beendet werden, ohne dass der Stamm neu erstellt wird.

## <a name="starting-a-virtualization-instance"></a>Starten einer virtualisierungsinstanz

Nachdem der virtualisierungsstamm erstellt wurde, muss der Anbieter die virtualisierungsinstanz starten.  Dadurch wird projfs signalisiert, dass der Anbieter bereit ist, Rückrufe zu empfangen und Daten bereitzustellen.

Zum Starten der virtualisierungsinstanz muss der Anbieter

1. Richten Sie die Rückruf Tabelle ein.

    Projfs kommuniziert mit dem Anbieter, indem Rückruf Routinen aufgerufen werden, die vom Anbieter implementiert werden.  Der Anbieter füllt eine [PRJ_CALLBACKS](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callbacks) Struktur mit Zeigern auf seine Rückruf Routinen auf.

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

1. Starten Sie die-Instanz.

    Der Anbieter ruft **[prjstartvirtualization](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)** auf, um die virtualisierungsinstanz zu starten.

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
    Der Parameter " _InstanceHandle_ " von **prjstartvirtualization** gibt ein Handle für die virtualisierungsinstanz zurück.  Der Anbieter verwendet dieses Handle, wenn andere projfs-APIs aufgerufen werden.

## <a name="virtualization-instance-runtime"></a>Laufzeit der virtualisierungsinstanz

Nachdem der Aufruf von **prjstartvirtualization** zurückgegeben wurde, werden die Rückruf Routinen des Anbieters von projfs als Reaktion auf Dateisystem Vorgänge in der virtualisierungsinstanz aufgerufen.  Informationen dazu, wie der Anbieter verschiedene Dateisystem Vorgänge verarbeiten kann, finden Sie in den folgenden Abschnitten:

* [Auflisten von Dateien und Verzeichnissen](enumerating-files-and-directories.md)
* [Bereitstellen von Dateidaten](providing-file-data.md)
* [Datei System-Vorgangs Benachrichtigungen](file-system-operation-notifications.md)
* [Behandeln von Änderungen der Ansicht](handling-view-changes.md)

## <a name="shutting-down-a-virtualization-instance"></a>Herunterfahren einer virtualisierungsinstanz

Um projfs zu signalisieren, dass der Anbieter keine Rückrufe mehr empfangen und Daten bereitstellen möchte, muss der Anbieter die virtualisierungsinstanz abbrechen.  Zu diesem Zweck ruft der Anbieter **[prjstopvirtualization](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing)** auf und übergibt ihm das Handle an die virtualisierungsinstanz, die er vom Aufruf an **prjstartvirtualization** empfangen hat.

```C++
PrjStopVirtualizing(instanceHandle);
```

Beachten Sie, dass projfs die Rückruf Routinen des Anbieters weiterhin aufrufen kann, bis dieser Aufruf zurückgegeben wird.