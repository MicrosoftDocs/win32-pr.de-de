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
# <a name="file-system-operation-notifications"></a><span data-ttu-id="bad7a-103">Datei System-Vorgangs Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="bad7a-103">File System Operation Notifications</span></span>

<span data-ttu-id="bad7a-104">Zusätzlich zu den erforderlichen Rückrufen für die Behandlung von Enumerationen, zurückgeben von Datei Metadaten und Dateiinhalten kann ein Anbieter optional einen **[PRJ_NOTIFICATION_CB]()** Rückruf beim Aufruf von **[prjstartvirtualisieren]()** registrieren.</span><span class="sxs-lookup"><span data-stu-id="bad7a-104">In addition to required callbacks for handling enumeration, returning file metadata, and file contents, a provider may optionally register a **[PRJ_NOTIFICATION_CB]()** callback in its call to **[PrjStartVirtualizing]()**.</span></span>  <span data-ttu-id="bad7a-105">Dieser Rückruf empfängt Benachrichtigungen zu Dateisystem Vorgängen, die für Dateien und Verzeichnisse unterhalb des virtualisierungsstamms der Instanz ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="bad7a-105">This callback receives notifications of file system operations performed on files and directories beneath the instance's virtualization root.</span></span>  <span data-ttu-id="bad7a-106">Einige der Benachrichtigungen sind Benachrichtigungen nach dem Vorgang, die dem Anbieter mitteilen, dass gerade ein Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="bad7a-106">Some of the notifications are "post-operation" notifications, which tell the provider that an operation has just completed.</span></span>  <span data-ttu-id="bad7a-107">Bei den anderen Benachrichtigungen handelt es sich um Benachrichtigungen vor dem Vorgang. Dies bedeutet, dass der Anbieter benachrichtigt wird, bevor der Vorgang durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bad7a-107">The other notifications are "pre-operation" notifications, meaning that the provider is notified before the operation happens.</span></span>  <span data-ttu-id="bad7a-108">In einer Benachrichtigung vor dem Vorgang kann der Anbieter ein Veto für den Vorgang durch Zurückgeben eines Fehlercodes aus dem Rückruf durchsetzen.</span><span class="sxs-lookup"><span data-stu-id="bad7a-108">In a pre-operation notification the provider can veto the operation by returning an error code from the callback.</span></span>  <span data-ttu-id="bad7a-109">Dies bewirkt, dass der Vorgang mit dem zurückgegebenen Fehlercode fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="bad7a-109">This causes the operation to fail with the returned error code.</span></span>

## <a name="how-to-specify-notifications-to-receive"></a><span data-ttu-id="bad7a-110">Angeben der zu empfangenden Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="bad7a-110">How to Specify Notifications to Receive</span></span>

<span data-ttu-id="bad7a-111">Wenn der Anbieter eine Implementierung von **PRJ_NOTIFICATION_CB** bereitstellt, wenn er eine virtualisierungsinstanz startet, sollte er auch angeben, welche Benachrichtigungen empfangen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bad7a-111">If the provider supplies an implementation of **PRJ_NOTIFICATION_CB** when it starts a virtualization instance, it should also specify which notifications it wishes to receive.</span></span>  <span data-ttu-id="bad7a-112">Die Benachrichtigungen, für die der Anbieter registriert werden kann, werden in der [PRJ_NOTIFICATION](/windows/win32/api/projectedfslib/ne-projectedfslib-prj_notification) -enum definiert.</span><span class="sxs-lookup"><span data-stu-id="bad7a-112">The notifications for which the provider can register are defined in the [PRJ_NOTIFICATION](/windows/win32/api/projectedfslib/ne-projectedfslib-prj_notification) enum.</span></span>

<span data-ttu-id="bad7a-113">Wenn der Anbieter die Benachrichtigungen angibt, die er empfangen möchte, erfolgt dies mithilfe eines Arrays aus mindestens einer [PRJ_NOTIFICATION_MAPPING](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_notification_mapping) Struktur.</span><span class="sxs-lookup"><span data-stu-id="bad7a-113">When the provider specifies the notifications it wishes to receive, it does so using an array of one or more [PRJ_NOTIFICATION_MAPPING](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_notification_mapping) structures.</span></span>  <span data-ttu-id="bad7a-114">Diese definieren "Benachrichtigungs Zuordnungen".</span><span class="sxs-lookup"><span data-stu-id="bad7a-114">These define "notification mappings".</span></span>  <span data-ttu-id="bad7a-115">Eine Benachrichtigungs Zuordnung ist eine Kopplung zwischen einem Verzeichnis, das als "Benachrichtigungs Stamm" bezeichnet wird, und einem Satz von Benachrichtigungen, ausgedrückt als Bitmaske, die von projfs für dieses Verzeichnis und seine Nachfolger gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bad7a-115">A notification mapping is a pairing between a directory, referred to as a "notification root", and a set of notifications, expressed as a bit mask, which ProjFS should send for that directory and its descendants.</span></span>  <span data-ttu-id="bad7a-116">Eine Benachrichtigungs Zuordnung kann auch für eine einzelne Datei eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="bad7a-116">A notification mapping can also be established for a single file.</span></span>  <span data-ttu-id="bad7a-117">Eine Datei oder ein Verzeichnis, das in einer Benachrichtigungs Zuordnung angegeben ist, muss nicht bereits zu dem Zeitpunkt vorhanden sein, an dem der Anbieter **prjstartvirtualisieren** aufruft. der Anbieter kann einen beliebigen Pfad angeben, und die Zuordnung wird darauf angewendet, wenn er erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="bad7a-117">A file or directory specified in a notification mapping does not have to exist already at the time the provider calls **PrjStartVirtualizing**, the provider can specify any path and the mapping will apply to it if it is ever created.</span></span>

<span data-ttu-id="bad7a-118">Wenn der Anbieter mehrere Benachrichtigungs Zuordnungen angibt und einige Nachfolger von anderen sind, müssen die Zuordnungen in absteigender Tiefe angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bad7a-118">If the provider specifies multiple notification mappings, and some are descendants of others, the mappings must be specified in descending depth.</span></span>  <span data-ttu-id="bad7a-119">Benachrichtigungs Zuordnungen auf tieferen Ebenen überschreiben höhere Ebenen für Ihre Nachfolger.</span><span class="sxs-lookup"><span data-stu-id="bad7a-119">Notification mappings at deeper levels override higher-level ones for their descendants.</span></span>

<span data-ttu-id="bad7a-120">Wenn der Anbieter keinen Satz von Benachrichtigungs Zuordnungen angibt, sendet projfs standardmäßig PRJ_NOTIFY_FILE_OPENED, PRJ_NOTIFY_NEW_FILE_CREATED und PRJ_NOTIFY_FILE_OVERWRITTEN für alle Dateien und Verzeichnisse unterhalb des virtualisierungsstamms an.</span><span class="sxs-lookup"><span data-stu-id="bad7a-120">If the provider does not specify a set of notification mappings, ProjFS will default to sending it PRJ_NOTIFY_FILE_OPENED, PRJ_NOTIFY_NEW_FILE_CREATED, and PRJ_NOTIFY_FILE_OVERWRITTEN for all files and directories beneath the virtualization root.</span></span>

<span data-ttu-id="bad7a-121">Der folgende Code Ausschnitt veranschaulicht, wie Sie einen Satz von Benachrichtigungen beim Starten einer virtualisierungsinstanz registrieren.</span><span class="sxs-lookup"><span data-stu-id="bad7a-121">The following code snippet illustrates how to register a set of notifications when starting a virtualization instance.</span></span>

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

## <a name="receiving-notifications"></a><span data-ttu-id="bad7a-122">Empfangen von Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="bad7a-122">Receiving Notifications</span></span>

<span data-ttu-id="bad7a-123">Projfs sendet Benachrichtigungen von Dateisystem Vorgängen durch Aufrufen des **PRJ_NOTIFICATION_CB** Rückrufs des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="bad7a-123">ProjFS sends notifications of file system operations by calling the provider's **PRJ_NOTIFICATION_CB** callback.</span></span>  <span data-ttu-id="bad7a-124">Dies erfolgt für jeden Vorgang, für den der Anbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="bad7a-124">It does this for each operation the provider has registered for.</span></span>  <span data-ttu-id="bad7a-125">Wenn, wie im obigen Beispiel, der für PRJ_NOTIFY_NEW_FILE_CREATED registrierte Anbieter | PRJ_NOTIFY_FILE_OPENED | PRJ_NOTIFY_PRE_DELETE | PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED | PRJ_NOTIFY_FILE_RENAMED und eine Anwendung eine neue Datei im Benachrichtigungs Stamm erstellt hat, ruft projfs den **PRJ_NOTIFICATION_CB** Rückruf mit dem Pfad Namen der neuen Datei und dem _Benachrichtigungs_ Parameter auf PRJ_NOTIFICATION_NEW_FILE_CREATED auf.</span><span class="sxs-lookup"><span data-stu-id="bad7a-125">If, as in the above example, the provider registered for PRJ_NOTIFY_NEW_FILE_CREATED | PRJ_NOTIFY_FILE_OPENED | PRJ_NOTIFY_PRE_DELETE | PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED | PRJ_NOTIFY_FILE_RENAMED, and an application created a new file in the notification root, ProjFS would call the **PRJ_NOTIFICATION_CB** callback with the new file's path name and the _notification_ parameter set to PRJ_NOTIFICATION_NEW_FILE_CREATED.</span></span>

<span data-ttu-id="bad7a-126">Projfs sendet die Benachrichtigungen in der folgenden Liste, bevor der zugehörige Dateisystem Vorgang stattfindet.</span><span class="sxs-lookup"><span data-stu-id="bad7a-126">ProjFS sends the notifications in the following list before the associated file system operation takes place.</span></span>  <span data-ttu-id="bad7a-127">Wenn der Anbieter einen Fehlercode aus dem **PRJ_NOTIFICATION_CB** Rückruf zurückgibt, schlägt der Dateisystem Vorgang fehl, und es wird der vom Anbieter angegebene Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bad7a-127">If the provider returns a failure code from the **PRJ_NOTIFICATION_CB** callback, the file system operation will fail and return the failure code the provider specified.</span></span>

* <span data-ttu-id="bad7a-128">PRJ_NOTIFICATION_PRE_DELETE: die Datei wird gerade gelöscht.</span><span class="sxs-lookup"><span data-stu-id="bad7a-128">PRJ_NOTIFICATION_PRE_DELETE - The file is about to be deleted.</span></span>
* <span data-ttu-id="bad7a-129">PRJ_NOTIFICATION_PRE_RENAME: die Datei wird im Begriff, umbenannt zu werden.</span><span class="sxs-lookup"><span data-stu-id="bad7a-129">PRJ_NOTIFICATION_PRE_RENAME - The file is about to be renamed.</span></span>
* <span data-ttu-id="bad7a-130">PRJ_NOTIFICATION_PRE_SET_HARDLINK: für die Datei wird ein fester Link erstellt.</span><span class="sxs-lookup"><span data-stu-id="bad7a-130">PRJ_NOTIFICATION_PRE_SET_HARDLINK - A hard link is about to be created for the file.</span></span>
* <span data-ttu-id="bad7a-131">PRJ_NOTIFICATION_FILE_PRE_CONVERT_TO_FULL: eine Datei soll von einem Platzhalter auf eine vollständige Datei erweitert werden, was darauf hinweist, dass Ihr Inhalt wahrscheinlich geändert wird.</span><span class="sxs-lookup"><span data-stu-id="bad7a-131">PRJ_NOTIFICATION_FILE_PRE_CONVERT_TO_FULL - A file is about to be expanded from a placeholder to a full file, which indicates its contents are likely to be modified.</span></span>

<span data-ttu-id="bad7a-132">Projfs sendet die Benachrichtigungen in der folgenden Liste, nachdem der zugehörige Dateisystem Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="bad7a-132">ProjFS sends the notifications in the following list after the associated file system operation has completed.</span></span>

* <span data-ttu-id="bad7a-133">PRJ_NOTIFICATION_FILE_OPENED: eine vorhandene Datei wurde geöffnet.</span><span class="sxs-lookup"><span data-stu-id="bad7a-133">PRJ_NOTIFICATION_FILE_OPENED - An existing file has been opened.</span></span>
  * <span data-ttu-id="bad7a-134">Obwohl diese Benachrichtigung gesendet wird, nachdem die Datei geöffnet wurde, kann der Anbieter einen Fehlercode zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="bad7a-134">Even though this notification is sent after the file has been opened, the provider can return a failure code.</span></span>  <span data-ttu-id="bad7a-135">Als Antwort bricht projfs den geöffneten ab und gibt den Fehler an den Aufrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="bad7a-135">In response, ProjFS will cancel the open and return the failure to the caller.</span></span>
* <span data-ttu-id="bad7a-136">PRJ_NOTIFICATION_NEW_FILE_CREATED: Es wurde eine neue Datei erstellt.</span><span class="sxs-lookup"><span data-stu-id="bad7a-136">PRJ_NOTIFICATION_NEW_FILE_CREATED - A new file has been created.</span></span>
* <span data-ttu-id="bad7a-137">PRJ_NOTIFICATION_FILE_OVERWRITTEN: eine vorhandene Datei wurde überschrieben, z. b. durch Aufrufen von [createfilew](/windows/desktop/api/fileapi/nf-fileapi-createfilew) mit dem **CREATE_ALWAYS** _dwcreationdisposition_ -Flag.</span><span class="sxs-lookup"><span data-stu-id="bad7a-137">PRJ_NOTIFICATION_FILE_OVERWRITTEN - An existing file has been overwritten, for example by calling [CreateFileW](/windows/desktop/api/fileapi/nf-fileapi-createfilew) with the **CREATE_ALWAYS** _dwCreationDisposition_ flag.</span></span>
* <span data-ttu-id="bad7a-138">PRJ_NOTIFICATION_FILE_RENAMED: eine Datei wurde umbenannt.</span><span class="sxs-lookup"><span data-stu-id="bad7a-138">PRJ_NOTIFICATION_FILE_RENAMED - A file has been renamed.</span></span>
* <span data-ttu-id="bad7a-139">PRJ_NOTIFICATION_HARDLINK_CREATED: für eine Datei wurde ein fester [Link](/windows/desktop/FileIO/hard-links-and-junctions#hard-links) erstellt.</span><span class="sxs-lookup"><span data-stu-id="bad7a-139">PRJ_NOTIFICATION_HARDLINK_CREATED - A [hard link](/windows/desktop/FileIO/hard-links-and-junctions#hard-links) has been created for a file.</span></span>
* <span data-ttu-id="bad7a-140">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_NO_MODIFICATION: ein Datei Handle wurde geschlossen, und der Inhalt der Datei wurde nicht geändert, und die Datei wurde nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="bad7a-140">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_NO_MODIFICATION - A file handle has been closed, and the file's content was not modified, nor was the file deleted.</span></span>
* <span data-ttu-id="bad7a-141">PRJ_NOTIFICATION_FILE_HANLDE_CLOSED_FILE_MODIFIED: ein Datei Handle wurde geschlossen, und der Inhalt der Datei wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="bad7a-141">PRJ_NOTIFICATION_FILE_HANLDE_CLOSED_FILE_MODIFIED - A file handle has been closed, and the file's content has been modified.</span></span>
* <span data-ttu-id="bad7a-142">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED: ein Datei Handle wurde geschlossen, und die Datei wurde beim Schließen des Handles gelöscht.</span><span class="sxs-lookup"><span data-stu-id="bad7a-142">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED - A file handle has been closed, and the file was deleted as part of closing the handle.</span></span>

<span data-ttu-id="bad7a-143">Weitere Informationen zu den einzelnen Benachrichtigungen finden Sie in der Dokumentation für **[PRJ_NOTIFICATION](/windows/desktop/api/projectedfslib/ne-projectedfslib-prj_notification)**.</span><span class="sxs-lookup"><span data-stu-id="bad7a-143">For more details on each notification refer to the documentation for **[PRJ_NOTIFICATION](/windows/desktop/api/projectedfslib/ne-projectedfslib-prj_notification)**.</span></span>

<span data-ttu-id="bad7a-144">Der _notificationparameters_ -Parameter des **PRJ_NOTIFICATION_CB** Rückrufs gibt zusätzliche Parameter für bestimmte Benachrichtigungen an.</span><span class="sxs-lookup"><span data-stu-id="bad7a-144">The **PRJ_NOTIFICATION_CB** callback's _notificationParameters_ parameter specifies extra parameters for certain notifications.</span></span>  <span data-ttu-id="bad7a-145">Wenn ein Anbieter eine PRJ_NOTIFICATION_FILE_OPENED, PRJ_NOTIFICATION_NEW_FILE_CREATED oder PRJ_NOTIFICATION_FILE_OVERWRITTEN oder PRJ_NOTIFICATION_FILE_RENAMED Benachrichtigung empfängt, kann der Anbieter einen neuen Satz von Benachrichtigungen angeben, der für die Datei empfangen werden soll.</span><span class="sxs-lookup"><span data-stu-id="bad7a-145">If a provider receives a PRJ_NOTIFICATION_FILE_OPENED, PRJ_NOTIFICATION_NEW_FILE_CREATED, or PRJ_NOTIFICATION_FILE_OVERWRITTEN, or PRJ_NOTIFICATION_FILE_RENAMED notification, the provider can specify a new set of notifications to receive for the file.</span></span> <span data-ttu-id="bad7a-146">Weitere Informationen finden Sie in der Dokumentation zu **[PRJ_NOTIFICATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb)**.</span><span class="sxs-lookup"><span data-stu-id="bad7a-146">For further details, refer to the documentation for **[PRJ_NOTIFICATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb)**.</span></span>

<span data-ttu-id="bad7a-147">Das folgende Beispiel zeigt einfache Beispiele dafür, wie ein Anbieter die Benachrichtigungen verarbeiten kann, die er für im obigen Code Ausschnitt registriert hat.</span><span class="sxs-lookup"><span data-stu-id="bad7a-147">The following sample shows simple examples of how a provider might process the notifications it registered for in the code snippet above.</span></span>

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