---
title: Private Schnittstellen Visual Basic
description: Private Schnittstellen Visual Basic
ms.assetid: 782e5d87-680e-4d0c-b1e6-cf97d1a37ce5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af32f46c02b9b76cdf3dd83e9a22a028aaa88d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037608"
---
# <a name="visual-basic-private-interfaces"></a><span data-ttu-id="ca9c5-103">Private Schnittstellen Visual Basic</span><span class="sxs-lookup"><span data-stu-id="ca9c5-103">Visual Basic Private Interfaces</span></span>

<span data-ttu-id="ca9c5-104">Hier werden zwei von Visual Basic implementierte Schnittstellen für Komponenten Kategorien identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ca9c5-104">Two interfaces that are implemented by Visual Basic are identified here for component categories.</span></span> <span data-ttu-id="ca9c5-105">Es ist nicht zu erwarten, dass Steuerelemente diese Kategorien benötigen, da Steuerelemente eine Alternative Funktionalität anbieten können, wenn diese nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ca9c5-105">It is not expected that controls should require these categories because it is possible for controls to offer alternative functionality when these are not available.</span></span>

<span data-ttu-id="ca9c5-106">Mit der [**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat) -Schnittstelle können Steuerelemente beim Formatieren von Daten besser in die Visual Basic Umgebung integriert werden.</span><span class="sxs-lookup"><span data-stu-id="ca9c5-106">The [**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat) interface allows controls to better integrate into the Visual Basic environment when formatting data.</span></span>

<span data-ttu-id="ca9c5-107">CATID-{02496840-3ac4-11CF-87b9-00aa006c8166} CATID \_ vbformat</span><span class="sxs-lookup"><span data-stu-id="ca9c5-107">CATID - {02496840-3AC4-11cf-87B9-00AA006C8166} CATID\_VBFormat</span></span>

<span data-ttu-id="ca9c5-108">Die [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol) -Schnittstelle ermöglicht es einem Steuerelement, andere Steuerelemente auf dem VB-Formular aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="ca9c5-108">The [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol) interface allows a control to enumerate other controls on the VB form.</span></span>

<span data-ttu-id="ca9c5-109">CATID-{02496841-3ac4-11CF-87b9-00aa006c8166} CATID \_ vbgetcontrol</span><span class="sxs-lookup"><span data-stu-id="ca9c5-109">CATID - {02496841-3AC4-11cf-87B9-00AA006C8166} CATID\_VBGetControl</span></span>

<span data-ttu-id="ca9c5-110">Zwei weitere private Schnittstellen, [**IGetVBAObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) und [**igetoleobject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject), werden hier beschrieben, auch wenn Sie keine Komponenten Kategorien definieren.</span><span class="sxs-lookup"><span data-stu-id="ca9c5-110">Two additional private interfaces, [**IGetVBAObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) and [**IGetOleObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject), are described here even though they do not define component categories.</span></span> <span data-ttu-id="ca9c5-111">Die Verwendung dieser vier Schnittstellen ist nicht empfehlenswert, da Sie von anderen Containern als Visual Basic nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ca9c5-111">Use of these four interfaces is not recommended because they are not supported by containers other than Visual Basic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca9c5-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ca9c5-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca9c5-113">Komponentenkategorien</span><span class="sxs-lookup"><span data-stu-id="ca9c5-113">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 




