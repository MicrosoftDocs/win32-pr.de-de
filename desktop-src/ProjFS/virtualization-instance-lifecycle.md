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
# <a name="virtualization-instance-lifecycle"></a><span data-ttu-id="48c67-103">Lebenszyklus der virtualisierungsinstanz</span><span class="sxs-lookup"><span data-stu-id="48c67-103">Virtualization Instance Lifecycle</span></span>

<span data-ttu-id="48c67-104">Die Anbieter Anwendung verwaltet mindestens eine virtualisierungsinstanz.</span><span class="sxs-lookup"><span data-stu-id="48c67-104">The provider application maintains one or more virtualization instances.</span></span>  <span data-ttu-id="48c67-105">Jede virtualisierungsinstanz durchläuft vier Phasen in Ihrem Lebenszyklus:</span><span class="sxs-lookup"><span data-stu-id="48c67-105">Each virtualization instance goes through four stages in its lifecycle:</span></span>

1. <span data-ttu-id="48c67-106">Erstellung</span><span class="sxs-lookup"><span data-stu-id="48c67-106">Creation</span></span>
2. <span data-ttu-id="48c67-107">Start</span><span class="sxs-lookup"><span data-stu-id="48c67-107">Startup</span></span>
3. <span data-ttu-id="48c67-108">Typ</span><span class="sxs-lookup"><span data-stu-id="48c67-108">Runtime</span></span>
4. <span data-ttu-id="48c67-109">Shutdown</span><span class="sxs-lookup"><span data-stu-id="48c67-109">Shutdown</span></span>

<span data-ttu-id="48c67-110">Beachten Sie, dass der Anbieter nach dem Herunterfahren einer virtualisierungsinstanz ihn nicht erneut erstellen muss, um ihn wiederzuverwenden.</span><span class="sxs-lookup"><span data-stu-id="48c67-110">Note that after shutting down a virtualization instance the provider does not need to re-create it to reuse it.</span></span>  <span data-ttu-id="48c67-111">Sie kann einfach erneut gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="48c67-111">It can simply start it up again.</span></span>

> <span data-ttu-id="48c67-112">**Hinweis**: in diesem Abschnitt werden Beispiele für projfs-APIs gezeigt.</span><span class="sxs-lookup"><span data-stu-id="48c67-112">**Note**: This section shows examples of ProjFS APIs.</span></span>  <span data-ttu-id="48c67-113">Jedes Beispiel dient zur Veranschaulichung der grundlegenden API-Verwendung.</span><span class="sxs-lookup"><span data-stu-id="48c67-113">Each example is meant to illustrate basic API usage.</span></span>  <span data-ttu-id="48c67-114">Eine Dokumentation der in diesen Beispielen nicht verwendeten Optionen finden Sie in der [projfs-API-Referenz](/windows/desktop/api/_projfs).</span><span class="sxs-lookup"><span data-stu-id="48c67-114">For documentation of options unused in these examples please consult the [ProjFS API reference](/windows/desktop/api/_projfs).</span></span>

## <a name="creating-a-virtualization-root"></a><span data-ttu-id="48c67-115">Erstellen eines virtualisierungsstamms</span><span class="sxs-lookup"><span data-stu-id="48c67-115">Creating a virtualization root</span></span>

<span data-ttu-id="48c67-116">Bevor ein Anbieter die virtualisierungsinstanz starten kann, mit der Elemente in das lokale Dateisystem integriert werden, muss der virtualisierungsstamm erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="48c67-116">Before a provider can start up the virtualization instance that will project items into the local file system, it must create the virtualization root.</span></span>  <span data-ttu-id="48c67-117">Der virtualisierungsstamm ist das Verzeichnis, in dem der Anbieter eine Struktur von Verzeichnissen und Dateien projiziert.</span><span class="sxs-lookup"><span data-stu-id="48c67-117">The virtualization root is the directory under which the provider projects a tree of directories and files.</span></span>

<span data-ttu-id="48c67-118">Zum Erstellen eines virtualisierungsstamms muss der Anbieter folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="48c67-118">To create a virtualization root the provider must:</span></span>

1. <span data-ttu-id="48c67-119">Erstellen Sie ein Verzeichnis, das als virtualisierungsstamm fungiert.</span><span class="sxs-lookup"><span data-stu-id="48c67-119">Create a directory to serve as the virtualization root.</span></span>

    <span data-ttu-id="48c67-120">Der Anbieter erstellt ein Verzeichnis, das als virtualisierungsstamm verwendet werden soll, z. b. " **[kreatedirectory](/windows/desktop/api/fileapi/nf-fileapi-createdirectoryw)**":</span><span class="sxs-lookup"><span data-stu-id="48c67-120">The provider creates a directory to serve as the virtualization root using, for example **[CreateDirectory](/windows/desktop/api/fileapi/nf-fileapi-createdirectoryw)**:</span></span>

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

1. <span data-ttu-id="48c67-121">Erstellen Sie eine Instanz-ID der Virtualisierung.</span><span class="sxs-lookup"><span data-stu-id="48c67-121">Create a virtualization instance ID.</span></span>

    <span data-ttu-id="48c67-122">Jede virtualisierungsinstanz verfügt über eine eindeutige ID, die als _virtualisierungsinstanz-ID_ bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="48c67-122">Every virtualization instance has a unique ID called the _virtualization instance ID_.</span></span>  <span data-ttu-id="48c67-123">Das System verwendet diesen Wert, um zu ermitteln, welcher virtualisierungsinstanz der Inhalt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="48c67-123">The system uses this value to identify which virtualization instance its contents are associated to.</span></span>

    ```C++
    GUID instanceId;
    hr = CoCreateGuid(&instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to create instance ID (0x%08x)\n", hr);
        return;
    }
    ```

1. <span data-ttu-id="48c67-124">Markieren Sie das neue Verzeichnis als virtualisierungsstamm.</span><span class="sxs-lookup"><span data-stu-id="48c67-124">Mark the new directory as the virtualization root.</span></span>

    <span data-ttu-id="48c67-125">Der Anbieter ruft **[prjmarkdirectoryasplachalter](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** auf, um das neue Verzeichnis als virtualisierungsstamm zu markieren und es der virtualisierungsinstanz zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="48c67-125">The provider calls **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** to mark the new directory as the virtualization root and assign it to the virtualization instance.</span></span>

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

<span data-ttu-id="48c67-126">Der Anbieter muss für jede virtualisierungsinstanz nur einmal den virtualisierungsstamm erstellen.</span><span class="sxs-lookup"><span data-stu-id="48c67-126">The provider only needs to create the virtualization root once for each virtualization instance.</span></span>  <span data-ttu-id="48c67-127">Nachdem ein Stamm erstellt wurde, kann die zugehörige Instanz wiederholt gestartet und beendet werden, ohne dass der Stamm neu erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="48c67-127">Once a root has been created, its associated instance can be repeatedly started and stopped without recreating the root.</span></span>

## <a name="starting-a-virtualization-instance"></a><span data-ttu-id="48c67-128">Starten einer virtualisierungsinstanz</span><span class="sxs-lookup"><span data-stu-id="48c67-128">Starting a virtualization instance</span></span>

<span data-ttu-id="48c67-129">Nachdem der virtualisierungsstamm erstellt wurde, muss der Anbieter die virtualisierungsinstanz starten.</span><span class="sxs-lookup"><span data-stu-id="48c67-129">Once the virtualization root has been created the provider must start the virtualization instance.</span></span>  <span data-ttu-id="48c67-130">Dadurch wird projfs signalisiert, dass der Anbieter bereit ist, Rückrufe zu empfangen und Daten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="48c67-130">This signals ProjFS that the provider is ready to receive callbacks and provide data.</span></span>

<span data-ttu-id="48c67-131">Zum Starten der virtualisierungsinstanz muss der Anbieter</span><span class="sxs-lookup"><span data-stu-id="48c67-131">To start the virtualization instance the provider must:</span></span>

1. <span data-ttu-id="48c67-132">Richten Sie die Rückruf Tabelle ein.</span><span class="sxs-lookup"><span data-stu-id="48c67-132">Set up the callback table.</span></span>

    <span data-ttu-id="48c67-133">Projfs kommuniziert mit dem Anbieter, indem Rückruf Routinen aufgerufen werden, die vom Anbieter implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="48c67-133">ProjFS communicates with the provider by invoking callback routines implemented by the provider.</span></span>  <span data-ttu-id="48c67-134">Der Anbieter füllt eine [PRJ_CALLBACKS](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callbacks) Struktur mit Zeigern auf seine Rückruf Routinen auf.</span><span class="sxs-lookup"><span data-stu-id="48c67-134">The provider populates a [PRJ_CALLBACKS](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callbacks) struct with pointers to its callback routines.</span></span>

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

1. <span data-ttu-id="48c67-135">Starten Sie die-Instanz.</span><span class="sxs-lookup"><span data-stu-id="48c67-135">Start the instance.</span></span>

    <span data-ttu-id="48c67-136">Der Anbieter ruft **[prjstartvirtualization](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)** auf, um die virtualisierungsinstanz zu starten.</span><span class="sxs-lookup"><span data-stu-id="48c67-136">The provider calls **[PrjStartVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)** to start the virtualization instance.</span></span>

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
    <span data-ttu-id="48c67-137">Der Parameter " _InstanceHandle_ " von **prjstartvirtualization** gibt ein Handle für die virtualisierungsinstanz zurück.</span><span class="sxs-lookup"><span data-stu-id="48c67-137">**PrjStartVirtualizing**'s _instanceHandle_ parameter returns a handle to the virtualization instance.</span></span>  <span data-ttu-id="48c67-138">Der Anbieter verwendet dieses Handle, wenn andere projfs-APIs aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="48c67-138">The provider uses this handle when calling other ProjFS APIs.</span></span>

## <a name="virtualization-instance-runtime"></a><span data-ttu-id="48c67-139">Laufzeit der virtualisierungsinstanz</span><span class="sxs-lookup"><span data-stu-id="48c67-139">Virtualization instance runtime</span></span>

<span data-ttu-id="48c67-140">Nachdem der Aufruf von **prjstartvirtualization** zurückgegeben wurde, werden die Rückruf Routinen des Anbieters von projfs als Reaktion auf Dateisystem Vorgänge in der virtualisierungsinstanz aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="48c67-140">Once the call to **PrjStartVirtualizing** returns, ProjFS will invoke the provider's callback routines in response to file system operations in the virtualization instance.</span></span>  <span data-ttu-id="48c67-141">Informationen dazu, wie der Anbieter verschiedene Dateisystem Vorgänge verarbeiten kann, finden Sie in den folgenden Abschnitten:</span><span class="sxs-lookup"><span data-stu-id="48c67-141">For information on how the provider can handle various file system operations, refer to the following sections:</span></span>

* [<span data-ttu-id="48c67-142">Auflisten von Dateien und Verzeichnissen</span><span class="sxs-lookup"><span data-stu-id="48c67-142">Enumerating Files and Directories</span></span>](enumerating-files-and-directories.md)
* [<span data-ttu-id="48c67-143">Bereitstellen von Dateidaten</span><span class="sxs-lookup"><span data-stu-id="48c67-143">Providing File Data</span></span>](providing-file-data.md)
* [<span data-ttu-id="48c67-144">Datei System-Vorgangs Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="48c67-144">File System Operation Notifications</span></span>](file-system-operation-notifications.md)
* [<span data-ttu-id="48c67-145">Behandeln von Änderungen der Ansicht</span><span class="sxs-lookup"><span data-stu-id="48c67-145">Handling View Changes</span></span>](handling-view-changes.md)

## <a name="shutting-down-a-virtualization-instance"></a><span data-ttu-id="48c67-146">Herunterfahren einer virtualisierungsinstanz</span><span class="sxs-lookup"><span data-stu-id="48c67-146">Shutting down a virtualization instance</span></span>

<span data-ttu-id="48c67-147">Um projfs zu signalisieren, dass der Anbieter keine Rückrufe mehr empfangen und Daten bereitstellen möchte, muss der Anbieter die virtualisierungsinstanz abbrechen.</span><span class="sxs-lookup"><span data-stu-id="48c67-147">To signal ProjFS that the provider wants to stop receiving callbacks and providing data, the provider must stop the virtualization instance.</span></span>  <span data-ttu-id="48c67-148">Zu diesem Zweck ruft der Anbieter **[prjstopvirtualization](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing)** auf und übergibt ihm das Handle an die virtualisierungsinstanz, die er vom Aufruf an **prjstartvirtualization** empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="48c67-148">To do this the provider calls **[PrjStopVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing)**, passing it the handle to the virtualization instance that it received from the call to **PrjStartVirtualizing**.</span></span>

```C++
PrjStopVirtualizing(instanceHandle);
```

<span data-ttu-id="48c67-149">Beachten Sie, dass projfs die Rückruf Routinen des Anbieters weiterhin aufrufen kann, bis dieser Aufruf zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="48c67-149">Note that until this call returns, ProjFS may continue to invoke the provider's callback routines.</span></span>