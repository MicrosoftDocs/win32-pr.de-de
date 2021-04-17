---
title: Ändern der Größe des Dialog Felds zum Erwerb von Lizenzen
description: Ändern der Größe des Dialog Felds zum Erwerb von Lizenzen
ms.assetid: e091d981-1574-4ffc-bdc4-b92f74396cb7
keywords:
- Windows Media Player, Ändern der Größe des Lizenz Erwerbs (Dialogfeld)
- Dialogfeld "Windows Media Player, Lizenzerwerb"
- Windows Media Player, DRM_LicenseAcqURL-Attribut
- Dialogfeld zum Ändern der Größe des Lizenz Erwerbs
- Dialogfeld "Lizenzerwerb"
- DRM_LicenseAcqURL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440683ce65417653251bbed58d59c4d9a34dbc57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388509"
---
# <a name="resizing-the-license-acquisition-dialog-box"></a><span data-ttu-id="7d134-109">Ändern der Größe des Dialog Felds zum Erwerb von Lizenzen</span><span class="sxs-lookup"><span data-stu-id="7d134-109">Resizing the License Acquisition Dialog Box</span></span>

<span data-ttu-id="7d134-110">Sie können Abfrage Zeichenfolgen-Parameter an die URL anfügen, die Sie für das DRM-Attribut " **\_ licenset URL** " bereitstellen, um eine Größe für das Dialogfeld "Lizenz Erfassung für Windows Media Player 10 oder höher" anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7d134-110">You can append query string parameters to the URL you provide for the **DRM\_LicenseAcqURL** attribute to specify a size for the Windows Media Player 10 or later license acquisition dialog box.</span></span> <span data-ttu-id="7d134-111">In der folgenden Tabelle sind die Parameter aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="7d134-111">The following table lists the parameters.</span></span>



| <span data-ttu-id="7d134-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d134-112">Parameter</span></span> | <span data-ttu-id="7d134-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d134-113">Description</span></span>                                        |
|-----------|----------------------------------------------------|
| <span data-ttu-id="7d134-114">*Dlgx*</span><span class="sxs-lookup"><span data-stu-id="7d134-114">*DlgX*</span></span>    | <span data-ttu-id="7d134-115">Gibt die Breite des Dialog Felds in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="7d134-115">Specifies the width of the dialog box, in pixels.</span></span>  |
| <span data-ttu-id="7d134-116">*Dlgy*</span><span class="sxs-lookup"><span data-stu-id="7d134-116">*DlgY*</span></span>    | <span data-ttu-id="7d134-117">Gibt die Höhe des Dialog Felds in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="7d134-117">Specifies the height of the dialog box, in pixels.</span></span> |



 

<span data-ttu-id="7d134-118">Beispielsweise würde die folgende Lizenz Erwerbs-URL bewirken, dass das Dialogfeld für die Lizenz Erfassung mit einer Größe von 800 x 600 Pixel geöffnet wird:</span><span class="sxs-lookup"><span data-stu-id="7d134-118">For example, the following license acquisition URL would cause the license acquisition dialog box to open with a size of 800 by 600 pixels:</span></span>


```C++
https://www.proseware.com/license/lic_acq.htm?DlgX=800&DlgY=600

```



<span data-ttu-id="7d134-119">Die maximale Größe für das Dialogfeld überschreitet niemals die aktuellen Bildschirm Abmessungen minus 20 Pixel.</span><span class="sxs-lookup"><span data-stu-id="7d134-119">The maximum size for the dialog box will never exceed the current screen dimensions minus 20 pixels.</span></span> <span data-ttu-id="7d134-120">Die Mindestgröße beträgt 333 x 210 Pixel (Standardgröße).</span><span class="sxs-lookup"><span data-stu-id="7d134-120">The minimum size is 333 x 210 pixels (the default size).</span></span>

<span data-ttu-id="7d134-121">Für dieses Feature ist Windows Media Player 10 oder höher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7d134-121">This feature requires Windows Media Player 10 or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d134-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7d134-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d134-123">**Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="7d134-123">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 




