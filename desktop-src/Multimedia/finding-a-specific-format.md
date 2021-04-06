---
title: Suchen nach einem bestimmten Format
description: Suchen nach einem bestimmten Format
ms.assetid: 0c892758-d409-4ed7-8f38-a24eee646b65
keywords:
- Audiokomprimierungs-Manager (ACM), suchen nach Formaten
- ACM (Audiokomprimierungs-Manager), suchen nach Formaten
- ACM-Beispiele, suchen nach Formaten
- Suchen nach Formaten
- acmformatenum-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c148c075df09cb702caf6b1d192fe8ce41b48ad0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947983"
---
# <a name="finding-a-specific-format"></a><span data-ttu-id="25d81-108">Suchen nach einem bestimmten Format</span><span class="sxs-lookup"><span data-stu-id="25d81-108">Finding a Specific Format</span></span>

<span data-ttu-id="25d81-109">Eine Anwendung verfügt möglicherweise nur über eine partielle Spezifikation für ein Format, wenn Sie die vollständige Spezifikation benötigt.</span><span class="sxs-lookup"><span data-stu-id="25d81-109">An application might have only a partial specification for a format when it needs the full specification.</span></span> <span data-ttu-id="25d81-110">Beispielsweise kann die Spezifikation ein 11-kHz-Mono-, 4-Bit-ADPCM-Format, jedoch nicht die durchschnittlichen Bytes pro Sekunde festlegen.</span><span class="sxs-lookup"><span data-stu-id="25d81-110">For example, the specification might stipulate an 11-kHz mono, 4-bit ADPCM format, but not the average bytes per second.</span></span> <span data-ttu-id="25d81-111">Die Anwendung kann das vollständige Format ohne Benutzereingriff mit der [**acmformatenum**](/windows/desktop/api/Msacm/nf-msacm-acmformatenum) -Funktion und der Angabe von Flags im Parameter " *sdwenum* " erhalten.</span><span class="sxs-lookup"><span data-stu-id="25d81-111">The application can get the full format without user intervention by using the [**acmFormatEnum**](/windows/desktop/api/Msacm/nf-msacm-acmformatenum) function and specifying flags in the *fdwEnum* parameter.</span></span>

 

 




