---
description: Alle Element Objekte verfügen über Eigenschaften.
ms.assetid: 00e04790-e319-41b3-b88f-8064912b91b1
title: Eigenschafts Attribute (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c635cb0d4e21fe2a1d65a3f21254f8e9c04d64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485059"
---
# <a name="property-attributes-wia"></a><span data-ttu-id="5fc80-103">Eigenschafts Attribute (WIA)</span><span class="sxs-lookup"><span data-stu-id="5fc80-103">Property Attributes (WIA)</span></span>

<span data-ttu-id="5fc80-104">Alle Element Objekte verfügen über Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5fc80-104">All item objects have properties.</span></span> <span data-ttu-id="5fc80-105">Die Eigenschaften verfügen über Attribute.</span><span class="sxs-lookup"><span data-stu-id="5fc80-105">The properties have attributes.</span></span> <span data-ttu-id="5fc80-106">Beispielsweise geben Eigenschafts Attribute an, ob eine Eigenschaft aus gelesen, geschrieben oder gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="5fc80-106">For instance, property attributes indicate whether a property is read from, written to, or deleted.</span></span> <span data-ttu-id="5fc80-107">Sie geben auch die gültigen Eigenschaftswerte an.</span><span class="sxs-lookup"><span data-stu-id="5fc80-107">They also indicate the valid property values.</span></span> <span data-ttu-id="5fc80-108">Die folgenden Konstanten sind gültige Eigenschafts Attribute:</span><span class="sxs-lookup"><span data-stu-id="5fc80-108">The following constants are valid property attributes:</span></span> 

| <span data-ttu-id="5fc80-109">Property-Attribut</span><span class="sxs-lookup"><span data-stu-id="5fc80-109">Property Attribute</span></span>        | <span data-ttu-id="5fc80-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5fc80-110">Meaning</span></span>                                                                                                  |
|---------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fc80-111">WIA-Unterstützung zwischen speicherbar \_ \_</span><span class="sxs-lookup"><span data-stu-id="5fc80-111">WIA\_PROP\_CACHEABLE</span></span>      | <span data-ttu-id="5fc80-112">Das Gerät kann den Wert der Eigenschaft Zwischenspeichern.</span><span class="sxs-lookup"><span data-stu-id="5fc80-112">The device can cache the property's value.</span></span>                                                               |
| <span data-ttu-id="5fc80-113">WIA- \_ Prop- \_ Flag</span><span class="sxs-lookup"><span data-stu-id="5fc80-113">WIA\_PROP\_FLAG</span></span>           | <span data-ttu-id="5fc80-114">Die-Eigenschaft verfügt über eine Liste der zulässigen Flagwerte.</span><span class="sxs-lookup"><span data-stu-id="5fc80-114">The property has a list of legal flag values.</span></span> <span data-ttu-id="5fc80-115">Flagwerte werden mithilfe einer bitweisen **or** -Operation kombiniert.</span><span class="sxs-lookup"><span data-stu-id="5fc80-115">Flag values are combined using a bitwise **OR** operation.</span></span> |
| <span data-ttu-id="5fc80-116">WIA- \_ Prop- \_ Liste</span><span class="sxs-lookup"><span data-stu-id="5fc80-116">WIA\_PROP\_LIST</span></span>           | <span data-ttu-id="5fc80-117">Die-Eigenschaft verfügt über eine Liste der zulässigen Werte.</span><span class="sxs-lookup"><span data-stu-id="5fc80-117">The property has a list of legal values.</span></span>                                                                 |
| <span data-ttu-id="5fc80-118">WIA- \_ Prop \_ None</span><span class="sxs-lookup"><span data-stu-id="5fc80-118">WIA\_PROP\_NONE</span></span>           | <span data-ttu-id="5fc80-119">Der-Eigenschaft sind keine gültigen Werte zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="5fc80-119">The property does not have any valid values associated with it.</span></span>                                          |
| <span data-ttu-id="5fc80-120">WIA- \_ Prop- \_ Bereich</span><span class="sxs-lookup"><span data-stu-id="5fc80-120">WIA\_PROP\_RANGE</span></span>          | <span data-ttu-id="5fc80-121">Die-Eigenschaft weist einen Bereich gültiger Werte auf.</span><span class="sxs-lookup"><span data-stu-id="5fc80-121">The property has a range of valid values.</span></span>                                                                |
| <span data-ttu-id="5fc80-122">WIA- \_ Prop- \_ Lesevorgang</span><span class="sxs-lookup"><span data-stu-id="5fc80-122">WIA\_PROP\_READ</span></span>           | <span data-ttu-id="5fc80-123">Die Anwendung kann den Wert der Eigenschaft lesen.</span><span class="sxs-lookup"><span data-stu-id="5fc80-123">The application can read the property's value.</span></span>                                                           |
| <span data-ttu-id="5fc80-124">WIA- \_ Prop- \_ RW</span><span class="sxs-lookup"><span data-stu-id="5fc80-124">WIA\_PROP\_RW</span></span>             | <span data-ttu-id="5fc80-125">Die Anwendung kann den Wert der Eigenschaft lesen und schreiben.</span><span class="sxs-lookup"><span data-stu-id="5fc80-125">The application can read and write the property's value.</span></span>                                                 |
| <span data-ttu-id="5fc80-126">WIA- \_ Prop- \_ Synchronisierung \_ erforderlich</span><span class="sxs-lookup"><span data-stu-id="5fc80-126">WIA\_PROP\_SYNC\_REQUIRED</span></span> | <span data-ttu-id="5fc80-127">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5fc80-127">Do not use.</span></span>                                                                                              |
| <span data-ttu-id="5fc80-128">WIA- \_ Prop- \_ Schreibvorgang</span><span class="sxs-lookup"><span data-stu-id="5fc80-128">WIA\_PROP\_WRITE</span></span>          | <span data-ttu-id="5fc80-129">Die Anwendung kann den Wert der Eigenschaft schreiben.</span><span class="sxs-lookup"><span data-stu-id="5fc80-129">The application can write the property's value.</span></span>                                                          |



 

 

 



