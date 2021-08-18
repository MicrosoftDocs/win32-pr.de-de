---
description: Verhindert Kantengestenverhalten, wenn ein Anwendungsfenster aktiv ist und sich im Vollbildmodus befindet (oder ein eigenes Fenster aktiv ist).
ms.assetid: F4242C05-181B-44FC-BE6C-8ABB76079981
title: System.EdgeGesture.DisableTouchWhenFullscreen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13132ba30fd3f1e594ec54966dfe2268ce66d570b66ca6d34b1c63b03bfc0c75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119845120"
---
# <a name="systemedgegesturedisabletouchwhenfullscreen"></a>System.EdgeGesture.DisableTouchWhenFullscreen

Verhindert Kantengestenverhalten, wenn ein Anwendungsfenster aktiv ist und sich im Vollbildmodus befindet (oder ein eigenes Fenster aktiv ist).

> [!Note]  
> Im Vollbildmodus entspricht die Größe des Anwendungsfensters der Bildschirmauflösung.

 

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a>Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8

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

## <a name="remarks"></a>Hinweise

In Windows 8 Benutzerinteraktionen mit den Rändern der Systembenutzeroberfläche der Bildschirmanzeige, z. B. App-Balken, Charms und ausgeführte Apps.

Bei Remoteanwendungen im Vollbildmodus kann dieses Benutzeroberflächenverhalten auf dem lokalen Computer die Benutzeroberfläche der Remotesitzung überschreiben und beeinträchtigen. Mit dieser Eigenschaft kann eine Anwendung die Edgebenutzeroberfläche auf dem lokalen Computer deaktivieren.

Um die Edgebenutzeroberfläche zu deaktivieren, legen Sie diese Eigenschaft auf VARIANT \_ TRUE fest. Der Standardwert ist VARIANT \_ FALSE.

Diese Eigenschaft hat keine Auswirkungen auf Windows Store Apps.

Das folgende Beispiel zeigt, wie Sie Verhalten der Edgebenutzeroberfläche festlegen.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[Typeinfo](./propdesc-schema-typeinfo.md)
</dt> </dl>

 

 
