---
title: /no_robust-Schalter
description: Der Schalter /no robust weist den MIDL-Compiler an, das Befehlszeilenfeature \_ /robust explizit zu deaktivieren. Der Befehlszeilenschalter /robust und die zugehörigen Features sind die Standardcompilereinstellung für MIDL Version 6.0.359 und höher.
ms.assetid: 17ece05a-d39d-4465-8553-199a45c8c073
keywords:
- /no_robust MIDL-Switch
topic_type:
- apiref
api_name:
- /no_robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1078a3eec25d6b6fdf44268ae915c20e7a2a9cf0c07a29730461bd544a7a0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808855"
---
# <a name="no_robust-switch"></a>/no \_ robust switch

Der **Schalter /no \_ robust** weist den MIDL-Compiler an, das Befehlszeilenfeature [**/robust**](-robust.md) explizit zu deaktivieren. Der **Befehlszeilenschalter /robust** und die zugehörigen Features sind die Standardcompilereinstellung für MIDL Version 6.0.359 und höher.

``` syntax
midl /no_robust
```

## <a name="switch-options"></a>Switch-Optionen

Dieser Schalter verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

Ab MIDL-Version 6.0.359 legt der MIDL-Compiler [**standardmäßig /robust**](-robust.md) fest. Der **Befehlszeilenschalter /no \_ robust** muss verwendet werden, um das **Feature /robust** zu deaktivieren, wenn generierte Stubs unter Microsoft Windows NT, Windows 95/98 oder Windows Ausgeführt werden müssen.

## <a name="examples"></a>Beispiele

**midl /no \_ robust filename.idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> </dl>

 

 




