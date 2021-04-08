---
title: ms_union-Attribut
description: Das Schlüsselwort \ MS \_ Union \ wird zum Steuern der NDR-Ausrichtung von nicht gekapselten Unions verwendet.
ms.assetid: 20ac2985-4552-4224-b03b-07378a2c0cdf
keywords:
- Ms_union Attribut-Mittel l
topic_type:
- apiref
api_name:
- ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7ad9b750027163aef806f5a66e51f87874a0ad2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037816"
---
# <a name="ms_union-attribute"></a><span data-ttu-id="db9ed-104">MS- \_ Union-Attribut</span><span class="sxs-lookup"><span data-stu-id="db9ed-104">ms\_union attribute</span></span>

<span data-ttu-id="db9ed-105">Das Schlüsselwort " \[ **MS \_ Union** " \] wird zum Steuern der NDR-Ausrichtung von nicht gekapselten Unions verwendet.</span><span class="sxs-lookup"><span data-stu-id="db9ed-105">The keyword \[**ms\_union**\] is used to control the NDR alignment of nonencapsulated unions.</span></span>

``` syntax
[
    ms_union,
    ...
]
interface interface-name 
{
    ...
}

[ms_union] procedure-type procedure-name(param-list);
```

## <a name="parameters"></a><span data-ttu-id="db9ed-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="db9ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db9ed-107">*Schnittstellen Name*</span><span class="sxs-lookup"><span data-stu-id="db9ed-107">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="db9ed-108">Gibt den Namen der Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="db9ed-108">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="db9ed-109">*Prozedurtyp*</span><span class="sxs-lookup"><span data-stu-id="db9ed-109">*procedure-type*</span></span> 
</dt> <dd>

<span data-ttu-id="db9ed-110">Gibt den Rückgabetyp der Prozedur an, auf die das Attribut angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="db9ed-110">Specifies the return type of the procedure to which the attribute is being applied.</span></span>

</dd> <dt>

<span data-ttu-id="db9ed-111">*Prozedur Name*</span><span class="sxs-lookup"><span data-stu-id="db9ed-111">*procedure-name*</span></span> 
</dt> <dd>

<span data-ttu-id="db9ed-112">Gibt den Namen der Prozedur an.</span><span class="sxs-lookup"><span data-stu-id="db9ed-112">Specifies the name of the procedure.</span></span>

</dd> <dt>

<span data-ttu-id="db9ed-113">*param-Liste*</span><span class="sxs-lookup"><span data-stu-id="db9ed-113">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="db9ed-114">Gibt die Parameterliste der Prozedur an, die möglicherweise leer ist.</span><span class="sxs-lookup"><span data-stu-id="db9ed-114">Specifies the procedure's parameter list, which may be empty.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db9ed-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db9ed-115">Remarks</span></span>

<span data-ttu-id="db9ed-116">Verwenden Sie diesen Switch oder dieses Attribut niemals mit neuen Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="db9ed-116">Never use this switch or attribute with new interfaces.</span></span> <span data-ttu-id="db9ed-117">Dies ist nur ein abwärts Kompatibilitäts Feature. Der mittlerer l-Compiler in dieser Version von Microsoft RPC spiegelt das Verhalten des OSF-DCE-IDL-Compilers für nicht gekapselte Unions wider.</span><span class="sxs-lookup"><span data-stu-id="db9ed-117">This is a backward compatibility feature only.The MIDL compiler in this version of Microsoft RPC mirrors the behavior of the OSF DCE IDL compiler for nonencapsulated unions.</span></span> <span data-ttu-id="db9ed-118">Da jedoch frühere Versionen des Mittel l-Compilers dies nicht getan haben, bietet der [**/MS \_ Union**](-ms-union.md) -Switch Kompatibilität mit Schnittstellen, die auf früheren Versionen des Mittel l-Compilers erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="db9ed-118">However, because earlier versions of the MIDL compiler did not do so, the [**/ms\_union**](-ms-union.md) switch provides compatibility with interfaces built on previous versions of the MIDL compiler.</span></span>

<span data-ttu-id="db9ed-119">Die **MS- \_ Union** -Funktion kann als idl-Schnittstellen Attribut, IDL-Typattribut oder als Befehls Zeilenschalter ( [**/MS \_ Union**](-ms-union.md)) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="db9ed-119">The **ms\_union** feature can be used as an IDL interface attribute, an IDL type attribute, or as a command-line switch ( [**/ms\_union**](-ms-union.md)).</span></span>

## <a name="examples"></a><span data-ttu-id="db9ed-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="db9ed-120">Examples</span></span>

``` syntax
[ms_union] long procedure (...);
```

## <a name="see-also"></a><span data-ttu-id="db9ed-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="db9ed-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db9ed-122">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="db9ed-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="db9ed-123">**/MS- \_ Union**</span><span class="sxs-lookup"><span data-stu-id="db9ed-123">**/ms\_union**</span></span>](-ms-union.md)
</dt> </dl>

 

 




