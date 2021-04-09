---
title: /no_default_epv Schalter
description: Der/No \_ Standard- \_ EPV-Switch weist den Mittelwert-Compiler an, keinen Standard-Einstiegspunkt Vektor (EPV) zu generieren. Die Verwendung dieses Attributs wird nicht empfohlen.
ms.assetid: 160b5fd3-cd9c-4f51-8c35-6cddab120021
keywords:
- /no_default_epv-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /no_default_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0a6e39319c5f03c1cd41959a009307b07bef66f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948629"
---
# <a name="no_default_epv-switch"></a>/No \_ Standard- \_ EPV-Switch

Der **/No \_ Standard- \_ EPV** -Switch weist den Mittelwert-Compiler an, keinen Standard-Einstiegspunkt Vektor (EPV) zu generieren. Die Verwendung dieses Attributs wird nicht empfohlen.

``` syntax
midl /no_default_epv
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Switch hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

In diesem Fall muss die Anwendung einen EPV mit dem [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) -Befehl registrieren. Vergleichen Sie diesen Switch mit dem [**/verwenden Sie " \_ EPV**](-use-epv.md) -Switch.

## <a name="examples"></a>Beispiele

**Mittel l/No \_ standardmäßiger \_ EPV-Dateiname. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/Verwenden Sie " \_ EPV**](-use-epv.md)
</dt> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 