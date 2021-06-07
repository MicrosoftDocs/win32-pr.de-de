---
title: UI_PKEY_FontProperties_BackgroundColorType
description: Identifiziert die \_ Ui-Eigenschaft PKEY \_ FontProperties \_ BackgroundColorType.
ms.assetid: d93f4d9f-3d35-4066-be94-f6b6b4302bff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45bbd2056087d584663c8ca716c4021554098dfa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443821"
---
# <a name="ui_pkey_fontproperties_backgroundcolortype"></a>UI \_ PKEY \_ FontProperties \_ BackgroundColorType

Identifiziert die \_ Ui-Eigenschaft PKEY \_ FontProperties \_ BackgroundColorType.

```
propertyDescription
   name = UI_PKEY_FontProperties_BackgroundColorType
   shellPKey = UI_PKEY_FontProperties_BackgroundColorType
   formatID = 00000311-7363-696e-8441798acf5aebb7
   propID = 311
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>Hinweise

Ui \_ PKEY \_ FontProperties \_ BackgroundColorType wird von einer Anwendung in Verbindung mit [der Benutzeroberfläche \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor)verwendet, um Einstellungen des **Textmarkerfarbkatalogs** abzufragen.

Der Eigenschaftswert stammt aus der [**\_ SWATCHCOLORTYPE-Enumeration der Benutzeroberfläche.**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)

Standardwert: `UI_SWATCHCOLORTYPE_RGB`.

Die folgende Tabelle enthält eine Beschreibung der Eigenschaftswerte.



|   Eigenschaft                             |   BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | Die Anwendung sollte die entsprechende Systemmetrik für den Farbwert abfragen, in der Regel die aktuelle **Hintergrundfarbe** des Windows-Designfensters, die mit GetSysColor(COLOR WINDOW) abgerufen \_ wird.                                                                                                                                                                                                                                                                 |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | Wird von [**FontControl**](windowsribbon-element-fontcontrol.md)nicht unterstützt.                                                                                                                                                                                                                                                                                                                                                                                |
| `UI_SWATCHCOLORTYPE_RGB`       | Die Anwendung sollte [die Benutzeroberfläche \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) nach dem Farbwert abfragen. Der Farbwert von [ \_ UI-PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) wird auf der Schaltfläche **Text highlight color (Text hervorhebungsfarbe)** angezeigt und im **Farbkatalog textmarkiert** ausgewählt.<br/> |



 

Ui \_ PKEY \_ FontProperties \_ BackgroundColorType wird an die [**IUICommandHandler::Execute-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) übergeben, wenn in einem [**FontControl**](windowsribbon-element-fontcontrol.md) **Text Highlight** Color Gallery eine Farbuhr ausgewählt ist.

> [!Note]  
> Es wird dringend empfohlen, dass die Anwendung nur einen anfänglichen **Textmarkierungsfarbwert** und diesen Wert nicht neu festlegen soll, wenn der Cursor innerhalb eines Dokuments neu positioniert wird. Die letzte Auswahl sollte beibehalten werden, um zu vermeiden, dass die gewünschte Farbe erneut ausgewählt werden muss.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaften des Schriftartsteuerelements](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[Schriftartsteuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

