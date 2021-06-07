---
title: UI_PKEY_FontProperties_Italic
description: Identifiziert die \_ italische PKEY \_ FontProperties-Eigenschaft der \_ Benutzeroberfläche.
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d0dfa07b5112e91d8c25a4ff8c4f31175adf9b7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443811"
---
# <a name="ui_pkey_fontproperties_italic"></a>UI \_ PKEY \_ FontProperties \_ Italic

Identifiziert die \_ italische PKEY \_ FontProperties-Eigenschaft der \_ Benutzeroberfläche.

```
propertyDescription
   name = UI_PKEY_FontProperties_Italic
   shellPKey = UI_PKEY_FontProperties_Italic
   formatID = 00000304-7363-696e-8441798acf5aebb7
   propID = 304
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Hinweise

Ui \_ PKEY \_ FontProperties \_ Italic wird von einer Anwendung verwendet, um den Zustand der **Italic-Schaltfläche** abzufragen.

Der Eigenschaftswert stammt aus der [**\_ FONTPROPERTIES-Enumeration der Benutzeroberfläche.**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)

Standardwert: `UI_FONTPROPERTIES_NOTSET`.

In der folgenden Tabelle werden die Eigenschaften und das Benutzeroberflächenergebnis beschrieben.



|    Eigenschaft                      |       Ergebnis der Benutzeroberfläche                                                       |
|----------------------------------|-----------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | **Die italische** Schaltfläche ist deaktiviert und kann nur von der Anwendung festgelegt werden. |
| `UI_FONTPROPERTIES_NOTSET`       | **Die italische** Schaltfläche ist nicht ausgewählt.                                    |
| `UI_FONTPROPERTIES_SET`          | **Die italische** Schaltfläche ist ausgewählt.                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaften des Schriftartsteuerelements](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Schriftartsteuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 