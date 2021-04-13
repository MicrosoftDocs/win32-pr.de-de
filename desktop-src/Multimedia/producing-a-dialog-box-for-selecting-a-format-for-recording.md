---
title: Erstellen eines Dialog Felds zum Auswählen eines Formats für die Aufzeichnung
description: Erstellen eines Dialog Felds zum Auswählen eines Formats für die Aufzeichnung
ms.assetid: e94ca8da-4ee6-4362-a144-27b86f2cadac
keywords:
- Audiokomprimierungs-Manager (ACM), Erstellen von Dialogfeldern
- ACM (Audiokomprimierungs-Manager), Erstellen von Dialogfeldern
- ACM-Beispiele, Erstellen von Dialogfeldern
- Erstellen von Dialogfeldern
- acmformatchoose-Funktion
- Audiokomprimierungs-Manager (ACM), auswählen des Formats für das umherstellen
- ACM (Audiokomprimierungs-Manager), auswählen des Formats für das umherstellen
- ACM-Beispiele, auswählen des Formats für das umherstellen
- Auswählen des Formats für das Aufzeichnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7584d5f56904a6aa5241930041bf89c10373f6b1
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/27/2020
ms.locfileid: "104389987"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-recording"></a><span data-ttu-id="9e59d-112">Erstellen eines Dialog Felds zum Auswählen eines Formats für die Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="9e59d-112">Producing a Dialog Box for Selecting a Format for Recording</span></span>

<span data-ttu-id="9e59d-113">Eine Anwendung kann es Benutzern ermöglichen, ein Format auszuwählen, für das ein installiertes Waveform-Audiogerät Native Unterstützung bietet.</span><span class="sxs-lookup"><span data-stu-id="9e59d-113">An application can allow the user to select a format for which an installed waveform-audio device provides native support.</span></span> <span data-ttu-id="9e59d-114">Angenommen, Sie möchten, dass ein Waveform-Audioeditor neue Waveform-Audiodaten aufzeichnen kann, ohne einen ACM-Kompressor oder-Debug zum Bereitstellen einer übersetzungsebene zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9e59d-114">For example, you might want a waveform-audio editor to record new waveform-audio data without using an ACM compressor or decompressor to provide a translation layer.</span></span> <span data-ttu-id="9e59d-115">Verwenden Sie hierzu die [**acmformatchoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) -Funktion, und geben Sie dabei die ACM \_ formatenumf \_ -Hardware und die ACM \_ formatenumf- \_ eingabeflags im **fdwenum** -Member der [**acmformatchoose**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) -Struktur an.</span><span class="sxs-lookup"><span data-stu-id="9e59d-115">To do this, use the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, specifying the ACM\_FORMATENUMF\_HARDWARE and ACM\_FORMATENUMF\_INPUT flags in the **fdwEnum** member of the [**ACMFORMATCHOOSE**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) structure.</span></span>

 

 




