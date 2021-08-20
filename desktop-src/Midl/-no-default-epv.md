---
title: /no_default_epv Switch
description: Der Schalter /no \_ default \_ epv weist den MIDL-Compiler an, keinen standardmäßigen Einstiegspunktvektor (epv) zu generieren. Die Verwendung dieses Attributs wird nicht empfohlen.
ms.assetid: 160b5fd3-cd9c-4f51-8c35-6cddab120021
keywords:
- /no_default_epv Switch MIDL
topic_type:
- apiref
api_name:
- /no_default_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69400ca5e3abfe73254648042e8b9f969f1ed9cf370407b38fdc42bcad5d4903
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117992185"
---
# <a name="no_default_epv-switch"></a>/no \_ default \_ epv switch

Der **Schalter /no \_ default \_ epv** weist den MIDL-Compiler an, keinen standardmäßigen Einstiegspunktvektor (epv) zu generieren. Die Verwendung dieses Attributs wird nicht empfohlen.

``` syntax
midl /no_default_epv
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Schalter verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

In diesem Fall muss die Anwendung einen epv beim [**RpcServerRegisterIf-Aufruf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) registrieren. Vergleichen Sie diesen Schalter mit dem Schalter [**/use \_ epv.**](-use-epv.md)

## <a name="examples"></a>Beispiele

**midl /no \_ default \_ epv filename.idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**/use \_ epv**](-use-epv.md)
</dt> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 