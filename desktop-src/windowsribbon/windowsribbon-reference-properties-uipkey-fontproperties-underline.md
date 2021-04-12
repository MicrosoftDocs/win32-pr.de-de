---
title: UI_PKEY_FontProperties_Underline
description: Gibt die Eigenschaft "UI \_ pkey fontproperties-Unterstreichung" an \_ \_ .
ms.assetid: 88492558-ab19-4606-8fe0-5f100677b88a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 380c3fdadb636775f80b789a585c42ff2369234a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473588"
---
# <a name="ui_pkey_fontproperties_underline"></a>Benutzeroberflächen- \_ pkey \_ fontproperties unter \_ streichen

Gibt die Eigenschaft "UI \_ pkey fontproperties-Unterstreichung" an \_ \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_Underline
   shellPKey = UI_PKEY_FontProperties_Underline
   formatID = 00000305-7363-696e-8441798acf5aebb7
   propID = 305
   typeInfo
      type = UI_FONTUNDERLINE
```

## <a name="remarks"></a>Bemerkungen

\_Die Unterstreichung von UI pkey \_ fontproperties \_ wird von einer Anwendung verwendet, um den Zustand der Schaltfläche "unter **streichen** " abzufragen.

Der Eigenschafts Wert ist aus der [**UI \_ fontstreicht**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) -Enumeration.

Der Standardwert ist `UI_FONTUNDERLINE_NOTSET`.

Der folgende Screenshot zeigt die unter **Streichung** -Schaltfläche des Menübands [**FontControl**](windowsribbon-element-fontcontrol.md).

![Screenshot des FontControl-Elements, bei dem das richfont-Attribut auf "true" festgelegt ist.](images/markup/fontcontrol-underline.png)

In der folgenden Tabelle werden die Eigenschaften und das Benutzeroberflächen Ergebnis beschrieben.



|                                 |                                                                          |
|---------------------------------|--------------------------------------------------------------------------|
| `UI_FONTUNDERLINE_NOTAVAILABLE` | Die Schaltfläche "unter **streichen** " ist deaktiviert und kann nur von der Anwendung festgelegt werden. |
| `UI_FONTUNDERLINE_NOTSET`       | Die Schaltfläche für unter **Streichung** ist nicht ausgewählt.                                    |
| `UI_FONTUNDERLINE_SET`          | Die Schaltfläche unter **Streichung** ist ausgewählt.                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schriftart Steuerelement-Eigenschaften](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ fontunter Streichung**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)
</dt> <dt>

[Schriftart-Steuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 