---
title: Agentsteuerungseigenschaften
description: Agentsteuerungseigenschaften
ms.assetid: e6a5b2db-9abf-4988-be41-fc7f4530507f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f5e80b10469e7e256b1b2bf3bcf55fb5a8a08b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036521"
---
# <a name="agent-control-properties"></a><span data-ttu-id="3b0c6-103">Agentsteuerungseigenschaften</span><span class="sxs-lookup"><span data-stu-id="3b0c6-103">Agent Control Properties</span></span>

<span data-ttu-id="3b0c6-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="3b0c6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="3b0c6-105">Der Zugriff auf die folgenden Eigenschaften erfolgt direkt über das-Agent-Steuerelement:</span><span class="sxs-lookup"><span data-stu-id="3b0c6-105">The following properties are directly accessed from the Agent control:</span></span>

-   [<span data-ttu-id="3b0c6-106">**Verbunden**</span><span class="sxs-lookup"><span data-stu-id="3b0c6-106">**Connected**</span></span>](connected-property.md)
-   [<span data-ttu-id="3b0c6-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="3b0c6-107">**Name**</span></span>](name-property-a.md)
-   [<span data-ttu-id="3b0c6-108">**Raiserequesterrors**</span><span class="sxs-lookup"><span data-stu-id="3b0c6-108">**RaiseRequestErrors**</span></span>](raiserequesterrors-property.md)

<span data-ttu-id="3b0c6-109">Darüber hinaus können einige Programmierumgebungen zusätzliche Entwurfszeit-oder Lauf Zeiteigenschaften zuweisen.</span><span class="sxs-lookup"><span data-stu-id="3b0c6-109">In addition, some programming environments may assign additional design-time or run-time properties.</span></span> <span data-ttu-id="3b0c6-110">Visual Basic fügt z. b. die Eigenschaften Left, Index, Tag und Top hinzu, die die Position des Steuer Elements in einem Formular definieren, auch wenn das Steuerelement zur Laufzeit nicht auf der Seite des Formulars angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3b0c6-110">For example, Visual Basic adds Left, Index, Tag, and Top properties that define the location of the control on a form even though the control does not appear on the form's page at run time.</span></span>

<span data-ttu-id="3b0c6-111">Die angehaltene Eigenschaft wird weiterhin aus Gründen der Abwärtskompatibilität unterstützt, gibt jedoch immer **false** zurück, da der Server keinen angehaltenen Zustand mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3b0c6-111">The Suspended property is still supported for backward compatibility, but always returns **False** because the server no longer supports a suspended state.</span></span>

 

 




