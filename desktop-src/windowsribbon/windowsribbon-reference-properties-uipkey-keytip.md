---
title: UI_PKEY_Keytip
description: Identifiziert die \_ PKEY \_ Keytip-Eigenschaft der Benutzeroberfläche.
ms.assetid: 7af4abcb-abb0-466a-bc58-274fa18b79af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 940a855561dfd30dfbf063323f4b86b03561163c4fbf34f9db08be4eb3e1ece3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028608"
---
# <a name="ui_pkey_keytip"></a>\_PKEY-Keytip der Benutzeroberfläche \_

Identifiziert die \_ PKEY \_ Keytip-Eigenschaft der Benutzeroberfläche.

```
propertyDescription
   name = UI_PKEY_Keytip
   shellPKey = UI_PKEY_Keytip
   formatID = 00000003-7363-696e-8441798acf5aebb7
   propID = 3
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Hinweise

Die PKEY-Keytip der Benutzeroberfläche \_ wird von einer Anwendung \_ verwendet, um die Tastaturbeschleunigung eines Menübandsteuerelements abzufragen.

Dieser Eigenschaftswert ist eine Zeichenfolge, die aus einer beliebigen Sequenz von Zeichen einschließlich Leerzeichen besteht.

Der Wert von \_ UI PKEY \_ Keytip fungiert als Tastaturbeschleunigung für einen Befehl, es sei denn, dieser Befehl wird über ein Menüelement verfügbar gemacht. In diesem Fall ignoriert das Framework den PKEY Keytip-Wert der Benutzeroberfläche \_ \_ und verwendet stattdessen ein Zeichen, dem ein ampersand vorangestellt ist, wie von [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) oder [UI \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md)angegeben. Wenn kein ampersand durch **Command.LabelTitle** oder UI PKEY Label angegeben \_ \_ wird, wird keine Keytip oder Tastaturtaste verfügbar gemacht.

Die maximale Länge von PKEY Keytip der Benutzeroberfläche \_ \_ ist nicht gebunden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourceneigenschaften](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command.Keytip**](windowsribbon-element-command-keytip.md)
</dt> </dl>

 

 




