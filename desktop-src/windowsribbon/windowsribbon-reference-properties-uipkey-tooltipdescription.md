---
title: UI_PKEY_TooltipDescription
description: Bezeichnet die UI \_ pkey- \_ tooltipdescription-Eigenschaft.
ms.assetid: 658e798a-f41e-4538-94ac-38a9cb20dd74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 900610c1302d3cc904dcde2d7c86801982fd4d10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340867"
---
# <a name="ui_pkey_tooltipdescription"></a>UI- \_ pkey- \_ tooltipdescription

Bezeichnet die UI \_ pkey- \_ tooltipdescription-Eigenschaft.

```
propertyDescription
   name = UI_PKEY_TooltipDescription
   shellPKey = UI_PKEY_TooltipDescription
   formatID = 00000005-7363-696e-8441798acf5aebb7
   propID = 5
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Bemerkungen

UI \_ pkey \_ tooltipdescription wird von einer Anwendung verwendet, um die einem [UI- \_ pkey- \_ ToolTipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)zugeordnete Beschreibung abzufragen.

Der Eigenschafts Wert ist eine Zeichenfolge, die auf eine beliebige Sequenz von Zeichen beschränkt ist, einschließlich Leerzeichen und Zeilenumbruch Zeichen.

> [!Note]  
> Verwenden Sie den XML-Zeichen Verweis Universal Character Set (UCS) `&#xA;` , um einen Zeilenumbruch anzugeben.

 

Die maximale Länge der UI \_ pkey- \_ tooltipdescription ist unbegrenzt.

Die Rechte Ausrichtung wird nicht unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen Eigenschaften](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command. tooltipdescription**](windowsribbon-element-command-tooltipdescription.md)
</dt> <dt>

[UI- \_ pkey- \_ ToolTipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)
</dt> </dl>

 

 




