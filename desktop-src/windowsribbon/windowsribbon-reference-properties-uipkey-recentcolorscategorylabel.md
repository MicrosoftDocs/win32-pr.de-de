---
title: UI_PKEY_RecentColorsCategoryLabel
description: Identifiziert die \_ PKEY \_ RecentColorsCategoryLabel-Eigenschaft der Benutzeroberfläche.
ms.assetid: e9336b98-59ae-4118-8535-009fc0fda4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f3a7a513afb50f01ee3a03c3a3240a2eae7a6ed7b6b8228c4a49e7343e052e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118031474"
---
# <a name="ui_pkey_recentcolorscategorylabel"></a>UI \_ PKEY \_ RecentColorsCategoryLabel

Identifiziert die \_ PKEY \_ RecentColorsCategoryLabel-Eigenschaft der Benutzeroberfläche.

```
propertyDescription
   name = UI_PKEY_RecentColorsCategoryLabel
   shellPKey = UI_PKEY_RecentColorsCategoryLabel
   formatID = 00000405-7363-696e-8441798acf5aebb7
   propID = 405
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Hinweise

Ui \_ PKEY RecentColorsCategoryLabel wird von einer Anwendung verwendet, um den Wert der Bezeichnung abfragt, die der Kategorie Zuletzt verwendete Farben eines \_ [**DropDownColorPicker zugeordnet ist.**](windowsribbon-element-dropdowncolorpicker.md) 

Ui \_ PKEY \_ RecentColorsCategoryLabel ist nur für [**dropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) gültig, wobei als Wert des `ThemeColors` **ColorTemplate-Attributs** angegeben wird (dies ist die einzige Vorlage, die bezeichnete Kategorien enthält).

Der folgende Screenshot zeigt ein `ThemeColors` [**DropDownColorPicker-Steuerelement.**](windowsribbon-element-dropdowncolorpicker.md)

![Screenshot des Dropdowncolorpicker-Elements, bei dem das colortemplate-Attribut auf themecolors festgelegt ist.](images/markup/colortemplate.themedcolors.recentcolors.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Farbwähler Eigenschaften](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




