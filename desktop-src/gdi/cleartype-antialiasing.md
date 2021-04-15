---
description: Das Microsoft ClearType-Antialiasing ist eine Glättungs Methode, die die Auflösung der Schriftart Anzeige gegenüber herkömmlichem Antialiasing verbessert.
ms.assetid: b9896934-1e4f-4ae1-922a-ef30e0edf94f
title: ClearType-Antialiasing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffbe7ae1a6c99fcee826c576b7671aea6e9ce6c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978776"
---
# <a name="cleartype-antialiasing"></a><span data-ttu-id="2d23e-103">ClearType-Antialiasing</span><span class="sxs-lookup"><span data-stu-id="2d23e-103">ClearType Antialiasing</span></span>

<span data-ttu-id="2d23e-104">Das Microsoft ClearType-Antialiasing ist eine Glättungs Methode, die die Auflösung der Schriftart Anzeige gegenüber herkömmlichem Antialiasing verbessert.</span><span class="sxs-lookup"><span data-stu-id="2d23e-104">Microsoft ClearType antialiasing is a smoothing method that improves font display resolution over traditional antialiasing.</span></span> <span data-ttu-id="2d23e-105">Dadurch wird die Lesbarkeit von Farb-LCD-Monitoren mit einer digitalen Oberfläche, wie z. b. den Laptops und hochwertigen flatdesktopdarstellungen, deutlich verbessert.</span><span class="sxs-lookup"><span data-stu-id="2d23e-105">It dramatically improves readability on color LCD monitors with a digital interface, such as those in laptops and high-quality flat desktop displays.</span></span> <span data-ttu-id="2d23e-106">Die Lesbarkeit von CRT-Bildschirmen wird ebenfalls verbessert.</span><span class="sxs-lookup"><span data-stu-id="2d23e-106">Readability on CRT screens is also somewhat improved.</span></span>

<span data-ttu-id="2d23e-107">ClearType ist jedoch von der Ausrichtung und Reihenfolge der LCD-Streifen abhängig.</span><span class="sxs-lookup"><span data-stu-id="2d23e-107">However, ClearType is dependent on the orientation and ordering of the LCD stripes.</span></span> <span data-ttu-id="2d23e-108">ClearType wird zurzeit nur für LCDs mit vertikalen Streifen implementiert, die in der RGB-Form angeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2d23e-108">Currently, ClearType is implemented only for LCDs with vertical stripes that are ordered RGB.</span></span> <span data-ttu-id="2d23e-109">Dies betrifft insbesondere Tablet PCs, bei denen die Anzeige in beliebiger Richtung ausgerichtet werden kann, und die Bildschirme, die von Landscape zu Hochformat geschaltet werden können.</span><span class="sxs-lookup"><span data-stu-id="2d23e-109">In particular, this affects tablet PCs, where the display can be oriented in any direction, and those screens that can be turned from landscape to portrait.</span></span>

<span data-ttu-id="2d23e-110">ClearType-Antialiasing ist zulässig:</span><span class="sxs-lookup"><span data-stu-id="2d23e-110">ClearType antialiasing is allowed:</span></span>

-   <span data-ttu-id="2d23e-111">Für 16-, 24-und 32-Bit-Farbe (deaktiviert für 256 Farben oder weniger)</span><span class="sxs-lookup"><span data-stu-id="2d23e-111">For 16-, 24-, and 32-bit color (disabled for 256 colors or less)</span></span>
-   <span data-ttu-id="2d23e-112">Für den Bildschirm-DC und den Speichercontroller (nicht für den Drucker-DC)</span><span class="sxs-lookup"><span data-stu-id="2d23e-112">For screen DC and memory DC (not for printer DC)</span></span>
-   <span data-ttu-id="2d23e-113">Für TrueType-Schriftarten und OpenType-Schriftarten mit TrueType-Gliederungen</span><span class="sxs-lookup"><span data-stu-id="2d23e-113">For TrueType fonts and OpenType fonts with TrueType outlines</span></span>

<span data-ttu-id="2d23e-114">ClearType-Antialiasing ist deaktiviert:</span><span class="sxs-lookup"><span data-stu-id="2d23e-114">ClearType antialiasing is disabled:</span></span>

-   <span data-ttu-id="2d23e-115">Unter Terminal Server Client</span><span class="sxs-lookup"><span data-stu-id="2d23e-115">Under terminal server client</span></span>
-   <span data-ttu-id="2d23e-116">Für Bitmap-Schriftarten, Vektor Schriftarten, Geräte Schriftarten, Type 1-Schriftarten oder PostScript OpenType-Schriftarten ohne TrueType-Gliederungen</span><span class="sxs-lookup"><span data-stu-id="2d23e-116">For bitmap fonts, vector fonts, device fonts, Type 1 fonts, or Postscript OpenType fonts without TrueType outlines</span></span>
-   <span data-ttu-id="2d23e-117">Wenn die Schriftart eingebettete Bitmaps optimiert hat, nur für die Schrift Grade, die eingebettete Bitmaps enthalten.</span><span class="sxs-lookup"><span data-stu-id="2d23e-117">If the font has tuned embedded bitmaps, only for those font sizes that contain the embedded bitmaps</span></span>

<span data-ttu-id="2d23e-118">Um das ClearType-Antialiasing zu aktivieren, müssen Sie [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) einmal aufrufen, um die Schriftart Glättung zu aktivieren, und dann ein zweites Mal, um den Glättungstyp auf FE \_ fonungmuothingcleartype festzulegen, wie im folgenden Codebeispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="2d23e-118">To activate ClearType antialiasing, call [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) once to turn on font smoothing and then a second time to set the smoothing type to FE\_FONTSMOOTHINGCLEARTYPE, as shown in the following code sample:</span></span>


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHING,
                     TRUE,
                     0,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE);
SystemParametersInfo(SPI_SETFONTSMOOTHINGTYPE,
                     0,
                     (PVOID)FE_FONTSMOOTHINGCLEARTYPE,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



<span data-ttu-id="2d23e-119">Sie können die Darstellung von Text anpassen, indem Sie den im ClearType-Algorithmus verwendeten Kontrastwert ändern.</span><span class="sxs-lookup"><span data-stu-id="2d23e-119">You can adjust the appearance of text by changing the contrast value used in the ClearType algorithm.</span></span> <span data-ttu-id="2d23e-120">Der Standardwert ist 1.400, aber es kann sich um einen beliebigen Wert zwischen 1.000 und 2.200 handeln.</span><span class="sxs-lookup"><span data-stu-id="2d23e-120">The default is 1,400, but it can be any value from 1,000 to 2,200.</span></span> <span data-ttu-id="2d23e-121">Abhängig vom Anzeigegerät und der Empfindlichkeit des Benutzers bei Farben kann ein höherer oder niedrigerer Kontrastwert die Lesbarkeit verbessern.</span><span class="sxs-lookup"><span data-stu-id="2d23e-121">Depending on the display device and the user's sensitivity to colors, a higher or lower contrast value may improve readability.</span></span> <span data-ttu-id="2d23e-122">Um den Kontrast zu ändern, wenden Sie [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) mit SPI \_ setfonstistingcontrast an.</span><span class="sxs-lookup"><span data-stu-id="2d23e-122">To change the contrast, call [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) with SPI\_SETFONTSMOOTHINGCONTRAST.</span></span> <span data-ttu-id="2d23e-123">Der folgende Code legt den Kontrastwert auf 1.600 fest.</span><span class="sxs-lookup"><span data-stu-id="2d23e-123">The following code sets the contrast value to 1,600.</span></span>


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHINGCONTRAST,
                     0,
                     (PVOID)1600,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



<span data-ttu-id="2d23e-124">Beachten Sie die folgenden Details zur Anwendungs Kompatibilität:</span><span class="sxs-lookup"><span data-stu-id="2d23e-124">You should consider the following details for application compatibility:</span></span>

-   <span data-ttu-id="2d23e-125">Das Rendern von Text mit ClearType ist etwas langsamer als bei Standard-Antialiasing.</span><span class="sxs-lookup"><span data-stu-id="2d23e-125">Text rendering with ClearType is slightly slower than with standard antialiasing.</span></span>
-   <span data-ttu-id="2d23e-126">Anwendungen sollten nicht XOR zum Anzeigen von ausgewähltem Text verwenden.</span><span class="sxs-lookup"><span data-stu-id="2d23e-126">Applications should not use XOR to display selected text.</span></span> <span data-ttu-id="2d23e-127">Anwendungen sollten die Hintergrundfarbe festlegen und den ausgewählten Text neu anzeigen.</span><span class="sxs-lookup"><span data-stu-id="2d23e-127">Applications should set the background color and redisplay the selected text.</span></span>
-   <span data-ttu-id="2d23e-128">Anwendungen sollten nicht denselben Text im transparenten Modus selbst zeichnen.</span><span class="sxs-lookup"><span data-stu-id="2d23e-128">Applications should not paint the same text on top of itself in transparent mode.</span></span> <span data-ttu-id="2d23e-129">Wenn dies der Fall ist, werden die edgepixel, bei denen ein Antialiasing durchgeführt wird, farblich anstelle der Hintergrundfarbe mit sich selbst zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="2d23e-129">If this occurs, the edge pixels that are antialiased will color merge with themselves instead of with the background color.</span></span> <span data-ttu-id="2d23e-130">Dies führt zu einem dunklen und farbigen Kanten.</span><span class="sxs-lookup"><span data-stu-id="2d23e-130">This results in darkened and colorful edges.</span></span>
-   <span data-ttu-id="2d23e-131">Anwendungen sollten keinen Text zeichnen, indem Sie die Zeichen einzeln zeichnen, wenn Sie sich im nicht transparenten Modus befinden, da der Rand eines Zeichens durch das folgende Zeichen abgeschnitten werden kann.</span><span class="sxs-lookup"><span data-stu-id="2d23e-131">Applications should not paint text by painting the characters individually when in opaque mode because the edge of a character may be clipped by the following character.</span></span> <span data-ttu-id="2d23e-132">Dies liegt daran, dass ein mit ClearType geglättes Zeichen möglicherweise eine negative Breite von a oder c aufweist, wobei das reguläre Zeichen eine positive a-oder c-Breite hat.</span><span class="sxs-lookup"><span data-stu-id="2d23e-132">This occurs because a character that is smoothed with ClearType may have a negative A or C width where the regular character has a positive A or C width.</span></span> <span data-ttu-id="2d23e-133">Nur die B-Breite des Zeichens ist garantiert identisch.</span><span class="sxs-lookup"><span data-stu-id="2d23e-133">Only the B width of the character is guaranteed to be the same.</span></span> <span data-ttu-id="2d23e-134">Ebenso sollten Anwendungen vorsichtig sein, wenn geglättter Text neben nicht gepuffertem Text steht.</span><span class="sxs-lookup"><span data-stu-id="2d23e-134">Likewise, applications should be careful if smoothed text is next to unsmoothed text.</span></span>
-   <span data-ttu-id="2d23e-135">Wenn eine Anwendung Text rendert und dann die Bitmap manipuliert, sollte die Schriftart Glättung deaktiviert werden, indem der **lfquality** -Member der [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur auf die nicht-Antialiasing-Qualität festgelegt wird \_ .</span><span class="sxs-lookup"><span data-stu-id="2d23e-135">If an application renders text and then manipulates the bitmap, font smoothing should be turned off by setting the **lfQuality** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure to NONANTIALIASED\_QUALITY.</span></span> <span data-ttu-id="2d23e-136">Beispielsweise kann ein Spiel einen Bitmap-Schatteneffekt hinzufügen, oder Text, der in eine Bitmap gerendert wird, kann skaliert werden, um eine thumbview zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2d23e-136">For example, a game may add a bitmap shadow effect, or text rendered into a bitmap may be scaled to produce a thumbview.</span></span>
-   <span data-ttu-id="2d23e-137">Wenn der Benutzer im Hochformat ausgeführt wird (d. h., das Monitor-Striping ist horizontal), sollte das ClearType-Antialiasing deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="2d23e-137">If the user is running in portrait mode (that is, monitor striping is horizontal) ClearType antialiasing should be disabled.</span></span>

<span data-ttu-id="2d23e-138">Der *fdwquality* -Parameter in " [**kreatefont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta) " und der **lfquality** -Member von " [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) " akzeptieren das ClearType \_ Quality-Flag.</span><span class="sxs-lookup"><span data-stu-id="2d23e-138">The *fdwQuality* parameter in [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta) and the **lfQuality** member of [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) accept the CLEARTYPE\_QUALITY flag.</span></span> <span data-ttu-id="2d23e-139">Bei der rasterisierung von mit diesem Flag erstellten Schriftarten wird der ClearType-Rasterizer verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d23e-139">Rasterization of fonts created with this flag will use the ClearType rasterizer.</span></span> <span data-ttu-id="2d23e-140">Dieses Flag hat keine Auswirkung auf frühere Versionen des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="2d23e-140">This flag has no effect on previous versions of the operating system.</span></span>

 

 
