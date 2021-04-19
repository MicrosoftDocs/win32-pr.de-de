---
title: UI_PKEY_FontProperties_Bold
description: Gibt die Eigenschaft "Bold Properties" der UI \_ pkey \_ fontproperties an \_ .
ms.assetid: 9d33142a-bd63-423e-ba77-083c86bce1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dca8a58b9c5bfa51cfba8d80a477dafb744dfb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338482"
---
# <a name="ui_pkey_fontproperties_bold"></a>UI- \_ pkey \_ fontproperties \_ Fett

Gibt die Eigenschaft "Bold Properties" der UI \_ pkey \_ fontproperties an \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_Bold
   shellPKey = UI_PKEY_FontProperties_Bold
   formatID = 00000303-7363-696e-8441798acf5aebb7
   propID = 303
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Bemerkungen

UI \_ pkey \_ fontproperties \_ Bold wird von einer Anwendung verwendet, um den Status der **Fett** formatierten Schaltfläche abzufragen.

Der Eigenschafts Wert ist aus der [**UI \_ fontproperties**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) -Enumeration.

Der Standardwert ist `UI_FONTPROPERTIES_NOTSET`.

In der folgenden Tabelle werden die Eigenschaften und das Benutzeroberflächen Ergebnis beschrieben.



|                                  |                                                                     |
|----------------------------------|---------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | Die **Fett** formatierte Schaltfläche ist deaktiviert und kann nur von der Anwendung festgelegt werden. |
| `UI_FONTPROPERTIES_NOTSET`       | Die Schaltfläche " **Fett** " ist nicht ausgewählt.                                    |
| `UI_FONTPROPERTIES_SET`          | Die Schaltfläche **Fett** ist ausgewählt.                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schriftart Steuerelement-Eigenschaften](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI- \_ fontproperties**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Schriftart-Steuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 