---
title: UI_PKEY_FontProperties_Underline
description: Identifiziert die \_ PKEY \_ FontProperties \_ Underline-Eigenschaft der Benutzeroberfläche.
ms.assetid: 88492558-ab19-4606-8fe0-5f100677b88a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066027e5f62416667619937eea7dbe493a3ff279
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443781"
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

Ui \_ PKEY \_ FontProperties \_ Underline wird von einer Anwendung verwendet, um den Status der Schaltfläche **Unterstreichung** abzufragen.

Der Eigenschaftswert stammt aus der [**\_ FONTUNDERLINE-Enumeration der Benutzeroberfläche.**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)

Standardwert: `UI_FONTUNDERLINE_NOTSET`.

Der folgende Screenshot zeigt die Schaltfläche **Unterstreichung** des [**Menübands FontControl**](windowsribbon-element-fontcontrol.md).

![Screenshot des fontcontrol-Elements mit dem richfont-Attribut, das auf TRUE festgelegt ist.](images/markup/fontcontrol-underline.png)

In der folgenden Tabelle werden die Eigenschaften und das Benutzeroberflächenergebnis beschrieben.



|      Eigenschaft                   |       Ergebnis der Benutzeroberfläche                                                          |
|---------------------------------|--------------------------------------------------------------------------|
| `UI_FONTUNDERLINE_NOTAVAILABLE` | Die Schaltfläche **Unterstreichung** ist deaktiviert und kann nur von der Anwendung festgelegt werden. |
| `UI_FONTUNDERLINE_NOTSET`       | Die Schaltfläche **Unterstreichung** ist nicht ausgewählt.                                    |
| `UI_FONTUNDERLINE_SET`          | Die Schaltfläche **Unterstreichung** ist ausgewählt.                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaften des Schriftartsteuerelements](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ FONTUNDERLINE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)
</dt> <dt>

[Schriftartsteuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 