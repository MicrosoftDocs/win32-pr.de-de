---
title: UI_PKEY_FontProperties_Bold
description: Identifiziert die \_ PKEY \_ FontProperties \_ Bold-Eigenschaft der Benutzeroberfläche.
ms.assetid: 9d33142a-bd63-423e-ba77-083c86bce1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68800d3cfed72382f3576edfc01272c82b46c825
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444381"
---
# <a name="ui_pkey_fontproperties_bold"></a>UI \_ PKEY \_ FontProperties \_ Bold

Identifiziert die \_ PKEY \_ FontProperties \_ Bold-Eigenschaft der Benutzeroberfläche.

```
propertyDescription
   name = UI_PKEY_FontProperties_Bold
   shellPKey = UI_PKEY_FontProperties_Bold
   formatID = 00000303-7363-696e-8441798acf5aebb7
   propID = 303
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Hinweise

Ui \_ PKEY \_ FontProperties \_ Bold wird von einer Anwendung verwendet, um den Zustand der Schaltfläche **Bold** abzufragen.

Der Eigenschaftswert stammt aus der [**\_ FONTPROPERTIES-Enumeration der Benutzeroberfläche.**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)

Standardwert: `UI_FONTPROPERTIES_NOTSET`.

In der folgenden Tabelle werden die Eigenschaften und das Benutzeroberflächenergebnis beschrieben.



|      Eigenschaft                    |    Ergebnis der Benutzeroberfläche                                                        |
|----------------------------------|---------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | **Die** Schaltfläche Fett ist deaktiviert und kann nur von der Anwendung festgelegt werden. |
| `UI_FONTPROPERTIES_NOTSET`       | **Die** Schaltfläche Fett ist nicht ausgewählt.                                    |
| `UI_FONTPROPERTIES_SET`          | **Die** Schaltfläche Fett ist ausgewählt.                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaften des Schriftartsteuerelements](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Schriftartsteuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 