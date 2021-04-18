---
title: Der OBJID_QUERYCLASSNAMEIDX Objekt Bezeichner.
description: Microsoft Active Accessibility verwendet die objID \_ queryclassnameidx-Objekt-ID mit der WM \_ GetObject-Nachricht, um die Klasse zu bestimmen, zu der ein standardmäßiges Windows-Steuerelement oder ein gemeinsames Steuerelement gehört.
ms.assetid: 2167df6d-5df3-40b7-bebe-142f4bd98cd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d73a152380411ef0b230de8f0e3372a6718b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337347"
---
# <a name="the-objid_queryclassnameidx-object-identifier"></a><span data-ttu-id="6f518-103">Der ObjID \_ queryclassnameidx-Objekt Bezeichner</span><span class="sxs-lookup"><span data-stu-id="6f518-103">The OBJID\_QUERYCLASSNAMEIDX Object Identifier</span></span>

<span data-ttu-id="6f518-104">Microsoft Active Accessibility verwendet die [**objID \_ queryclassnameidx**](object-identifiers.md) -Objekt-ID mit der [**WM \_ GetObject**](wm-getobject.md) -Nachricht, um die Klasse zu bestimmen, zu der ein standardmäßiges Windows-Steuerelement oder ein gemeinsames Steuerelement gehört.</span><span class="sxs-lookup"><span data-stu-id="6f518-104">Microsoft Active Accessibility uses the [**OBJID\_QUERYCLASSNAMEIDX**](object-identifiers.md) object identifier with the [**WM\_GETOBJECT**](wm-getobject.md) message to determine the class to which a standard Windows control or common control belongs.</span></span> <span data-ttu-id="6f518-105">Ein-Steuerelement reagiert auf diese Meldung, indem ein Wert zurückgegeben wird, den Microsoft Active Accessibility dem Klassennamen des Steuer Elements zuordnet.</span><span class="sxs-lookup"><span data-stu-id="6f518-105">A control responds to this message by returning a value that Microsoft Active Accessibility maps to the class name of the control.</span></span> <span data-ttu-id="6f518-106">Microsoft Active Accessibility verwendet diese Informationen, um Barrierefreiheits Unterstützung für standardmäßige Windows-Steuerelemente und allgemeine Steuerelemente bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6f518-106">Microsoft Active Accessibility uses this information to provide accessibility support for standard Windows controls and common controls.</span></span>

<span data-ttu-id="6f518-107">Im allgemeinen reagieren nur die standardmäßigen Windows-Steuerelemente und die allgemeinen Steuerelemente auf die [**objID \_ queryclassnameidx**](object-identifiers.md) -Objekt Kennung.</span><span class="sxs-lookup"><span data-stu-id="6f518-107">Generally, only the standard Windows controls and the common controls respond to the [**OBJID\_QUERYCLASSNAMEIDX**](object-identifiers.md) object identifier.</span></span> <span data-ttu-id="6f518-108">Ein benutzerdefiniertes Steuerelement kann jedoch auch Antworten, wenn es die gleiche Funktionalität wie ein vorhandenes standardmäßiges Windows-Steuerelement oder ein gemeinsames Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="6f518-108">However, a custom control can also respond if it includes all of the same functionality as an existing standard Windows control or common control.</span></span> <span data-ttu-id="6f518-109">Dadurch wird das benutzerdefinierte Steuerelement von einem der Standard Proxy Objekte, die von Microsoft Active Accessibility bereitgestellt werden, unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6f518-109">This enables the custom control to be supported by one of the standard proxy objects provided by Microsoft Active Accessibility.</span></span>

<span data-ttu-id="6f518-110">Weitere Informationen finden Sie unter [Anhang F: objektbezeichnerwerte für objID \_ queryclassnameidx](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).</span><span class="sxs-lookup"><span data-stu-id="6f518-110">For more information, see [Appendix F: Object Identifier Values for OBJID\_QUERYCLASSNAMEIDX](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).</span></span>

 

 




