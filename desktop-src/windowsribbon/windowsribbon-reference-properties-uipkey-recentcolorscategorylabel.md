---
title: UI_PKEY_RecentColorsCategoryLabel
description: Bezeichnet die Benutzeroberflächen- \_ pkey- \_ Eigenschaft "recentcolorscategorylabel".
ms.assetid: e9336b98-59ae-4118-8535-009fc0fda4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bcb2e3f5df1ba66204a8df6b088ca3a2808ced
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712030"
---
# <a name="ui_pkey_recentcolorscategorylabel"></a>UI \_ pkey \_ recentcolorscategorylabel

Bezeichnet die Benutzeroberflächen- \_ pkey- \_ Eigenschaft "recentcolorscategorylabel".

```
propertyDescription
   name = UI_PKEY_RecentColorsCategoryLabel
   shellPKey = UI_PKEY_RecentColorsCategoryLabel
   formatID = 00000405-7363-696e-8441798acf5aebb7
   propID = 405
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Bemerkungen

UI \_ pkey \_ recentcolorscategorylabel wird von einer Anwendung verwendet, um den Wert der Bezeichnung abzufragen, die der Kategorie **zuletzt verwendete Farben** von [**dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md)zugeordnet ist.

Die UI \_ pkey \_ recentcolorscategorylabel ist nur für eine [**dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md) gültig, bei der `ThemeColors` als Wert des **colortemplate** -Attributs angegeben ist (Dies ist die einzige Vorlage, die bezeichnete Kategorien enthält).

Der folgende Screenshot zeigt eine `ThemeColors`  [**dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md).

![Screenshot des dropdowncolorpicker-Elements, bei dem das colortemplate-Attribut auf "mecolors" festgelegt ist.](images/markup/colortemplate.themedcolors.recentcolors.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Farbauswahl Eigenschaften](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




