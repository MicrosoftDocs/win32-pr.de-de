---
title: Calendar-Steuer Element (MSAA-Benutzeroberflächen Element-Referenz)
description: Kalender Steuerelemente bieten eine einfache und intuitive Möglichkeit für einen Benutzer, ein Datum aus einer vertrauten Oberfläche auszuwählen.
ms.assetid: cfb1e420-bb8f-4100-9c83-304d11573c0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63acb3ca83f6b7e71740acee4232e081e11594e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855780"
---
# <a name="calendar-control-msaa-ui-element-reference"></a><span data-ttu-id="7d97b-103">Calendar-Steuer Element (MSAA-Benutzeroberflächen Element-Referenz)</span><span class="sxs-lookup"><span data-stu-id="7d97b-103">Calendar Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="7d97b-104">In diesem Thema werden **Kalender Steuer** Element Objekte für den MSAA-Benutzeroberflächen-Element Verweis beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7d97b-104">This topic describes **Calendar Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="7d97b-105">Die Vorgehensweise zum Erstellen von **Kalender Steuer** Objekten in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7d97b-105">How to create **Calendar Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="7d97b-106">Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.</span><span class="sxs-lookup"><span data-stu-id="7d97b-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="7d97b-107">Kalender Steuerelemente bieten eine einfache und intuitive Möglichkeit für einen Benutzer, ein Datum aus einer vertrauten Oberfläche auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="7d97b-107">Calendar controls provide a simple and intuitive way for a user to select a date from a familiar interface.</span></span>

<span data-ttu-id="7d97b-108">Der Fenster Klassenname für ein Monatskalender-Steuerelement ist eine monthcal- \_ Klasse, die in "kommctrl. h" als "SysMonthCal32" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="7d97b-108">The window class name for a month calendar control is MONTHCAL\_CLASS, which is defined as "SysMonthCal32" in Commctrl.h.</span></span> <span data-ttu-id="7d97b-109">Die Informationen in diesem Thema gelten für das Month Calendar-Steuerelement in Version 5 von "kommctrl. h".</span><span class="sxs-lookup"><span data-stu-id="7d97b-109">Information in this topic applies to the month calendar control in version 5 of Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="7d97b-110">IAccessible-Methoden</span><span class="sxs-lookup"><span data-stu-id="7d97b-110">IAccessible Methods</span></span>

<span data-ttu-id="7d97b-111">Kalender Steuerelemente unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:</span><span class="sxs-lookup"><span data-stu-id="7d97b-111">Calendar controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="7d97b-112">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="7d97b-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="7d97b-113">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="7d97b-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="7d97b-114">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="7d97b-114">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="7d97b-115">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="7d97b-115">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="7d97b-116">IAccessible-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7d97b-116">IAccessible Properties</span></span>

<span data-ttu-id="7d97b-117">Kalender Steuerelemente unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7d97b-117">Calendar controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="7d97b-118">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7d97b-118">Property</span></span>                                                                 | <span data-ttu-id="7d97b-119">Kommentare</span><span class="sxs-lookup"><span data-stu-id="7d97b-119">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d97b-120">**get \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="7d97b-120">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="7d97b-121">Die **childCount** -Eigenschaft ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="7d97b-121">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="7d97b-122">**\_Zugriffs Fokus erhalten**</span><span class="sxs-lookup"><span data-stu-id="7d97b-122">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="7d97b-123">**\_accName erhalten**</span><span class="sxs-lookup"><span data-stu-id="7d97b-123">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="7d97b-124">Die **Name** -Eigenschaft wird aus dem statischen Text Steuerelement abgerufen, das das Kalender Steuerelement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7d97b-124">The **Name** property is obtained from the static text control that labels the calendar control.</span></span> <span data-ttu-id="7d97b-125">Beim Erstellen von Steuerelementen müssen Server Entwickler sicherstellen, dass ein statisches Text Steuerelement unmittelbar vor dem Steuerelement liegt, das es in der Aktivier Reihenfolge bezeichnet</span><span class="sxs-lookup"><span data-stu-id="7d97b-125">When creating controls, server developers must ensure that a static text control immediately precedes the control that it labels within the tab order.</span></span>                                                                                                                                                                                                                 |
| [<span data-ttu-id="7d97b-126">**\_accParent erhalten**</span><span class="sxs-lookup"><span data-stu-id="7d97b-126">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="7d97b-127">Die über **geordnete** Eigenschaft ist ein Fenster ( [**Rollen \_ System \_ Fenster**](object-roles.md) ), das das Steuerelement umgibt und die gleiche **Name** -Eigenschaft und den Fenster Klassennamen wie das Steuerelement aufweist.</span><span class="sxs-lookup"><span data-stu-id="7d97b-127">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="7d97b-128">**get- \_ Zugriffs Rolle**</span><span class="sxs-lookup"><span data-stu-id="7d97b-128">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="7d97b-129">Die **Role** -Eigenschaft ist [**role \_ System \_ Client**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7d97b-129">The **Role** property is [**ROLE\_SYSTEM\_CLIENT**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="7d97b-130">**\_accState erhalten**</span><span class="sxs-lookup"><span data-stu-id="7d97b-130">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="7d97b-131">Die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md)[**Zustands \_ System nicht \_**](object-state-constants.md) \| [**\_ \_ verfüg**](object-state-constants.md) bares Zustands System mit \| [**\_ \_ Fokus**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="7d97b-131">The **State** property is a combination of one or more of the following [values](object-state-constants.md)[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="7d97b-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7d97b-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d97b-133">IAccessible-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7d97b-133">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





