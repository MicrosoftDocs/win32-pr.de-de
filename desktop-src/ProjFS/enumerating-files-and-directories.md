---
title: Auflisten von Dateien und Verzeichnissen
description: Beschreibt, wie ein projfs-Anbieter an der verzeichnisenumeration teilnimmt.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/25/2018
ms.topic: article
ms.openlocfilehash: e0712ceb927388b090a84a89f80f0e2d3a1befbb
ms.sourcegitcommit: 80d74c0bf4fc402865a1ad223480abe1ce4d1115
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2020
ms.locfileid: "103723992"
---
# <a name="enumerating-files-and-directories"></a><span data-ttu-id="3f488-103">Auflisten von Dateien und Verzeichnissen</span><span class="sxs-lookup"><span data-stu-id="3f488-103">Enumerating Files and Directories</span></span>

<span data-ttu-id="3f488-104">Wenn ein Anbieter erstmalig einen virtualisierungsstamm erstellt, ist er auf dem lokalen System leer.</span><span class="sxs-lookup"><span data-stu-id="3f488-104">When a provider first creates a virtualization root it is empty on the local system.</span></span>  <span data-ttu-id="3f488-105">Das heißt, keines der Elemente im Sicherungsdaten Speicher wurde noch auf dem Datenträger zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="3f488-105">That is, none of the items in the backing data store have yet been cached to disk.</span></span>  <span data-ttu-id="3f488-106">Beim Öffnen eines Elements wird es zwischengespeichert, aber bis ein Element geöffnet ist, ist es nur im Sicherungsdaten Speicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3f488-106">As each item is opened it is cached, but until an item is opened it only exists in the backing data store.</span></span>

<span data-ttu-id="3f488-107">Da nicht geöffnete Elemente nicht lokal vorhanden sind, gibt die normale Verzeichnis Enumeration dem Benutzer nicht offen.</span><span class="sxs-lookup"><span data-stu-id="3f488-107">Since unopened items have no local presence, normal directory enumeration would not reveal their existence to the user.</span></span>  <span data-ttu-id="3f488-108">Daher muss der Anbieter an der verzeichnisenumeration teilnehmen, indem er Informationen über Elemente in seinem Sicherungsdaten Speicher an projfs zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="3f488-108">Therefore the provider must participate in directory enumeration by returning information to ProjFS about items in its backing data store.</span></span>  <span data-ttu-id="3f488-109">Projfs führt die Informationen vom Anbieter mit dem Inhalt des lokalen Dateisystems zusammen, mit dem der Benutzer eine einheitliche Liste der Inhalte eines Verzeichnisses enthält.</span><span class="sxs-lookup"><span data-stu-id="3f488-109">ProjFS merges the information from the provider with what is on the local file system to present to the user a unified list of the contents of a directory.</span></span>

## <a name="directory-enumeration-callbacks"></a><span data-ttu-id="3f488-110">Verzeichnisenumerationsrückrufe</span><span class="sxs-lookup"><span data-stu-id="3f488-110">Directory Enumeration Callbacks</span></span>

<span data-ttu-id="3f488-111">Um an der verzeichnisenumeration teilnehmen zu können, muss der Anbieter die **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)**, **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** und **[PRJ_END_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb)** Rückrufe implementieren.</span><span class="sxs-lookup"><span data-stu-id="3f488-111">To participate in directory enumeration the provider must implement the **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)**, **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)**, and **[PRJ_END_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb)** callbacks.</span></span>  <span data-ttu-id="3f488-112">Wenn ein Verzeichnis unter dem virtualisierungsstamm des Anbieters aufgezählt wird, führt projfs die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="3f488-112">When a directory under the provider's virtualization root gets enumerated, ProjFS performs the following actions:</span></span>

1. <span data-ttu-id="3f488-113">Projfs Ruft den **PRJ_START_DIRECTORY_ENUMERATION_CB** Rückruf des Anbieters auf, um eine enumerationssitzung zu starten.</span><span class="sxs-lookup"><span data-stu-id="3f488-113">ProjFS calls the provider's **PRJ_START_DIRECTORY_ENUMERATION_CB** callback to start an enumeration session.</span></span>

    <span data-ttu-id="3f488-114">Im Rahmen der Verarbeitung dieses Rückrufs sollte der Anbieter die Ausführung der-Enumeration vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="3f488-114">As part of processing this callback the provider should prepare to perform the enumeration.</span></span>  <span data-ttu-id="3f488-115">Beispielsweise muss der Arbeitsspeicher belegt werden, der möglicherweise erforderlich ist, um den Fortschritt der Enumeration im Sicherungsdaten Speicher zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="3f488-115">For example, it should allocate any memory it may need to track the progress of the enumeration in its backing data store.</span></span>

    <span data-ttu-id="3f488-116">Projfs identifiziert das Verzeichnis, das im **FilePathName** -Member des _callBackData_ -Parameters des Rückrufs aufgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f488-116">ProjFS identifies the directory being enumerated in the **FilePathName** member of the callback's _callbackData_ parameter.</span></span>  <span data-ttu-id="3f488-117">Dies wird als Pfad relativ zum virtualisierungsstamm angegeben.</span><span class="sxs-lookup"><span data-stu-id="3f488-117">This is specified as a path relative to the virtualization root.</span></span>  <span data-ttu-id="3f488-118">Wenn sich beispielsweise der virtualisierungsstamm unter befindet `C:\virtRoot` und das aufgelistete Verzeichnis ist `C:\virtRoot\dir1\dir2` , enthält das Member **FilePathName** `dir1\dir2` .</span><span class="sxs-lookup"><span data-stu-id="3f488-118">For example, if the virtualization root is located at `C:\virtRoot`, and the directory being enumerated is `C:\virtRoot\dir1\dir2`, the **FilePathName** member will contain `dir1\dir2`.</span></span>  <span data-ttu-id="3f488-119">Der Anbieter bereitet sich darauf vor, diesen Pfad im Sicherungsdaten Speicher aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="3f488-119">The provider will prepare to enumerate that path in its backing data store.</span></span>  <span data-ttu-id="3f488-120">Abhängig von den Funktionen des Sicherungs Speicher eines Anbieters ist es möglicherweise sinnvoll, die Sicherungs Speicher-Enumeration im **PRJ_START_DIRECTORY_ENUMERATION_CB** Rückruf auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3f488-120">Depending on the capabilities of a provider's backing store it may make sense to perform the backing store enumeration in the **PRJ_START_DIRECTORY_ENUMERATION_CB** callback.</span></span>

    <span data-ttu-id="3f488-121">Da mehrere Enumerationen parallel im gleichen Verzeichnis auftreten können, weist jeder enumerationsrückruf ein _enumerationid_ -Argument auf, damit der Anbieter die Rückruf Aufrufe einer einzelnen enumerationssitzung zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="3f488-121">Because multiple enumerations may occur in parallel in the same directory, each enumeration callback has an _enumerationId_ argument to enable the provider to associate the callback invocations into a single enumeration session.</span></span>

    <span data-ttu-id="3f488-122">Wenn der Anbieter S_OK vom **PRJ_START_DIRECTORY_ENUMERATION_CB** Rückruf zurückgibt, muss er alle aufgelisteten enumerationssitzungsinformationen aufbewahren, bis der **PRJ_END_DIRECTORY_ENUMERATION_CB** -Rückruf mit dem gleichen Wert für _enumerationid_ von projfs aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3f488-122">If the provider returns S_OK from the **PRJ_START_DIRECTORY_ENUMERATION_CB** callback, it must maintain any enumeration session information it has until ProjFS invokes the **PRJ_END_DIRECTORY_ENUMERATION_CB** callback with the same value for _enumerationId_.</span></span>  <span data-ttu-id="3f488-123">Wenn der Anbieter einen Fehler von **PRJ_START_DIRECTORY_ENUMERATION_CB** zurückgibt, ruft projfs den **PRJ_END_DIRECTORY_ENUMERATION_CB** -Rückruf für diese _enumerationid_ nicht auf.</span><span class="sxs-lookup"><span data-stu-id="3f488-123">If the provider returns an error from **PRJ_START_DIRECTORY_ENUMERATION_CB**, ProjFS will not invoke the **PRJ_END_DIRECTORY_ENUMERATION_CB** callback for that _enumerationId_.</span></span>

1. <span data-ttu-id="3f488-124">Der **PRJ_GET_DIRECTORY_ENUMERATION_CB** Rückruf des Anbieters wird von projfs einmal oder mehrmals aufgerufen, um den Verzeichnis Inhalt des Anbieters zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3f488-124">ProjFS calls the provider's **PRJ_GET_DIRECTORY_ENUMERATION_CB** callback one or more times to get the directory contents from the provider.</span></span>

    <span data-ttu-id="3f488-125">Als Reaktion auf diesen Rückruf gibt der Anbieter eine sortierte Liste von Elementen aus dem Sicherungsdaten Speicher zurück.</span><span class="sxs-lookup"><span data-stu-id="3f488-125">In response to this callback the provider returns a sorted list of items from its backing data store.</span></span>

    <span data-ttu-id="3f488-126">Der Rückruf kann einen Such Ausdruck in seinem _SearchExpression_ -Parameter bereitstellen, den der Anbieter für den Bereich der Ergebnisse der-Enumeration verwendet.</span><span class="sxs-lookup"><span data-stu-id="3f488-126">The callback may provide a search expression in its _searchExpression_ parameter that the provider uses to scope the results of the enumeration.</span></span>  <span data-ttu-id="3f488-127">Wenn _SearchExpression_ NULL ist, gibt der Anbieter alle Einträge in dem aufgelisteten Verzeichnis zurück.</span><span class="sxs-lookup"><span data-stu-id="3f488-127">If _searchExpression_ is NULL, the provider returns all the entries in the directory being enumerated.</span></span>  <span data-ttu-id="3f488-128">Wenn er nicht NULL ist, kann der Anbieter **[prjdoesnamecontainwildcards](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards)** verwenden, um zu bestimmen, ob der Ausdruck Platzhalter enthält.</span><span class="sxs-lookup"><span data-stu-id="3f488-128">If it is non-NULL, the provider can use **[PrjDoesNameContainWildCards](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards)** to determine whether there are wildcards in the expression.</span></span>  <span data-ttu-id="3f488-129">Wenn dies der Fall ist, verwendet der Anbieter **[prjdatamematch](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch)** , um zu bestimmen, ob ein Eintrag im Verzeichnis mit dem Such Ausdruck übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="3f488-129">If there are, the provider uses **[PrjFileNameMatch](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch)** to determine whether an entry in the directory matches the search expression.</span></span>

    <span data-ttu-id="3f488-130">Der Anbieter sollte beim ersten Aufruf dieses Rückrufs den Wert von _SearchExpression_ erfassen.</span><span class="sxs-lookup"><span data-stu-id="3f488-130">The provider should capture the value of _searchExpression_ on the first invocation of this callback.</span></span>  <span data-ttu-id="3f488-131">Der erfasste Wert wird bei jedem nachfolgenden Aufruf des Rückrufs in derselben enumerationssitzung verwendet, es sei denn, PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN im **Flags** -Feld des _callBackData_ -Parameters des Rückrufs festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3f488-131">It uses the captured value on any subsequent invocation of the callback in the same enumeration session, unless PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN is set in the **Flags** field of the callback's _callbackData_ parameter.</span></span>  <span data-ttu-id="3f488-132">In diesem Fall sollte der Wert von _SearchExpression_ erneut erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="3f488-132">In that case it should recapture the value of _searchExpression_.</span></span>

    <span data-ttu-id="3f488-133">Wenn der Sicherungs Speicher keine übereinstimmenden Einträge enthält, gibt der Anbieter einfach S_OK aus dem Rückruf zurück.</span><span class="sxs-lookup"><span data-stu-id="3f488-133">If there are no matching entries in its backing store, the provider simply returns S_OK from the callback.</span></span>  <span data-ttu-id="3f488-134">Andernfalls formatiert der Anbieter jeden übereinstimmenden Eintrag aus dem Sicherungs Speicher in eine **[PRJ_FILE_BASIC_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info)** Struktur und verwendet dann **[prjfilldirentrybuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer)** , um den Puffer auszufüllen, der vom _direntrybufferhandle_ -Parameter des Rückrufs bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3f488-134">Otherwise the provider formats each matching entry from its backing store into a **[PRJ_FILE_BASIC_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info)** structure, and then uses **[PrjFillDirEntryBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer)** to fill the buffer provided by the callback's _dirEntryBufferHandle_ parameter.</span></span>  <span data-ttu-id="3f488-135">Der Anbieter fügt weiterhin Einträge hinzu, bis Sie alle hinzugefügt haben oder bis **prjfilldirentrybuffer** HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER) zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="3f488-135">The provider keeps adding entries until it has added them all or until **PrjFillDirEntryBuffer** returns HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER).</span></span>  <span data-ttu-id="3f488-136">Anschließend gibt der Anbieter S_OK aus dem Rückruf zurück.</span><span class="sxs-lookup"><span data-stu-id="3f488-136">Then the provider returns S_OK from the callback.</span></span>  <span data-ttu-id="3f488-137">Beachten Sie, dass der Anbieter die Einträge dem _direntrybufferhandle_ -Puffer in der richtigen Sortierreihenfolge hinzufügen muss.</span><span class="sxs-lookup"><span data-stu-id="3f488-137">Note that the provider must add the entries to the _dirEntryBufferHandle_ buffer in the correct sort order.</span></span>  <span data-ttu-id="3f488-138">Der Anbieter sollte **[prjdatamecompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** verwenden, um die richtige Sortierreihenfolge zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="3f488-138">The provider should use **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** to determine the correct sort order.</span></span>

    > <span data-ttu-id="3f488-139">Der Anbieter muss einen Wert für das **IsDirectory** -Mitglied von **PRJ_FILE_BASIC_INFO** bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="3f488-139">The provider must supply a value for the **IsDirectory** member of **PRJ_FILE_BASIC_INFO**.</span></span>  <span data-ttu-id="3f488-140">Wenn **IsDirectory** den Wert false hat, muss der Anbieter auch einen Wert für das **FileSize** -Element angeben.</span><span class="sxs-lookup"><span data-stu-id="3f488-140">If **IsDirectory** is FALSE, the provider must also supply a value for the **FileSize** member.</span></span>
    >
    > <span data-ttu-id="3f488-141">Wenn der Anbieter keine Werte für die Member " **comationtime**", " **LastAccessTime**", " **lastschreitetime**" und " **changetime** " bereitstellt, verwendet projfs die aktuelle Systemzeit.</span><span class="sxs-lookup"><span data-stu-id="3f488-141">If the provider does not supply values for the **CreationTime**, **LastAccessTime**, **LastWriteTime**, and **ChangeTime** members, ProjFS will use the current system time.</span></span>
    >
    > <span data-ttu-id="3f488-142">Projfs verwendet alle FILE_ATTRIBUTE Flags, die der Anbieter im **FileAttribute** -Member festlegt, außer FILE_ATTRIBUTE_DIRECTORY; Er legt den korrekten Wert für FILE_ATTRIBUTE_DIRECTORY im **fileattributmember** gemäß dem angegebenen Wert des **IsDirectory** -Members fest.</span><span class="sxs-lookup"><span data-stu-id="3f488-142">ProjFS will use whatever FILE_ATTRIBUTE flags the provider sets in the **FileAttributes** member except for FILE_ATTRIBUTE_DIRECTORY; it will set the correct value for FILE_ATTRIBUTE_DIRECTORY in the **FileAttributes** member according to the supplied value of the **IsDirectory** member.</span></span>

    <span data-ttu-id="3f488-143">Wenn **prjfilldirentrybuffer** HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER) zurückgibt, bevor der Anbieter keine Einträge mehr hinzufügt, um ihn hinzuzufügen, muss der Anbieter den Eintrag nachverfolgen, den er beim Empfangen des Fehlers hinzufügen wollte.</span><span class="sxs-lookup"><span data-stu-id="3f488-143">If **PrjFillDirEntryBuffer** returns HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) before the provider runs out of entries to add to it, the provider must keep track of the entry it was trying to add when it received the error.</span></span>  <span data-ttu-id="3f488-144">Beim nächsten Aufrufen des **PRJ_GET_DIRECTORY_ENUMERATION_CB** Rückrufs für die gleiche enumerationssitzung durch projfs muss der Anbieter das Hinzufügen von Einträgen zum _direntrybufferhandle_ -Puffer mit dem hinzu zufügenden Eintrag fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="3f488-144">The next time ProjFS calls the **PRJ_GET_DIRECTORY_ENUMERATION_CB** callback for the same enumeration session, the provider must resume adding entries to the _dirEntryBufferHandle_ buffer with the entry it was trying to add.</span></span>

    > <span data-ttu-id="3f488-145">Wenn der Sicherungs Speicher symbolische Verknüpfungen unterstützt, muss der Anbieter **[PrjFillDirEntryBuffer2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2)** verwenden, um den Puffer auszufüllen, der vom _direntrybufferhandle_ -Parameter des Rückrufs bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3f488-145">If the backing store supports symbolic links, the provider must use **[PrjFillDirEntryBuffer2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2)** to fill the buffer provided by the callback's _dirEntryBufferHandle_ parameter.</span></span>  <span data-ttu-id="3f488-146">**PrjFillDirEntryBuffer2** unterstützt eine zusätzliche Puffer Eingabe, die es dem Anbieter ermöglicht, anzugeben, dass es sich bei dem Enumerationseintrag um einen symbolischen Link handelt und was sein Ziel ist.</span><span class="sxs-lookup"><span data-stu-id="3f488-146">**PrjFillDirEntryBuffer2** supports an extra buffer input that allows the provider to specify that the enumeration entry is a symbolic link and what its target is.</span></span>  <span data-ttu-id="3f488-147">Andernfalls verhält sie sich wie oben für **prjfilldirentrybuffer** beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3f488-147">It otherwise behaves as described above for **PrjFillDirEntryBuffer**.</span></span>  <span data-ttu-id="3f488-148">Im folgenden Beispiel wird **PrjFillDirEntryBuffer2** verwendet, um die Unterstützung für symbolische Verknüpfungen zu veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="3f488-148">The following sample uses **PrjFillDirEntryBuffer2** to illustrate support for symbolic links.</span></span>
    >
    > <span data-ttu-id="3f488-149">Beachten Sie, dass **PrjFillDirEntryBuffer2** ab Windows 10, Version 2004, unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="3f488-149">Note that **PrjFillDirEntryBuffer2** is supported as of Windows 10, version 2004.</span></span>  <span data-ttu-id="3f488-150">Ein Anbieter sollte überprüfen, ob PrjFillDirEntryBuffer2 vorhanden ist, z. . mithilfe von **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.</span><span class="sxs-lookup"><span data-stu-id="3f488-150">A provider should probe for the existence of **PrjFillDirEntryBuffer2**, for instance by using **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.</span></span>

    ```C++
    typedef struct MY_ENUM_ENTRY MY_ENUM_ENTRY;

    typedef struct MY_ENUM_ENTRY {
        MY_ENUM_ENTRY* Next;
        PWSTR Name;
        BOOLEAN IsDirectory;
        INT64 FileSize;
        BOOLEAN IsSymlink;
        PWSTR SymlinkTarget;
    } MY_ENUM_ENTRY;

    typedef struct MY_ENUM_SESSION {
        GUID EnumerationId;
        PWSTR SearchExpression;
        USHORT SearchExpressionMaxLen;
        BOOLEAN SearchExpressionCaptured;
        MY_ENUM_ENTRY* EnumHead;
        MY_ENUM_ENTRY* LastEnumEntry;
        BOOLEAN EnumCompleted;
    } MY_ENUM_SESSION;

    HRESULT
    MyGetEnumCallback(
        _In_ const PRJ_CALLBACK_DATA* callbackData,
        _In_ const GUID* enumerationId,
        _In_opt_z_ PCWSTR searchExpression,
        _In_ PRJ_DIR_ENTRY_BUFFER_HANDLE dirEntryBufferHandle
        )
    {
        // MyGetEnumSession is a routine the provider might implement to find
        // information about the enumeration session that it first stored
        // when processing its PRJ_START_DIRECTORY_ENUMERATION_CB callback.
        //
        // In this example the PRJ_START_DIRECTORY_ENUMERATION_CB callback has
        // already retrieved a list of the items in the backing store located at
        // callbackData->FilePathName, sorted them using PrjFileNameCompare()
        // to determine collation order, and stored the list in session->EnumHead.
        MY_ENUM_SESSION* session = NULL;
        session = MyGetEnumSession(enumerationId);

        if (session == NULL)
        {
            return HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER);
        }

        if (!session->SearchExpressionCaptured ||
            (callbackData->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
        {
            if (searchExpression != NULL)
            {
                if (wcsncpy_s(session->SearchExpression,
                              session->SearchExpressionMaxLen,
                              searchExpression,
                              wcslen(searchExpression)))
                {
                    // Failed to copy the search expression; perhaps the provider
                    // could try reallocating session->SearchExpression.
                }
            }
            else
            {
                if (wcsncpy_s(session->SearchExpression,
                              session->SearchExpressionMaxLen,
                              "*",
                              1))
                {
                    // Failed to copy the search expression; perhaps the provider
                    // could try reallocating session->SearchExpression.
                }
            }
            session->SearchExpressionCaptured = TRUE;
        }

        MY_ENUM_ENTRY* enumHead = NULL;

        // We have to start the enumeration from the beginning if we aren't
        // continuing an existing session or if the caller is requesting a restart.
        if (((session->LastEnumEntry == NULL) &&
             !session->EnumCompleted) ||
            (callbackData->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
        {
            // Ensure that if the caller is requesting a restart we reset our
            // bookmark of how far we got in the enumeration.
            session->LastEnumEntry = NULL;

            // In case we're restarting ensure we don't think we're done.
            session->EnumCompleted = FALSE;

            // We need to start considering items from the beginning of the list
            // retrieved from the backing store.
            enumHead = session->EnumHead;
        }
        else
        {
            // We are resuming an existing enumeration session.  Note that
            // session->LastEnumEntry may be NULL.  That is okay; it means
            // we got all the entries the last time this callback was invoked.
            // Returning S_OK without adding any new entries to the
            // dirEntryBufferHandle buffer signals ProjFS that the enumeration
            // has returned everything it can.
            enumHead = session->LastEnumEntry;
        }

        if (enumHead == NULL)
        {
            // There are no items to return.  Remember that we've returned everything
            // we can.
            session->EnumCompleted = TRUE;
        }
        else
        {
            MY_ENUM_ENTRY* thisEntry = enumHead;
            while (thisEntry != NULL)
            {
                // We'll insert the entry into the return buffer if it matches
                // the search expression captured for this enumeration session.
                if (PrjFileNameMatch(thisEntry->Name, session->SearchExpression))
                {
                    PRJ_FILE_BASIC_INFO fileBasicInfo = {};
                    fileBasicInfo.IsDirectory = thisEntry->IsDirectory;
                    fileBasicInfo.FileSize = thisEntry->FileSize;

                    // If our backing store says this is really a symbolic link,
                    // set up to tell ProjFS that it is a symlink and what its
                    // target is.
                    PRJ_EXTENDED_INFO extraInfo = {};
                    if (thisEntry->IsSymlink)
                    {
                        extraInfo.InfoType = PRJ_EXT_INFO_SYMLINK;
                        extraInfo.Symlink.TargetName = thisEntry->SymlinkTarget;
                    }

                    // Format the entry for return to ProjFS.
                    HRESULT fillResult = PrjFillDirEntryBuffer2(dirEntryBufferHandle,
                                                                thisEntry->Name,
                                                                &fileBasicInfo,
                                                                thisEntry->IsSymlink ? &extraInfo : NULL);

                    if (fillResult == HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER))
                    {
                        // We couldn't add this entry to the buffer; remember where we left
                        // off for the next time we're called for this enumeration session.
                        session->LastEnumEntry = thisEntry;
                        return S_OK;
                    }
                }

                thisEntry = thisEntry->Next;
            }

            // We reached the end of the list of entries; remember that we've returned
            // everything we can.
            session->EnumCompleted = TRUE;
        }

        return S_OK;
    }
    ```

1. <span data-ttu-id="3f488-151">Projfs Ruft den **PRJ_END_DIRECTORY_ENUMERATION_CB** Rückruf des Anbieters auf, um die enumerationssitzung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="3f488-151">ProjFS calls the provider's **PRJ_END_DIRECTORY_ENUMERATION_CB** callback to end the enumeration session.</span></span>

    <span data-ttu-id="3f488-152">Der Anbieter sollte sämtliche Bereinigungs Schritte ausführen, um die enumerationssitzung zu beenden, wie z. b. das Aufheben der Zuordnung von Arbeitsspeicher, der im Rahmen der Verarbeitung **PRJ_START_DIRECTORY_ENUMERATION_CB** zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="3f488-152">The provider should perform any cleanup it needs to do to end the enumeration session, such as deallocate memory allocated as part of processing **PRJ_START_DIRECTORY_ENUMERATION_CB**.</span></span>
