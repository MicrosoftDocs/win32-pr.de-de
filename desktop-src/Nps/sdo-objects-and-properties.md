---
title: Objekte und Eigenschaften
description: Die Eigenschaften eines Objekts in SDO werden durch die Eigenschaften des Objekts und die diesem Eigenschaften zugeordneten Werte bestimmt.
ms.assetid: 9faa7759-cad5-4429-94b0-6cba145cfadb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efed7720388e61b9d6131acafd4b9bda17694d29
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338276"
---
# <a name="objects-and-properties"></a><span data-ttu-id="6c826-103">Objekte und Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6c826-103">Objects and Properties</span></span>

<span data-ttu-id="6c826-104">Die Eigenschaften eines Objekts in SDO werden durch die Eigenschaften des Objekts und die diesem Eigenschaften zugeordneten Werte bestimmt.</span><span class="sxs-lookup"><span data-stu-id="6c826-104">The characteristics of an object in SDO are determined by the object's properties, and the values associated with those properties.</span></span> <span data-ttu-id="6c826-105">Im Gegensatz zu einigen anderen Objekt Modellen verfügen SDO-Objekte selbst über keine Methoden.</span><span class="sxs-lookup"><span data-stu-id="6c826-105">Unlike some other object models, SDO objects themselves do not have methods.</span></span> <span data-ttu-id="6c826-106">Allerdings machen SDO-Objekte com-Schnittstellen verfügbar, die Methoden bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6c826-106">However, SDO objects do expose COM interfaces that provide methods.</span></span>

<span data-ttu-id="6c826-107">Objekte in SDO machen die [**isdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) -Schnittstelle verfügbar, die Methoden zum Bearbeiten der Objekteigenschaften bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6c826-107">Objects in SDO expose the [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface that provides methods for manipulating the objects properties.</span></span> <span data-ttu-id="6c826-108">Um auf die Eigenschaften des Objekts zuzugreifen, rufen Sie eine **isdo** -Schnittstelle für das Objekt ab, und verwenden Sie die Methoden [**GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) und [**PutProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty) Interface, um Werte für die Eigenschaften abzurufen und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="6c826-108">To access the object's properties, obtain an **ISdo** interface for the object, and use the [**GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) and [**PutProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty) interface methods to retrieve and set values for the properties.</span></span> <span data-ttu-id="6c826-109">Das Thema [Abrufen eines Benutzers SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) enthält Beispielcode, der das Abrufen der **isdo** -Schnittstelle für ein Benutzerobjekt veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="6c826-109">The topic [Retrieving a User SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contains sample code that demonstrates obtaining the **ISdo** interface for a User object.</span></span>

<span data-ttu-id="6c826-110">Nachdem Sie die Eigenschaften eines Objekts geändert haben, verwenden Sie die [**isdo:: apply**](/windows/desktop/api/sdoias/nf-sdoias-isdo-apply) -Methode, um die Änderungen in den persistenten Speicher für das Objekt zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="6c826-110">After making changes to the properties of an object, use the [**ISdo::Apply**](/windows/desktop/api/sdoias/nf-sdoias-isdo-apply) method to write the changes to persistent storage for the object.</span></span> <span data-ttu-id="6c826-111">Sie können Änderungen, die an den Eigenschaften eines Objekts vorgenommen wurden, Abbrechen, bevor Sie **isdo:: apply** aufrufen, indem Sie die [**isdo:: Restore**](/windows/desktop/api/sdoias/nf-sdoias-isdo-restore) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6c826-111">You can cancel changes made to an object's properties before you call **ISdo::Apply** by calling the [**ISdo::Restore**](/windows/desktop/api/sdoias/nf-sdoias-isdo-restore) method.</span></span> <span data-ttu-id="6c826-112">Diese Methode stellt die Werte der Eigenschaften eines Objekts aus dem permanenten Speicher wieder her.</span><span class="sxs-lookup"><span data-stu-id="6c826-112">This method restores the values of an object's properties from persistent storage.</span></span>

<span data-ttu-id="6c826-113">In der folgenden Tabelle sind die Enumerationstypen aufgeführt, die die Eigenschaften einiger der Objekte in SDO auflisten.</span><span class="sxs-lookup"><span data-stu-id="6c826-113">The following table shows the enumeration types that enumerate the properties of some of the objects in SDO.</span></span>



| <span data-ttu-id="6c826-114">Object</span><span class="sxs-lookup"><span data-stu-id="6c826-114">Object</span></span>                                 | <span data-ttu-id="6c826-115">Enumerationstyp</span><span class="sxs-lookup"><span data-stu-id="6c826-115">Enumeration type</span></span>                                       |
|----------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="6c826-116">Alle SDO-Objekte</span><span class="sxs-lookup"><span data-stu-id="6c826-116">All SDO objects</span></span>                        | [<span data-ttu-id="6c826-117">**Iascommonproperties**</span><span class="sxs-lookup"><span data-stu-id="6c826-117">**IASCOMMONPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties) |
| <span data-ttu-id="6c826-118">User-Objekt</span><span class="sxs-lookup"><span data-stu-id="6c826-118">User Object</span></span>                            | [<span data-ttu-id="6c826-119">**Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="6c826-119">**USERPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-userproperties)           |
| <span data-ttu-id="6c826-120">Dienst Objekt (Netzwerk Richtlinien Server)</span><span class="sxs-lookup"><span data-stu-id="6c826-120">Service Object (Network Policy Server)</span></span> | [<span data-ttu-id="6c826-121">**Iasproperties**</span><span class="sxs-lookup"><span data-stu-id="6c826-121">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)             |
| <span data-ttu-id="6c826-122">Microsoft RADIUS-Protokoll Objekt</span><span class="sxs-lookup"><span data-stu-id="6c826-122">Microsoft RADIUS Protocol Object</span></span>       | [<span data-ttu-id="6c826-123">**Radiusproperties**</span><span class="sxs-lookup"><span data-stu-id="6c826-123">**RADIUSPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-radiusproperties)       |



 

> [!Note]  
> <span data-ttu-id="6c826-124">Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt.</span><span class="sxs-lookup"><span data-stu-id="6c826-124">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

## <a name="collections"></a><span data-ttu-id="6c826-125">Sammlungen</span><span class="sxs-lookup"><span data-stu-id="6c826-125">Collections</span></span>

<span data-ttu-id="6c826-126">Objekte werden häufig in Auflistungen gruppiert.</span><span class="sxs-lookup"><span data-stu-id="6c826-126">Objects are often grouped into collections.</span></span> <span data-ttu-id="6c826-127">Die SDO-API bietet über die [**isdo**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) -Auflistungs Schnittstelle Funktionen zum Auflisten der Objekte in einer Auflistung und zum Hinzufügen und Löschen von Objekten aus einer Auflistung.</span><span class="sxs-lookup"><span data-stu-id="6c826-127">The SDO API provides functionality, through the [**ISdo Collection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) interface, to enumerate the objects in a collection and to add and delete objects from a collection.</span></span>

<span data-ttu-id="6c826-128">Der Zugriff auf eine Auflistung wird durch Abrufen einer Auflistungs Eigenschaft für das Objekt abgerufen, das die Auflistung enthält.</span><span class="sxs-lookup"><span data-stu-id="6c826-128">Access to a collection is obtained by retrieving a collection property on the object that contains the collection.</span></span> <span data-ttu-id="6c826-129">Weitere Informationen finden Sie im Abschnitt [Objektmodell Hierarchie](/windows/desktop/Nps/sdo-object-model-hierarchy).</span><span class="sxs-lookup"><span data-stu-id="6c826-129">For more information, see the section [Object Model Hierarchy](/windows/desktop/Nps/sdo-object-model-hierarchy).</span></span>

<span data-ttu-id="6c826-130">Der Datentyp für alle Eigenschaften, die Auflistungen entsprechen, ist VT \_ Dispatch.</span><span class="sxs-lookup"><span data-stu-id="6c826-130">The data type for all properties that correspond to collections is VT\_DISPATCH.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c826-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6c826-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c826-132">SDO-Objektmodell Hierarchie</span><span class="sxs-lookup"><span data-stu-id="6c826-132">SDO Object Model Hierarchy</span></span>](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[<span data-ttu-id="6c826-133">Unterstützte SDO-Attribute</span><span class="sxs-lookup"><span data-stu-id="6c826-133">SDO Supported Attributes</span></span>](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 