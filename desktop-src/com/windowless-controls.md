---
title: Fensterlose Steuerelemente
description: Fensterlose Steuerelemente
ms.assetid: 1759e5db-423c-44cc-b901-f50046c91956
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 762c839067f32a5ac182ccd6b48bfb81c1c68f13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388777"
---
# <a name="windowless-controls"></a><span data-ttu-id="8e7f8-103">Fensterlose Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="8e7f8-103">Windowless Controls</span></span>

<span data-ttu-id="8e7f8-104">Die ActiveX-Steuerelemente 96-Spezifikation enthält eine Definition für fensterlose Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="8e7f8-104">The ActiveX Controls 96 specification includes a definition for windowless controls.</span></span> <span data-ttu-id="8e7f8-105">Solche Steuerelemente werden nicht in einem eigenen Fenster betrieben, und es ist erforderlich, dass ein Container ein frei gegebenes Fenster bereitstellt, in dem das Steuerelement gezeichnet werden kann, siehe das ActiveX SDK</span><span class="sxs-lookup"><span data-stu-id="8e7f8-105">Such controls do not operate in their own window and require a container to offer a shared window into which the control may draw, see the ActiveX SDK.</span></span> <span data-ttu-id="8e7f8-106">Fensterlose Steuerelemente sind so konzipiert, dass Sie mit älteren Steuerelement Containern kompatibel sind, indem Sie in dieser Situation ein eigenes Fenster erstellen. fensterlose Steuerelement Container sollten Fenster-Steuerelemente auf herkömmliche Weise ohne Probleme hosten.</span><span class="sxs-lookup"><span data-stu-id="8e7f8-106">Windowless controls are designed to be compatible with older control containers by creating their own window in that situation, windowless control containers should host windowed controls in the traditional way with no problem.</span></span> <span data-ttu-id="8e7f8-107">Es kann jedoch hilfreich sein, wenn die Steuerelemente, die in einem fensterlosen Modus betrieben werden können, von einem Container unterschieden werden können, sodass eine passende Komponenten Kategorie definiert ist.</span><span class="sxs-lookup"><span data-stu-id="8e7f8-107">It may however be useful for a container to distinguish those controls that can operate in a windowless mode, so an appropriate component category is defined.</span></span>

<span data-ttu-id="8e7f8-108">CATID-{1d06b600-3ae3-11CF-87b9-00aa006c8166} CATID \_ windowlessobject</span><span class="sxs-lookup"><span data-stu-id="8e7f8-108">CATID - {1D06B600-3AE3-11cf-87B9-00AA006C8166} CATID\_WindowlessObject</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e7f8-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8e7f8-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e7f8-110">Komponentenkategorien</span><span class="sxs-lookup"><span data-stu-id="8e7f8-110">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 




