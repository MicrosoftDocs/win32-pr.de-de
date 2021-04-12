---
title: UI_PKEY_ColorType
description: Bezeichnet die Benutzeroberflächen- \_ pkey \_ ColorType-Eigenschaft.
ms.assetid: 7eaa9d8b-0c21-487c-9093-79ddffcae131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313d2a657d889a7c582d86d8f8c9e4ebd2cfd01e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315699"
---
# <a name="ui_pkey_colortype"></a>UI \_ pkey \_ ColorType

Bezeichnet die Benutzeroberflächen- \_ pkey \_ ColorType-Eigenschaft.

```
propertyDescription
   name = UI_PKEY_ColorType
   shellPKey = UI_PKEY_ColorType
   formatID = 00000401-7363-696e-8441798acf5aebb7
   propID = 401
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>Bemerkungen

UI \_ pkey \_ ColorType wird von einer Anwendung verwendet, um die Farbeinstellung des [**dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md) -Steuer Elements abzufragen.

Der Eigenschafts Wert ist aus der [**UI- \_ swatchcolortype**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) -Enumeration.



|                                |                                                                                                                                                                                 |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UI \_ swatchcolortype \_ nocolor   | Die Anwendung sollte die Farbeinstellung als transparent behandeln. Wird in der Regel in Verbindung mit der Einstellung " **keine farbfarbe** " verwendet.                                                   |
| UI \_ swatchcolortype \_ automatisch | Die Anwendung sollte [GetSysColor (Color \_ WindowText)](/windows/win32/api/winuser/nf-winuser-getsyscolor)Abfragen. Wird in der Regel in Verbindung mit der **automatischen** Farbeinstellung verwendet. |
| UI- \_ swatchcolortype \_ RGB       | Die Anwendung sollte die Benutzeroberflächen- [ \_ pkey- \_ Farbe](windowsribbon-reference-properties-uipkey-color.md) für die Farbeinstellung Abfragen.                                                          |



 

\_Der UI pkey \_ ColorType wird an die [**iuicommandhandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) -Rückruf Methode übergeben, wenn in einem [**dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md)ein Farbmuster ausgewählt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Farbauswahl Eigenschaften](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 