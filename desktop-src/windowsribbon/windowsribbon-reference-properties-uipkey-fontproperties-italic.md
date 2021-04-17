---
title: UI_PKEY_FontProperties_Italic
description: Bezeichnet die Eigenschaft für die Eigenschaft "Benutzeroberflächen- \_ pkey \_ fontproperties" \_ .
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00825807c57632b1bbea69c47bc9b90d705efa94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390458"
---
# <a name="ui_pkey_fontproperties_italic"></a>UI \_ pkey \_ fontproperties \_ kursiv

Bezeichnet die Eigenschaft für die Eigenschaft "Benutzeroberflächen- \_ pkey \_ fontproperties" \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_Italic
   shellPKey = UI_PKEY_FontProperties_Italic
   formatID = 00000304-7363-696e-8441798acf5aebb7
   propID = 304
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Bemerkungen

UI \_ pkey \_ fontproperties \_ Italic wird von einer Anwendung verwendet, um den Zustand der **kursiv** Schaltfläche abzufragen.

Der Eigenschafts Wert ist aus der [**UI \_ fontproperties**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) -Enumeration.

Der Standardwert ist `UI_FONTPROPERTIES_NOTSET`.

In der folgenden Tabelle werden die Eigenschaften und das Benutzeroberflächen Ergebnis beschrieben.



|                                  |                                                                       |
|----------------------------------|-----------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | Die Schaltfläche " **kursiv** " ist deaktiviert und kann nur von der Anwendung festgelegt werden. |
| `UI_FONTPROPERTIES_NOTSET`       | Die Schaltfläche " **kursiv** " ist nicht ausgewählt.                                    |
| `UI_FONTPROPERTIES_SET`          | Die Schaltfläche **kursiv** formatiert ist ausgewählt.                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schriftart Steuerelement-Eigenschaften](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI- \_ fontproperties**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Schriftart-Steuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 