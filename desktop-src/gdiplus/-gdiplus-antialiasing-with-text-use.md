---
description: Windows GDI+ bietet verschiedene Qualitätsstufen zum Zeichnen von Text. In der Regel benötigt das Rendern höherer Qualität mehr Verarbeitungszeit als das Rendering mit niedrigerer Qualität.
ms.assetid: 780d97ec-f446-4d19-837f-517a7d6dd27d
title: Antialiasing mit Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24c7b7c59a436db6c16251aa8e866648eed5cc51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994462"
---
# <a name="antialiasing-with-text"></a><span data-ttu-id="83403-104">Antialiasing mit Text</span><span class="sxs-lookup"><span data-stu-id="83403-104">Antialiasing with Text</span></span>

<span data-ttu-id="83403-105">Windows GDI+ bietet verschiedene Qualitätsstufen zum Zeichnen von Text.</span><span class="sxs-lookup"><span data-stu-id="83403-105">Windows GDI+ provides various quality levels for drawing text.</span></span> <span data-ttu-id="83403-106">In der Regel benötigt das Rendern höherer Qualität mehr Verarbeitungszeit als das Rendering mit niedrigerer Qualität.</span><span class="sxs-lookup"><span data-stu-id="83403-106">Typically, higher quality rendering takes more processing time than lower quality rendering.</span></span>

<span data-ttu-id="83403-107">Die Qualitätsstufe ist eine Eigenschaft der [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse.</span><span class="sxs-lookup"><span data-stu-id="83403-107">The quality level is a property of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="83403-108">Um die Qualitätsstufe festzulegen, müssen Sie die [**Graphics:: settextrenderinghint**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) -Methode eines **Grafik** Objekts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="83403-108">To set the quality level, call the [**Graphics::SetTextRenderingHint**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) method of a **Graphics** object.</span></span> <span data-ttu-id="83403-109">Die **Graphics:: settextrenderinghint** -Methode empfängt eines der Elemente der [**TextRenderingHint**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint) -Enumeration, die in "gdiplusenums. h" deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="83403-109">The **Graphics::SetTextRenderingHint** method receives one of the elements of the [**TextRenderingHint**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint) enumeration, which is declared in Gdiplusenums.h.</span></span>

<span data-ttu-id="83403-110">GDI+ bietet herkömmliches Antialiasing und eine neue Art von Antialiasing auf der Grundlage von Microsoft ClearType-Anzeige Technologie, die nur unter Windows XP und Windows Server 2003 und höheren Versionen von Windows verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="83403-110">GDI+ provides traditional antialiasing and a new kind of antialiasing based on Microsoft ClearType display technology only available on Windows XP and Windows Server 2003 and later versions of Windows.</span></span> <span data-ttu-id="83403-111">ClearType Glättung verbessert die Lesbarkeit von Farb-LCD-Monitoren, die über eine digitale Schnittstelle verfügen, z. b. die Monitore in Laptops und hochwertige flatdesktopdisplays.</span><span class="sxs-lookup"><span data-stu-id="83403-111">ClearType smoothing improves readability on color LCD monitors that have a digital interface, such as the monitors in laptops and high-quality flat desktop displays.</span></span> <span data-ttu-id="83403-112">Die Lesbarkeit von CRT-Bildschirmen wird ebenfalls verbessert.</span><span class="sxs-lookup"><span data-stu-id="83403-112">Readability on CRT screens is also somewhat improved.</span></span>

<span data-ttu-id="83403-113">ClearType ist von der Ausrichtung und Reihenfolge der LCD-Streifen abhängig.</span><span class="sxs-lookup"><span data-stu-id="83403-113">ClearType is dependent on the orientation and ordering of the LCD stripes.</span></span> <span data-ttu-id="83403-114">ClearType wird zurzeit nur für vertikale Streifen implementiert, die mit einer beliebigen Bestellung geordnet sind.</span><span class="sxs-lookup"><span data-stu-id="83403-114">Currently, ClearType is implemented only for vertical stripes that are ordered RGB.</span></span> <span data-ttu-id="83403-115">Dies kann ein Problem sein, wenn Sie einen Tablet PC verwenden, bei dem die Anzeige in beliebiger Richtung ausgerichtet werden kann, oder wenn Sie einen Bildschirm verwenden, der von Querformat zu Hochformat geschaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="83403-115">This might be a concern if you are using a tablet PC, where the display can be oriented in any direction, or if you are using a screen that can be turned from landscape to portrait.</span></span>

<span data-ttu-id="83403-116">Im folgenden Beispiel wird Text mit zwei verschiedenen Qualitätseinstellungen gezeichnet:</span><span class="sxs-lookup"><span data-stu-id="83403-116">The following example draws text with two different quality settings:</span></span>


```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 32, FontStyleRegular, UnitPixel);
SolidBrush  solidBrush(Color(255, 0, 0, 255));
WCHAR       string1[] = L"SingleBitPerPixel";
WCHAR       string2[] = L"AntiAlias";

graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);
graphics.DrawString(string1, -1, &font, PointF(10.0f, 10.0f), &solidBrush);

graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
graphics.DrawString(string2, -1, &font, PointF(10.0f, 60.0f), &solidBrush);
            
```



<span data-ttu-id="83403-117">Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes.</span><span class="sxs-lookup"><span data-stu-id="83403-117">The following illustration shows the output of the preceding code.</span></span>

![Screenshot einer Zeichenfolge, deren Zeichen verzweigte Ränder aufweisen, mit einem mit glatten Kanten](images/fontstext10.png)

 

 



