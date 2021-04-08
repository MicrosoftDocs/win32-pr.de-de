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
# <a name="rpc_mgr_epv"></a><span data-ttu-id="eef4e-104">RPC- \_ Mgr- \_ EPV</span><span class="sxs-lookup"><span data-stu-id="eef4e-104">RPC\_MGR\_EPV</span></span>

<span data-ttu-id="eef4e-105">Der Datentyp **RPC \_ Mgr \_ EPV** definiert einen Manager-Einstiegspunkt Vektor.</span><span class="sxs-lookup"><span data-stu-id="eef4e-105">The data type **RPC\_MGR\_EPV** defines a manager entry-point vector.</span></span>

``` syntax
typedef void RPC_MGR_EPV;
typedef _if-name_SERVER-EPV {
  return-type (* Functionname)  (param-list);
...  //one entry for each function in IDL file
} if-name_SERVER_EPV:
```

## <a name="members"></a><span data-ttu-id="eef4e-106">Member</span><span class="sxs-lookup"><span data-stu-id="eef4e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="eef4e-107"><span id="if-name"></span><span id="IF-NAME"></span>**If-Name**</span><span class="sxs-lookup"><span data-stu-id="eef4e-107"><span id="if-name"></span><span id="IF-NAME"></span>**if-name**</span></span>
</dt> <dd>

<span data-ttu-id="eef4e-108">Gibt den Namen der Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="eef4e-108">Specifies the name of the interface</span></span>

</dd> <dt>

<span data-ttu-id="eef4e-109"><span id="return-type"></span><span id="RETURN-TYPE"></span>**Rückgabetyp**</span><span class="sxs-lookup"><span data-stu-id="eef4e-109"><span id="return-type"></span><span id="RETURN-TYPE"></span>**return-type**</span></span>
</dt> <dd>

<span data-ttu-id="eef4e-110">Gibt den Typ an, der von der in der IDL-Datei festgelegten **funktionname** -Funktion zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="eef4e-110">Specifies the type returned by the function **Functionname** indicated in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="eef4e-111"><span id="Functionname"></span><span id="functionname"></span><span id="FUNCTIONNAME"></span>**FunctionName**</span><span class="sxs-lookup"><span data-stu-id="eef4e-111"><span id="Functionname"></span><span id="functionname"></span><span id="FUNCTIONNAME"></span>**Functionname**</span></span>
</dt> <dd>

<span data-ttu-id="eef4e-112">Gibt den Namen der Funktion an, die in der IDL-Datei angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="eef4e-112">Specifies the name of the function indicated in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="eef4e-113"><span id="param-list"></span><span id="PARAM-LIST"></span>**param-Liste**</span><span class="sxs-lookup"><span data-stu-id="eef4e-113"><span id="param-list"></span><span id="PARAM-LIST"></span>**param-list**</span></span>
</dt> <dd>

<span data-ttu-id="eef4e-114">Gibt die Parameter an, die für den **funktionname** der Funktion in der IDL-Datei angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="eef4e-114">Specifies the parameters indicated for the function **Functionname** in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eef4e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eef4e-115">Remarks</span></span>

<span data-ttu-id="eef4e-116">Der Manager-Einstiegspunkt Vektor (EPV) ist ein Array von Funktions Zeigern.</span><span class="sxs-lookup"><span data-stu-id="eef4e-116">The manager entry-point vector (EPV) is an array of function pointers.</span></span> <span data-ttu-id="eef4e-117">Das Array enthält Zeiger auf die Implementierungen der Funktionen, die in der IDL-Datei angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="eef4e-117">The array contains pointers to the implementations of the functions specified in the IDL file.</span></span> <span data-ttu-id="eef4e-118">Die Anzahl der Elemente im-Array wird auf die Anzahl der in der IDL-Datei angegebenen Funktionen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eef4e-118">The number of elements in the array is set to the number of functions specified in the IDL file.</span></span> <span data-ttu-id="eef4e-119">Eine Anwendung kann auch über mehrere EPVs verfügen, die mehrere Implementierungen der Funktionen darstellen, die in der-Schnittstelle angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="eef4e-119">An application can also have multiple EPVs, representing multiple implementations of the functions specified in the interface.</span></span>

<span data-ttu-id="eef4e-120">Der mittlerer l-Compiler generiert einen **EPV** -Standard Datentyp namens \* If-Name \***\_ Server \_ EPV**, wobei *if-Name* den Schnittstellen Bezeichner in der IDL-Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="eef4e-120">The MIDL compiler generates a default **EPV** data type named \*if-name\***\_SERVER\_EPV**, where *if-name* specifies the interface identifier in the IDL file.</span></span> <span data-ttu-id="eef4e-121">Der mittlerer l-Compiler initialisiert diesen Standard- **EPV** , um Funktionszeiger für jede der Prozeduren zu enthalten, die in der IDL-Datei angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="eef4e-121">The MIDL compiler initializes this default **EPV** to contain function pointers for each of the procedures specified in the IDL file.</span></span>

<span data-ttu-id="eef4e-122">Wenn der Server mehrere Implementierungen derselben Schnittstelle bietet, muss die Serveranwendung eine Variable vom Typ " \*if-Name \* \* \* \_ Server \_ EPV\*\*" für jede Implementierung der Schnittstelle deklarieren und initialisieren.</span><span class="sxs-lookup"><span data-stu-id="eef4e-122">When the server offers multiple implementations of the same interface, the server application must declare and initialize one variable of type *if-name\*\*\*\_SERVER\_EPV*\* for each implementation of the interface.</span></span> <span data-ttu-id="eef4e-123">Jeder **EPV** muss einen Einstiegspunkt (Funktionszeiger) für jede Prozedur enthalten, die in der IDL-Datei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="eef4e-123">Each **EPV** must contain one entry point (function pointer) for each procedure defined in the IDL file.</span></span>

## <a name="requirements"></a><span data-ttu-id="eef4e-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eef4e-124">Requirements</span></span>



| <span data-ttu-id="eef4e-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eef4e-125">Requirement</span></span> | <span data-ttu-id="eef4e-126">Wert</span><span class="sxs-lookup"><span data-stu-id="eef4e-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eef4e-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eef4e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="eef4e-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eef4e-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="eef4e-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eef4e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="eef4e-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eef4e-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="eef4e-131">Header</span><span class="sxs-lookup"><span data-stu-id="eef4e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="eef4e-132"><dt>Rpcdce. h (Include RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eef4e-132"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eef4e-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eef4e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eef4e-134">**RpcServerRegisterIf**</span><span class="sxs-lookup"><span data-stu-id="eef4e-134">**RpcServerRegisterIf**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> <dt>

[<span data-ttu-id="eef4e-135">**RpcServerRegisterIf2**</span><span class="sxs-lookup"><span data-stu-id="eef4e-135">**RpcServerRegisterIf2**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)
</dt> <dt>

[<span data-ttu-id="eef4e-136">**RpcServerRegisterIfEx**</span><span class="sxs-lookup"><span data-stu-id="eef4e-136">**RpcServerRegisterIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)
</dt> <dt>

[<span data-ttu-id="eef4e-137">**Rpcserverunregisterif**</span><span class="sxs-lookup"><span data-stu-id="eef4e-137">**RpcServerUnregisterIf**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)
</dt> <dt>

[<span data-ttu-id="eef4e-138">**Rpcserverunregisterifex**</span><span class="sxs-lookup"><span data-stu-id="eef4e-138">**RpcServerUnregisterIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex)
</dt> </dl>

 

 





