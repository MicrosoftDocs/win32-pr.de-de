---
title: UI_PKEY_FontProperties_ForegroundColorType
description: Identifiziert die \_ PKEY \_ FontProperties \_ ForegroundColorType-Eigenschaft der Benutzeroberfläche.
ms.assetid: ab04c0b0-911f-4649-9ce8-5ecd847abf9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26b324a4e504c5ef98850f2bbcabd55b34525650b0ecfd3c201d45896e0c800
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118438649"
---
# <a name="ui_pkey_fontproperties_foregroundcolortype"></a>UI \_ PKEY \_ FontProperties \_ ForegroundColorType

Identifiziert die \_ PKEY \_ FontProperties \_ ForegroundColorType-Eigenschaft der Benutzeroberfläche.

```
propertyDescription
   name = UI_PKEY_FontProperties_ForegroundColorType
   shellPKey = UI_PKEY_FontProperties_ForegroundColorType
   formatID = 00000310-7363-696e-8441798acf5aebb7
   propID = 310
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>Hinweise

Ui PKEY FontProperties ForegroundColorType wird von einer Anwendung in Verbindung mit UI \_ \_ \_ [ \_ PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md)verwendet, um Einstellungen des **Textfarbkatalogs** abfragt.

Der Eigenschaftswert ist aus der [**\_ SWATCHCOLORTYPE-Enumeration der Benutzeroberfläche.**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)

Der Standardwert ist `UI_SWATCHCOLORTYPE_RGB`.

Die folgende Tabelle enthält eine Beschreibung der Eigenschaftswerte.



|     Wert                           |     BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | Wird von [**FontControl nicht unterstützt.**](windowsribbon-element-fontcontrol.md)                                                                                                                                                                                                                                                                                                                                        |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | Die Anwendung sollte die entsprechende Systemmetrik für den Farbwert  abfragen, in der Regel die aktuelle Windows Designtextfarbe, die mit GetSysColor(COLOR \_ WINDOWTEXT) abgerufen wird.                                                                                                                                                                                                                                  |
| `UI_SWATCHCOLORTYPE_RGB`       | Die Anwendung sollte [ \_ PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) für die Benutzeroberfläche nach dem Farbwert abfragen. Der Farbwert von [ \_ UI PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) wird auf der **Schaltfläche Textfarbe** angezeigt und im **Textfarbkatalog** ausgewählt.<br/> |



 

Ui \_ PKEY FontProperties ForegroundColorType wird an die \_ \_ [**IUICommandHandler::Execute-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) übergeben, wenn ein Farbmuster in einem FontControl-Textfarbkatalog [](windowsribbon-element-fontcontrol.md) **ausgewählt** wird.

> [!Note]  
> Es wird dringend empfohlen, dass  die Anwendung nur einen anfänglichen Textfarbwert und diesen Wert nicht erneut festlegen sollte, wenn der Cursor innerhalb eines Dokuments neu positioniert wird. Die letzte Auswahl sollte beibehalten werden, um zu vermeiden, dass die gewünschte Farbe erneut ausgewählt werden muss.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaften des Schriftart-Steuerelements](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[Schriftart-Steuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

