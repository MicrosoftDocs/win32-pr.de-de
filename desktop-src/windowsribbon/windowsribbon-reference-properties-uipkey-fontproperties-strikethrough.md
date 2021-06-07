---
title: UI_PKEY_FontProperties_Strikethrough
description: Identifiziert die \_ PKEY \_ FontProperties \_ Strikethrough-Eigenschaft der Benutzeroberfläche.
ms.assetid: 18ee653d-db01-4615-a85d-ad4ac6a0f422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b684704fdd90a8dd1b88b14db2b52540b15fccb
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443791"
---
# <a name="ui_pkey_fontproperties_strikethrough"></a>UI \_ PKEY \_ FontProperties \_ Strikethrough

Identifiziert die \_ PKEY \_ FontProperties \_ Strikethrough-Eigenschaft der Benutzeroberfläche.

```
propertyDescription
   name = UI_PKEY_FontProperties_Strikethrough
   shellPKey = UI_PKEY_FontProperties_Strikethrough
   formatID = 00000306-7363-696e-8441798acf5aebb7
   propID = 306
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Hinweise

PKEY FontProperties Strikethrough der Benutzeroberfläche wird von einer Anwendung verwendet, um den Zustand der \_ \_ Schaltfläche \_ **Durchgestreichen** abfragt.

Der -Eigenschaftswert ist aus der [**\_ FONTPROPERTIES-Enumeration der Benutzeroberfläche.**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)

Standardwert: `UI_FONTPROPERTIES_NOTSET`.

Der folgende Screenshot zeigt die Schaltfläche **Durchstreichen** des [**FontControl-Menübands.**](windowsribbon-element-fontcontrol.md)

![Screenshot des fontcontrol-Elements mit dem richfont-Attribut, das auf TRUE festgelegt ist.](images/markup/fontcontrol-strikethrough.png)

In der folgenden Tabelle werden die Eigenschaften und das Ergebnis der Benutzeroberfläche beschrieben.



|   Eigenschaft                       |    Ergebnis der Benutzeroberfläche                                                                 |
|----------------------------------|------------------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | **Die Schaltfläche** "Durchgestreichen" ist deaktiviert und kann nur von der Anwendung festgelegt werden. |
| `UI_FONTPROPERTIES_NOTSET`       | **Die Durchstreichschaltfläche** ist nicht ausgewählt.                                    |
| `UI_FONTPROPERTIES_SET`          | **Die Schaltfläche Durchgestreichen** ist ausgewählt.                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaften des Schriftart-Steuerelements](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**SCHRIFTARTEIGENSCHAFTEN \_ DER BENUTZEROBERFLÄCHE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Schriftart-Steuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 