---
title: Dateisystem-Vorgangsbenachrichtigungen
description: Beschreibt, wie ein Anbieter Benachrichtigungen über Dateisystemvorgänge empfangen kann.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/04/2018
ms.topic: article
ms.openlocfilehash: 2e09efcc9d1a1aea99f79b70446162df5e3ef924067ac6619a443aa15e06e9df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031240"
---
# <a name="file-system-operation-notifications"></a>Dateisystem-Vorgangsbenachrichtigungen

Zusätzlich zu den erforderlichen Rückrufen zum Behandeln von Enumerationen, Zurückgeben von Dateimetadaten und Dateiinhalten kann ein Anbieter optional einen **[PRJ_NOTIFICATION_CB-Rückruf]()** in seinem Aufruf von **[PrjStartVirtualizing registrieren.]()**  Dieser Rückruf empfängt Benachrichtigungen über Dateisystemvorgänge, die für Dateien und Verzeichnisse unter dem Virtualisierungsstamm der Instanz ausgeführt werden.  Einige der Benachrichtigungen sind Benachrichtigungen nach dem Vorgang, die den Anbieter darüber informieren, dass ein Vorgang gerade abgeschlossen wurde.  Bei den anderen Benachrichtigungen handelt es sich um Benachrichtigungen vor dem Vorgang. Dies bedeutet, dass der Anbieter benachrichtigt wird, bevor der Vorgang erfolgt.  In einer Benachrichtigung vor dem Vorgang kann der Anbieter den Vorgang blockieren, indem er einen Fehlercode aus dem Rückruf zurücksendet.  Dies führt dazu, dass der Vorgang mit dem zurückgegebenen Fehlercode fehlschlägt.

## <a name="how-to-specify-notifications-to-receive"></a>Angeben von zu empfangenden Benachrichtigungen

Wenn der Anbieter eine Implementierung von **PRJ_NOTIFICATION_CB** beim Starten einer Virtualisierungsinstanz an stellt, sollte er auch angeben, welche Benachrichtigungen empfangen werden sollen.  Die Benachrichtigungen, für die sich der Anbieter registrieren kann, werden in [der](/windows/win32/api/projectedfslib/ne-projectedfslib-prj_notification) PRJ_NOTIFICATION definiert.

Wenn der Anbieter die Benachrichtigungen angibt, die er empfangen möchte, verwendet er dazu ein Array aus einer oder [PRJ_NOTIFICATION_MAPPING](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_notification_mapping) Strukturen.  Diese definieren "Benachrichtigungszuordnungen".  Eine Benachrichtigungszuordnung ist eine Kopplung zwischen einem Verzeichnis, das als "Benachrichtigungsstamm" bezeichnet wird, und einem Satz von Benachrichtigungen, ausgedrückt als Bitmaske, die ProjFS für dieses Verzeichnis und seine Nachfolger senden soll.  Für eine einzelne Datei kann auch eine Benachrichtigungszuordnung eingerichtet werden.  Eine Datei oder ein Verzeichnis, die in einer Benachrichtigungszuordnung angegeben ist, muss nicht bereits vorhanden sein, wenn der Anbieter **PrjStartVirtualizing** aufruft. Der Anbieter kann einen beliebigen Pfad angeben, und die Zuordnung wird auf ihn angewendet, wenn er erstellt wird.

Wenn der Anbieter mehrere Benachrichtigungszuordnungen angibt und einige Nachfolger von anderen sind, müssen die Zuordnungen in absteigender Tiefe angegeben werden.  Benachrichtigungszuordnungen auf tieferen Ebenen überschreiben höhere Ebenen für ihre Nachfolger.

Wenn vom Anbieter keine Benachrichtigungszuordnungen angegeben werden, sendet ProjFS ihn standardmäßig PRJ_NOTIFY_FILE_OPENED, PRJ_NOTIFY_NEW_FILE_CREATED und PRJ_NOTIFY_FILE_OVERWRITTEN für alle Dateien und Verzeichnisse unterhalb des Virtualisierungsstamms.

Der folgende Codeausschnitt veranschaulicht, wie sie eine Gruppe von Benachrichtigungen beim Starten einer Virtualisierungsinstanz registrieren.

```C++
PRJ_CALLBACKS callbackTable;

// Supply required callbacks.
callbackTable.StartDirectoryEnumerationCallback = MyStartEnumCallback;
callbackTable.EndDirectoryEnumerationCallback = MyEndEnumCallback;
callbackTable.GetDirectoryEnumerationCallback = MyGetEnumCallback;
callbackTable.GetPlaceholderInfoCallback = MyGetPlaceholderInfoCallback;
callbackTable.GetFileDataCallback = MyGetFileDataCallback;

// The rest of the callbacks are optional.  We want notifications, so specify
// our notification callback.
callbackTable.QueryFileNameCallback = nullptr;
callbackTable.NotificationCallback = MyNotificationCallback;
callbackTable.CancelCommandCallback = nullptr;

// Assume the provider has created a new virtualization root at C:\VirtRoot and
// initialized it with this layout:
//
//     C:\VirtRoot
//     +--- baz
//     \--- foo
//          +--- subdir1
//          \--- subdir2
//
// The provider wants these notifications:
// * Notification of new file/directory creates for all locations within the
//   virtualization root that are not subject to one of the following more
//   specific notification mappings.
// * Notification of new file/directory creates, file opens, post-renames, and
//   pre- and post-deletes for C:\VirtRoot\foo
// * No notifications for C:\VirtRoot\foo\subdir1
PRJ_STARTVIRTUALIZING_OPTIONS startOpts = {};
PRJ_VIRTUALIZATION_MAPPING notificationMappings[3];

// Configure default notifications - notify of new files for most of the tree.
notificationMappings[0].NotificationRoot = L"";
notificationMappings[0].NotificationBitMask = PRJ_NOTIFY_NEW_FILE_CREATED;

// Override default notifications - notify of new files, opened files, and file
// deletes for C:\VirtRoot\foo and its descendants.
notificationMappings[1].NotificationRoot = L"foo";
notificationMappings[1].NotificationBitMask = PRJ_NOTIFY_NEW_FILE_CREATED |
                                              PRJ_NOTIFY_FILE_OPENED |
                                              PRJ_NOTIFY_PRE_DELETE |
                                              PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED |
                                              PRJ_NOTIFY_FILE_RENAMED;

// Override all notifications for C:\VirtRoot\foo\subdir1 and its descendants.
notificationMappings[2].NotificationRoot = L"foo\\subdir1";
notificationMappings[2].NotificationBitMask = PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS;

startOpts.NotificationMappings = notificationMappings;
startOpts.NotificationMappingsCount = ARRAYSIZE(notificationMapping);

// Start the instance and provide our notification mappings.
HRESULT hr;
PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT instanceHandle;
hr = PrjStartVirtualizing(rootName,
                          &callbackTable,
                          nullptr,
                          &startOpts,
                          &instanceHandle);
if (FAILED(hr))
{
    wprintf(L"Failed to start the virtualization instance (0x%08x)\n", hr);
    return;
}
```

## <a name="receiving-notifications"></a>Empfangen von Benachrichtigungen

ProjFS sendet Benachrichtigungen zu Dateisystemvorgängen, indem der PRJ_NOTIFICATION_CB des **Anbieters** aufruft.  Dies wird für jeden Vorgang durchgeführt, für den der Anbieter registriert ist.  Wenn, wie im obigen Beispiel, der für die Registrierung PRJ_NOTIFY_NEW_FILE_CREATED | PRJ_NOTIFY_FILE_OPENED | PRJ_NOTIFY_PRE_DELETE | PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED | PRJ_NOTIFY_FILE_RENAMED eine Anwendung eine neue Datei im Benachrichtigungsstamm erstellt hat, würde ProjFS den **PRJ_NOTIFICATION_CB-Rückruf** aufrufen,  bei dem der Pfadname der neuen Datei und der Benachrichtigungsparameter auf PRJ_NOTIFICATION_NEW_FILE_CREATED.

ProjFS sendet die Benachrichtigungen in der folgenden Liste, bevor der zugeordnete Dateisystemvorgang stattfindet.  Wenn der Anbieter einen Fehlercode aus dem PRJ_NOTIFICATION_CB zurückgibt, wird beim Dateisystemvorgang ein Fehler und der vom Anbieter angegebene Fehlercode zurückgegeben. 

* PRJ_NOTIFICATION_PRE_DELETE: Die Datei wird gelöscht.
* PRJ_NOTIFICATION_PRE_RENAME: Die Datei wird umbenannt.
* PRJ_NOTIFICATION_PRE_SET_HARDLINK: Für die Datei wird ein harter Link erstellt.
* PRJ_NOTIFICATION_FILE_PRE_CONVERT_TO_FULL: Eine Datei wird von einem Platzhalter auf eine vollständige Datei erweitert, was darauf hinweist, dass ihr Inhalt wahrscheinlich geändert wird.

ProjFS sendet die Benachrichtigungen in der folgenden Liste, nachdem der zugeordnete Dateisystemvorgang abgeschlossen wurde.

* PRJ_NOTIFICATION_FILE_OPENED: Eine vorhandene Datei wurde geöffnet.
  * Obwohl diese Benachrichtigung gesendet wird, nachdem die Datei geöffnet wurde, kann der Anbieter einen Fehlercode zurückgeben.  Als Antwort bricht ProjFS das Öffnen ab und gibt den Fehler an den Aufrufer zurück.
* PRJ_NOTIFICATION_NEW_FILE_CREATED: Eine neue Datei wurde erstellt.
* PRJ_NOTIFICATION_FILE_OVERWRITTEN: Eine vorhandene Datei wurde überschrieben, z. B. durch  Aufrufen von [CreateFileW](/windows/desktop/api/fileapi/nf-fileapi-createfilew) mit dem CREATE_ALWAYS _dwCreationDisposition-Flag._
* PRJ_NOTIFICATION_FILE_RENAMED: Eine Datei wurde umbenannt.
* PRJ_NOTIFICATION_HARDLINK_CREATED: Für eine [Datei](/windows/desktop/FileIO/hard-links-and-junctions#hard-links) wurde ein harter Link erstellt.
* PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_NO_MODIFICATION: Ein Dateihand handle wurde geschlossen, und der Inhalt der Datei wurde weder geändert noch gelöscht.
* PRJ_NOTIFICATION_FILE_HANLDE_CLOSED_FILE_MODIFIED: Ein Dateihand handle wurde geschlossen, und der Inhalt der Datei wurde geändert.
* PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED: Ein Dateihand handle wurde geschlossen, und die Datei wurde beim Schließen des Handles gelöscht.

Weitere Informationen zu den einzelnen Benachrichtigungen finden Sie in der Dokumentation zu **[PRJ_NOTIFICATION](/windows/desktop/api/projectedfslib/ne-projectedfslib-prj_notification)**.

Der **PRJ_NOTIFICATION_CB** _notificationParameters-Parameter_ des Rückrufs gibt zusätzliche Parameter für bestimmte Benachrichtigungen an.  Wenn ein Anbieter eine Benachrichtigung PRJ_NOTIFICATION_FILE_OPENED, PRJ_NOTIFICATION_NEW_FILE_CREATED, PRJ_NOTIFICATION_FILE_OVERWRITTEN oder PRJ_NOTIFICATION_FILE_RENAMED empfängt, kann der Anbieter einen neuen Satz von Benachrichtigungen angeben, die für die Datei empfangen werden sollen. Weitere Informationen finden Sie in der Dokumentation zu **[PRJ_NOTIFICATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb)**.

Das folgende Beispiel zeigt einfache Beispiele dafür, wie ein Anbieter die Benachrichtigungen verarbeiten kann, für die er im obigen Codeausschnitt registriert wurde.

```C++
#include <windows.h>

HRESULT
MyNotificationCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData,
    _In_ BOOLEAN isDirectory,
    _In_ PRJ_NOTIFICATION notification,
    _In_opt_z_ PCWSTR destinationFileName,
    _Inout_ PRJ_NOTIFICATION_PARAMETERS* operationParameters
    )
{
    HRESULT hr = S_OK;

    switch (notification)
    {
    case PRJ_NOTIFY_NEW_FILE_CREATED:

        wprintf(L"A new %ls was created at [%ls].\n",
                isDirectory ? L"directory" : L"file",
                callbackData->FilePathName);

        // Let's stop getting notifications inside newly-created directories.
        if (isDirectory)
        {
            operationParameters->PostCreate.NotificationMask = PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS;
        }
        break;

    case PRJ_NOTIFY_FILE_OPENED:

        wprintf(L"Handle opened to %ls [%ls].\n",
                isDirectory ? L"directory": L"file",
                callbackData->FilePathName);
        break;

    case PRJ_NOTIFY_PRE_DELETE:

        wprintf(L"Attempt to delete %ls [%ls]: ",
                isDirectory ? L"directory": L"file",
                callbackData->FilePathName);

        // MyAllowDelete is a routine the provider might implement to decide
        // whether to allow a given file/directory to be deleted.
        if (!MyAllowDelete(callbackData->FilePathName, isDirectory))
        {
            wprintf(L"DENIED\n");
            hr = HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED);
        }
        else
        {
            wprintf(L"ALLOWED\n");
        }
        break;

    case PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED:

        wprintf(L"The %ls [%ls] was deleted.\n",
                isDirectory ? L"directory": L"file",
                callbackData->FilePathName);
        break;

    case PRJ_NOTIFY_FILE_RENAMED:

        if (wcslen(callbackData->FilePathName) == 0)
        {
            // If callbackData->FilePathName is an empty string, then the item
            // that was renamed was originally in a location not under the
            // virtualization root.
            wprintf(L"A %ls was renamed into the virtualization root,\n",
                    isDirectory ? L"directory": L"file");
            wprintf(L"Its new location is [%ls].\n",
                    destinationFileName);
        }
        else if (wcslen(destinationFileName) == 0)
        {
            // If destinationFileName is an empty string, then the item that was
            // renamed is now in a location not under the virtualization root.
            wprintf(L"A %ls was renamed out of the virtualization root.\n",
                    isDirectory ? L"directory": L"file");
            wprintf(L"Its original location was [%ls].\n",
                    callbackData->FilePathName);
        }
        else
        {
            // If both names are specified, both the new and old names are under
            // the virtualization root (it is never the case that nether name is
            // specified).
            wprintf(L"A %ls [%ls] was renamed.\n",
                    isDirectory ? L"directory": L"file",
                    callbackData->FilePathName);
            wprintf(L"Its new name is [%ls].\n", destinationFileName);
        }
        break;

    default:
        wprintf(L"Unrecognized notification: 0x%08x");
    }

    // Note that this may be a failure code from MyAllowDelete().
    return hr;
}
```