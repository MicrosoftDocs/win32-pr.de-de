---
title: UI_PKEY_FontProperties_VerticalPositioning
description: Bezeichnet die \_ verticalpositionierungs-Eigenschaft der UI-pkey- \_ fontproperties \_ .
ms.assetid: a92f845e-b0fc-4e23-9d06-ca16d2becf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88b67e2a099b7ce02b3c94f7c9d799fcdda5e881
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039458"
---
# <a name="ui_pkey_fontproperties_verticalpositioning"></a>Benutzeroberflächen- \_ pkey \_ fontproperties \_ verticalpositionierung

Bezeichnet die \_ verticalpositionierungs-Eigenschaft der UI-pkey- \_ fontproperties \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_VerticalPositioning
   shellPKey = UI_PKEY_FontProperties_VerticalPositioning
   formatID = 00000307-7363-696e-8441798acf5aebb7
   propID = 307
   typeInfo
      type = UI_FONTVERTICALPOSITION
```

## <a name="remarks"></a>Bemerkungen

Benutzeroberflächen \_ -pkey \_ fontproperties \_ verticalpositionierung wird von einer Anwendung verwendet, um den Wert der **SuperScript** -und Index Steuerelemente abzufragen. 

Der Eigenschafts Wert ist aus der [**UI \_ fontverticalposition**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) -Enumeration.

Der Standardwert ist `UI_FONTVERTICALPOSITION_NOTSET`.

Der folgende Screenshot zeigt die Schaltflächen **SuperScript** **und Index** des Menübands [**FontControl**](windowsribbon-element-fontcontrol.md).

![Screenshot des FontControl-Elements, bei dem das richfont-Attribut auf "true" festgelegt ist.](images/markup/fontcontrol-subsuper.png)

In der folgenden Tabelle werden die Eigenschaften und das Benutzeroberflächen Ergebnis beschrieben.



|                                        |                                                                                                |
|----------------------------------------|------------------------------------------------------------------------------------------------|
| `UI_FONTVERTICALPOSITION_NOTAVAILABLE` | **SuperScript** -und Index **-Schaltflächen sind deaktiviert und können** nur von der Anwendung festgelegt werden. |
| `UI_FONTVERTICALPOSITION_NOTSET`       | Die **Schaltflächen** **SuperScript** und Index werden nicht ausgewählt.                                    |
| `UI_FONTVERTICALPOSITION_SUPERSCRIPT`  | Die Schaltfläche **SuperScript** ist ausgewählt.                                                            |
| `UI_FONTVERTICALPOSITION_SUBSCRIPT`    | Die Schaltfläche " **Abonnement** " ist ausgewählt.                                                              |



 

> [!Note]  
> Die **Schaltflächen** " **SuperScript** " und "index" können nicht gleichzeitig ausgewählt werden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schriftart Steuerelement-Eigenschaften](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ fontverticalposition**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition)
</dt> <dt>

[Schriftart-Steuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 