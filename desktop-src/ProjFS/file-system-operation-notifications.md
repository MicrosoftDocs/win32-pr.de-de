---
title: Datei System-Vorgangs Benachrichtigungen
description: Beschreibt, wie ein Anbieter Benachrichtigungen von Dateisystem Vorgängen empfangen kann.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/04/2018
ms.topic: article
ms.openlocfilehash: 9eae9bde6d56592f371dcd48c24fef96a9eecbdf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727808"
---
# <a name="file-system-operation-notifications"></a>Datei System-Vorgangs Benachrichtigungen

Zusätzlich zu den erforderlichen Rückrufen für die Behandlung von Enumerationen, zurückgeben von Datei Metadaten und Dateiinhalten kann ein Anbieter optional einen **[PRJ_NOTIFICATION_CB]()** Rückruf beim Aufruf von **[prjstartvirtualisieren]()** registrieren.  Dieser Rückruf empfängt Benachrichtigungen zu Dateisystem Vorgängen, die für Dateien und Verzeichnisse unterhalb des virtualisierungsstamms der Instanz ausgeführt werden.  Einige der Benachrichtigungen sind Benachrichtigungen nach dem Vorgang, die dem Anbieter mitteilen, dass gerade ein Vorgang abgeschlossen wurde.  Bei den anderen Benachrichtigungen handelt es sich um Benachrichtigungen vor dem Vorgang. Dies bedeutet, dass der Anbieter benachrichtigt wird, bevor der Vorgang durchgeführt wird.  In einer Benachrichtigung vor dem Vorgang kann der Anbieter ein Veto für den Vorgang durch Zurückgeben eines Fehlercodes aus dem Rückruf durchsetzen.  Dies bewirkt, dass der Vorgang mit dem zurückgegebenen Fehlercode fehlschlägt.

## <a name="how-to-specify-notifications-to-receive"></a>Angeben der zu empfangenden Benachrichtigungen

Wenn der Anbieter eine Implementierung von **PRJ_NOTIFICATION_CB** bereitstellt, wenn er eine virtualisierungsinstanz startet, sollte er auch angeben, welche Benachrichtigungen empfangen werden sollen.  Die Benachrichtigungen, für die der Anbieter registriert werden kann, werden in der [PRJ_NOTIFICATION](/windows/win32/api/projectedfslib/ne-projectedfslib-prj_notification) -enum definiert.

Wenn der Anbieter die Benachrichtigungen angibt, die er empfangen möchte, erfolgt dies mithilfe eines Arrays aus mindestens einer [PRJ_NOTIFICATION_MAPPING](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_notification_mapping) Struktur.  Diese definieren "Benachrichtigungs Zuordnungen".  Eine Benachrichtigungs Zuordnung ist eine Kopplung zwischen einem Verzeichnis, das als "Benachrichtigungs Stamm" bezeichnet wird, und einem Satz von Benachrichtigungen, ausgedrückt als Bitmaske, die von projfs für dieses Verzeichnis und seine Nachfolger gesendet werden sollen.  Eine Benachrichtigungs Zuordnung kann auch für eine einzelne Datei eingerichtet werden.  Eine Datei oder ein Verzeichnis, das in einer Benachrichtigungs Zuordnung angegeben ist, muss nicht bereits zu dem Zeitpunkt vorhanden sein, an dem der Anbieter **prjstartvirtualisieren** aufruft. der Anbieter kann einen beliebigen Pfad angeben, und die Zuordnung wird darauf angewendet, wenn er erstellt wird.

Wenn der Anbieter mehrere Benachrichtigungs Zuordnungen angibt und einige Nachfolger von anderen sind, müssen die Zuordnungen in absteigender Tiefe angegeben werden.  Benachrichtigungs Zuordnungen auf tieferen Ebenen überschreiben höhere Ebenen für Ihre Nachfolger.

Wenn der Anbieter keinen Satz von Benachrichtigungs Zuordnungen angibt, sendet projfs standardmäßig PRJ_NOTIFY_FILE_OPENED, PRJ_NOTIFY_NEW_FILE_CREATED und PRJ_NOTIFY_FILE_OVERWRITTEN für alle Dateien und Verzeichnisse unterhalb des virtualisierungsstamms an.

Der folgende Code Ausschnitt veranschaulicht, wie Sie einen Satz von Benachrichtigungen beim Starten einer virtualisierungsinstanz registrieren.

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

Projfs sendet Benachrichtigungen von Dateisystem Vorgängen durch Aufrufen des **PRJ_NOTIFICATION_CB** Rückrufs des Anbieters.  Dies erfolgt für jeden Vorgang, für den der Anbieter registriert wurde.  Wenn, wie im obigen Beispiel, der für PRJ_NOTIFY_NEW_FILE_CREATED registrierte Anbieter | PRJ_NOTIFY_FILE_OPENED | PRJ_NOTIFY_PRE_DELETE | PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED | PRJ_NOTIFY_FILE_RENAMED und eine Anwendung eine neue Datei im Benachrichtigungs Stamm erstellt hat, ruft projfs den **PRJ_NOTIFICATION_CB** Rückruf mit dem Pfad Namen der neuen Datei und dem _Benachrichtigungs_ Parameter auf PRJ_NOTIFICATION_NEW_FILE_CREATED auf.

Projfs sendet die Benachrichtigungen in der folgenden Liste, bevor der zugehörige Dateisystem Vorgang stattfindet.  Wenn der Anbieter einen Fehlercode aus dem **PRJ_NOTIFICATION_CB** Rückruf zurückgibt, schlägt der Dateisystem Vorgang fehl, und es wird der vom Anbieter angegebene Fehlercode zurückgegeben.

* PRJ_NOTIFICATION_PRE_DELETE: die Datei wird gerade gelöscht.
* PRJ_NOTIFICATION_PRE_RENAME: die Datei wird im Begriff, umbenannt zu werden.
* PRJ_NOTIFICATION_PRE_SET_HARDLINK: für die Datei wird ein fester Link erstellt.
* PRJ_NOTIFICATION_FILE_PRE_CONVERT_TO_FULL: eine Datei soll von einem Platzhalter auf eine vollständige Datei erweitert werden, was darauf hinweist, dass Ihr Inhalt wahrscheinlich geändert wird.

Projfs sendet die Benachrichtigungen in der folgenden Liste, nachdem der zugehörige Dateisystem Vorgang abgeschlossen wurde.

* PRJ_NOTIFICATION_FILE_OPENED: eine vorhandene Datei wurde geöffnet.
  * Obwohl diese Benachrichtigung gesendet wird, nachdem die Datei geöffnet wurde, kann der Anbieter einen Fehlercode zurückgeben.  Als Antwort bricht projfs den geöffneten ab und gibt den Fehler an den Aufrufer zurück.
* PRJ_NOTIFICATION_NEW_FILE_CREATED: Es wurde eine neue Datei erstellt.
* PRJ_NOTIFICATION_FILE_OVERWRITTEN: eine vorhandene Datei wurde überschrieben, z. b. durch Aufrufen von [createfilew](/windows/desktop/api/fileapi/nf-fileapi-createfilew) mit dem **CREATE_ALWAYS** _dwcreationdisposition_ -Flag.
* PRJ_NOTIFICATION_FILE_RENAMED: eine Datei wurde umbenannt.
* PRJ_NOTIFICATION_HARDLINK_CREATED: für eine Datei wurde ein fester [Link](/windows/desktop/FileIO/hard-links-and-junctions#hard-links) erstellt.
* PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_NO_MODIFICATION: ein Datei Handle wurde geschlossen, und der Inhalt der Datei wurde nicht geändert, und die Datei wurde nicht gelöscht.
* PRJ_NOTIFICATION_FILE_HANLDE_CLOSED_FILE_MODIFIED: ein Datei Handle wurde geschlossen, und der Inhalt der Datei wurde geändert.
* PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED: ein Datei Handle wurde geschlossen, und die Datei wurde beim Schließen des Handles gelöscht.

Weitere Informationen zu den einzelnen Benachrichtigungen finden Sie in der Dokumentation für **[PRJ_NOTIFICATION](/windows/desktop/api/projectedfslib/ne-projectedfslib-prj_notification)**.

Der _notificationparameters_ -Parameter des **PRJ_NOTIFICATION_CB** Rückrufs gibt zusätzliche Parameter für bestimmte Benachrichtigungen an.  Wenn ein Anbieter eine PRJ_NOTIFICATION_FILE_OPENED, PRJ_NOTIFICATION_NEW_FILE_CREATED oder PRJ_NOTIFICATION_FILE_OVERWRITTEN oder PRJ_NOTIFICATION_FILE_RENAMED Benachrichtigung empfängt, kann der Anbieter einen neuen Satz von Benachrichtigungen angeben, der für die Datei empfangen werden soll. Weitere Informationen finden Sie in der Dokumentation zu **[PRJ_NOTIFICATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb)**.

Das folgende Beispiel zeigt einfache Beispiele dafür, wie ein Anbieter die Benachrichtigungen verarbeiten kann, die er für im obigen Code Ausschnitt registriert hat.

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