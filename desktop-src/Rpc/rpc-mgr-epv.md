---
title: RPC_MGR_EPV (rpcdce. h)
description: Der Datentyp RPC \_ Mgr \_ EPV definiert einen Manager-Einstiegspunkt Vektor.
ms.assetid: 396e76de-065f-471e-ade9-34770b16a958
keywords:
- RPC-RPC_MGR_EPV
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
ms.openlocfilehash: 549ca4b5245b12bda07b46407041a01175955693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740216"
---
# <a name="rpc_mgr_epv"></a>RPC- \_ Mgr- \_ EPV

Der Datentyp **RPC \_ Mgr \_ EPV** definiert einen Manager-Einstiegspunkt Vektor.

``` syntax
typedef void RPC_MGR_EPV;
typedef _if-name_SERVER-EPV {
  return-type (* Functionname)  (param-list);
...  //one entry for each function in IDL file
} if-name_SERVER_EPV:
```

## <a name="members"></a>Member

<dl> <dt>

<span id="if-name"></span><span id="IF-NAME"></span>**If-Name**
</dt> <dd>

Gibt den Namen der Schnittstelle an.

</dd> <dt>

<span id="return-type"></span><span id="RETURN-TYPE"></span>**Rückgabetyp**
</dt> <dd>

Gibt den Typ an, der von der in der IDL-Datei festgelegten **funktionname** -Funktion zurückgegeben wird

</dd> <dt>

<span id="Functionname"></span><span id="functionname"></span><span id="FUNCTIONNAME"></span>**FunctionName**
</dt> <dd>

Gibt den Namen der Funktion an, die in der IDL-Datei angegeben ist.

</dd> <dt>

<span id="param-list"></span><span id="PARAM-LIST"></span>**param-Liste**
</dt> <dd>

Gibt die Parameter an, die für den **funktionname** der Funktion in der IDL-Datei angegeben sind.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Manager-Einstiegspunkt Vektor (EPV) ist ein Array von Funktions Zeigern. Das Array enthält Zeiger auf die Implementierungen der Funktionen, die in der IDL-Datei angegeben sind. Die Anzahl der Elemente im-Array wird auf die Anzahl der in der IDL-Datei angegebenen Funktionen festgelegt. Eine Anwendung kann auch über mehrere EPVs verfügen, die mehrere Implementierungen der Funktionen darstellen, die in der-Schnittstelle angegeben sind.

Der mittlerer l-Compiler generiert einen **EPV** -Standard Datentyp namens * If-Name ***\_ Server \_ EPV**, wobei *if-Name* den Schnittstellen Bezeichner in der IDL-Datei angibt. Der mittlerer l-Compiler initialisiert diesen Standard- **EPV** , um Funktionszeiger für jede der Prozeduren zu enthalten, die in der IDL-Datei angegeben sind.

Wenn der Server mehrere Implementierungen derselben Schnittstelle bietet, muss die Serveranwendung eine Variable vom Typ " *if-Name * * * \_ Server \_ EPV**" für jede Implementierung der Schnittstelle deklarieren und initialisieren. Jeder **EPV** muss einen Einstiegspunkt (Funktionszeiger) für jede Prozedur enthalten, die in der IDL-Datei definiert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Rpcdce. h (Include RPC. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> <dt>

[**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)
</dt> <dt>

[**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)
</dt> <dt>

[**Rpcserverunregisterif**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)
</dt> <dt>

[**Rpcserverunregisterifex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex)
</dt> </dl>

 

 





