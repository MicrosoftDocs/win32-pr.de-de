---
title: Automatisches Abschneiden
description: Automatisches Abschneiden
ms.assetid: 9107ee47-52aa-48c8-b141-c821f93fda45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71fb39f3a9f15ed6e1e96493ed2cbdd62db40403
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310676"
---
# <a name="automatic-clipping"></a><span data-ttu-id="5a151-103">Automatisches Abschneiden</span><span class="sxs-lookup"><span data-stu-id="5a151-103">Automatic Clipping</span></span>

<span data-ttu-id="5a151-104">Es wird dringend empfohlen, dass ein ActiveX-Steuerelement Container das automatische Abschneiden seiner Steuerelemente unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5a151-104">It is strongly recommended that an ActiveX control container supports automatic clipping of its controls.</span></span> <span data-ttu-id="5a151-105">Dies führt für die meisten Steuerelemente zu einem effizienteren Betrieb.</span><span class="sxs-lookup"><span data-stu-id="5a151-105">This will result in more efficient operation for most controls.</span></span> <span data-ttu-id="5a151-106">Wenn Automatisches Abschneiden unterstützt wird, muss die autoclip Ambient-Eigenschaft unterstützt werden und den Wert **true** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="5a151-106">If automatic clipping is supported, the AutoClip ambient property must be supported and have a value of **TRUE**.</span></span>

<span data-ttu-id="5a151-107">Das automatische Abschneiden ist die Fähigkeit eines Containers sicherzustellen, dass die gezeichnete Ausgabe eines Steuer Elements nur in den aktuellen Clippingbereich des Containers übergeht.</span><span class="sxs-lookup"><span data-stu-id="5a151-107">Automatic clipping is the ability of a container to ensure that a control's drawn output goes only to the container's current clipping region.</span></span> <span data-ttu-id="5a151-108">In einem Container, der das automatische Clipping unterstützt, kann ein Steuerelement ohne Rücksicht auf den Ausschneide Bereich zeichnen, da der Container automatisch alle Zeichnungen Ausschneide, die außerhalb des Bereichs des Steuer Elements auftreten.</span><span class="sxs-lookup"><span data-stu-id="5a151-108">In a container that supports automatic clipping, a control can paint without regard to its clipping region, because the container will automatically clip any painting that occurs outside the control's area.</span></span> <span data-ttu-id="5a151-109">Wenn ein Container das automatische Abschneiden nicht unterstützt, wird von cdk-generierten Steuerelementen ein zusätzliches übergeordnetes Fenster erstellt, wenn ein Clippingbereich außerhalb von NULL übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5a151-109">If a container does not support automatic clipping, then CDK-generated controls will create an extra parent window if a non-null clipping region is passed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a151-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5a151-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a151-111">Container</span><span class="sxs-lookup"><span data-stu-id="5a151-111">Containers</span></span>](containers.md)
</dt> </dl>

 

 




