---
title: Iagentex showdefaultcharacters-Eigenschaften
description: Iagentex showdefaultcharacters-Eigenschaften
ms.assetid: 4817b52a-7168-4008-9cda-0b8d598daea0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65436135d9763f1cb75db6fb92b9e5f0672e17a8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473060"
---
# <a name="iagentexshowdefaultcharacterproperties"></a><span data-ttu-id="2322b-103">Iagentex:: showdefaultcharacters-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2322b-103">IAgentEx::ShowDefaultCharacterProperties</span></span>

<span data-ttu-id="2322b-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="2322b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ShowDefaultCharacterProperties(
   short x,          // x-coordinate of window
   short y,          // y-coordinate of window
   long bUseDefault  // default position flag
);
```

<span data-ttu-id="2322b-105">Zeigt das Standard Zeichen Eigenschaften Fenster an.</span><span class="sxs-lookup"><span data-stu-id="2322b-105">Displays default character properties window.</span></span>

-   <span data-ttu-id="2322b-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="2322b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="2322b-107"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="2322b-107"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="2322b-108">Die x-Koordinate des Fensters in Pixel relativ zum Bildschirm Ursprung (oben links).</span><span class="sxs-lookup"><span data-stu-id="2322b-108">The x-coordinate of the window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="2322b-109"><span id="y"></span><span id="Y"></span>*Teenie*</span><span class="sxs-lookup"><span data-stu-id="2322b-109"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="2322b-110">Die y-Koordinate des Fensters in Pixel relativ zum Bildschirm Ursprung (oben links).</span><span class="sxs-lookup"><span data-stu-id="2322b-110">The y-coordinate of the window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="2322b-111"><span id="bUseDefault"></span><span id="busedefault"></span><span id="BUSEDEFAULT"></span>*busekunden default*</span><span class="sxs-lookup"><span data-stu-id="2322b-111"><span id="bUseDefault"></span><span id="busedefault"></span><span id="BUSEDEFAULT"></span>*bUseDefault*</span></span>
</dt> <dd>

<span data-ttu-id="2322b-112">Standardpositionsflag.</span><span class="sxs-lookup"><span data-stu-id="2322b-112">Default position flag.</span></span> <span data-ttu-id="2322b-113">Wenn dieser Parameter **true** ist, zeigt der Microsoft-Agent das Eigenschaften Blatt Fenster für das Standard Zeichen an der letzten Position an, an der es aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="2322b-113">If this parameter is **True**, Microsoft Agent displays the property sheet window for the default character at the last location it appeared.</span></span>

> [!Note]  
> <span data-ttu-id="2322b-114">Für Windows 2000 ist es möglicherweise erforderlich, die neue [**allowsetforegroundwindow**](/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow) -API aufzurufen, um sicherzustellen, dass dieses Fenster zum Vordergrund Fenster wird.</span><span class="sxs-lookup"><span data-stu-id="2322b-114">For Windows 2000, it may be necessary to call the new [**AllowSetForegroundWindow**](/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow) API to ensure that this window becomes the foreground window.</span></span> <span data-ttu-id="2322b-115">Weitere Informationen zum Festlegen des Vordergrund Fensters unter Windows 2000 finden Sie in der Platform SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="2322b-115">For more information about setting the foreground window under Windows 2000, see the Platform SDK documentation.</span></span>

 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="2322b-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2322b-116">See Also</span></span>

[<span data-ttu-id="2322b-117">**Iagentnotifysinkex::D efaultcharacters-Änderung**</span><span class="sxs-lookup"><span data-stu-id="2322b-117">**IAgentNotifySinkEx::DefaultCharacterChange**</span></span>](iagentnotifysinkex--defaultcharacterchange.md)


 

 