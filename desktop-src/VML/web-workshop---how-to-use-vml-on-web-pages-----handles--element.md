---
title: Verwenden des Handles-Elements
description: Verwenden des Handles-Elements
ms.assetid: d748f74c-40e5-499a-bb61-94862eb3811c
keywords:
- Webworkshop, Handles-Element
- Entwerfen von Webseiten, Handles-Element
- Vector Markup Language (VML), Handles-Element
- VML (Vector Markup Language), Handles-Element
- Vektorgrafiken, Handles-Element
- Handles-Element
- VML-Elemente, Handles
- VML-Formen, Handles-Element
- Vector Markup Language (VML), Anfügen von Text an Formen
- VML (Vector Markup Language), Anfügen von Text an Formen
- Vektorgrafiken, Anfügen von Text an Formen
- VML-Formen, Anfügen von Text
- Anfügen von Text an Formen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d54c721d50f51c46cd4bf08393e85ad83307fc1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039048"
---
# <a name="using-the-handles-element"></a><span data-ttu-id="d15eb-116">Verwenden des Handles-Elements</span><span class="sxs-lookup"><span data-stu-id="d15eb-116">Using the Handles Element</span></span>

<span data-ttu-id="d15eb-117">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="d15eb-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d15eb-118">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="d15eb-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d15eb-119">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="d15eb-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d15eb-120">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="d15eb-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d15eb-121">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d15eb-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d15eb-122">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d15eb-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d15eb-123">In diesem Thema wird veranschaulicht, wie das-Element verwendet wird, `<handles>` um Text an eine Form anzufügen.</span><span class="sxs-lookup"><span data-stu-id="d15eb-123">In this topic, we will illustrate how to use the `<handles>` element to attach text to a shape.</span></span>

<span data-ttu-id="d15eb-124">Sie können das `<handles>` untergeordnete Element innerhalb `<shape>` von oder platzieren `<shapetype>` , um Benutzeroberflächen Elemente zu definieren, die die **ADJ** -Werte in der Form variieren können.</span><span class="sxs-lookup"><span data-stu-id="d15eb-124">You can place the `<handles>` sub-element inside `<shape>` or `<shapetype>` to define user interface elements that can vary the **adj** values on the shape.</span></span>

<span data-ttu-id="d15eb-125">Wie die folgende VML-Darstellung zeigt, können Sie z. b. ein Anpassungs handle (gelbes Feld) bereitstellen, das Benutzer einfach ziehen können, um die Form anzupassen.</span><span class="sxs-lookup"><span data-stu-id="d15eb-125">For example, as shown the following VML representation, you can provide an adjust handle (yellow box) that users can simply drag to adjust the shape.</span></span>

<span data-ttu-id="d15eb-126">Hinweis: die Handles sind verfügbar, wenn diese VML-Form in Microsoft Office Anwendungen angezeigt wird, in denen die Form manipuliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d15eb-126">Note: the handles are available when this VML shape is viewed in Microsoft Office applications, where the shape is intended to be manipulable.</span></span>

![shape1.gif (564 bytes)](images/shape1h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="16200,5400"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





<span data-ttu-id="d15eb-128">Beachten Sie, dass der einzige Unterschied zwischen der vorangehenden VML-Darstellung und der folgenden der **ADJ** -Wert ist.</span><span class="sxs-lookup"><span data-stu-id="d15eb-128">Notice that the only difference between the preceding VML representation and the following one is the **adj** value.</span></span>

![shape2.gif (1361 Bytes)](images/shape2h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="11304,6600"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





<span data-ttu-id="d15eb-130">Weitere Informationen zu diesem Element finden Sie in der [VML-Spezifikation](https://www.w3.org/TR/NOTE-VML#-toc416858393) .</span><span class="sxs-lookup"><span data-stu-id="d15eb-130">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858393) .</span></span>

 

 