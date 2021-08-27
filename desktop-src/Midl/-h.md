---
title: /h-Schalter
description: Die Option /h entspricht funktional der Option /header.
ms.assetid: 1b74d5f2-6624-4b71-832d-fb55a0e84c86
keywords:
- /h switch MIDL
topic_type:
- apiref
api_name:
- /h
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71bf02668a583b330684338cbc3f639fbbda5a340c7226e10956233aa8dc9ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105610"
---
# <a name="h-switch"></a>/h-Schalter

Die Option **/h** entspricht funktional der Option [**/header.**](-header.md)

``` syntax
midl /h filename
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*filename* 
</dt> <dd>

Gibt einen Headerdateinamen an, der den Standardnamen der Headerdatei überschreibt. Dateinamen können explizit mit doppelten Anführungszeichen (") angegeben werden, um zu verhindern, dass die Shell Sonderzeichen interpretiert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Schalter **/h** gibt *dateiname* als Namen für eine Headerdatei an, die alle definitionen enthält, die in der IDL-Datei enthalten sind, ohne die IDL-Syntax. Diese Datei kann als C- oder C++-Headerdatei verwendet werden.

## <a name="examples"></a>Beispiele

**midl /h tlibhead.h filename.idl**

**midl /h "midl.h" filename.idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**/header**](-header.md)
</dt> </dl>

 

 




