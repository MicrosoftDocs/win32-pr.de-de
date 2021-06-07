---
title: UI_PKEY_FontProperties_DeltaSize
description: Identifiziert die \_ PKEY \_ FontProperties \_ DeltaSize-Eigenschaft der Benutzeroberfläche.
ms.assetid: 021a6c79-1d3e-47d2-9601-cdaa2e66a50a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67778a710de8f69e0aea1134c12fb9ee3ebe0133
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444391"
---
# <a name="ui_pkey_fontproperties_deltasize"></a>UI \_ PKEY \_ FontProperties \_ DeltaSize

Identifiziert die \_ PKEY \_ FontProperties \_ DeltaSize-Eigenschaft der Benutzeroberfläche.

```
propertyDescription
   name = UI_PKEY_FontProperties_DeltaSize
   shellPKey = UI_PKEY_FontProperties_DeltaSize
   formatID = 00000309-7363-696e-8441798acf5aebb7
   propID = 313
   typeInfo
      type = UI_FONTDELTASIZE
```

## <a name="remarks"></a>Hinweise

Ui \_ PKEY \_ FontProperties \_ DeltaSize wird von einer Anwendung in Fällen verwendet, in denen es für die Anwendung nicht möglich ist, einen Wert für **Schriftgrad** anzugeben, z. B. wenn eine Ausführung von text heterogener Größe ausgewählt wird. Das **Steuerelement Schriftgrad** ist auf blank festgelegt, und die Ui \_ PKEY \_ FontProperties \_ DeltaSize wird verwendet, um Benutzerinteraktionen mit den Schaltflächen **Schriftvergrößerung** und **Schriftver verkleinern** zu erfassen.

Ui \_ PKEY \_ FontProperties \_ DeltaSize ist in [ui \_ PKEY \_ FontProperties \_ ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md)enthalten.

Der folgende Screenshot zeigt die Schaltflächen **Schriftgröße** und **Schrift verkleinern** des Menübands [**FontControl**](windowsribbon-element-fontcontrol.md).

![Screenshot der Schaltflächen "Schrift vergrößern" und "Schrift verkleinern" auf dem fontcontrol.)](images/markup/fontcontrol-incdec.png)

Die folgende Tabelle enthält eine Beschreibung der Eigenschaftswerte.



|     Wert                 |  BESCHREIBUNG                    |
|---------------------------|---------------------------------|
| `UI_FONTDELTASIZE_GROW`   | Auf die Schaltfläche **"Schriftart** vergrößern" geklickt.   |
| `UI_FONTDELTASIZE_SHRINK` | Auf die Schaltfläche **Schriftart verkleinern** geklickt. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaften des Schriftartsteuerelements](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ FONTDELTASIZE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontdeltasize)
</dt> <dt>

[Schriftartsteuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 