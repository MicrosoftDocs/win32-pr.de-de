---
title: /oldnames-Schalter
description: Der Schalter /oldnames leitet den MIDL-Compiler an, Schnittstellennamen zu generieren, die die Versionsnummer nicht enthalten.
ms.assetid: 3a79c399-e115-46fd-9559-681b85cd872d
keywords:
- /oldnames switch MIDL
topic_type:
- apiref
api_name:
- /oldnames
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b7906878c7ba10681cbf361a4671370331fbcb5abee73eb212dcac4ab41443d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117992030"
---
# <a name="oldnames-switch"></a>/oldnames-Schalter

Der **Schalter /oldnames** leitet den MIDL-Compiler an, Schnittstellennamen zu generieren, die die Versionsnummer nicht enthalten.

``` syntax
midl /oldnames
```

## <a name="switch-options"></a>Switch-Optionen

Dieser Schalter verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

Der MIDL-Compiler integriert die Versionsnummer der Schnittstelle in den Schnittstellennamen, der im Stub generiert wird (z. B. iface \_ v1 \_ 0 \_ ServerIfHandle). Dieses Benennungsformat entspricht dem Format, das vom OSF-DCE-IDL-Compiler verwendet wird. Es unterscheidet sich jedoch vom Benennungsformat, das vom MIDL 1.0-Compiler verwendet wird. Der MIDL 1.0-Compiler hat keine Versionsnummern in Schnittstellennamen (z. B. iface \_ ServerIfHandle) enthalten. Mit **dem Schalter /oldnames** können Sie den MIDL-Compiler anweisen, Schnittstellennamen zu generieren, die die Versionsnummer nicht enthalten. Auf diese Weise entspricht das Format den Namen, die vom MIDL 1.0-Compiler generiert werden.

Wenn Sie über Serveranwendungscode verfügen, der für die Verwendung mit einem vom MIDL 1.0-Compiler generierten Stub geschrieben wurde und auf den von MIDL generierten Schnittstellennamen verweist (z. B. in einem Aufruf von [**RpcServerRegisterIf),**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)sollten Sie ihn ändern, um auf den Stil des Schnittstellennamens zu verweisen, der von Version 2.0 oder höher des MIDL-Compilers unterstützt wird. Alternativ können Sie beim Aufrufen des MIDL-Compilers den Schalter **/oldnames** verwenden.

## <a name="examples"></a>Beispiele

**midl /oldnames filename.idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> </dl>

 

 