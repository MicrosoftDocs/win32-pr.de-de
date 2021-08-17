---
title: UI_PKEY_FontProperties_Underline
description: Identifiziert die \_ PKEY \_ FontProperties \_ Underline-Eigenschaft der Benutzeroberfläche.
ms.assetid: 88492558-ab19-4606-8fe0-5f100677b88a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b75142e08549c2084ebcd37e82943ed63fdfb5b278faef01c4ad79441fa36915
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706720"
---
# <a name="ui_pkey_fontproperties_underline"></a>UI \_ PKEY \_ FontProperties \_ Underline

Identifiziert die \_ PKEY \_ FontProperties \_ Underline-Eigenschaft der Benutzeroberfläche.

```
propertyDescription
   name = UI_PKEY_FontProperties_Underline
   shellPKey = UI_PKEY_FontProperties_Underline
   formatID = 00000305-7363-696e-8441798acf5aebb7
   propID = 305
   typeInfo
      type = UI_FONTUNDERLINE
```

## <a name="remarks"></a>Hinweise

PKEY FontProperties Underline auf der Benutzeroberfläche wird von einer Anwendung verwendet, um den Zustand \_ \_ der Schaltfläche \_ **Unterstrichen** abfragt.

Der -Eigenschaftswert ist aus der [**\_ FONTUNDERLINE-Enumeration der Benutzeroberfläche.**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)

Der Standardwert ist `UI_FONTUNDERLINE_NOTSET`.

Der folgende Screenshot zeigt die Schaltfläche **Unterstrichen** des [**FontControl-Menübands.**](windowsribbon-element-fontcontrol.md)

![Screenshot des fontcontrol-Elements mit dem richfont-Attribut, das auf TRUE festgelegt ist.](images/markup/fontcontrol-underline.png)

In der folgenden Tabelle werden die Eigenschaften und das Ergebnis der Benutzeroberfläche beschrieben.



|      Eigenschaft                   |       Ergebnis der Benutzeroberfläche                                                          |
|---------------------------------|--------------------------------------------------------------------------|
| `UI_FONTUNDERLINE_NOTAVAILABLE` | **Die** Schaltfläche "Unterstrichen" ist deaktiviert und kann nur von der Anwendung festgelegt werden. |
| `UI_FONTUNDERLINE_NOTSET`       | **Die Schaltfläche** "Unterstrichen" ist nicht ausgewählt.                                    |
| `UI_FONTUNDERLINE_SET`          | **Die Schaltfläche** "Unterstrichen" ist ausgewählt.                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaften des Schriftart-Steuerelements](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**\_BENUTZEROBERFLÄCHENSCHRIFTARTUNDERLINE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)
</dt> <dt>

[Schriftart-Steuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 