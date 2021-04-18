---
title: Sicherheitsüberlegungen für Windows Color System
description: Sicherheitsüberlegungen für Windows Color System
ms.assetid: 9e8b7c38-3c4f-4537-a7e1-6ad0daa39497
keywords:
- Windows Color System (WCS), Sicherheit
- WCS (Windows Color System), Sicherheit
- Bildfarben Verwaltung, Sicherheit
- Farbverwaltung, Sicherheit
- Sicherheit für Windows Color System (WCS)
- Farb Verwaltungsmodul (CMM)
- CMM (Farb Verwaltungsmodul)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef47ada0c233900f6e56a1e438d411a2ae84abd3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106351856"
---
# <a name="security-considerations-windows-color-system"></a><span data-ttu-id="c8927-110">Sicherheitsüberlegungen: Windows Color System</span><span class="sxs-lookup"><span data-stu-id="c8927-110">Security Considerations: Windows Color System</span></span>

<span data-ttu-id="c8927-111">Dieses Dokument enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit der Bild Farbverwaltung.</span><span class="sxs-lookup"><span data-stu-id="c8927-111">This document provides information about security considerations related to image color management.</span></span> <span data-ttu-id="c8927-112">Dieses Dokument bietet Ihnen nicht alles, was Sie über Sicherheitsprobleme wissen müssen – sondern als Ausgangspunkt und Verweis für diesen Technologiebereich.</span><span class="sxs-lookup"><span data-stu-id="c8927-112">This document doesn't provide all you need to know about security issues—instead, use it as a starting point and reference for this technology area.</span></span>

## <a name="non-microsoft-cmms-can-run-in-system-context"></a><span data-ttu-id="c8927-113">Nicht-Microsoft-CMMS können im Systemkontext ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c8927-113">Non-Microsoft CMMs can run in system context</span></span>

<span data-ttu-id="c8927-114">Farb Verwaltungs Module (CMMS), die nicht von Microsoft unterliegen, sollten wie nicht-Microsoft-Druckertreiber behandelt werden, da Sie in einem Systemkontext für Druckvorgänge ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="c8927-114">Non-Microsoft Color Management Modules (CMMs) should be treated like non-Microsoft printer drivers because they have the potential to run in a system context for printing operations.</span></span>
