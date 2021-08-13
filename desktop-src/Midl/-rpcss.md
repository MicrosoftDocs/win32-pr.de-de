---
title: /rpcss-Schalter
description: Der Schalter /rpcss verhält sich, wenn er angegeben wird, so, als ob das Attribut enable allocate für alle \_ Vorgänge der Schnittstelle angegeben wurde. Die Verwendung dieses Attributs wird nicht empfohlen.
ms.assetid: a4507779-7d07-4517-8592-39f0d9460bc3
keywords:
- /rpcss switch MIDL
topic_type:
- apiref
api_name:
- /rpcss
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e0c3087f47bd12c852ef168b2684d5b094239cdac45933c8e7d831fc6461c1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643740"
---
# <a name="rpcss-switch"></a>/rpcss-Schalter

Der **Schalter /rpcss** verhält sich, wenn er angegeben wird, so, als ob das [**Attribut enable \_ allocate**](enable-allocate.md) für alle Vorgänge der Schnittstelle angegeben wurde. Die Verwendung dieses Attributs wird nicht empfohlen.

``` syntax
midl /rpcss
```

## <a name="switch-options"></a>Switch-Optionen

Dieser Schalter verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

Im Standardmodus ist das RpcSs-Paket nur aktiviert, wenn entweder die Prozedur oder Schnittstelle über das [**Attribut enable \_ allocate**](enable-allocate.md) verfügt oder der **Schalter /rpcss** in der Befehlszeile angegeben ist. Im **/osf-Modus** aktiviert der serverseitige Stub das RpcSs-Zuordnungspaket.

## <a name="examples"></a>Beispiele

**midl /rpcss filename.idl**

## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[Schnittstellendefinitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**\_"Allocate" aktivieren**](enable-allocate.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 




