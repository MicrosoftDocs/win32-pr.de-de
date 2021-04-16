---
title: UI_PKEY_FontProperties_ForegroundColorType
description: Identifiziert die Eigenschaft "Benutzeroberflächen- \_ pkey \_ fontproperties \_ foregroundcolortype".
ms.assetid: ab04c0b0-911f-4649-9ce8-5ecd847abf9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5589e9b21fc7ab0884a3cac51eba114ee77036b3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390574"
---
# <a name="ui_pkey_fontproperties_foregroundcolortype"></a>UI \_ pkey \_ fontproperties \_ foregroundcolortype

Identifiziert die Eigenschaft "Benutzeroberflächen- \_ pkey \_ fontproperties \_ foregroundcolortype".

```
propertyDescription
   name = UI_PKEY_FontProperties_ForegroundColorType
   shellPKey = UI_PKEY_FontProperties_ForegroundColorType
   formatID = 00000310-7363-696e-8441798acf5aebb7
   propID = 310
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>Bemerkungen

UI \_ pkey \_ fontproperties \_ foregroundcolortype wird von einer Anwendung verwendet, in Verbindung mit der [UI \_ pkey \_ fontproperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), um die Einstellungen für die **Textfarbe** -Galerie abzufragen.

Der Eigenschafts Wert ist aus der [**UI- \_ swatchcolortype**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) -Enumeration.

Der Standardwert ist `UI_SWATCHCOLORTYPE_RGB`.

Die folgende Tabelle enthält eine Beschreibung der Eigenschaftswerte.



|                                |                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | Wird vom [**FontControl-Steuer**](windowsribbon-element-fontcontrol.md)Element nicht unterstützt.                                                                                                                                                                                                                                                                                                                                        |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | Die Anwendung sollte die entsprechende Systemmetrik für den Farbwert Abfragen, der in der Regel die aktuelle Windows-Design **Textfarbe** ist, die mit GetSysColor (Color \_ WindowText) abgerufen wird.                                                                                                                                                                                                                                  |
| `UI_SWATCHCOLORTYPE_RGB`       | Die Anwendung sollte die Benutzeroberflächen- [ \_ pkey- \_ fontproperties- \_ Vordergrundfarbe](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) für den Farbwert Abfragen. Der Farbwert von [UI \_ pkey \_ fontproperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) wird auf der **Textfarbe** -Schaltfläche angezeigt und im **Text** Katalog ausgewählt.<br/> |



 

UI \_ pkey \_ fontproperties \_ foregroundcolortype wird an die [**iuicommandhandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) -Rückruf Methode übergeben, wenn ein Farbmuster in einer [**FontControl**](windowsribbon-element-fontcontrol.md) - **textfarb** Galerie ausgewählt wird.

> [!Note]  
> Es wird dringend empfohlen, dass die Anwendung nur einen anfänglichen **textfarbwert** festlegen und diesen Wert nicht erneut festlegen, wenn der Cursor innerhalb eines Dokuments neu positioniert wird. Die letzte Auswahl sollte beibehalten werden, um zu vermeiden, dass die gewünschte Farbe erneut ausgewählt werden muss.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schriftart Steuerelement-Eigenschaften](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI- \_ swatchcolortype**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[Schriftart-Steuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

