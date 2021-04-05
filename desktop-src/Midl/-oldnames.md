---
title: /OLDNAMES-Schalter
description: Der/OLDNAMES-Schalter leitet den Mittelwert Compiler an, um Schnittstellennamen zu generieren, die die Versionsnummer nicht enthalten.
ms.assetid: 3a79c399-e115-46fd-9559-681b85cd872d
keywords:
- /OLDNAMES-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /oldnames
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44cf861d2bf4f4123d7a1ee103e6966e5d404946
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725448"
---
# <a name="oldnames-switch"></a>/OLDNAMES-Schalter

Der **/OLDNAMES** -Schalter leitet den Mittelwert Compiler an, um Schnittstellennamen zu generieren, die die Versionsnummer nicht enthalten.

``` syntax
midl /oldnames
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Switch hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

Der mittlerer l-Compiler integriert die Versionsnummer der Schnittstelle in den Schnittstellennamen, der im Stub generiert wird (z. b. iface \_ v1 \_ 0 \_ serveribhandle). Dieses Benennungs Format entspricht dem Format, das vom OSF-DCE-IDL-Compiler verwendet wird. Es unterscheidet sich jedoch von dem Namensformat, das vom-Compiler von "Mittel l 1,0" verwendet wird. Der Compiler für die Mittel l 1,0 enthielt keine Versionsnummern in Schnittstellennamen (z. b. iface \_ serveribhandle). Der **/OLDNAMES** -Schalter ermöglicht es Ihnen, den Mittelwert Compiler anzuweisen, Schnittstellennamen zu generieren, die die Versionsnummer nicht enthalten. Auf diese Weise ist das Format mit den Namen konsistent, die vom compl 1,0-Compiler generiert werden.

Wenn Sie über einen Server Anwendungscode verfügen, der für die Verwendung mit einem Stub geschrieben wurde, der vom Mittel l 1,0-Compiler generiert wurde, und der sich auf den von der Mitte generierten Schnittstellennamen bezieht (z. b. in einem Aufrufen von [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)), sollten Sie ihn so ändern, dass er auf den Stil des Schnittstellen namens verweist, der von Version 2,0 Alternativ können Sie den Schalter **/OLDNAMES** verwenden, wenn Sie den Mittel l-Compiler aufrufen.

## <a name="examples"></a>Beispiele

**Mittel l/OLDNAMES Dateiname. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 