---
description: Das stretchmode-Attribut gibt an, wie ein Bild gestreckt wird, das nicht den Ausgabe Dimensionen entspricht.
ms.assetid: 9a26bb8b-2b1c-424a-ae30-e175c60c76a1
title: stretchmode-Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48a629a34dc1875a7f1d3669e32c53d0e8d3d29c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867084"
---
# <a name="stretchmode-attribute"></a><span data-ttu-id="da8e4-103">stretchmode-Attribut</span><span class="sxs-lookup"><span data-stu-id="da8e4-103">stretchmode Attribute</span></span>

> [!Note]  
> <span data-ttu-id="da8e4-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="da8e4-104">\[Deprecated.</span></span> <span data-ttu-id="da8e4-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="da8e4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="da8e4-106">Das- `stretchmode` Attribut gibt an, wie ein Bild gestreckt wird, das nicht den Ausgabe Dimensionen entspricht.</span><span class="sxs-lookup"><span data-stu-id="da8e4-106">The `stretchmode` attribute specifies how to stretch an image that does not match the output dimensions.</span></span>

## <a name="possible-values"></a><span data-ttu-id="da8e4-107">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="da8e4-107">Possible Values</span></span>

<span data-ttu-id="da8e4-108">Muss einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="da8e4-108">Must have one of the following values.</span></span>

-   <span data-ttu-id="da8e4-109">"Stretch": das Bild wird so gestreckt, dass es der Ausgabe Frame Größe entspricht, ohne das Seitenverhältnis beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="da8e4-109">"stretch": The image is stretched to fit the output frame size without preserving aspect ratio.</span></span> <span data-ttu-id="da8e4-110">(Standardwert)</span><span class="sxs-lookup"><span data-stu-id="da8e4-110">(Default)</span></span>
-   <span data-ttu-id="da8e4-111">"Zuschneiden": das Bild wird an die Ausgabe Frame Größe angepasst.</span><span class="sxs-lookup"><span data-stu-id="da8e4-111">"crop": The image is cropped to fit the output frame size.</span></span>
-   <span data-ttu-id="da8e4-112">"preserveaspectratio": das ursprüngliche Seitenverhältnis wird beibehalten, wobei ein schwarzes buchfeld entlang der kürzeren Dimension liegt.</span><span class="sxs-lookup"><span data-stu-id="da8e4-112">"preserveaspectratio": The original aspect ratio is preserved, with a black letterbox along the shorter dimension.</span></span>
-   <span data-ttu-id="da8e4-113">"preserveaspectrationoletterbox": die Größe des Bilds wird geändert, um den gesamten Zielframe auszufüllen und gleichzeitig das Seitenverhältnis beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="da8e4-113">"preserveaspectrationoletterbox": The image is resized to fill the entire target frame while preserving the aspect ratio.</span></span>

## <a name="applies-to"></a><span data-ttu-id="da8e4-114">Gilt für</span><span class="sxs-lookup"><span data-stu-id="da8e4-114">Applies To</span></span>

[<span data-ttu-id="da8e4-115">**Techno**</span><span class="sxs-lookup"><span data-stu-id="da8e4-115">**clip**</span></span>](clip-element.md)

## <a name="see-also"></a><span data-ttu-id="da8e4-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da8e4-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da8e4-117">XTL-Attribute</span><span class="sxs-lookup"><span data-stu-id="da8e4-117">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="da8e4-118">**Iamtimelinesrc:: setstretchmode**</span><span class="sxs-lookup"><span data-stu-id="da8e4-118">**IAMTimelineSrc::SetStretchMode**</span></span>](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 



