---
title: Auschecken unnötiger Objekte
description: Wenn Sie überprüfen verwenden, um ein einfaches Steuerelement zu untersuchen, z. b. eine Schaltfläche "OK" im Microsoft WordPad-Zubehör, sehen Sie, dass diese übergeordneten Fenster Objekte auch mehrere unsichtbare untergeordnete Objekte enthalten.
ms.assetid: 30884e11-cc73-4bb8-9d9e-b9f1b53c4193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb341881ee2ea503b1f74643723a1f90c8e5d1d5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340414"
---
# <a name="screening-out-unnecessary-objects"></a><span data-ttu-id="fc7ed-103">Auschecken unnötiger Objekte</span><span class="sxs-lookup"><span data-stu-id="fc7ed-103">Screening Out Unnecessary Objects</span></span>

<span data-ttu-id="fc7ed-104">Wenn Sie über [prüfen](inspect-objects.md) verwenden, um ein einfaches Steuerelement zu untersuchen, z. b. eine Schaltfläche "OK" im Microsoft WordPad-Zubehör, sehen Sie, dass diese übergeordneten Fenster Objekte auch mehrere unsichtbare untergeordnete Objekte enthalten.</span><span class="sxs-lookup"><span data-stu-id="fc7ed-104">If you use [Inspect](inspect-objects.md) to examine a simple control such as an OK push button in the Microsoft WordPad accessory, you can see that these parent window objects also contain several invisible child objects.</span></span> <span data-ttu-id="fc7ed-105">Diese nicht sichtbaren Objekte haben denselben Fenster Klassennamen wie das Steuerelement, und die [State-Eigenschaft](state-property.md) des [**Zustands Systems ist \_ \_ unsichtbar**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="fc7ed-105">These invisible objects have the same window class name as the control and have the [State property](state-property.md) of [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md).</span></span> <span data-ttu-id="fc7ed-106">In der folgenden Tabelle sind die unsichtbaren untergeordneten Objekte aufgelistet, die von Active Accessibility Microsoft für das-Steuerelement erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="fc7ed-106">The following table lists the invisible child objects that Microsoft Active Accessibility creates for the control.</span></span>



| <span data-ttu-id="fc7ed-107">Name</span><span class="sxs-lookup"><span data-stu-id="fc7ed-107">Name</span></span>          | <span data-ttu-id="fc7ed-108">Role</span><span class="sxs-lookup"><span data-stu-id="fc7ed-108">Role</span></span>                                                                  | <span data-ttu-id="fc7ed-109">ChildCount</span><span class="sxs-lookup"><span data-stu-id="fc7ed-109">ChildCount</span></span> |
|---------------|-----------------------------------------------------------------------|------------|
| <span data-ttu-id="fc7ed-110">Anlage</span><span class="sxs-lookup"><span data-stu-id="fc7ed-110">"System"</span></span>      | [<span data-ttu-id="fc7ed-111">**Rollen \_ System- \_ Menüleiste**</span><span class="sxs-lookup"><span data-stu-id="fc7ed-111">**ROLE\_SYSTEM\_MENUBAR**</span></span>](object-roles.md)     | <span data-ttu-id="fc7ed-112">0</span><span class="sxs-lookup"><span data-stu-id="fc7ed-112">0</span></span>          |
| <span data-ttu-id="fc7ed-113">Keine</span><span class="sxs-lookup"><span data-stu-id="fc7ed-113">None</span></span>          | [<span data-ttu-id="fc7ed-114">**Rollen \_ System- \_ TitleBar**</span><span class="sxs-lookup"><span data-stu-id="fc7ed-114">**ROLE\_SYSTEM\_TITLEBAR**</span></span>](object-roles.md)   | <span data-ttu-id="fc7ed-115">5</span><span class="sxs-lookup"><span data-stu-id="fc7ed-115">5</span></span>          |
| <span data-ttu-id="fc7ed-116">Asyl</span><span class="sxs-lookup"><span data-stu-id="fc7ed-116">"Application"</span></span> | [<span data-ttu-id="fc7ed-117">**Rollen \_ System- \_ Menüleiste**</span><span class="sxs-lookup"><span data-stu-id="fc7ed-117">**ROLE\_SYSTEM\_MENUBAR**</span></span>](object-roles.md)     | <span data-ttu-id="fc7ed-118">0</span><span class="sxs-lookup"><span data-stu-id="fc7ed-118">0</span></span>          |
| <span data-ttu-id="fc7ed-119">Rechtes</span><span class="sxs-lookup"><span data-stu-id="fc7ed-119">"Vertical"</span></span>    | [<span data-ttu-id="fc7ed-120">**Rollen \_ System- \_ Scrollleiste**</span><span class="sxs-lookup"><span data-stu-id="fc7ed-120">**ROLE\_SYSTEM\_SCROLLBAR**</span></span>](object-roles.md) | <span data-ttu-id="fc7ed-121">5</span><span class="sxs-lookup"><span data-stu-id="fc7ed-121">5</span></span>          |
| <span data-ttu-id="fc7ed-122">Ales</span><span class="sxs-lookup"><span data-stu-id="fc7ed-122">"Horizontal"</span></span>  | [<span data-ttu-id="fc7ed-123">**Rollen \_ System- \_ Scrollleiste**</span><span class="sxs-lookup"><span data-stu-id="fc7ed-123">**ROLE\_SYSTEM\_SCROLLBAR**</span></span>](object-roles.md) | <span data-ttu-id="fc7ed-124">5</span><span class="sxs-lookup"><span data-stu-id="fc7ed-124">5</span></span>          |
| <span data-ttu-id="fc7ed-125">"Size Box"</span><span class="sxs-lookup"><span data-stu-id="fc7ed-125">"Size Box"</span></span>    | [<span data-ttu-id="fc7ed-126">**Rollen System-Zieh Punkt \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fc7ed-126">**ROLE\_SYSTEM\_GRIP**</span></span>](object-roles.md)           | <span data-ttu-id="fc7ed-127">0</span><span class="sxs-lookup"><span data-stu-id="fc7ed-127">0</span></span>          |



 

<span data-ttu-id="fc7ed-128">Client Entwickler müssen diese Objekte des übergeordneten Fensters und die untergeordneten Objekte identifizieren und herausfiltern, da Sie keinen sinnvollen Informationen für Endbenutzer bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="fc7ed-128">Client developers must identify and filter out these parent window objects and invisible child objects because they do not provide meaningful information to end users.</span></span>

 

 




