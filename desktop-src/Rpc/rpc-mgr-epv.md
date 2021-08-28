---
title: RPC_MGR_EPV (Rpcdce.h)
description: Der Rpc \_ MGR \_ EPV-Datentyp definiert einen Manager-Einstiegspunktvektor.
ms.assetid: 396e76de-065f-471e-ade9-34770b16a958
keywords:
- RPC_MGR_EPV RPC
topic_type:
- apiref
api_name:
- RPC_MGR_EPV
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55e40b883192adc53b11f9965f1a92f4637b320d32b5fd6909e2b6d615437a6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926294"
---
# <a name="rpc_mgr_epv"></a>RPC \_ MGR \_ EPV

Der Rpc **\_ MGR \_ EPV-Datentyp** definiert einen Manager-Einstiegspunktvektor.

``` syntax
typedef void RPC_MGR_EPV;
typedef _if-name_SERVER-EPV {
  return-type (* Functionname)  (param-list);
...  //one entry for each function in IDL file
} if-name_SERVER_EPV:
```

## <a name="members"></a>Member

<dl> <dt>

<span id="if-name"></span><span id="IF-NAME"></span>**if-name**
</dt> <dd>

Gibt den Namen der Schnittstelle an

</dd> <dt>

<span id="return-type"></span><span id="RETURN-TYPE"></span>**rückgabetyp**
</dt> <dd>

Gibt den Typ an, der von der funktion Functionname zurückgegeben wird, die in der **IDL-Datei** angegeben ist.

</dd> <dt>

<span id="Functionname"></span><span id="functionname"></span><span id="FUNCTIONNAME"></span>**Functionname**
</dt> <dd>

Gibt den Namen der Funktion an, die in der IDL-Datei angegeben ist.

</dd> <dt>

<span id="param-list"></span><span id="PARAM-LIST"></span>**param-list**
</dt> <dd>

Gibt die Parameter an, die für die Funktion Functionname in der **IDL-Datei** angegeben sind.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Manager-Einstiegspunktvektor (EPV) ist ein Array von Funktionszeigern. Das Array enthält Zeiger auf die Implementierungen der in der IDL-Datei angegebenen Funktionen. Die Anzahl der Elemente im Array wird auf die Anzahl von Funktionen festgelegt, die in der IDL-Datei angegeben sind. Eine Anwendung kann auch über mehrere EPVs verfügen, die mehrere Implementierungen der in der -Schnittstelle angegebenen Funktionen darstellen.

Der MIDL-Compiler generiert einen **EPV-Standarddatentyp** mit dem Namen *if-name***\_ SERVER \_ EPV,** wobei *if-name* den Schnittstellenbezeichner in der IDL-Datei angibt. Der MIDL-Compiler initialisiert diese **Standard-EPV** so, dass sie Funktionszeiger für jede der in der IDL-Datei angegebenen Prozeduren enthält.

Wenn der Server mehrere Implementierungen derselben Schnittstelle anbietet, muss die Serveranwendung für jede Implementierung der Schnittstelle eine Variable vom Typ *if-name** \_ SERVER \_ EPV** deklarieren und initialisieren. Jede **EPV** muss einen Einstiegspunkt (Funktionszeiger) für jede in der IDL-Datei definierte Prozedur enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Rpcdce.h (include Rpc.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> <dt>

[**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)
</dt> <dt>

[**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)
</dt> <dt>

[**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)
</dt> <dt>

[**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex)
</dt> </dl>

 

 





