---
title: UI_PKEY_LabelDescription
description: Identifiziert die \_ PKEY \_ LabelDescription-Eigenschaft der Benutzeroberfläche.
ms.assetid: e7dfbe7e-c9c9-44fe-9e2d-39e20f5f7062
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80a2db487988f66fcc393b3ba449dfda789248dabc3cd9e1d3e48acf9ba3473
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437997"
---
# <a name="ui_pkey_labeldescription"></a>UI \_ PKEY \_ LabelDescription

Identifiziert die \_ PKEY \_ LabelDescription-Eigenschaft der Benutzeroberfläche.

```
propertyDescription
   name = UI_PKEY_LabelDescription
   shellPKey = UI_PKEY_LabelDescription
   formatID = 00000002-7363-696e-8441798acf5aebb7
   propID = 2
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Hinweise

Ui PKEY LabelDescription wird von einer Anwendung verwendet, um die Beschreibung abfragt, \_ \_ die einer [ \_ PKEY-Bezeichnung der Benutzeroberfläche \_ zugeordnet ist.](windowsribbon-reference-properties-uipkey-label.md)

Der -Eigenschaftswert ist eine Zeichenfolge, die auf eine beliebige Folge von Zeichen beschränkt ist, einschließlich Leerzeichen und Zeilenumbruchzeichen.

> [!Note]  
> Verwenden Sie den UCS-XML-Zeichenverweis (Universal Character Set), `&#xA;` um einen Zeilenumbruch anzugeben.

 

Die maximale Länge ist ungebunden.

Die richtige Ausrichtung wird nicht unterstützt.

Der folgende Screenshot veranschaulicht die Verwendung einer Bezeichnung und einer zugehörigen Bezeichnungsbeschreibung in einem Anwendungsmenü.

![Screenshot, der eine Bezeichnung und eine zugehörige Bezeichnungsbeschreibung in einem Anwendungsmenü zeigt.](images/properties/ui-pkey-labeldescription.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourceneigenschaften](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md)
</dt> <dt>

[\_PKEY-Bezeichnung der \_ Benutzeroberfläche](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 




