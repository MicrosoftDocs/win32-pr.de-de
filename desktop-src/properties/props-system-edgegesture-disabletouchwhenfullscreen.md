---
description: Verhindert das Verhalten von Rand Gesten, wenn ein Anwendungsfenster aktiv ist und sich im Vollbildmodus befindet (oder wenn ein eigenes Fenster aktiv ist).
ms.assetid: F4242C05-181B-44FC-BE6C-8ABB76079981
title: System. edgegesture. disabletouchvon Fullscreen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 208962f11b96420a8e0ef771ada846a3f802e815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352540"
---
# <a name="systemedgegesturedisabletouchwhenfullscreen"></a><span data-ttu-id="e0ccb-103">System. edgegesture. disabletouchvon Fullscreen</span><span class="sxs-lookup"><span data-stu-id="e0ccb-103">System.EdgeGesture.DisableTouchWhenFullscreen</span></span>

<span data-ttu-id="e0ccb-104">Verhindert das Verhalten von Rand Gesten, wenn ein Anwendungsfenster aktiv ist und sich im Vollbildmodus befindet (oder wenn ein eigenes Fenster aktiv ist).</span><span class="sxs-lookup"><span data-stu-id="e0ccb-104">Prevents edge gesture behaviors when an application window is active and in full-screen mode (or an owned window is active).</span></span>

> [!Note]  
> <span data-ttu-id="e0ccb-105">Im Vollbildmodus entspricht die Größe des Anwendungsfensters der Bildschirmauflösung.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-105">In full-screen mode, the size of the application window matches the screen resolution.</span></span>

 

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="e0ccb-106">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="e0ccb-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.EdgeGesture.DisableTouchWhenFullscreen
   shellPKey = PKEY_EdgeGesture_DisableTouchWhenFullscreen
   formatID = 32CE38B2-2C9A-41B1-9BC5-B3784394AA44
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a><span data-ttu-id="e0ccb-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0ccb-107">Remarks</span></span>

<span data-ttu-id="e0ccb-108">In Windows 8 zeigen Benutzerinteraktionen mit den Rändern des Bildschirms die Systembenutzer Oberfläche an, z. b. app-leisten, Charms und ausgestellte apps.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-108">In Windows 8, user interactions with the edges of the screen display system UI such as app bars, charms, and running apps.</span></span>

<span data-ttu-id="e0ccb-109">Für voll Bild-Remote Anwendungen kann dieses Verhalten der Benutzeroberfläche auf dem lokalen Computer die Benutzeroberfläche der Remote Sitzung überschreiben und stören.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-109">For full-screen, remote applications, this UI behavior on the local machine might override and interfere with the UI of the remote session.</span></span> <span data-ttu-id="e0ccb-110">Diese Eigenschaft ermöglicht es einer Anwendung, die Edge-Benutzeroberfläche auf dem lokalen Computer zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-110">This property enables an application to disable the edge UI on the local machine.</span></span>

<span data-ttu-id="e0ccb-111">Zum Deaktivieren der Edge-Benutzeroberfläche legen Sie diese Eigenschaft auf Variant \_ true fest.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-111">To disable edge UI, set this property to VARIANT\_TRUE.</span></span> <span data-ttu-id="e0ccb-112">Der Standardwert ist Variant \_ false.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-112">The default value is VARIANT\_FALSE.</span></span>

<span data-ttu-id="e0ccb-113">Diese Eigenschaft hat keine Auswirkung auf Windows Store-Apps.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-113">This property has no effect on Windows Store apps.</span></span>

<span data-ttu-id="e0ccb-114">Im folgenden Beispiel wird gezeigt, wie Sie das Verhalten der Benutzeroberfläche von Edge festlegen</span><span class="sxs-lookup"><span data-stu-id="e0ccb-114">The following example shows how to set edge UI behaviors.</span></span>


```
HRESULT SetTouchDisableProperty(HWND hwnd, BOOL fDisableTouch)
{
    IPropertyStore* pPropStore;
    HRESULT hrReturnValue = SHGetPropertyStoreForWindow(hwnd, IID_PPV_ARGS(&pPropStore));
    if (SUCCEEDED(hrReturnValue))
    {
        PROPVARIANT var;
        var.vt = VT_BOOL;
        var.boolVal = fDisableTouch ? VARIANT_TRUE : VARIANT_FALSE;
        hrReturnValue = pPropStore->SetValue(PKEY_EdgeGesture_DisableTouchWhenFullscreen, var);
        pPropStore->Release();
    }
    return hrReturnValue;
}
```



## <a name="related-topics"></a><span data-ttu-id="e0ccb-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e0ccb-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0ccb-116">propertydescription</span><span class="sxs-lookup"><span data-stu-id="e0ccb-116">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="e0ccb-117">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="e0ccb-117">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="e0ccb-118">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="e0ccb-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> </dl>

 

 
