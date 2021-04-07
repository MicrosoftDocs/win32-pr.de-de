---
title: UI_PKEY_StandardColorsCategoryLabel
description: Identifiziert die Benutzeroberflächen- \_ pkey \_ standardcolorscategorylabel-Eigenschaft.
ms.assetid: 59452d4b-acc9-4a5f-a06c-a67b0e676a57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcaecc19213ab82ebafaa76dc2e88a0db836a97a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712024"
---
# <a name="ui_pkey_standardcolorscategorylabel"></a>UI \_ pkey \_ standardcolorscategorylabel

Identifiziert die Benutzeroberflächen- \_ pkey \_ standardcolorscategorylabel-Eigenschaft.

```
propertyDescription
   name = UI_PKEY_StandardColorsCategoryLabel
   shellPKey = UI_PKEY_StandardColorsCategoryLabel
   formatID = 00000404-7363-696e-8441798acf5aebb7
   propID = 404
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Bemerkungen

UI \_ pkey \_ standardcolorscategorylabel wird von einer Anwendung verwendet, um den Wert der Bezeichnung abzufragen, die mit der Kategorie **Standard Farben** von [**dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md)verknüpft ist.

Der Benutzeroberflächen- \_ pkey \_ standardcolorscategorylabel ist nur für eine [**dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md) gültig, bei der `ThemeColors` als Wert des **colortemplate** -Attributs angegeben ist (Dies ist die einzige Vorlage, die bezeichnete Kategorien enthält).

Der folgende Screenshot zeigt eine `ThemeColors`  [**dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md).

![Screenshot des dropdowncolorpicker-Elements, bei dem das colortemplate-Attribut auf "mecolors" festgelegt ist.](images/markup/colortemplate.themedcolors.1.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Farbauswahl Eigenschaften](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




