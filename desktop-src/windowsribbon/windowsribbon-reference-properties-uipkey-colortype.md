---
title: UI_PKEY_ColorType
description: Identifiziert die \_ PKEY \_ ColorType-Eigenschaft der Benutzeroberfläche.
ms.assetid: 7eaa9d8b-0c21-487c-9093-79ddffcae131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9240d8c816adcf2674efcc2e7428d22b765f542
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443891"
---
# <a name="ui_pkey_colortype"></a>UI \_ PKEY \_ ColorType

Identifiziert die \_ PKEY \_ ColorType-Eigenschaft der Benutzeroberfläche.

```
propertyDescription
   name = UI_PKEY_ColorType
   shellPKey = UI_PKEY_ColorType
   formatID = 00000401-7363-696e-8441798acf5aebb7
   propID = 401
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>Hinweise

Ui \_ PKEY \_ ColorType wird von einer Anwendung zum Abfragen der Farbeinstellung des [**DropDownColorPicker-Steuerelements**](windowsribbon-element-dropdowncolorpicker.md) verwendet.

Der Eigenschaftswert stammt aus der [**\_ SWATCHCOLORTYPE-Enumeration der Benutzeroberfläche.**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)



|    Eigenschaft                            |    BESCHREIBUNG                                                                                                                                                                             |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UI \_ SWATCHCOLORTYPE \_ NOCOLOR   | Die Anwendung sollte die Farbeinstellung als transparent behandeln. Wird in der Regel in Verbindung mit der Einstellung **Keine Farbe** verwendet.                                                   |
| UI \_ SWATCHCOLORTYPE \_ AUTOMATIC | Die Anwendung sollte [GetSysColor(COLOR \_ WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor)abfragen. Wird in der Regel in Verbindung mit der Farbeinstellung **Automatisch** verwendet. |
| UI \_ SWATCHCOLORTYPE \_ RGB       | Die Anwendung sollte [die \_ \_ PKEY-Farbe](windowsribbon-reference-properties-uipkey-color.md) der Benutzeroberfläche für die Farbeinstellung abfragen.                                                          |



 

Ui \_ PKEY \_ ColorType wird an die [**IUICommandHandler::Execute-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) übergeben, wenn eine Farbwatch in einem [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)ausgewählt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Farbwähler-Eigenschaften](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 