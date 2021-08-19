---
title: UI_PKEY_FontProperties_DeltaSize
description: Identifiziert die \_ PKEY \_ FontProperties \_ DeltaSize-Eigenschaft der Benutzeroberfläche.
ms.assetid: 021a6c79-1d3e-47d2-9601-cdaa2e66a50a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a35d2660d2221b4edad567b0fd05eb8283fce4b3cc7d1cb8e35c735838f385d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118438752"
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

Ui \_ PKEY \_ FontProperties \_ DeltaSize wird von einer Anwendung in Fällen verwendet, in denen es der Anwendung nicht möglich ist, einen Wert für Schriftgrad anzugeben, z. B. wenn eine Ausführung von heterogenem Text ausgewählt ist. Das **Steuerelement Schriftgrad** ist auf leer festgelegt, und UI PKEY FontProperties DeltaSize wird verwendet, um Benutzerinteraktion mit den Schaltflächen Schriftartvergrößerung und \_ \_ \_ **Schriftartverkleinerung zu** erfassen. 

Ui \_ PKEY \_ FontProperties \_ DeltaSize ist in [UI \_ PKEY \_ FontProperties \_ ChangedProperties enthalten.](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md)

Der folgende Screenshot zeigt die Schaltflächen **Schriftartvergrößerung** und **Schriftverkleinerung** des Menübands [**FontControl.**](windowsribbon-element-fontcontrol.md)

![Screenshot der Schaltflächen zum Verkleinern und Verkleinern von Schriftarten auf dem FontControl-Objekt.](images/markup/fontcontrol-incdec.png)

Die folgende Tabelle enthält eine Beschreibung der Eigenschaftswerte.



|     Wert                 |  BESCHREIBUNG                    |
|---------------------------|---------------------------------|
| `UI_FONTDELTASIZE_GROW`   | **Klicken Sie auf die Schaltfläche** Schriftart vergrößern.   |
| `UI_FONTDELTASIZE_SHRINK` | **Klicken Sie auf die** Schaltfläche Schriftart verkleinern. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaften des Schriftart-Steuerelements](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ FONTDELTASIZE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontdeltasize)
</dt> <dt>

[Schriftart-Steuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 