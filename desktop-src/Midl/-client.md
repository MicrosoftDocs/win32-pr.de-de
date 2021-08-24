---
title: /client switch
description: Der Schalter /client leitet den MIDL-Compiler an, clientseitige C-Quelldateien für eine RPC-Schnittstelle zu generieren.
ms.assetid: bce5af72-2201-4b42-9348-cb97f08b7fdf
keywords:
- /client switch MIDL
topic_type:
- apiref
api_name:
- /client
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8361a41aa0e7c87c42eb41508fee0973d6fd4dd821e2008aa2148c8460fc63ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764360"
---
# <a name="client-switch"></a>/client switch

Der **Schalter /client** leitet den MIDL-Compiler an, clientseitige C-Quelldateien für eine RPC-Schnittstelle zu generieren.

``` syntax
midl /client { stub | none }
```

## <a name="switch-options"></a>Switch-Optionen

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span id="stub"></span><span id="STUB"></span>stub**


</dt> <dd>

Generiert die clientseitigen Dateien.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>none**


</dt> <dd>

Generiert keine clientseitigen Dateien.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn der **Schalter /client** nicht angegeben ist, generiert der MIDL-Compiler die Clientstubdatei. Dieser Schalter wirkt sich nicht auf OLE-Schnittstellen aus.

Der **Schalter /client** hat Vorrang vor dem [**Schalter /cstub.**](-cstub.md)

## <a name="examples"></a>Beispiele

**midl /client none filename.idl**

**midl /client stub filename.idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/server**](-server.md)
</dt> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




