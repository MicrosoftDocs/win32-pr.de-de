---
description: Das System stellt sechs Aktien Schriftarten bereit.
ms.assetid: 349ea57f-dd25-4e33-bbdf-63a320eae3a0
title: Verwenden einer Kurs Schriftart zum Zeichnen von Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a7e580175956185bcc26a7ebbae8d46dfff078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960517"
---
# <a name="using-a-stock-font-to-draw-text"></a><span data-ttu-id="6320c-103">Verwenden einer Kurs Schriftart zum Zeichnen von Text</span><span class="sxs-lookup"><span data-stu-id="6320c-103">Using a Stock Font to Draw Text</span></span>

<span data-ttu-id="6320c-104">Das System stellt sechs Aktien Schriftarten bereit.</span><span class="sxs-lookup"><span data-stu-id="6320c-104">The system provides six stock fonts.</span></span> <span data-ttu-id="6320c-105">Eine Aktien Schriftart ist eine logische Schriftart, die eine Anwendung abrufen kann, indem Sie die [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) -Funktion aufrufen und die angeforderte Schriftart angibt.</span><span class="sxs-lookup"><span data-stu-id="6320c-105">A stock font is a logical font that an application can obtain by calling the [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) function and specifying the requested font.</span></span> <span data-ttu-id="6320c-106">Die folgende Liste enthält die Werte, die Sie angeben können, um eine Aktien Schriftart zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6320c-106">The following list contains the values that you can specify to obtain a stock font.</span></span>



| <span data-ttu-id="6320c-107">Wert</span><span class="sxs-lookup"><span data-stu-id="6320c-107">Value</span></span>                 | <span data-ttu-id="6320c-108">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6320c-108">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6320c-109">ANSI \_ - \_ Schriftart</span><span class="sxs-lookup"><span data-stu-id="6320c-109">ANSI\_FIXED\_FONT</span></span>     | <span data-ttu-id="6320c-110">Gibt eine fest breiten-Schriftart an, die auf dem Windows-Zeichensatz basiert.</span><span class="sxs-lookup"><span data-stu-id="6320c-110">Specifies a monospace font based on the Windows character set.</span></span> <span data-ttu-id="6320c-111">In der Regel wird eine Courier Schriftart verwendet.</span><span class="sxs-lookup"><span data-stu-id="6320c-111">A Courier font is typically used.</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="6320c-112">ANSI \_ var- \_ Schriftart</span><span class="sxs-lookup"><span data-stu-id="6320c-112">ANSI\_VAR\_FONT</span></span>       | <span data-ttu-id="6320c-113">Gibt eine proportionale Schriftart basierend auf dem Windows-Zeichensatz an.</span><span class="sxs-lookup"><span data-stu-id="6320c-113">Specifies a proportional font based on the Windows character set.</span></span> <span data-ttu-id="6320c-114">MS Sans Serif wird normalerweise verwendet.</span><span class="sxs-lookup"><span data-stu-id="6320c-114">MS Sans Serif is typically used.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="6320c-115">\_Standard \_ Schriftart des Geräts</span><span class="sxs-lookup"><span data-stu-id="6320c-115">DEVICE\_DEFAULT\_FONT</span></span> | <span data-ttu-id="6320c-116">Gibt die bevorzugte Schriftart für das angegebene Gerät an.</span><span class="sxs-lookup"><span data-stu-id="6320c-116">Specifies the preferred font for the specified device.</span></span> <span data-ttu-id="6320c-117">Dies ist in der Regel die System Schriftart für Anzeigegeräte. bei einigen Punktmatrix Druckern ist dies jedoch eine Schriftart, die sich auf dem Gerät befindet.</span><span class="sxs-lookup"><span data-stu-id="6320c-117">This is typically the System font for display devices; however, for some dot-matrix printers this is a font that is resident on the device.</span></span> <span data-ttu-id="6320c-118">(Das Drucken mit dieser Schriftart ist in der Regel schneller als das Drucken mit einer heruntergeladenen Bitmapschriftart).</span><span class="sxs-lookup"><span data-stu-id="6320c-118">(Printing with this font is usually faster than printing with a downloaded, bitmap font).</span></span>    |
| <span data-ttu-id="6320c-119">\_Schriftart für festes OEM \_</span><span class="sxs-lookup"><span data-stu-id="6320c-119">OEM\_FIXED\_FONT</span></span>      | <span data-ttu-id="6320c-120">Gibt eine fest breiten-Schriftart an, die auf einem OEM-Zeichensatz basiert.</span><span class="sxs-lookup"><span data-stu-id="6320c-120">Specifies a monospace font based on an OEM character set.</span></span> <span data-ttu-id="6320c-121">Bei IBM-Computern und-Kompatibilitäten basiert die OEM-Schriftart auf dem IBM-PC-Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="6320c-121">For IBM computers and compatibles, the OEM font is based on the IBM PC character set.</span></span>                                                                                                                                                 |
| <span data-ttu-id="6320c-122">System \_ Schriftart</span><span class="sxs-lookup"><span data-stu-id="6320c-122">SYSTEM\_FONT</span></span>          | <span data-ttu-id="6320c-123">Gibt die System Schriftart an.</span><span class="sxs-lookup"><span data-stu-id="6320c-123">Specifies the System font.</span></span> <span data-ttu-id="6320c-124">Dabei handelt es sich um eine proportionale Schriftart, die auf dem Windows-Zeichensatz basiert und vom Betriebssystem verwendet wird, um Fenstertitel, Menü Namen und Text in Dialogfeldern anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6320c-124">This is a proportional font based on the Windows character set, and is used by the operating system to display window titles, menu names, and text in dialog boxes.</span></span> <span data-ttu-id="6320c-125">Die System Schriftart ist immer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6320c-125">The System font is always available.</span></span> <span data-ttu-id="6320c-126">Andere Schriftarten sind nur verfügbar, wenn Sie installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="6320c-126">Other fonts are available only if they have been installed.</span></span> |
| <span data-ttu-id="6320c-127">\_Schriftart des fixierten Systems \_</span><span class="sxs-lookup"><span data-stu-id="6320c-127">SYSTEM\_FIXED\_FONT</span></span>   | <span data-ttu-id="6320c-128">Gibt eine fest breiten-Schriftart an, die in frühen Versionen von Windows mit der System Schriftart kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="6320c-128">Specifies a monospace font compatible with the System font in early versions of Windows.</span></span>                                                                                                                                                                                                        |



 

<span data-ttu-id="6320c-129">Weitere Informationen zu Schriftarten finden Sie unter Informationen [zu Schriftarten](about-fonts.md).</span><span class="sxs-lookup"><span data-stu-id="6320c-129">For more information on fonts, see [About Fonts](about-fonts.md).</span></span>

<span data-ttu-id="6320c-130">Im folgenden Beispiel wird ein Handle der Variablen Aktien Schriftart abgerufen, in einen Gerätekontext ausgewählt und dann mithilfe der Schriftart eine Zeichenfolge geschrieben:</span><span class="sxs-lookup"><span data-stu-id="6320c-130">The following example retrieves a handle to the variable stock font, selects it into a device context, and then writes a string using that font:</span></span>


```C++
HFONT hFont, hOldFont; 

// Retrieve a handle to the variable stock font.  
hFont = (HFONT)GetStockObject(ANSI_VAR_FONT); 

// Select the variable stock font into the specified device context. 
if (hOldFont = (HFONT)SelectObject(hdc, hFont)) 
{
    // Display the text string.  
    TextOut(hdc, 10, 50, L"Sample ANSI_VAR_FONT text", 25); 

    // Restore the original font.        
    SelectObject(hdc, hOldFont); 
}
```



<span data-ttu-id="6320c-131">Wenn keine anderen Aktien Schriftarten verfügbar sind, gibt [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) ein Handle für die System Schriftart (System \_ Schriftart) zurück.</span><span class="sxs-lookup"><span data-stu-id="6320c-131">If other stock fonts are not available, [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) returns a handle to the System font (SYSTEM\_FONT).</span></span> <span data-ttu-id="6320c-132">Sie sollten nur dann Stock Fonts verwenden, wenn der Kartenmodus für den Gerätekontext der Anwendung mm- \_ Text ist.</span><span class="sxs-lookup"><span data-stu-id="6320c-132">You should use stock fonts only if the mapping mode for your application's device context is MM\_TEXT.</span></span>

 

 



