---
description: Die Farbfunktionen von Geräten, wie z. b. anzeigen und Druckern, können zwischen Monochrom und Tausenden von Farben reichen.
ms.assetid: 3d71c24c-77f4-4344-91c3-439052402fae
title: Farbgrundlagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 992953bef75b2bab1f33dbd044a9c80387b5ccd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215211"
---
# <a name="color-basics"></a><span data-ttu-id="fda25-103">Farbgrundlagen</span><span class="sxs-lookup"><span data-stu-id="fda25-103">Color Basics</span></span>

<span data-ttu-id="fda25-104">Die Farbfunktionen von Geräten, wie z. b. anzeigen und Druckern, können zwischen Monochrom und Tausenden von Farben reichen.</span><span class="sxs-lookup"><span data-stu-id="fda25-104">The color capabilities of devices, such as displays and printers, can range from monochrome to thousands of colors.</span></span> <span data-ttu-id="fda25-105">Da eine Anwendung möglicherweise in diesem Bereich eine Ausgabe für Geräte generieren muss, sollte Sie darauf vorbereitet sein, unterschiedliche Farbfunktionen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="fda25-105">Because an application may need to generate output for devices throughout this range, it should be prepared to handle varying color capabilities.</span></span>

<span data-ttu-id="fda25-106">Eine Anwendung kann die Anzahl der für ein bestimmtes Gerät verfügbaren Farben ermitteln, indem Sie die [**gettovicecaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) -Funktion zum Abrufen des numcolors-Werts verwendet.</span><span class="sxs-lookup"><span data-stu-id="fda25-106">An application can discover the number of colors available for a given device by using the [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function to retrieve the NUMCOLORS value.</span></span> <span data-ttu-id="fda25-107">Dieser Wert gibt die Anzahl der Farben an, die für die Verwendung durch die Anwendung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="fda25-107">This value specifies the count of colors available for use by the application.</span></span> <span data-ttu-id="fda25-108">In der Regel entspricht diese Anzahl einer physischen Eigenschaft des Ausgabegeräts, z. b. der Anzahl der Farben im Drucker oder der Anzahl der unterschiedlichen Farbsignale, die der Anzeige Adapter an den Monitor übertragen kann.</span><span class="sxs-lookup"><span data-stu-id="fda25-108">Usually, this count corresponds to a physical property of the output device, such as the number of inks in the printer or the number of distinct color signals the display adapter can transmit to the monitor.</span></span>

<span data-ttu-id="fda25-109">Obwohl der numcolors-Wert die Anzahl von Farben angibt, identifiziert er nicht die verfügbaren Farben.</span><span class="sxs-lookup"><span data-stu-id="fda25-109">Although the NUMCOLORS value specifies the count of colors, it does not identify what the available colors are.</span></span> <span data-ttu-id="fda25-110">Eine Anwendung kann ermitteln, welche Farben verfügbar sind, indem alle Stifte aufgelistet werden, die den Typ "PS Solid" aufweisen \_ .</span><span class="sxs-lookup"><span data-stu-id="fda25-110">An application can discover what colors are available by enumerating all pens having the PS\_SOLID type.</span></span> <span data-ttu-id="fda25-111">Da der Gerätetreiber, der ein bestimmtes Gerät unterstützt, in der Regel über einen vollständigen Bereich von ausgefülltem Stifte verfügt, und da das System erfordert, dass solide Stifte nur Farben enthalten, die vom Gerät generiert werden können, ist die Enumeration dieser Stifte häufig Äquivalent zum Auflisten der Farben.</span><span class="sxs-lookup"><span data-stu-id="fda25-111">Because the device driver that supports a given device usually has a full range of solid pens and because the system requires that solid pens have only colors that the device can generate, enumerating these pens is often equivalent to enumerating the colors.</span></span> <span data-ttu-id="fda25-112">Eine Anwendung kann die Stifte mithilfe der [**enumubjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) -Funktion auflisten.</span><span class="sxs-lookup"><span data-stu-id="fda25-112">An application can enumerate the pens by using the [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) function.</span></span> <span data-ttu-id="fda25-113">Ein Codebeispiel finden Sie unter Auflisten von [Farben](enumerating-colors.md).</span><span class="sxs-lookup"><span data-stu-id="fda25-113">For a code example, see [Enumerating Colors](enumerating-colors.md).</span></span>

<span data-ttu-id="fda25-114">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="fda25-114">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="fda25-115">Farbwerte</span><span class="sxs-lookup"><span data-stu-id="fda25-115">Color Values</span></span>](color-values.md)
-   [<span data-ttu-id="fda25-116">Farb Näherungen und Dithering</span><span class="sxs-lookup"><span data-stu-id="fda25-116">Color Approximations and Dithering</span></span>](color-approximations-and-dithering.md)
-   [<span data-ttu-id="fda25-117">Farbe in Bitmaps</span><span class="sxs-lookup"><span data-stu-id="fda25-117">Color in Bitmaps</span></span>](color-in-bitmaps.md)
-   [<span data-ttu-id="fda25-118">Farbmischung</span><span class="sxs-lookup"><span data-stu-id="fda25-118">Color Mixing</span></span>](color-mixing.md)

 

 



