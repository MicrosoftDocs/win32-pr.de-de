---
title: Nachrichten Reflektion
description: Nachrichten Reflektion
ms.assetid: 26a124d7-6499-4e8f-9001-d2782c1cc290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96cb563597e5aa92440e1b1434420e983268d9b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036283"
---
# <a name="message-reflection"></a><span data-ttu-id="e3d7d-103">Nachrichten Reflektion</span><span class="sxs-lookup"><span data-stu-id="e3d7d-103">Message Reflection</span></span>

<span data-ttu-id="e3d7d-104">Es wird dringend empfohlen, dass ein ActiveX-Steuerelement Container Nachrichten Reflektion unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e3d7d-104">It is strongly recommended that an ActiveX control container supports message reflection.</span></span> <span data-ttu-id="e3d7d-105">Dies führt zu einer effizienteren Operation für untergeordnete Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="e3d7d-105">This will result in more efficient operation for subclassed controls.</span></span> <span data-ttu-id="e3d7d-106">Wenn Nachrichten Reflektion unterstützt wird, muss die Ambient-Eigenschaft MessageReflect unterstützt werden und den Wert **true** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e3d7d-106">If message reflection is supported, the MessageReflect ambient property must be supported and have a value of **TRUE**.</span></span> <span data-ttu-id="e3d7d-107">Wenn ein Container keine Nachrichten Reflektion implementiert, erstellt das OLE CDK zwei Fenster für jedes untergeordnete Steuerelement, um Nachrichten Reflektion für den Steuerungs Container bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e3d7d-107">If a container does not implement message reflection, then the OLE CDK creates two windows for every subclassed control, to provide message reflection on behalf on the control container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3d7d-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e3d7d-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3d7d-109">Container</span><span class="sxs-lookup"><span data-stu-id="e3d7d-109">Containers</span></span>](containers.md)
</dt> </dl>

 

 




