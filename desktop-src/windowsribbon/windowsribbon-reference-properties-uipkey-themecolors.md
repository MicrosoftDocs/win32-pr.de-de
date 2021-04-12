---
title: UI_PKEY_ThemeColors
description: Gibt die Benutzeroberflächen- \_ pkey- \_ Eigenschaft "mecolors" an.
ms.assetid: d539cbaa-45dc-4f9e-830e-e81fb289b4ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5991ce5058de5a6f49ca8929de02e19657a610
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315357"
---
# <a name="ui_pkey_themecolors"></a>UI- \_ pkey-Elemente \_

Gibt die Benutzeroberflächen- \_ pkey- \_ Eigenschaft "mecolors" an.

```
propertyDescription
   name = UI_PKEY_ThemeColors
   shellPKey = UI_PKEY_ThemeColors
   formatID = 00000409-7363-696e-8441798acf5aebb7
   propID = 409
   typeInfo
      type = VT_VECTOR | VT_UI4
```

## <a name="remarks"></a>Bemerkungen

Die Benutzeroberflächen- \_ pkey-Datei \_ wird von einer Anwendung verwendet, um die Farbmuster Werte von [**dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md)abzufragen.

Jeder [COLORREF](../gdi/colorref.md) -Wert entspricht einem Farbmuster in einer [**dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md) , wobei `ThemeColors` als Wert des **colortemplate** -Attributs angegeben wird.

Der Eigenschafts Wert ist ein Array von [COLORREF](../gdi/colorref.md) -Werten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Farbauswahl Eigenschaften](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 