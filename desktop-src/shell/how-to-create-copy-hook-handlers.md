---
description: Verwenden von Shellerweiterungen zum Implementieren eines kopierhook-Handlers.
ms.assetid: 05808281-84fb-402d-9fa1-3a747b29d030
title: Erstellen von Kopier-Hook-Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1468839eacc10272f8f97a120b98ada6d580bacf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215945"
---
# <a name="how-to-create-copy-hook-handlers"></a><span data-ttu-id="64559-103">Erstellen von Kopier-Hook-Handlern</span><span class="sxs-lookup"><span data-stu-id="64559-103">How to Create Copy Hook Handlers</span></span>

<span data-ttu-id="64559-104">Die allgemeinen Verfahren zum Implementieren und Registrieren eines Shellerweiterungs Handlers werden unter [Erstellen von Shellerweiterungs Handlern](handlers.md)erläutert.</span><span class="sxs-lookup"><span data-stu-id="64559-104">The general procedures for implementing and registering a Shell extension handler are discussed in [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="64559-105">Dieses Dokument konzentriert sich auf die Aspekte der Implementierung, die für das Kopieren von Hook-Handlern spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="64559-105">This document focuses on those aspects of implementation that are specific to copy hook handlers.</span></span>

-   [<span data-ttu-id="64559-106">Implementieren von Kopier-Hook-Handlern</span><span class="sxs-lookup"><span data-stu-id="64559-106">Implementing Copy Hook Handlers</span></span>](#step-1-implementing-copy-hook-handlers)
-   [<span data-ttu-id="64559-107">Registrieren von Kopier-Hook-Handlern</span><span class="sxs-lookup"><span data-stu-id="64559-107">Registering Copy Hook Handlers</span></span>](#step-2-registering-copy-hook-handlers)
-   [<span data-ttu-id="64559-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="64559-108">Related topics</span></span>](#related-topics)

## <a name="instructions"></a><span data-ttu-id="64559-109">Instructions</span><span class="sxs-lookup"><span data-stu-id="64559-109">Instructions</span></span>

### <a name="step-1-implementing-copy-hook-handlers"></a><span data-ttu-id="64559-110">Schritt 1: Implementieren von Kopier-Hook-Handlern</span><span class="sxs-lookup"><span data-stu-id="64559-110">Step 1: Implementing Copy Hook Handlers</span></span>

<span data-ttu-id="64559-111">Wie bei allen Shellerweiterungs Handlern sind kopierhandler für den Kopiervorgang in-Process-Component Object Model (com)-Objekten, die als DLLs implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="64559-111">Like all Shell extension handlers, copy hook handlers are in-process Component Object Model (COM) objects implemented as DLLs.</span></span> <span data-ttu-id="64559-112">Sie exportieren zusätzlich zu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**icopyhook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))eine Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="64559-112">They export one interface in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)).</span></span> <span data-ttu-id="64559-113">Die Shell initialisiert den Handler direkt, sodass keine Initialisierungs Schnittstelle wie [**ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="64559-113">The Shell initializes the handler directly, so there is no need for an initialization interface such as [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit).</span></span>

<span data-ttu-id="64559-114">Die [**icopyhook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)) -Schnittstelle verfügt über eine einzelne Methode, [**icopyhook:: copycallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="64559-114">The [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)) interface has a single method, [**ICopyHook::CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)).</span></span> <span data-ttu-id="64559-115">Wenn ein Ordner gerade verschoben wird, ruft die Shell diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="64559-115">When a folder is about to be moved, the Shell calls this method.</span></span> <span data-ttu-id="64559-116">Sie übergibt eine Vielzahl von Informationen, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="64559-116">It passes in a variety of information, including:</span></span>

-   <span data-ttu-id="64559-117">Der Name des Ordners.</span><span class="sxs-lookup"><span data-stu-id="64559-117">The folder's name.</span></span>
-   <span data-ttu-id="64559-118">Der Ziel-oder neue Name des Ordners.</span><span class="sxs-lookup"><span data-stu-id="64559-118">The folder's destination or new name.</span></span>
-   <span data-ttu-id="64559-119">Der Vorgang, der versucht wird.</span><span class="sxs-lookup"><span data-stu-id="64559-119">The operation that is being attempted.</span></span>
-   <span data-ttu-id="64559-120">Die Attribute der Quell-und Zielordner.</span><span class="sxs-lookup"><span data-stu-id="64559-120">The attributes of the source and destination folders.</span></span>
-   <span data-ttu-id="64559-121">Ein Fenster Handle, das verwendet werden kann, um eine Benutzeroberfläche anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="64559-121">A window handle that can be used to display a user interface.</span></span>

<span data-ttu-id="64559-122">Wenn die [**icopyhook:: copycallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)) -Methode Ihres Handlers aufgerufen wird, gibt Sie einen der drei folgenden Werte zurück, um der Shell anzuzeigen, wie Sie fortfahren soll.</span><span class="sxs-lookup"><span data-stu-id="64559-122">When your handler's [**ICopyHook::CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)) method is called, it returns one of the three following values to indicate to the Shell how it should proceed.</span></span>



| <span data-ttu-id="64559-123">Wert</span><span class="sxs-lookup"><span data-stu-id="64559-123">Value</span></span>    | <span data-ttu-id="64559-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64559-124">Description</span></span>                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64559-125">IDYES</span><span class="sxs-lookup"><span data-stu-id="64559-125">IDYES</span></span>    | <span data-ttu-id="64559-126">Ermöglicht den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="64559-126">Allows the operation.</span></span>                                                                                                                            |
| <span data-ttu-id="64559-127">IDNO</span><span class="sxs-lookup"><span data-stu-id="64559-127">IDNO</span></span>     | <span data-ttu-id="64559-128">Verhindert den Vorgang in diesem Ordner.</span><span class="sxs-lookup"><span data-stu-id="64559-128">Prevents the operation on this folder.</span></span> <span data-ttu-id="64559-129">Die Shell kann mit allen anderen Vorgängen, die genehmigt wurden, fortgesetzt werden, z. b. einem Batch Kopiervorgang.</span><span class="sxs-lookup"><span data-stu-id="64559-129">The Shell can continue with any other operations that have been approved, such as a batch copy operation.</span></span> |
| <span data-ttu-id="64559-130">IDCANCEL</span><span class="sxs-lookup"><span data-stu-id="64559-130">IDCANCEL</span></span> | <span data-ttu-id="64559-131">Verhindert den aktuellen Vorgang und bricht alle ausstehenden Vorgänge ab.</span><span class="sxs-lookup"><span data-stu-id="64559-131">Prevents the current operation and cancels any pending operations.</span></span>                                                                               |



 

### <a name="step-2-registering-copy-hook-handlers"></a><span data-ttu-id="64559-132">Schritt 2: Registrieren von Kopier-Hook-Handlern</span><span class="sxs-lookup"><span data-stu-id="64559-132">Step 2: Registering Copy Hook Handlers</span></span>

<span data-ttu-id="64559-133">Kopieren Sie Hook-Handler für Ordner unter dem Stammverzeichnis der **HKEY- \_ Klassen \_** Stamm \\ **Verzeichnis** \\ **shellex** \\ **copyhookhandlers** .</span><span class="sxs-lookup"><span data-stu-id="64559-133">Copy hook handlers for folders are registered under the **HKEY\_CLASSES\_ROOT**\\**Directory**\\**shellex**\\**CopyHookHandlers** subkey.</span></span> <span data-ttu-id="64559-134">Erstellen Sie einen Unterschlüssel von **copyhuokhandlers** , der für den Handler benannt ist, und legen Sie den Standardwert des unter Schlüssels auf das Zeichen folgen Format der Klassen Bezeichner-GUID (CLSID) des Handlers fest.</span><span class="sxs-lookup"><span data-stu-id="64559-134">Create a subkey of **CopyHookHandlers** named for the handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span>

<span data-ttu-id="64559-135">Das folgende Beispiel fügt den Unterschlüssel **mycopyhandler** der Liste der Kopier-Hook-Handler der Shell hinzu.</span><span class="sxs-lookup"><span data-stu-id="64559-135">The following example adds the **MyCopyHandler** subkey to the Shell's list of copy hook handlers.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         CopyHookHandlers
            MyCopyHandler
               (Default) = {MyCopyHandler CLSID GUID}
```

<span data-ttu-id="64559-136">Das Kopieren von Hook-Handlern für Drucker Objekte wird im Wesentlichen auf die gleiche Weise registriert.</span><span class="sxs-lookup"><span data-stu-id="64559-136">Copy hook handlers for printer objects are registered in essentially the same way.</span></span> <span data-ttu-id="64559-137">Der einzige Unterschied besteht darin, dass Sie Sie unter dem Unterschlüssel **HKEY \_ Classes \_ root** \\ **Printer** unter Key registrieren müssen.</span><span class="sxs-lookup"><span data-stu-id="64559-137">The only difference is that you must register them under the **HKEY\_CLASSES\_ROOT**\\**Printers** subkey.</span></span>

## <a name="remarks"></a><span data-ttu-id="64559-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64559-138">Remarks</span></span>

<span data-ttu-id="64559-139">Normalerweise können Benutzer und Anwendungen Ordner mit wenigen Einschränkungen kopieren, verschieben, löschen oder umbenennen.</span><span class="sxs-lookup"><span data-stu-id="64559-139">Normally, users and applications can copy, move, delete, or rename folders with few restrictions.</span></span> <span data-ttu-id="64559-140">Durch Implementieren eines kopierhook-Handlers können Sie steuern, ob diese Vorgänge stattfinden.</span><span class="sxs-lookup"><span data-stu-id="64559-140">By implementing a copy hook handler, you can control whether these operations take place.</span></span> <span data-ttu-id="64559-141">Beispielsweise können Sie durch Implementieren eines solchen Handlers verhindern, dass wichtige Ordner umbenannt oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="64559-141">For instance, implementing such a handler allows you to prevent critical folders from being renamed or deleted.</span></span> <span data-ttu-id="64559-142">Das Kopieren von Hook-Handlern kann auch für Drucker Objekte implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="64559-142">Copy hook handlers can also be implemented for printer objects.</span></span>

<span data-ttu-id="64559-143">Kopieren von Hook-Handlern ist Global.</span><span class="sxs-lookup"><span data-stu-id="64559-143">Copy hook handlers are global.</span></span> <span data-ttu-id="64559-144">Alle registrierten Handler werden von der Shell jedes Mal aufgerufen, wenn eine Anwendung oder ein Benutzer versucht, einen Ordner oder ein Drucker Objekt zu kopieren, zu verschieben, zu löschen oder umzubenennen.</span><span class="sxs-lookup"><span data-stu-id="64559-144">The Shell calls all registered handlers every time an application or user attempts to copy, move, delete, or rename a folder or printer object.</span></span> <span data-ttu-id="64559-145">Der Handler führt den Vorgang selbst nicht aus.</span><span class="sxs-lookup"><span data-stu-id="64559-145">The handler does not perform the operation itself.</span></span> <span data-ttu-id="64559-146">Sie genehmigt oder überprüft Sie nur.</span><span class="sxs-lookup"><span data-stu-id="64559-146">It only approves or vetoes it.</span></span> <span data-ttu-id="64559-147">Wenn alle Handler eine Genehmigung durchführt, führt die Shell den Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="64559-147">If all handlers approve, the Shell does the operation.</span></span> <span data-ttu-id="64559-148">Wenn ein Handler den Vorgang überprüft, wird er abgebrochen, und die restlichen Handler werden nicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="64559-148">If any handler vetoes the operation, it is canceled and the remaining handlers are not called.</span></span> <span data-ttu-id="64559-149">Kopieren von Hook-Handlern wird nicht über den Erfolg oder Misserfolg des Vorgangs informiert, sodass Sie nicht zum Überwachen von Datei Vorgängen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="64559-149">Copy hook handlers are not informed of the success or failure of the operation, so they cannot be used to monitor file operations.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64559-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="64559-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64559-151">Erstellen von Shellerweiterungshandlern</span><span class="sxs-lookup"><span data-stu-id="64559-151">Creating Shell Extension Handlers</span></span>](handlers.md)
</dt> <dt>

<span data-ttu-id="64559-152">[**Icopyhook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="64559-152">[**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))</span></span>
</dt> </dl>

 

 
