---
title: Erstellen eines Dialog Felds zum Auswählen eines Formats zum Speichern
description: Erstellen eines Dialog Felds zum Auswählen eines Formats zum Speichern
ms.assetid: f833b28c-13e1-497c-bfc4-2e3bc84d7fff
keywords:
- Audiokomprimierungs-Manager (ACM), Erstellen von Dialogfeldern
- ACM (Audiokomprimierungs-Manager), Erstellen von Dialogfeldern
- ACM-Beispiele, Erstellen von Dialogfeldern
- Erstellen von Dialogfeldern
- acmformatchoose-Funktion
- Audiokomprimierungs-Manager (ACM), auswählen des zu speichenden Formats
- ACM (Audiokomprimierungs-Manager), auswählen des zu speichenden Formats
- ACM-Beispiele, auswählen des Formats zum Speichern
- Auswählen des Formats zum Speichern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55df4cd89a04bf1d3dd34512c4014928b6d5d4fb
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/27/2020
ms.locfileid: "104389988"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-saving"></a><span data-ttu-id="38ea3-112">Erstellen eines Dialog Felds zum Auswählen eines Formats zum Speichern</span><span class="sxs-lookup"><span data-stu-id="38ea3-112">Producing a Dialog Box for Selecting a Format for Saving</span></span>

<span data-ttu-id="38ea3-113">Möglicherweise möchten Sie, dass eine Anwendung vorhandene Waveform-Audiodaten in einem anderen Format speichert.</span><span class="sxs-lookup"><span data-stu-id="38ea3-113">You might want an application to save existing waveform-audio data in another format.</span></span> <span data-ttu-id="38ea3-114">Beispielsweise könnte ein Waveform-Audioeditor eine Waveform-Audiodatei als komprimierte Datei speichern.</span><span class="sxs-lookup"><span data-stu-id="38ea3-114">For example, a waveform-audio editor could save a waveform-audio file as a compressed file.</span></span> <span data-ttu-id="38ea3-115">Um nur die vorgeschlagenen Zielformate für ein angegebenes Quellformat im Dialogfeld aufzulisten, das von der [**acmformatchoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) -Funktion erstellt wurde, geben Sie das Quellformat im **pwfxenum** -Element und das ACM \_ formatenumf-Vorschlags \_ Flag im **fdwenum** -Member der [**acmformatchoose**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) -Struktur an.</span><span class="sxs-lookup"><span data-stu-id="38ea3-115">To list only the suggested destination formats for a specified source format in the dialog box created by the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, specify the source format in the **pwfxEnum** member and the ACM\_FORMATENUMF\_SUGGEST flag in the **fdwEnum** member of the [**ACMFORMATCHOOSE**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) structure.</span></span>

<span data-ttu-id="38ea3-116">Um gültige Zielformate für ein bestimmtes Format aufzulisten, verwenden Sie das ACM \_ formatenumf \_ Convert-Flag anstelle des ACM \_ formatenumf- \_ Flag zum vorschlagen.</span><span class="sxs-lookup"><span data-stu-id="38ea3-116">Similarly, to list valid destination formats for a specified format, use the ACM\_FORMATENUMF\_CONVERT flag instead of the ACM\_FORMATENUMF\_SUGGEST flag.</span></span>

 

 




