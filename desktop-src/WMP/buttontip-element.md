---
title: Buttontip-Element
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Buttontip-Element
ms.assetid: 93e5d0c8-8d2d-45c1-9d47-bbd0b6eb8b88
keywords:
- Buttontip-Element Fenster Media Player
topic_type:
- apiref
api_name:
- ButtonTip Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ab94794232ade6f924b87fd3f4d73d4452d544
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353823"
---
# <a name="buttontip-element"></a><span data-ttu-id="67665-105">Buttontip-Element</span><span class="sxs-lookup"><span data-stu-id="67665-105">ButtonTip Element</span></span>

> [!Note]  
> <span data-ttu-id="67665-106">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="67665-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="67665-107">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="67665-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="67665-108">Das **buttontip** -Element gibt die Text Zeichenfolge an, die angezeigt wird, wenn der Benutzer auf eine Schaltfläche des Aufgabenbereichs zeigt.</span><span class="sxs-lookup"><span data-stu-id="67665-108">The **ButtonTip** element specifies the text string that is displayed when the user points to a task pane button.</span></span>

``` syntax
<ButtonTip>
   text string
</ButtonTip>
```

## <a name="attributes"></a><span data-ttu-id="67665-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="67665-109">Attributes</span></span>

<span data-ttu-id="67665-110">Dieses Element weist keine Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="67665-110">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="67665-111">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="67665-111">Parent/Child Elements</span></span>



| <span data-ttu-id="67665-112">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="67665-112">Hierarchy</span></span>       | <span data-ttu-id="67665-113">Element</span><span class="sxs-lookup"><span data-stu-id="67665-113">Element</span></span>                                              |
|-----------------|------------------------------------------------------|
| <span data-ttu-id="67665-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="67665-114">Parent elements</span></span> | <span data-ttu-id="67665-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="67665-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span></span> |
| <span data-ttu-id="67665-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="67665-116">Child elements</span></span>  | <span data-ttu-id="67665-117">Keine</span><span class="sxs-lookup"><span data-stu-id="67665-117">None</span></span>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="67665-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67665-118">Remarks</span></span>

<span data-ttu-id="67665-119">Dieses Element ist für jede Instanz von **ServiceTask1**, **ServiceTask2** oder **ServiceTask3** optional.</span><span class="sxs-lookup"><span data-stu-id="67665-119">This element is optional for each instance of **ServiceTask1**, **ServiceTask2**, or **ServiceTask3**.</span></span> <span data-ttu-id="67665-120">Wenn dieses Element nicht angegeben wird, verwendet Windows Media Player den Schaltflächen Text als Standardwert.</span><span class="sxs-lookup"><span data-stu-id="67665-120">If this element is not supplied, Windows Media Player uses the button text as the default value.</span></span>

> [!Note]  
> <span data-ttu-id="67665-121">Windows Media Player 10 umfasst drei Aufgabenbereiche, in denen ein Online Shop seine Webseiten anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="67665-121">Windows Media Player 10 has three task panes where an online store can display its webpages.</span></span> <span data-ttu-id="67665-122">Der Online Shop kann einen, zwei oder alle drei Aufgabenbereiche verwenden.</span><span class="sxs-lookup"><span data-stu-id="67665-122">The online store can choose to use one, two, or all three of the task panes.</span></span> <span data-ttu-id="67665-123">Windows Media Player 11 verfügt nur über einen Aufgabenbereich, den der Benutzer durch Klicken auf die Registerkarte " **Online Stores** " anzeigen kann. die **ServiceTask2** -und **ServiceTask3** -Elemente werden von Windows Media Player 11 ignoriert.</span><span class="sxs-lookup"><span data-stu-id="67665-123">Windows Media Player 11 has only one task pane, which the user can view by clicking on the **Online Stores** tab. Windows Media Player 11 ignores the **ServiceTask2** and **ServiceTask3** elements.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="67665-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67665-124">Requirements</span></span>



| <span data-ttu-id="67665-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67665-125">Requirement</span></span> | <span data-ttu-id="67665-126">Wert</span><span class="sxs-lookup"><span data-stu-id="67665-126">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="67665-127">Version</span><span class="sxs-lookup"><span data-stu-id="67665-127">Version</span></span><br/> | <span data-ttu-id="67665-128">Windows Media Player 10 oder höher.</span><span class="sxs-lookup"><span data-stu-id="67665-128">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="67665-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67665-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67665-130">**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**</span><span class="sxs-lookup"><span data-stu-id="67665-130">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="67665-131">**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**</span><span class="sxs-lookup"><span data-stu-id="67665-131">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="67665-132">**Servicinfo-Dokument**</span><span class="sxs-lookup"><span data-stu-id="67665-132">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





