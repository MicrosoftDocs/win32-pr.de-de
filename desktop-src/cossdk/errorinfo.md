---
description: Ruft erweiterte Fehlerinformationen zu Methoden ab, die mehrere Objekte behandeln, z. b. auffüllen und SaveChanges des comadmincatalogcollection-Objekts, und Methoden zum Installieren, importieren oder Exportieren von Anwendungen oder Komponenten für das comadmincatalog-Objekt.
ms.assetid: cf612fc4-55dd-4706-8c41-2654ca922b9a
title: ErrorInfo-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ErrorInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: ebcb4b89eee51b475869cfc62676feda10e53084
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483606"
---
# <a name="errorinfo-collection"></a><span data-ttu-id="a3b0b-103">ErrorInfo-Sammlung</span><span class="sxs-lookup"><span data-stu-id="a3b0b-103">ErrorInfo collection</span></span>

<span data-ttu-id="a3b0b-104">Ruft erweiterte Fehlerinformationen zu [**Methoden ab,**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) die mehrere Objekte behandeln, z. b. auffüllen und [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts, und Methoden zum Installieren, importieren oder Exportieren von Anwendungen oder Komponenten für das [**comadmincatalog**](comadmincatalog.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-104">Retrieves extended error information regarding methods that deal with multiple objects, such as [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, and methods to install, import, or export applications or components on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

<span data-ttu-id="a3b0b-105">Verwenden Sie die [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) -Methode für eine [**comadmincatalogcollection**](comadmincatalogcollection.md) , um auf die **errorInfo** -Auflistung zuzugreifen, die der ursprünglichen Auflistung mit einem Fehler zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-105">Use the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) method on a [**COMAdminCatalogCollection**](comadmincatalogcollection.md) to access the **ErrorInfo** collection associated with the original collection that has an error.</span></span>

<span data-ttu-id="a3b0b-106">Sie müssen [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) direkt nach einem Fehler auf **errorInfo** aufrufen. Andernfalls gehen die Fehlerinformationen verloren.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-106">You must call [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) on **ErrorInfo** immediately after an error occurs; otherwise, the error information is lost.</span></span>

<span data-ttu-id="a3b0b-107">Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts nicht.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-107">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="a3b0b-108">Member</span><span class="sxs-lookup"><span data-stu-id="a3b0b-108">Members</span></span>

<span data-ttu-id="a3b0b-109">Die **errorInfo** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-109">The **ErrorInfo** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="a3b0b-110">Verwandte Auflistungen</span><span class="sxs-lookup"><span data-stu-id="a3b0b-110">Related Collections</span></span>

<span data-ttu-id="a3b0b-111">Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:</span><span class="sxs-lookup"><span data-stu-id="a3b0b-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="a3b0b-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="a3b0b-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="a3b0b-113">**Relatedcollectioninfo**</span><span class="sxs-lookup"><span data-stu-id="a3b0b-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="a3b0b-114">Sie können von jeder Sammlung mit Ausnahme von **errorInfo**, [**inprocservers**](inprocservers.md), [**PropertyInfo**](propertyinfo.md), [**relatedcollectioninfo**](relatedcollectioninfo.md), [**root**](root.md)und [**wowinprocservers**](wowinprocservers.md)zu dieser Sammlung navigieren.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-114">You can navigate to this collection from every collection except for **ErrorInfo**, [**InprocServers**](inprocservers.md), [**PropertyInfo**](propertyinfo.md), [**RelatedCollectionInfo**](relatedcollectioninfo.md), [**Root**](root.md), and [**WOWInprocServers**](wowinprocservers.md).</span></span>

## <a name="properties"></a><span data-ttu-id="a3b0b-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a3b0b-115">Properties</span></span>

<span data-ttu-id="a3b0b-116">Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="a3b0b-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="a3b0b-117">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="a3b0b-117">ErrorCode</span></span>](#errorcode)
-   [<span data-ttu-id="a3b0b-118">Majorref</span><span class="sxs-lookup"><span data-stu-id="a3b0b-118">MajorRef</span></span>](#majorref)
-   [<span data-ttu-id="a3b0b-119">MinorRef</span><span class="sxs-lookup"><span data-stu-id="a3b0b-119">MinorRef</span></span>](#minorref)
-   [<span data-ttu-id="a3b0b-120">Name</span><span class="sxs-lookup"><span data-stu-id="a3b0b-120">Name</span></span>](#name)

### <a name="errorcode"></a><span data-ttu-id="a3b0b-121">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="a3b0b-121">ErrorCode</span></span>



| <span data-ttu-id="a3b0b-122">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a3b0b-122">Entry</span></span> | <span data-ttu-id="a3b0b-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a3b0b-123">Value</span></span> |
|----------------|----------------------------------------|
| <span data-ttu-id="a3b0b-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3b0b-124">Description</span></span>    | <span data-ttu-id="a3b0b-125">Der Fehlercode für das Objekt oder die Datei.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-125">The error code for the object or file.</span></span> |
| <span data-ttu-id="a3b0b-126">Access</span><span class="sxs-lookup"><span data-stu-id="a3b0b-126">Access</span></span>         | <span data-ttu-id="a3b0b-127">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a3b0b-127">ReadOnly</span></span>                               |
| <span data-ttu-id="a3b0b-128">type</span><span class="sxs-lookup"><span data-stu-id="a3b0b-128">Type</span></span>           | <span data-ttu-id="a3b0b-129">String</span><span class="sxs-lookup"><span data-stu-id="a3b0b-129">String</span></span>                                 |
| <span data-ttu-id="a3b0b-130">Standard</span><span class="sxs-lookup"><span data-stu-id="a3b0b-130">Default</span></span>        | <span data-ttu-id="a3b0b-131">Keine</span><span class="sxs-lookup"><span data-stu-id="a3b0b-131">None</span></span>                                   |
| <span data-ttu-id="a3b0b-132">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="a3b0b-132">Minimum system</span></span> | <span data-ttu-id="a3b0b-133">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a3b0b-133">Windows 2000</span></span>                           |



 

### <a name="majorref"></a><span data-ttu-id="a3b0b-134">Majorref</span><span class="sxs-lookup"><span data-stu-id="a3b0b-134">MajorRef</span></span>



| <span data-ttu-id="a3b0b-135">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a3b0b-135">Entry</span></span> | <span data-ttu-id="a3b0b-136">Wert</span><span class="sxs-lookup"><span data-stu-id="a3b0b-136">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3b0b-137">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3b0b-137">Description</span></span>    | <span data-ttu-id="a3b0b-138">Der [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) Eigenschafts Wert für das Objekt, das einen Fehler aufweist.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-138">The [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property value for the object that has an error.</span></span> <span data-ttu-id="a3b0b-139">Wenn beispielsweise ein [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) -Vorgang für eine Auflistung für ein bestimmtes Objekt in der Auflistung fehlschlägt, wird der **Schlüssel** Eigenschafts Wert für dieses Objekt als majorref-Wert gemeldet.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-139">For example, if a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) call for a collection fails on a particular object in the collection, the **Key** property value for that object is reported as the MajorRef value.</span></span> <span data-ttu-id="a3b0b-140">Verwenden Sie diese Eigenschaft, um das Element zu überprüfen, das nicht aktualisiert werden kann, oder um die Komponente oder dll zu finden, die nicht installiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-140">Use this property to look at the item that fails to update or to find the component or DLL that fails to install.</span></span> |
| <span data-ttu-id="a3b0b-141">Access</span><span class="sxs-lookup"><span data-stu-id="a3b0b-141">Access</span></span>         | <span data-ttu-id="a3b0b-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a3b0b-142">ReadOnly</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="a3b0b-143">type</span><span class="sxs-lookup"><span data-stu-id="a3b0b-143">Type</span></span>           | <span data-ttu-id="a3b0b-144">String</span><span class="sxs-lookup"><span data-stu-id="a3b0b-144">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="a3b0b-145">Standard</span><span class="sxs-lookup"><span data-stu-id="a3b0b-145">Default</span></span>        | <span data-ttu-id="a3b0b-146">Keine</span><span class="sxs-lookup"><span data-stu-id="a3b0b-146">None</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a3b0b-147">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="a3b0b-147">Minimum system</span></span> | <span data-ttu-id="a3b0b-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a3b0b-148">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="minorref"></a><span data-ttu-id="a3b0b-149">MinorRef</span><span class="sxs-lookup"><span data-stu-id="a3b0b-149">MinorRef</span></span>



| <span data-ttu-id="a3b0b-150">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a3b0b-150">Entry</span></span> | <span data-ttu-id="a3b0b-151">Wert</span><span class="sxs-lookup"><span data-stu-id="a3b0b-151">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3b0b-152">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3b0b-152">Description</span></span>    | <span data-ttu-id="a3b0b-153">Eine genaue Angabe des Elements, das einen Fehler aufweist, z. b. einen Eigenschaftsnamen.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-153">A precise specification of the item that has an error, such as a property name.</span></span> <span data-ttu-id="a3b0b-154">Wenn mehrere Fehler auftreten oder in Kontexten, in denen dies nicht zutrifft, ist MinorRef gleich <Invalid> .</span><span class="sxs-lookup"><span data-stu-id="a3b0b-154">If multiple errors occur or in contexts in which this doesn't apply, MinorRef is <Invalid>.</span></span> |
| <span data-ttu-id="a3b0b-155">Access</span><span class="sxs-lookup"><span data-stu-id="a3b0b-155">Access</span></span>         | <span data-ttu-id="a3b0b-156">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a3b0b-156">ReadOnly</span></span>                                                                                                                                                                          |
| <span data-ttu-id="a3b0b-157">type</span><span class="sxs-lookup"><span data-stu-id="a3b0b-157">Type</span></span>           | <span data-ttu-id="a3b0b-158">String</span><span class="sxs-lookup"><span data-stu-id="a3b0b-158">String</span></span>                                                                                                                                                                            |
| <span data-ttu-id="a3b0b-159">Standard</span><span class="sxs-lookup"><span data-stu-id="a3b0b-159">Default</span></span>        | <span data-ttu-id="a3b0b-160">Keine</span><span class="sxs-lookup"><span data-stu-id="a3b0b-160">None</span></span>                                                                                                                                                                              |
| <span data-ttu-id="a3b0b-161">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="a3b0b-161">Minimum system</span></span> | <span data-ttu-id="a3b0b-162">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a3b0b-162">Windows 2000</span></span>                                                                                                                                                                      |



 

### <a name="name"></a><span data-ttu-id="a3b0b-163">Name</span><span class="sxs-lookup"><span data-stu-id="a3b0b-163">Name</span></span>



| <span data-ttu-id="a3b0b-164">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a3b0b-164">Entry</span></span> | <span data-ttu-id="a3b0b-165">Wert</span><span class="sxs-lookup"><span data-stu-id="a3b0b-165">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3b0b-166">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3b0b-166">Description</span></span>    | <span data-ttu-id="a3b0b-167">Der Name des Objekts oder der Datei, die einen Fehler aufweist.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-167">The name of the object or file that has an error.</span></span> <span data-ttu-id="a3b0b-168">Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-168">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="a3b0b-169">Access</span><span class="sxs-lookup"><span data-stu-id="a3b0b-169">Access</span></span>         | <span data-ttu-id="a3b0b-170">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a3b0b-170">ReadOnly</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="a3b0b-171">type</span><span class="sxs-lookup"><span data-stu-id="a3b0b-171">Type</span></span>           | <span data-ttu-id="a3b0b-172">String</span><span class="sxs-lookup"><span data-stu-id="a3b0b-172">String</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="a3b0b-173">Standard</span><span class="sxs-lookup"><span data-stu-id="a3b0b-173">Default</span></span>        | <span data-ttu-id="a3b0b-174">Keine</span><span class="sxs-lookup"><span data-stu-id="a3b0b-174">None</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="a3b0b-175">Minimalsystem</span><span class="sxs-lookup"><span data-stu-id="a3b0b-175">Minimum system</span></span> | <span data-ttu-id="a3b0b-176">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a3b0b-176">Windows 2000</span></span>                                                                                                                                                                                                             |



 

## <a name="see-also"></a><span data-ttu-id="a3b0b-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3b0b-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3b0b-178">Com+-Verwaltungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="a3b0b-178">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
