---
title: /use_epv Schalter
description: Der/verwenden Sie " \_ EPV-Switch leitet den Mittelwert Compiler zum Generieren von Server-Stub-Code, der die Server Anwendungs Routine über einen Einstiegspunkt Vektor (EPV) aufruft, anstelle eines statischen Aufrufs. Die Verwendung dieses Attributs wird nicht empfohlen.
ms.assetid: 2853d836-ded3-412a-916b-1143968123a2
keywords:
- /use_epv-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /use_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec73b5cb9833c15a77c96a784e1ded88d266f9a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106341926"
---
# <a name="use_epv-switch"></a>/Verwenden Sie " \_ EPV-Switch

Der **/verwenden Sie " \_ EPV** -Switch leitet den Mittelwert Compiler zum Generieren von Server-Stub-Code, der die Server Anwendungs Routine über einen Einstiegspunkt Vektor (EPV) aufruft, anstelle eines statischen Aufrufs. Die Verwendung dieses Attributs wird nicht empfohlen.

``` syntax
midl /use_epv
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Switch hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

Anwendungen erfordern in der Regel eine statische Verknüpfung mit der Server Anwendungs Routine. Der mittlerer l-Compiler generiert einen solchen-Aufrufwert standardmäßig. Wenn eine Anwendung jedoch erfordert, dass der Serverstub die Server Anwendungs Routine mithilfe von EPV aufruft, muss der **/verwenden Sie " \_ EPV** -Switch angegeben werden. Wenn der **/verwenden Sie " \_ EPV** -Schalter angegeben wird, generiert der-compilercompiler einen EPV-Standardwert. Dieser Standard-EPV wird dann verwendet, wenn die Anwendung keinen anderen EPV über den [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) -Befehl registriert.

## <a name="examples"></a>Beispiele

**Mittel l/verwenden Sie " \_ EPV** *filename * * *. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/No \_ Standard- \_ EPV**](-no-default-epv.md)
</dt> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 