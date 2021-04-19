---
title: ButtonText-Element
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | ButtonText-Element
ms.assetid: 1afe1626-769a-40c8-883a-968ebd995a93
keywords:
- Fenster "ButtonText-Element" Media Player
topic_type:
- apiref
api_name:
- ButtonText Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c94577ad772a5c6fa198bd43f2475d53821da72c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369303"
---
# <a name="buttontext-element"></a><span data-ttu-id="2a2f1-105">ButtonText-Element</span><span class="sxs-lookup"><span data-stu-id="2a2f1-105">ButtonText Element</span></span>

> [!Note]  
> <span data-ttu-id="2a2f1-106">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="2a2f1-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="2a2f1-107">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2a2f1-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="2a2f1-108">Das **ButtonText** -Element gibt die Text Zeichenfolge an, die Windows Media Player für eine Aufgabenbereichs Schaltfläche anzeigt.</span><span class="sxs-lookup"><span data-stu-id="2a2f1-108">The **ButtonText** element specifies the text string that Windows Media Player displays for a task pane button.</span></span>

``` syntax
<ButtonText>
   text string
</ButtonText>
```

## <a name="attributes"></a><span data-ttu-id="2a2f1-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="2a2f1-109">Attributes</span></span>

<span data-ttu-id="2a2f1-110">Dieses Element weist keine Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="2a2f1-110">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="2a2f1-111">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="2a2f1-111">Parent/Child Elements</span></span>



| <span data-ttu-id="2a2f1-112">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="2a2f1-112">Hierarchy</span></span>       | <span data-ttu-id="2a2f1-113">Element</span><span class="sxs-lookup"><span data-stu-id="2a2f1-113">Element</span></span>                                              |
|-----------------|------------------------------------------------------|
| <span data-ttu-id="2a2f1-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2a2f1-114">Parent elements</span></span> | <span data-ttu-id="2a2f1-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="2a2f1-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span></span> |
| <span data-ttu-id="2a2f1-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2a2f1-116">Child elements</span></span>  | <span data-ttu-id="2a2f1-117">Keine</span><span class="sxs-lookup"><span data-stu-id="2a2f1-117">None</span></span>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="2a2f1-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a2f1-118">Remarks</span></span>

<span data-ttu-id="2a2f1-119">Dieses Element ist für jede Instanz von **ServiceTask1**, **ServiceTask2** oder **ServiceTask3** erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2a2f1-119">This element is required for each instance of **ServiceTask1**, **ServiceTask2**, or **ServiceTask3**.</span></span>

> [!Note]  
> <span data-ttu-id="2a2f1-120">Windows Media Player 10 umfasst drei Aufgabenbereiche, in denen ein Online Shop seine Webseiten anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="2a2f1-120">Windows Media Player 10 has three task panes where an online store can display its webpages.</span></span> <span data-ttu-id="2a2f1-121">Der Online Shop kann einen, zwei oder alle drei Aufgabenbereiche verwenden.</span><span class="sxs-lookup"><span data-stu-id="2a2f1-121">The online store can choose to use one, two, or all three of the task panes.</span></span> <span data-ttu-id="2a2f1-122">Windows Media Player 11 verfügt nur über einen Aufgabenbereich, den der Benutzer durch Klicken auf die Registerkarte " **Online Stores** " anzeigen kann. die **ServiceTask2** -und **ServiceTask3** -Elemente werden von Windows Media Player 11 ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2a2f1-122">Windows Media Player 11 has only one task pane, which the user can view by clicking on the **Online Stores** tab. Windows Media Player 11 ignores the **ServiceTask2** and **ServiceTask3** elements.</span></span>

 

<span data-ttu-id="2a2f1-123">Windows Media Player kann den Text der Schaltfläche an den verfügbaren Platz anpassen.</span><span class="sxs-lookup"><span data-stu-id="2a2f1-123">Windows Media Player may crop button text to fit the available space.</span></span> <span data-ttu-id="2a2f1-124">Der Player verwendet immer die "Tahoma Bold"-Schriftart mit 8 Punkten für diesen Text.</span><span class="sxs-lookup"><span data-stu-id="2a2f1-124">The Player always uses the Tahoma bold 8-point font for this text.</span></span> <span data-ttu-id="2a2f1-125">Es stehen zwei Zeilen zum Anzeigen von Schaltflächen Text zur Verfügung, der Spieler umschließt jedoch nicht automatisch den Text von der ersten Zeile zum zweiten.</span><span class="sxs-lookup"><span data-stu-id="2a2f1-125">There are two lines available to display button text, but the Player does not automatically wrap text from the first line to the second.</span></span> <span data-ttu-id="2a2f1-126">Wenn Sie einen Zeilenumbruch im Schaltflächen Text angeben möchten, fügen Sie die neue Zeilen-Escapesequenz " \\ n" in die Text Zeichenfolge ein.</span><span class="sxs-lookup"><span data-stu-id="2a2f1-126">To specify a line break in the button text, insert the new line escape sequence "\\n" in your text string.</span></span>

<span data-ttu-id="2a2f1-127">Die Text Zeichenfolge wird auch im Menü "Gehe **zu** " in der Windows Media Player-Benutzeroberfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2a2f1-127">The text string is also displayed in the **GoTo** menu in the Windows Media Player user interface.</span></span>

<span data-ttu-id="2a2f1-128">Sie sollten Ihren Online Shop mithilfe verschiedener Anzeigeeinstellungen testen, um sicherzustellen, dass der Text erwartungsgemäß angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2a2f1-128">You should test your online store using a variety of display settings to ensure that text displays as you expect.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a2f1-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a2f1-129">Requirements</span></span>



| <span data-ttu-id="2a2f1-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a2f1-130">Requirement</span></span> | <span data-ttu-id="2a2f1-131">Wert</span><span class="sxs-lookup"><span data-stu-id="2a2f1-131">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="2a2f1-132">Version</span><span class="sxs-lookup"><span data-stu-id="2a2f1-132">Version</span></span><br/> | <span data-ttu-id="2a2f1-133">Windows Media Player 10 oder höher.</span><span class="sxs-lookup"><span data-stu-id="2a2f1-133">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2a2f1-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a2f1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a2f1-135">**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**</span><span class="sxs-lookup"><span data-stu-id="2a2f1-135">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="2a2f1-136">**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**</span><span class="sxs-lookup"><span data-stu-id="2a2f1-136">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="2a2f1-137">**Servicinfo-Dokument**</span><span class="sxs-lookup"><span data-stu-id="2a2f1-137">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





