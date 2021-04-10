---
title: VML-Bogen Element
description: VML-Bogen Element
ms.assetid: 46b5b78a-9a69-432b-9008-0ce7a658b9dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd35d59349e10f38495807ceb3f08dc254c117e2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316298"
---
# <a name="vml-arc-element"></a><span data-ttu-id="05447-103">VML-Bogen Element</span><span class="sxs-lookup"><span data-stu-id="05447-103">VML Arc Element</span></span>

<span data-ttu-id="05447-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="05447-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="05447-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="05447-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="05447-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="05447-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="05447-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="05447-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="05447-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="05447-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="05447-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="05447-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="05447-110">Vordefinierte Arkus Form.</span><span class="sxs-lookup"><span data-stu-id="05447-110">Predefined arc shape.</span></span>

<span data-ttu-id="05447-111">**Bogen** verwendet [die Attribute "](msdn-online-vml-endangle-attribute.md) [Start Angle](msdn-online-vml-startangle-attribute.md) " und "ein".</span><span class="sxs-lookup"><span data-stu-id="05447-111">**Arc** uses the [startangle](msdn-online-vml-startangle-attribute.md) and [endangle](msdn-online-vml-endangle-attribute.md) attributes.</span></span>

<span data-ttu-id="05447-112">Im folgenden finden Sie den minimalen Code, der zum Entwickeln eines Bilds erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="05447-112">The following is the minimum code needed to produce an image.</span></span>


```HTML
   <v:arc
   style="top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```





 

 