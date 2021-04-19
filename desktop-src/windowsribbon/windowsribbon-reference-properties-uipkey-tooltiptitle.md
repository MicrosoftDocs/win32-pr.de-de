---
title: UI_PKEY_TooltipTitle
description: Bezeichnet die Benutzeroberflächen- \_ pkey- \_ ToolTipTitle-Eigenschaft.
ms.assetid: ed9f422d-a782-4950-a579-060185550891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e62fe9ebdb6418f5790e0073e32e81d7f7aba75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341469"
---
# <a name="ui_pkey_tooltiptitle"></a>UI- \_ pkey- \_ ToolTipTitle

Bezeichnet die Benutzeroberflächen- \_ pkey- \_ ToolTipTitle-Eigenschaft.

```
propertyDescription
   name = UI_PKEY_TooltipTitle
   shellPKey = UI_PKEY_TooltipTitle
   formatID = 00000006-7363-696e-8441798acf5aebb7
   propID = 6
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Bemerkungen

\_Der UI pkey \_ -ToolTipTitle wird von einer Anwendung verwendet, um die QuickInfo von Registerkarten, Gruppen, Schaltflächen, Galerie Elementen und anderen Menü Band Steuerelementen abzufragen.

Der Eigenschafts Wert ist eine Zeichenfolge, die auf eine beliebige Sequenz von Zeichen beschränkt ist, einschließlich Leerzeichen und Zeilenumbruch Zeichen.

> [!Note]  
> Verwenden Sie den XML-Zeichen Verweis Universal Character Set (UCS) `&#xA;` , um einen Zeilenumbruch anzugeben.

 

Die Rechte Ausrichtung wird nicht unterstützt.

Die maximale Länge des UI- \_ pkey- \_ ToolTipTitle ist unbegrenzt.

Um ein kaufmännisches und-Zeichen in einer QuickInfo anzuzeigen, versehen Sie die Bezeichnung für Sonderzeichen mit einem doppelten kaufmännisches und-Zeichen ( `&&` ), wie im folgenden Beispiel gezeigt.


```XML
<Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen Eigenschaften](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command. ToolTipTitle**](windowsribbon-element-command-tooltiptitle.md)
</dt> <dt>

[UI- \_ pkey- \_ tooltipdescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 




