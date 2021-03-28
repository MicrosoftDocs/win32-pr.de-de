---
description: In diesem Abschnitt werden die Funktionen zur Handhabung der Farbpalette von Windows Shell beschrieben. Die in dieser Dokumentation erläuterten Programmier Elemente werden von Shlwapi.dll exportiert und in "shlwapi. h" und "shlwapi. lib" definiert.
title: Verarbeitungsfunktionen für shellfarb Palette
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 93848cb3-60c6-4b2f-82d9-abfee97e372a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ba92dcf280b8d54b8778e276bb603d888f5991c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216416"
---
# <a name="shell-color-palette-handling-functions"></a><span data-ttu-id="76df8-104">Verarbeitungsfunktionen für shellfarb Palette</span><span class="sxs-lookup"><span data-stu-id="76df8-104">Shell Color Palette Handling Functions</span></span>

<span data-ttu-id="76df8-105">In diesem Abschnitt werden die Funktionen zur Handhabung der Farbpalette von Windows Shell beschrieben.</span><span class="sxs-lookup"><span data-stu-id="76df8-105">This section describes the Windows Shell color palette handling functions.</span></span> <span data-ttu-id="76df8-106">Die in dieser Dokumentation erläuterten Programmier Elemente werden von Shlwapi.dll exportiert und in "shlwapi. h" und "shlwapi. lib" definiert.</span><span class="sxs-lookup"><span data-stu-id="76df8-106">The programming elements explained in this documentation are exported by Shlwapi.dll and defined in Shlwapi.h and Shlwapi.lib.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="76df8-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="76df8-107">In this section</span></span>



| <span data-ttu-id="76df8-108">Thema</span><span class="sxs-lookup"><span data-stu-id="76df8-108">Topic</span></span>                                                           | <span data-ttu-id="76df8-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76df8-109">Description</span></span>                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="76df8-110">**Color-Luma**</span><span class="sxs-lookup"><span data-stu-id="76df8-110">**ColorAdjustLuma**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-coloradjustluma)<br/>           | <span data-ttu-id="76df8-111">Ändert die Leuchtkraft eines RGB-Werts.</span><span class="sxs-lookup"><span data-stu-id="76df8-111">Changes the luminance of a RGB value.</span></span> <span data-ttu-id="76df8-112">Farbton und Sättigung sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="76df8-112">Hue and saturation are not affected.</span></span><br/> |
| [<span data-ttu-id="76df8-113">**Colorhlstorgb**</span><span class="sxs-lookup"><span data-stu-id="76df8-113">**ColorHLSToRGB**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-colorhlstorgb)<br/>               | <span data-ttu-id="76df8-114">Konvertiert Farben von "Hue-Luminance-Sättigung (HLS)" in das RGB-Format.</span><span class="sxs-lookup"><span data-stu-id="76df8-114">Converts colors from hue-luminance-saturation (HLS) to RGB format.</span></span><br/>         |
| [<span data-ttu-id="76df8-115">**Colorrgbper HLS**</span><span class="sxs-lookup"><span data-stu-id="76df8-115">**ColorRGBToHLS**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-colorrgbtohls)<br/>               | <span data-ttu-id="76df8-116">Konvertiert Farben von RGB in das HLS-Format (Hue-Luminance-Sättigung).</span><span class="sxs-lookup"><span data-stu-id="76df8-116">Converts colors from RGB to hue-luminance-saturation (HLS) format.</span></span><br/>         |
| [<span data-ttu-id="76df8-117">**Shkreateshellpalette**</span><span class="sxs-lookup"><span data-stu-id="76df8-117">**SHCreateShellPalette**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreateshellpalette)<br/> | <span data-ttu-id="76df8-118">Erstellt eine halbftone-Palette für den angegebenen Gerätekontext.</span><span class="sxs-lookup"><span data-stu-id="76df8-118">Creates a halftone palette for the specified device context.</span></span><br/>               |



 

 

 




