---
description: Greift auf die Daten zu, die im com+-Katalog gespeichert sind.
ms.assetid: d77123f6-9821-4c80-860c-5f1feaca7987
title: Comadmincatalog-Klasse (COMAdmin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalog
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: fa6e71d13f5a3d157bd3ce1035d0616dc1e5a519
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483614"
---
# <a name="comadmincatalog-class"></a><span data-ttu-id="abd81-103">Comadmincatalog-Klasse</span><span class="sxs-lookup"><span data-stu-id="abd81-103">COMAdminCatalog class</span></span>

<span data-ttu-id="abd81-104">Greift auf die Daten zu, die im com+-Katalog gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="abd81-104">Accesses the data that is stored in the COM+ catalog.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="abd81-105">Gründe für die Implementierung</span><span class="sxs-lookup"><span data-stu-id="abd81-105">When to implement</span></span>

<span data-ttu-id="abd81-106">Diese Klasse wird von com+ implementiert.</span><span class="sxs-lookup"><span data-stu-id="abd81-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="abd81-107">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abd81-107">Requirement</span></span> | <span data-ttu-id="abd81-108">Wert</span><span class="sxs-lookup"><span data-stu-id="abd81-108">Value</span></span> |
|------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abd81-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="abd81-109">CLSID</span></span>      | <span data-ttu-id="abd81-110">CLSID \_ comadmincatalog</span><span class="sxs-lookup"><span data-stu-id="abd81-110">CLSID\_COMAdminCatalog</span></span>                                                                                            |
| <span data-ttu-id="abd81-111">ProgID</span><span class="sxs-lookup"><span data-stu-id="abd81-111">ProgID</span></span>     | <span data-ttu-id="abd81-112">L "COMAdmin. comadmincatalog"</span><span class="sxs-lookup"><span data-stu-id="abd81-112">L"COMAdmin.COMAdminCatalog"</span></span>                                                                                       |
| <span data-ttu-id="abd81-113">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="abd81-113">Interfaces</span></span> | [<span data-ttu-id="abd81-114">**Icomadmincatalog**</span><span class="sxs-lookup"><span data-stu-id="abd81-114">**ICOMAdminCatalog**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)<br/> [<span data-ttu-id="abd81-115">**ICOMAdminCatalog2**</span><span class="sxs-lookup"><span data-stu-id="abd81-115">**ICOMAdminCatalog2**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)<br/> |



 

## <a name="when-to-use"></a><span data-ttu-id="abd81-116">Verwendung</span><span class="sxs-lookup"><span data-stu-id="abd81-116">When to use</span></span>

<span data-ttu-id="abd81-117">Mithilfe von Objekten, die aus der **comadmincatalog** -Klasse erstellt wurden, können Sie den programmgesteuerten Zugriff auf die im com+-Katalog gespeicherten com+-Konfigurationsdaten starten</span><span class="sxs-lookup"><span data-stu-id="abd81-117">You use objects created from the **COMAdminCatalog** class to begin programmatic access to COM+ configuration data stored in the COM+ catalog.</span></span> <span data-ttu-id="abd81-118">Diese Informationen unterliegen den Ordnern und Elementen in der Konsolen Struktur des Verwaltungs Tools Komponenten Dienste.</span><span class="sxs-lookup"><span data-stu-id="abd81-118">This information underlies the folders and items in the console tree of the Component Services administration tool.</span></span> <span data-ttu-id="abd81-119">Mit der **comadmincatalog** -Klasse können Sie auf Auflistungen im-Katalog zugreifen, com+-Anwendungen und-Komponenten installieren, Dienste starten und starten und eine Verbindung mit Remote Servern herstellen und diese verwalten.</span><span class="sxs-lookup"><span data-stu-id="abd81-119">The **COMAdminCatalog** class enables you to access collections in the catalog, install COM+ applications and components, start and stop services, and connect to and administer remote servers.</span></span>

<span data-ttu-id="abd81-120">Ordner im Verwaltungs Tool Komponenten Dienste entsprechen Sammlungen im-Katalog, die Sie mithilfe von Objekten darstellen können, die aus der [**comadmincatalogcollection**](comadmincatalogcollection.md) -Klasse erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="abd81-120">Folders in the Component Services administration tool correspond to collections in the catalog, which you can represent by using objects created from the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) class.</span></span> <span data-ttu-id="abd81-121">Elemente in den Ordnern entsprechen Elementen in den Auflistungen, die Sie mithilfe von Objekten darstellen können, die aus der [**COMAdminCatalogObject**](comadmincatalogobject.md) -Klasse erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="abd81-121">Items in the folders correspond to items in the collections, which you can represent by using objects created from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span>

<span data-ttu-id="abd81-122">Nicht alle Auflistungen und Elemente, die über " [**comadmincatalogcollection**](comadmincatalogcollection.md) " und " [**COMAdminCatalogObject**](comadmincatalogobject.md) " verfügbar gemacht werden, sind im Verwaltungs Tool für Komponenten Dienste verfügbar.</span><span class="sxs-lookup"><span data-stu-id="abd81-122">Not all of the collections and items exposed through [**COMAdminCatalogCollection**](comadmincatalogcollection.md) and [**COMAdminCatalogObject**](comadmincatalogobject.md) are available in the Component Services administration tool.</span></span>

<span data-ttu-id="abd81-123">Informationen zu bestimmten Sammlungen und deren Eigenschaften finden Sie unter [com+-Verwaltungs Sammlungen](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="abd81-123">For information regarding specific collections and their properties, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="abd81-124">Eine Einführung in die programmgesteuerte Verwaltung von com+ finden Sie unter [Automatisieren der com+-Verwaltung](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="abd81-124">For an introduction to programmatic administration of COM+, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="abd81-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="abd81-125">Remarks</span></span>

<span data-ttu-id="abd81-126">Um dieses Objekt zu erstellen, rufen Sie [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)auf.</span><span class="sxs-lookup"><span data-stu-id="abd81-126">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="abd81-127">Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-admin-Typbibliothek hinzu.</span><span class="sxs-lookup"><span data-stu-id="abd81-127">To use this class from Microsoft Visual Basic, add a reference to the COM+ Admin Type Library.</span></span> <span data-ttu-id="abd81-128">Ein comadmincatalog-Objekt kann mithilfe von "COMAdmin. comadmincatalog" als Klassenname deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="abd81-128">A COMAdminCatalog object can be declared using "COMAdmin.COMAdminCatalog" as the class name.</span></span>

<span data-ttu-id="abd81-129">In com+ 1,5, das mit Windows XP veröffentlicht wurde, implementiert die **comadmincatalog** -Klasse die [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="abd81-129">In COM+ 1.5, released with Windows XP, the **COMAdminCatalog** class implements the [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) interface.</span></span> <span data-ttu-id="abd81-130">In com+ 1,0, veröffentlicht mit Windows 2000, implementiert die **comadmincatalog** -Klasse jedoch nur die [**icomadmincatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="abd81-130">However, in COM+ 1.0, released with Windows 2000, the **COMAdminCatalog** class implements only the [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="abd81-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abd81-131">Requirements</span></span>



| <span data-ttu-id="abd81-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abd81-132">Requirement</span></span> | <span data-ttu-id="abd81-133">Wert</span><span class="sxs-lookup"><span data-stu-id="abd81-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="abd81-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="abd81-134">Minimum supported client</span></span><br/> | <span data-ttu-id="abd81-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abd81-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="abd81-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="abd81-136">Minimum supported server</span></span><br/> | <span data-ttu-id="abd81-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abd81-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="abd81-138">Header</span><span class="sxs-lookup"><span data-stu-id="abd81-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="abd81-139"><dt>"COMAdmin. h"</dt></span><span class="sxs-lookup"><span data-stu-id="abd81-139"><dt>ComAdmin.h</dt></span></span> </dl>   |
| <span data-ttu-id="abd81-140">IDL</span><span class="sxs-lookup"><span data-stu-id="abd81-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="abd81-141"><dt>COMAdmin. idl</dt></span><span class="sxs-lookup"><span data-stu-id="abd81-141"><dt>ComAdmin.Idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abd81-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abd81-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abd81-143">**Comadmincatalogcollection**</span><span class="sxs-lookup"><span data-stu-id="abd81-143">**COMAdminCatalogCollection**</span></span>](comadmincatalogcollection.md)
</dt> <dt>

[<span data-ttu-id="abd81-144">**COMAdminCatalogObject**</span><span class="sxs-lookup"><span data-stu-id="abd81-144">**COMAdminCatalogObject**</span></span>](comadmincatalogobject.md)
</dt> <dt>

[<span data-ttu-id="abd81-145">**Icomadmincatalog**</span><span class="sxs-lookup"><span data-stu-id="abd81-145">**ICOMAdminCatalog**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
</dt> <dt>

[<span data-ttu-id="abd81-146">**ICOMAdminCatalog2**</span><span class="sxs-lookup"><span data-stu-id="abd81-146">**ICOMAdminCatalog2**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
</dt> </dl>

 

