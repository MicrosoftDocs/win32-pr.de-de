---
title: UI_PKEY_TooltipTitle
description: Identifiziert die \_ PKEY \_ TooltipTitle-Eigenschaft der Benutzeroberfläche.
ms.assetid: ed9f422d-a782-4950-a579-060185550891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6a9e479d2f963acd4041d23e2b1ca075db609f9d45b556cd2aab34e6b2c6a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437785"
---
# <a name="ui_pkey_tooltiptitle"></a>UI \_ PKEY \_ TooltipTitle

Identifiziert die \_ PKEY \_ TooltipTitle-Eigenschaft der Benutzeroberfläche.

```
propertyDescription
   name = UI_PKEY_TooltipTitle
   shellPKey = UI_PKEY_TooltipTitle
   formatID = 00000006-7363-696e-8441798acf5aebb7
   propID = 6
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Hinweise

Ui \_ PKEY \_ TooltipTitle wird von einer Anwendung verwendet, um die QuickInfo von Registerkarten, Gruppen, Schaltflächen, Katalogelementen und anderen Menübandsteuerelementen abzufragen.

Der -Eigenschaftswert ist eine Zeichenfolge, die auf eine beliebige Zeichensequenz beschränkt ist, einschließlich Leerzeichen und Zeilenunterbrechungszeichen.

> [!Note]  
> Verwenden Sie den UCS-XML-Zeichenverweis (Universal Character Set), `&#xA;` um einen Zeilenbreak anzugeben.

 

Die rechte Ausrichtung wird nicht unterstützt.

Die maximale Länge von \_ PKEY TooltipTitle für die Benutzeroberfläche \_ ist nicht gebunden.

Um ein ampersand in einer QuickInfo anzuzeigen, escapen Sie die Sonderzeichenbezeichnung mit einem doppelten Ampersand ( `&&` ), wie im folgenden Beispiel gezeigt.


```XML
<Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourceneigenschaften](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)
</dt> <dt>

[UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 




