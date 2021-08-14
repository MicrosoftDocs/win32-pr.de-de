---
title: UI_PKEY_FontProperties_Italic
description: Identifiziert die italische \_ Eigenschaft PKEY \_ FontProperties \_ der Benutzeroberfläche.
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 000bb72e1ba43b29f5e3815fe42d0ace454ff0219a188a128b422e4a621af210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118438535"
---
# <a name="ui_pkey_fontproperties_italic"></a>UI \_ PKEY \_ FontProperties \_ Italic

Identifiziert die italische \_ Eigenschaft PKEY \_ FontProperties \_ der Benutzeroberfläche.

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

Ui PKEY FontProperties Italic wird von einer Anwendung verwendet, um den Zustand der \_ \_ \_ **italischen Schaltfläche abfragt.**

Der -Eigenschaftswert ist aus der [**\_ FONTPROPERTIES-Enumeration der Benutzeroberfläche.**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)

Der Standardwert ist `UI_FONTPROPERTIES_NOTSET`.

In der folgenden Tabelle werden die Eigenschaften und das Ergebnis der Benutzeroberfläche beschrieben.



|    Eigenschaft                      |       Ergebnis der Benutzeroberfläche                                                       |
|----------------------------------|-----------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | **Die italische** Schaltfläche ist deaktiviert und kann nur von der Anwendung festgelegt werden. |
| `UI_FONTPROPERTIES_NOTSET`       | **Die schaltfläche "Italic"** ist nicht ausgewählt.                                    |
| `UI_FONTPROPERTIES_SET`          | **Die Schaltfläche "Italic" (Italic)** ist ausgewählt.                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaften des Schriftartsteuersteuer steuerelements](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**SCHRIFTARTEIGENSCHAFTEN \_ DER BENUTZEROBERFLÄCHE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Schriftart-Steuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 