---
title: UI_PKEY_FontProperties_BackgroundColorType
description: Gibt die Benutzeroberflächen- \_ Eigenschaft "pkey \_ fontproperties \_ backgroundcolortype" an.
ms.assetid: d93f4d9f-3d35-4066-be94-f6b6b4302bff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568898cb2706eb932ea708f929aa4791f0643c74
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473268"
---
# <a name="ui_pkey_fontproperties_backgroundcolortype"></a>UI \_ pkey \_ fontproperties \_ backgroundcolortype

Gibt die Benutzeroberflächen- \_ Eigenschaft "pkey \_ fontproperties \_ backgroundcolortype" an.

```
propertyDescription
   name = UI_PKEY_FontProperties_BackgroundColorType
   shellPKey = UI_PKEY_FontProperties_BackgroundColorType
   formatID = 00000311-7363-696e-8441798acf5aebb7
   propID = 311
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>Bemerkungen

UI \_ pkey \_ fontproperties \_ backgroundcolortype wird von einer Anwendung in Verbindung mit der [UI \_ pkey \_ fontproperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor)verwendet, um Text Hervorhebungs **Farb** Galerie-Einstellungen abzufragen.

Der Eigenschafts Wert ist aus der [**UI- \_ swatchcolortype**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) -Enumeration.

Der Standardwert ist `UI_SWATCHCOLORTYPE_RGB`.

Die folgende Tabelle enthält eine Beschreibung der Eigenschaftswerte.



|                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | Die Anwendung sollte die entsprechende Systemmetrik für den Farbwert Abfragen, der in der Regel die aktuelle **Hintergrundfarbe** des Windows-Design Fensters ist, die mit GetSysColor (Farb \_ Fenster) abgerufen wird.                                                                                                                                                                                                                                                                 |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | Wird vom [**FontControl-Steuer**](windowsribbon-element-fontcontrol.md)Element nicht unterstützt.                                                                                                                                                                                                                                                                                                                                                                                |
| `UI_SWATCHCOLORTYPE_RGB`       | Die Anwendung sollte die [UI \_ pkey \_ fontproperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) für den Farbwert Abfragen. Der Farbwert von [UI \_ pkey \_ fontproperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) wird auf der Schaltfläche Text Hervorhebungs **Farbe** angezeigt und in der **Farb Galerie Text hervorheben** ausgewählt.<br/> |



 

UI \_ pkey \_ fontproperties \_ backgroundcolortype wird an die [**iuicommandhandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) -Rückruf Methode übergeben, wenn in einer [**FontControl**](windowsribbon-element-fontcontrol.md) -Text Hervorhebungs **Farb** Galerie ein Farbmuster ausgewählt wird.

> [!Note]  
> Es wird dringend empfohlen, dass die Anwendung nur einen anfänglichen Text Hervorhebungs **Farbwert** festlegen und diesen Wert nicht neu festlegen, wenn der Cursor innerhalb eines Dokuments neu positioniert wird. Die letzte Auswahl sollte beibehalten werden, um zu vermeiden, dass die gewünschte Farbe erneut ausgewählt werden muss.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schriftart Steuerelement-Eigenschaften](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI- \_ swatchcolortype**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[Schriftart-Steuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

