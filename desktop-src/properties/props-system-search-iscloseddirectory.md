---
description: Wird von einem Containerelement als true ausgegeben, um anzugeben, dass die untergeordneten Elemente nicht durch einen Indexer aufgezählt werden müssen, wenn das Containerelement seit der letzten durch Forstung der Indexüberprüfung nicht geändert wurde.
ms.assetid: 8bb487b9-4a51-4a6b-939e-946a8aad85de
title: System. search. iscloseddirectory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea97aeb8d0192eea7d71ca65fd0ec109780702f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366120"
---
# <a name="systemsearchiscloseddirectory"></a><span data-ttu-id="b325f-103">System. search. iscloseddirectory</span><span class="sxs-lookup"><span data-stu-id="b325f-103">System.Search.IsClosedDirectory</span></span>

<span data-ttu-id="b325f-104">Wird von einem Containerelement als **true** ausgegeben, um anzugeben, dass die untergeordneten Elemente nicht durch einen Indexer aufgezählt werden müssen, wenn das Containerelement seit der letzten durch Forstung der Indexüberprüfung nicht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="b325f-104">Emitted as **TRUE** by a container item to indicate that its child items do not need to be enumerated by an indexer if the container item has not changed since the last incremental index verification crawl.</span></span> <span data-ttu-id="b325f-105">Dies trägt zur Optimierung der Leistung von Indexern bei.</span><span class="sxs-lookup"><span data-stu-id="b325f-105">This contributes to the optimization of indexer performance.</span></span> <span data-ttu-id="b325f-106">In diesen Container Fällen (Beispiele sind eine e-Mail mit Anlagen oder eine komprimierte Datei mit der Erweiterung ". zip") sind untergeordnete Elemente nicht mit ihrem übergeordneten Element verbunden.</span><span class="sxs-lookup"><span data-stu-id="b325f-106">In these container cases (examples are an e-mail with attachments or a compressed file with a .zip name extension), child items are inseparable from their parent item.</span></span> <span data-ttu-id="b325f-107">Wenn beispielsweise die [System. DateModified](./props-system-datemodified.md) -Eigenschaft eines enthaltenen Elements geändert wird, ändert sich der System. DateModified-Wert des Containers in Match.</span><span class="sxs-lookup"><span data-stu-id="b325f-107">For instance, if the [System.DateModified](./props-system-datemodified.md) property of a contained item changes, then the System.DateModified value of the container changes to match.</span></span> <span data-ttu-id="b325f-108">Außerdem werden auch alle untergeordneten Elemente gelöscht, wenn ein übergeordnetes Element gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="b325f-108">Also, if a parent item is deleted, all of the child items are deleted as well.</span></span> <span data-ttu-id="b325f-109">Wenn sich der Container nicht geändert hat, weiß der Indexer daher, dass sich nichts darin geändert hat, und muss den Container nicht öffnen, um den Inhalt einzeln zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b325f-109">Therefore, if the container has not changed, the indexer knows that nothing within it has changed and does not need to open the container to examine the contents individually.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="b325f-110">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b325f-110">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.IsClosedDirectory
   shellPKey = PKEY_Search_IsClosedDirectory
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 23
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a><span data-ttu-id="b325f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b325f-111">Remarks</span></span>

<span data-ttu-id="b325f-112">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="b325f-112">PKEY values are defined in Propkey.h.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b325f-113">Wenn ein Element **true** für diese Eigenschaft ausgibt, muss jedes seiner untergeordneten Elemente die [System. search. isfullyenthalteneigenschaft](./props-system-search-isfullycontained.md) als **true** ausgeben, um zu verhindern, dass diese Elemente aus dem Index gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="b325f-113">If an item emits **TRUE** for this property, each of its child items must emit the [System.Search.IsFullyContained](./props-system-search-isfullycontained.md) property as **TRUE** to prevent those items from being deleted from the index.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b325f-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b325f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b325f-115">propertydescription</span><span class="sxs-lookup"><span data-stu-id="b325f-115">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="b325f-116">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="b325f-116">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="b325f-117">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="b325f-117">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="b325f-118">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="b325f-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="b325f-119">Display Info</span><span class="sxs-lookup"><span data-stu-id="b325f-119">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="b325f-120">StringFormat</span><span class="sxs-lookup"><span data-stu-id="b325f-120">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="b325f-121">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="b325f-121">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="b325f-122">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="b325f-122">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="b325f-123">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="b325f-123">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="b325f-124">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="b325f-124">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="b325f-125">DrawControl</span><span class="sxs-lookup"><span data-stu-id="b325f-125">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="b325f-126">editcontrol</span><span class="sxs-lookup"><span data-stu-id="b325f-126">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="b325f-127">FilterControl</span><span class="sxs-lookup"><span data-stu-id="b325f-127">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="b325f-128">querycontrol</span><span class="sxs-lookup"><span data-stu-id="b325f-128">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
