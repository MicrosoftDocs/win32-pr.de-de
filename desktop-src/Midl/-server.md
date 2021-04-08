---
title: /Server-Schalter
description: Der/Server-Schalter leitet den Mittelwert Compiler zum Generieren serverseitiger C-Quelldateien für eine RPC-Schnittstelle.
ms.assetid: c5ca6a47-e8b0-4a13-ba73-2d35a9ac8240
keywords:
- /Server-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /server
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31449133fa795a90d1f11d8c06b960b74909548d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038006"
---
# <a name="server-switch"></a>/Server-Schalter

Der **/Server** -Schalter leitet den Mittelwert Compiler zum Generieren serverseitiger C-Quelldateien für eine RPC-Schnittstelle.

``` syntax
midl /server { stub | none }
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span id="stub"></span><span id="STUB"></span>Stub * * * *


</dt> <dd>

Generiert die serverseitigen Dateien.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>keine * * * *


</dt> <dd>

Generiert keine serverseitigen Dateien.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn der **/Server** -Schalter nicht angegeben wird, generiert der kompil-Compiler die Server-Stub-Datei. Dieser Schalter wirkt sich nicht auf OLE-Schnittstellen aus.

Die Option **None** bewirkt, dass keine Dateien generiert werden.

Der **/Server** -Schalter hat Vorrang vor dem **/sstub** -Schalter.

## <a name="examples"></a>Beispiele

**Mittel l/Server keine**

**Mittel l/Server Stub**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Client**](-client.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




