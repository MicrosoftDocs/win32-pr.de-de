---
title: void-Attribut
description: Der Basistyp void gibt eine Prozedur ohne Argumente oder eine Prozedur an, die keinen Ergebniswert zurückgibt.
ms.assetid: a3eebfe7-bf43-4bab-b87b-9188a54ab9bf
keywords:
- void-Attribut-Mittel l
topic_type:
- apiref
api_name:
- void
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b14a5ae4a2325f840d8a840cb0a1bc5283bb4a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106339249"
---
# <a name="void-attribute"></a><span data-ttu-id="922a5-104">void-Attribut</span><span class="sxs-lookup"><span data-stu-id="922a5-104">void attribute</span></span>

<span data-ttu-id="922a5-105">Der Basistyp **void** gibt eine Prozedur ohne Argumente oder eine Prozedur an, die keinen Ergebniswert zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="922a5-105">The base type **void** indicates a procedure with no arguments or a procedure that does not return a result value.</span></span>

``` syntax
void function-name(parameter-list);

return-type function-name(void);

typedef [context_handle] void * context-handle-type;

return-type function-name(
    [context_handle] void * * context-handle-type
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="922a5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="922a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="922a5-107">*Funktionsname*</span><span class="sxs-lookup"><span data-stu-id="922a5-107">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="922a5-108">Gibt den Namen der Remote Prozedur an.</span><span class="sxs-lookup"><span data-stu-id="922a5-108">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="922a5-109">*Parameter-List*</span><span class="sxs-lookup"><span data-stu-id="922a5-109">*parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="922a5-110">Gibt die Liste der Parameter an, die an die Funktion übergeben werden, zusammen mit den zugeordneten Parametertypen und Parameter Attributen.</span><span class="sxs-lookup"><span data-stu-id="922a5-110">Specifies the list of parameters passed to the function along with the associated parameter types and parameter attributes.</span></span>

</dd> <dt>

<span data-ttu-id="922a5-111">*Rückgabetyp*</span><span class="sxs-lookup"><span data-stu-id="922a5-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="922a5-112">Gibt den Namen des Typs an, der von der Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="922a5-112">Specifies the name of the type returned by the function.</span></span>

</dd> <dt>

<span data-ttu-id="922a5-113">*Context-Handle-type*</span><span class="sxs-lookup"><span data-stu-id="922a5-113">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="922a5-114">Gibt den Namen des Typs an, der das **\[** [**Kontext \_ handle**](context-handle.md) - **\]** Attribut annimmt.</span><span class="sxs-lookup"><span data-stu-id="922a5-114">Specifies the name of the type that takes the **\[**[**context\_handle**](context-handle.md)**\]** attribute.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="922a5-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="922a5-115">Remarks</span></span>

<span data-ttu-id="922a5-116">Der Zeigertyp " **void \***", der in C einen generischen Zeiger beschreibt, der in einen beliebigen Zeigertyp umgewandelt werden kann, ist in der mittleren l auf seine Verwendung mit dem **\[ Kontext \_ handle \]** -Schlüsselwort begrenzt.</span><span class="sxs-lookup"><span data-stu-id="922a5-116">The pointer type **void \***, which in C describes a generic pointer that can be cast to represent any pointer type, is limited in MIDL to its use with the **\[context\_handle\]** keyword.</span></span>

## <a name="examples"></a><span data-ttu-id="922a5-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="922a5-117">Examples</span></span>

``` syntax
void VoidFunc1(void); 
HRESULT VoidFunc2([in, out] short s1); 
typedef [context_handle] void * MY_CX_HNDL_TYPE; 
HRESULT InitHandle([out] MY_CX_HNDL_TYPE * ppCxHndl);
```

## <a name="see-also"></a><span data-ttu-id="922a5-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="922a5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="922a5-119">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="922a5-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="922a5-120">**Kontext \_ handle**</span><span class="sxs-lookup"><span data-stu-id="922a5-120">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="922a5-121">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="922a5-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> </dl>

 

 




