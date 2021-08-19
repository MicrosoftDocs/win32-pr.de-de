---
title: /use_epv Schalter
description: Der Schalter /use epv leitet den MIDL-Compiler an, Serverstubcode zu generieren, der die Serveranwendungsroutine über einen Einstiegspunktvektor (epv) anstatt durch einen statischen \_ Aufruf aufruft. Die Verwendung dieses Attributs wird nicht empfohlen.
ms.assetid: 2853d836-ded3-412a-916b-1143968123a2
keywords:
- /use_epv MIDL-Switch
topic_type:
- apiref
api_name:
- /use_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 614abaf4c124aa0a6e1ca5f7da347ab4a9a2264e174c91734e6a75b188500a3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014058"
---
# <a name="use_epv-switch"></a>/use \_ epv-Schalter

Der **Schalter /use \_ epv** leitet den MIDL-Compiler an, Serverstubcode zu generieren, der die Serveranwendungsroutine über einen Einstiegspunktvektor (epv) anstatt durch einen statischen Aufruf aufruft. Die Verwendung dieses Attributs wird nicht empfohlen.

``` syntax
midl /use_epv
```

## <a name="switch-options"></a>Switch-Optionen

Dieser Schalter verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

In der Regel erfordern Anwendungen eine statische Verknüpfung mit der Serveranwendungsroutine. Der MIDL-Compiler generiert standardmäßig einen solchen Aufruf. Wenn eine Anwendung jedoch erfordert, dass der Serverstub die Serveranwendungsroutine mithilfe von epv aufruft, muss der **Schalter /use \_ epv** angegeben werden. Wenn der **Schalter /use \_ epv** angegeben wird, generiert der MIDL-Compiler eine Standard-epv. Diese epv-Standardeinstellung wird dann verwendet, wenn die Anwendung keine weitere epv über den [**RpcServerRegisterIf-Aufruf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) registriert.

## <a name="examples"></a>Beispiele

**midl /use \_ epv** *filename**.idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**/no \_ default \_ epv**](-no-default-epv.md)
</dt> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 