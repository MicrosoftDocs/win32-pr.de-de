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
# <a name="systemedgegesturedisabletouchwhenfullscreen"></a>System. edgegesture. disabletouchvon Fullscreen

Verhindert das Verhalten von Rand Gesten, wenn ein Anwendungsfenster aktiv ist und sich im Vollbildmodus befindet (oder wenn ein eigenes Fenster aktiv ist).

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

## <a name="remarks"></a>Bemerkungen

In Windows 8 zeigen Benutzerinteraktionen mit den Rändern des Bildschirms die Systembenutzer Oberfläche an, z. b. app-leisten, Charms und ausgestellte apps.

Für voll Bild-Remote Anwendungen kann dieses Verhalten der Benutzeroberfläche auf dem lokalen Computer die Benutzeroberfläche der Remote Sitzung überschreiben und stören. Diese Eigenschaft ermöglicht es einer Anwendung, die Edge-Benutzeroberfläche auf dem lokalen Computer zu deaktivieren.

Zum Deaktivieren der Edge-Benutzeroberfläche legen Sie diese Eigenschaft auf Variant \_ true fest. Der Standardwert ist Variant \_ false.

Diese Eigenschaft hat keine Auswirkung auf Windows Store-Apps.

Im folgenden Beispiel wird gezeigt, wie Sie das Verhalten der Benutzeroberfläche von Edge festlegen


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

[propertydescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[SearchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[TypeInfo](./propdesc-schema-typeinfo.md)
</dt> </dl>

 

 
