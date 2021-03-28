---
description: In diesem Thema werden die DrawString-Methoden der Grafikklasse aufgelistet. Eine umfassende Liste der Methoden für die Grafikklasse finden Sie unter Grafiken.
ms.assetid: b3568ed9-e359-4916-a83d-7553c021d197
title: Graphics. DrawString-Methoden (gdiplegraphics. h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 275c256ec2c7284401d37794bccf368538cbdd80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982996"
---
# <a name="graphicsdrawstring-methods"></a><span data-ttu-id="4f129-104">Graphics. DrawString-Methoden</span><span class="sxs-lookup"><span data-stu-id="4f129-104">Graphics.DrawString methods</span></span>

<span data-ttu-id="4f129-105">In diesem Thema werden die DrawString-Methoden der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4f129-105">This topic lists the DrawString methods of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="4f129-106">Eine umfassende Liste der Methoden für die **Grafik** Klasse finden Sie unter [**Grafiken**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).</span><span class="sxs-lookup"><span data-stu-id="4f129-106">For a complete list of methods for the **Graphics** class, see [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).</span></span>

### <a name="overload-list"></a><span data-ttu-id="4f129-107">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="4f129-107">Overload list</span></span>



| <span data-ttu-id="4f129-108">Methode</span><span class="sxs-lookup"><span data-stu-id="4f129-108">Method</span></span>                                                                                                                                                       | <span data-ttu-id="4f129-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f129-109">Description</span></span>                                                                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f129-110">[**DrawString (WChar \* , int, Font \* , PointF&, Brush \* )**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))</span><span class="sxs-lookup"><span data-stu-id="4f129-110">[**DrawString(WCHAR\*,INT,Font\*,PointF&,Brush\*)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))</span></span>                                | <span data-ttu-id="4f129-111">Die [**Grafik::D rawstring**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) -Methode zeichnet eine Zeichenfolge basierend auf einer Schriftart und einem Ursprung für die Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="4f129-111">The [**Graphics::DrawString**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method draws a string based on a font and an origin for the string.</span></span><br/>                        |
| <span data-ttu-id="4f129-112">[**DrawString (WChar \* , int, Font \* , RectF&, StringFormat \* , Brush \* )**](/previous-versions//ms535991(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4f129-112">[**DrawString(WCHAR\*,INT,Font\*,RectF&,StringFormat\*,Brush\*)**](/previous-versions//ms535991(v=vs.85))</span></span> | <span data-ttu-id="4f129-113">Die [**Grafik::D rawstring**](/previous-versions//ms535991(v=vs.85)) -Methode zeichnet eine Zeichenfolge auf Grundlage einer Schriftart, eines layoutrerechtecks und eines Formats.</span><span class="sxs-lookup"><span data-stu-id="4f129-113">The [**Graphics::DrawString**](/previous-versions//ms535991(v=vs.85)) method draws a string based on a font, a layout rectangle, and a format.</span></span> <br/> |
| <span data-ttu-id="4f129-114">[**DrawString (WChar \* , int, Font \* , PointF&, StringFormat \* , Brush \* )**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush))</span><span class="sxs-lookup"><span data-stu-id="4f129-114">[**DrawString(WCHAR\*,INT,Font\*,PointF&,StringFormat\*,Brush\*)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush))</span></span>    | <span data-ttu-id="4f129-115">Die [**Grafik::D rawstring**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) -Methode zeichnet eine Zeichenfolge auf Grundlage einer Schriftart, eines Zeichen folgen Ursprungs und eines Formats.</span><span class="sxs-lookup"><span data-stu-id="4f129-115">The [**Graphics::DrawString**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method draws a string based on a font, a string origin, and a format.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="4f129-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="4f129-116">Requirements</span></span>



| <span data-ttu-id="4f129-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f129-117">Requirement</span></span> | <span data-ttu-id="4f129-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4f129-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f129-119">Header</span><span class="sxs-lookup"><span data-stu-id="4f129-119">Header</span></span><br/> | <dl> <span data-ttu-id="4f129-120"><dt>Gdipl-Grafik. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f129-120"><dt>Gdiplusgraphics.h</dt></span></span> </dl> |



 

 
