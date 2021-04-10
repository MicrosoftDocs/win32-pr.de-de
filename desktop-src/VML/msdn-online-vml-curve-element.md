---
title: VML-Kurven Element
description: VML-Kurven Element
ms.assetid: 37197ef0-7597-465a-bc37-7ffcde2e736b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b9e04086652bf9dde7d7e7f5ebdea0992f774c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209262"
---
# <a name="vml-curve-element"></a><span data-ttu-id="a4186-103">VML-Kurven Element</span><span class="sxs-lookup"><span data-stu-id="a4186-103">VML Curve Element</span></span>

<span data-ttu-id="a4186-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="a4186-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a4186-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="a4186-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a4186-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="a4186-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a4186-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="a4186-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a4186-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a4186-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a4186-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a4186-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a4186-110">Vordefinierte Kurvenform.</span><span class="sxs-lookup"><span data-stu-id="a4186-110">Predefined curve shape.</span></span>

<span data-ttu-id="a4186-111">Die **Kurve** verwendet die Attribute [to](to-attribute--curve--vml.md), [from](from-attribute--curve--vml.md), [Control1](msdn-online-vml-control1-attribute.md)und [Control2](msdn-online-vml-control2-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="a4186-111">**Curve** uses the [to](to-attribute--curve--vml.md), [from](from-attribute--curve--vml.md), [control1](msdn-online-vml-control1-attribute.md), and [control2](msdn-online-vml-control2-attribute.md) attributes.</span></span>

<span data-ttu-id="a4186-112">Im folgenden finden Sie den minimalen Code, der zum Entwickeln eines Bilds erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a4186-112">The following is the minimum code needed to produce an image.</span></span>


```HTML
   <v:curve
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,30pt" control2="70pt,30pt">
   </v:curve>
```





 

 