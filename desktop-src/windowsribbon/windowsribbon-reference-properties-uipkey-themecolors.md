---
title: UI_PKEY_ThemeColors
description: Identifiziert die \_ PKEY \_ ThemeColors-Eigenschaft der Benutzeroberfläche.
ms.assetid: d539cbaa-45dc-4f9e-830e-e81fb289b4ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab5c4582561e3c86ba19b2821cf600d0a1da614cfc9fc7144b935665c8af7f14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437795"
---
# <a name="ui_pkey_themecolors"></a>UI \_ PKEY \_ ThemeColors

Identifiziert die \_ PKEY \_ ThemeColors-Eigenschaft der Benutzeroberfläche.

```
propertyDescription
   name = UI_PKEY_ThemeColors
   shellPKey = UI_PKEY_ThemeColors
   formatID = 00000409-7363-696e-8441798acf5aebb7
   propID = 409
   typeInfo
      type = VT_VECTOR | VT_UI4
```

## <a name="remarks"></a>Hinweise

Ui \_ PKEY \_ ThemeColors wird von einer Anwendung verwendet, um die Farbwatchwerte eines [**DropDownColorPicker abzufragen.**](windowsribbon-element-dropdowncolorpicker.md)

Jeder [COLORREF-Wert](../gdi/colorref.md) entspricht einem Farbmuster in einem [**DropDownColorPicker,**](windowsribbon-element-dropdowncolorpicker.md) wobei `ThemeColors` als Wert des **ColorTemplate-Attributs** angegeben wird.

Der Eigenschaftswert ist ein Array von [COLORREF-Werten.](../gdi/colorref.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Farbwähler-Eigenschaften](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 