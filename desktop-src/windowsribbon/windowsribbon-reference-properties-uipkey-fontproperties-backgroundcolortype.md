---
title: UI_PKEY_FontProperties_BackgroundColorType
description: Identifiziert die \_ PKEY \_ FontProperties \_ BackgroundColorType-Eigenschaft der Benutzeroberfläche.
ms.assetid: d93f4d9f-3d35-4066-be94-f6b6b4302bff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28bd653b3bcf62eaf8cab797b3bc45d97b88e15bef4bb0fdd3407bdd95ca28e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118438669"
---
# <a name="ui_pkey_fontproperties_backgroundcolortype"></a>UI \_ PKEY \_ FontProperties \_ BackgroundColorType

Identifiziert die \_ PKEY \_ FontProperties \_ BackgroundColorType-Eigenschaft der Benutzeroberfläche.

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

Ui PKEY FontProperties BackgroundColorType wird von einer Anwendung in Verbindung mit \_ \_ ui \_ [ \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor)verwendet,  um Text highlight color gallery settings (Farbkatalogeinstellungen für Text hervorheben) abfragt.

Der Eigenschaftswert ist aus der [**\_ SWATCHCOLORTYPE-Enumeration der Benutzeroberfläche.**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)

Der Standardwert ist `UI_SWATCHCOLORTYPE_RGB`.

Die folgende Tabelle enthält eine Beschreibung der Eigenschaftswerte.



|   Eigenschaft                             |   BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | Die Anwendung sollte die entsprechende Systemmetrik für den Farbwert  abfragen, in der Regel die aktuelle Windows Hintergrundfarbe des Designfensters, die mit GetSysColor(COLOR WINDOW) abgerufen \_ wird.                                                                                                                                                                                                                                                                 |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | Wird von [**FontControl nicht unterstützt.**](windowsribbon-element-fontcontrol.md)                                                                                                                                                                                                                                                                                                                                                                                |
| `UI_SWATCHCOLORTYPE_RGB`       | Die Anwendung sollte [ui \_ PKEY \_ FontProperties \_ BackgroundColor nach](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) dem Farbwert abfragen. Der Farbwert von [ \_ UI PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) wird auf der **Schaltfläche Text hervorhebungsfarbe** angezeigt und im **Farbkatalog Text hervorheben** ausgewählt.<br/> |



 

Ui \_ PKEY \_ FontProperties BackgroundColorType wird an die \_ [**IUICommandHandler::Execute-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) [](windowsribbon-element-fontcontrol.md) übergeben, wenn ein Farbmuster in einem FontControl **Text Highlight-Farbkatalog** ausgewählt wird.

> [!Note]  
> Es wird dringend empfohlen, dass  die Anwendung nur einen anfänglichen Text-Hervorhebungsfarbwert und diesen Wert nicht erneut festlegen sollte, wenn der Cursor innerhalb eines Dokuments neu positioniert wird. Die letzte Auswahl sollte beibehalten werden, um zu vermeiden, dass die gewünschte Farbe erneut ausgewählt werden muss.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaften des Schriftart-Steuerelements](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[Schriftart-Steuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

