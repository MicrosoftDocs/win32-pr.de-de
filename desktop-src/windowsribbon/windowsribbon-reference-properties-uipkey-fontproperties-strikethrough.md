---
title: UI_PKEY_FontProperties_Strikethrough
description: Identifiziert die Eigenschaft "Benutzeroberflächen- \_ pkey- \_ fontproperties-Eigenschaften" \_ .
ms.assetid: 18ee653d-db01-4615-a85d-ad4ac6a0f422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b07804a74671bb219b34b1c67580af083fd5c34c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390853"
---
# <a name="ui_pkey_fontproperties_strikethrough"></a>UI- \_ pkey- \_ fontproperties \_ durchgestrichen

Identifiziert die Eigenschaft "Benutzeroberflächen- \_ pkey- \_ fontproperties-Eigenschaften" \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_Strikethrough
   shellPKey = UI_PKEY_FontProperties_Strikethrough
   formatID = 00000306-7363-696e-8441798acf5aebb7
   propID = 306
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Bemerkungen

UI \_ pkey \_ fontproperties durchgestrichen \_ wird von einer Anwendung verwendet, um den Zustand der Schaltfläche **durch** gestrichen abzufragen.

Der Eigenschafts Wert ist aus der [**UI \_ fontproperties**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) -Enumeration.

Der Standardwert ist `UI_FONTPROPERTIES_NOTSET`.

Der folgende Screenshot zeigt die Schaltfläche **durch** gestrichen des Menübands [**FontControl**](windowsribbon-element-fontcontrol.md).

![Screenshot des FontControl-Elements, bei dem das richfont-Attribut auf "true" festgelegt ist.](images/markup/fontcontrol-strikethrough.png)

In der folgenden Tabelle werden die Eigenschaften und das Benutzeroberflächen Ergebnis beschrieben.



|                                  |                                                                              |
|----------------------------------|------------------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | Die Schaltfläche " **durch** gestrichen" ist deaktiviert und kann nur von der Anwendung festgelegt werden. |
| `UI_FONTPROPERTIES_NOTSET`       | Die Schaltfläche " **durch** gestrichen" ist nicht ausgewählt.                                    |
| `UI_FONTPROPERTIES_SET`          | Die Schaltfläche " **durch** gestrichen" ist ausgewählt.                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schriftart Steuerelement-Eigenschaften](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI- \_ fontproperties**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Schriftart-Steuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 