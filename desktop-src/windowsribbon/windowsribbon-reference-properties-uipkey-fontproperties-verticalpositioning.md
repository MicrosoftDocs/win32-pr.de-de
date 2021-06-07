---
title: UI_PKEY_FontProperties_VerticalPositioning
description: Identifiziert die \_ PKEY \_ FontProperties \_ VerticalPositioning-Eigenschaft der Benutzeroberfläche.
ms.assetid: a92f845e-b0fc-4e23-9d06-ca16d2becf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 954b01ff3271b9f74fac2c130c697a70e910fc93
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444301"
---
# <a name="ui_pkey_fontproperties_verticalpositioning"></a>UI \_ PKEY \_ FontProperties \_ VerticalPositioning

Identifiziert die \_ PKEY \_ FontProperties \_ VerticalPositioning-Eigenschaft der Benutzeroberfläche.

```
propertyDescription
   name = UI_PKEY_FontProperties_VerticalPositioning
   shellPKey = UI_PKEY_FontProperties_VerticalPositioning
   formatID = 00000307-7363-696e-8441798acf5aebb7
   propID = 307
   typeInfo
      type = UI_FONTVERTICALPOSITION
```

## <a name="remarks"></a>Hinweise

Ui \_ PKEY \_ FontProperties \_ VerticalPositioning wird von einer Anwendung verwendet, um den Wert der **Steuerelemente Superscript** und **Subscript** abzufragen.

Der Eigenschaftswert stammt aus der [**\_ FONTVERTICALPOSITION-Enumeration der Benutzeroberfläche.**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition)

Standardwert: `UI_FONTVERTICALPOSITION_NOTSET`.

Der folgende Screenshot zeigt die Schaltflächen **Superscript** und **Subscript** des Menübands [**FontControl**](windowsribbon-element-fontcontrol.md).

![Screenshot des fontcontrol-Elements mit dem richfont-Attribut, das auf TRUE festgelegt ist.](images/markup/fontcontrol-subsuper.png)

In der folgenden Tabelle werden die Eigenschaften und das Benutzeroberflächenergebnis beschrieben.



|     Eigenschaft                           |          Ergebnis der Benutzeroberfläche                                                                             |
|----------------------------------------|------------------------------------------------------------------------------------------------|
| `UI_FONTVERTICALPOSITION_NOTAVAILABLE` | Die Schaltflächen **"Superscript"** und **"Subscript"** sind deaktiviert und können nur von der Anwendung festgelegt werden. |
| `UI_FONTVERTICALPOSITION_NOTSET`       | **Schaltflächen "Superscript"** und **"Subscript"** sind nicht ausgewählt.                                    |
| `UI_FONTVERTICALPOSITION_SUPERSCRIPT`  | Die Schaltfläche **"Superscript"** ist ausgewählt.                                                            |
| `UI_FONTVERTICALPOSITION_SUBSCRIPT`    | Die Schaltfläche **"Tiefgestellt"** ist ausgewählt.                                                              |



 

> [!Note]  
> Die Schaltflächen **Superscript** und **Subscript** können nicht beide ausgewählt werden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaften des Schriftartsteuerelements](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ FONTVERTICALPOSITION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition)
</dt> <dt>

[Schriftartsteuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 