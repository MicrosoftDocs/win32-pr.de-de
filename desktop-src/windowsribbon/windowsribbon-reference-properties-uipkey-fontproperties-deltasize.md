---
title: UI_PKEY_FontProperties_DeltaSize
description: Bezeichnet die Eigenschaft "Benutzeroberflächen- \_ pkey \_ fontproperties \_ Delta size".
ms.assetid: 021a6c79-1d3e-47d2-9601-cdaa2e66a50a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c0046edf41fa61382d45a0662119d8fda237a0f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039006"
---
# <a name="ui_pkey_fontproperties_deltasize"></a>UI- \_ pkey \_ fontproperties \_ Delta size

Bezeichnet die Eigenschaft "Benutzeroberflächen- \_ pkey \_ fontproperties \_ Delta size".

```
propertyDescription
   name = UI_PKEY_FontProperties_DeltaSize
   shellPKey = UI_PKEY_FontProperties_DeltaSize
   formatID = 00000309-7363-696e-8441798acf5aebb7
   propID = 313
   typeInfo
      type = UI_FONTDELTASIZE
```

## <a name="remarks"></a>Bemerkungen

UI \_ pkey \_ fontproperties \_ Delta Size wird von einer Anwendung in Fällen verwendet, in denen es nicht möglich ist, dass die Anwendung einen Wert für den **Schrift** Grad angibt, z. b. Wenn eine Textgröße mit Hetero gener Größe ausgewählt wird. Das Steuerelement **Schriftart Größe** ist auf Blank festgelegt, und die \_ Benutzeroberfläche pkey \_ fontproperties \_ Delta Size wird verwendet, um die Benutzerinteraktion mit den Schaltflächen für **Schriftart** Vergrößerung und **Schriftart verkleinern** zu erfassen.

UI \_ pkey \_ fontproperties \_ Delta size ist in [UI \_ pkey \_ fontproperties \_ changedproperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md)enthalten.

Der folgende Screenshot zeigt die Schaltflächen **vergrößern** und **Verkleinern der Schriftart** des Menübands [**FontControl**](windowsribbon-element-fontcontrol.md).

![Screenshot der Schaltflächen zum Vergrößern der Schriftart und zum Verkleinern der Schriftart auf dem FontControl-Steuerelement.](images/markup/fontcontrol-incdec.png)

Die folgende Tabelle enthält eine Beschreibung der Eigenschaftswerte.



|                           |                                 |
|---------------------------|---------------------------------|
| `UI_FONTDELTASIZE_GROW`   | Schaltfläche " **Schriftart vergrößern** " geklickt.   |
| `UI_FONTDELTASIZE_SHRINK` | Schaltfläche zum **Verkleinern der Schriftart** . |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schriftart Steuerelement-Eigenschaften](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ fontdelta size**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontdeltasize)
</dt> <dt>

[Schriftart-Steuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 