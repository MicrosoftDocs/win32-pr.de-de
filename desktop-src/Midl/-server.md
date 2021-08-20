---
title: /server switch
description: Der Schalter /server weist den MIDL-Compiler an, serverseitige C-Quelldateien für eine RPC-Schnittstelle zu generieren.
ms.assetid: c5ca6a47-e8b0-4a13-ba73-2d35a9ac8240
keywords:
- /server switch MIDL
topic_type:
- apiref
api_name:
- /server
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bf634e9ce91e937ff1e43b9059d12181dc723695139001ec368109d6fdf4a3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067470"
---
# <a name="server-switch"></a>/server switch

Der Schalter **/server** weist den MIDL-Compiler an, serverseitige C-Quelldateien für eine RPC-Schnittstelle zu generieren.

``` syntax
midl /server { stub | none }
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span id="stub"></span><span id="STUB"></span>stub**


</dt> <dd>

Generiert die serverseitigen Dateien.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>none(


</dt> <dd>

Generiert keine serverseitigen Dateien.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn der Schalter **/server** nicht angegeben ist, generiert der MIDL-Compiler die Serverstubdatei. Dieser Schalter wirkt sich nicht auf OLE-Schnittstellen aus.

Die Option **none** bewirkt, dass keine Dateien generiert werden.

Der Schalter **/server** hat Vorrang vor dem Schalter **/sstub.**

## <a name="examples"></a>Beispiele

**midl /server none**

**midl /server stub**

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**/client**](-client.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




