---
title: Aufzählungs Attribut
description: Die Schlüsselwort-Enumeration identifiziert einen enumerierten Typ.
ms.assetid: 1aaa3c36-17f7-42ff-8f4c-66133fcf4a1a
keywords:
- Aufzählungs Attribut-Mittell
topic_type:
- apiref
api_name:
- enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681244c9d852c25d8e63ad389b03f16e6db8148c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312221"
---
# <a name="enum-attribute"></a><span data-ttu-id="6dd7a-104">Aufzählungs Attribut</span><span class="sxs-lookup"><span data-stu-id="6dd7a-104">enum attribute</span></span>

<span data-ttu-id="6dd7a-105">Die Schlüssel **Wort** -Enumeration identifiziert einen enumerierten Typ.</span><span class="sxs-lookup"><span data-stu-id="6dd7a-105">The keyword **enum** identifies an enumerated type.</span></span>

``` syntax
enum [tag ] 
{ 
    identifier [=integer-value ] 
    [ , ... ] 
}
```

## <a name="parameters"></a><span data-ttu-id="6dd7a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6dd7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dd7a-107">*Tag*</span><span class="sxs-lookup"><span data-stu-id="6dd7a-107">*tag*</span></span> 
</dt> <dd>

<span data-ttu-id="6dd7a-108">Gibt ein optionales Tag für den enumerierten Typ an.</span><span class="sxs-lookup"><span data-stu-id="6dd7a-108">Specifies an optional tag for the enumerated type.</span></span>

</dd> <dt>

<span data-ttu-id="6dd7a-109">*identifier*</span><span class="sxs-lookup"><span data-stu-id="6dd7a-109">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="6dd7a-110">Gibt die jeweilige Enumeration an.</span><span class="sxs-lookup"><span data-stu-id="6dd7a-110">Specifies the particular enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="6dd7a-111">*ganzzahliger Wert*</span><span class="sxs-lookup"><span data-stu-id="6dd7a-111">*integer-value*</span></span> 
</dt> <dd>

<span data-ttu-id="6dd7a-112">Gibt einen Konstanten ganzzahligen Wert an.</span><span class="sxs-lookup"><span data-stu-id="6dd7a-112">Specifies a constant integer value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6dd7a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6dd7a-113">Remarks</span></span>

<span data-ttu-id="6dd7a-114"> Enumerationstypen können als Typspezifizierer in [**typedef**](typedef.md) -Deklarationen, allgemeinen Deklarationen und Funktions Deklaratoren (entweder als Funktions Rückgabetyp oder als Parametertyp Spezifizierer) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6dd7a-114">**enum** types can appear as type specifiers in [**typedef**](typedef.md) declarations, general declarations, and function declarators (either as the function-return-type or as a parameter-type specifier).</span></span> <span data-ttu-id="6dd7a-115">Informationen zu dem Kontext, in dem typspezifier angezeigt wird, finden Sie unter [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="6dd7a-115">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="6dd7a-116">Im Standardmodus des compl-Compilers können Enumeratoren ganzzahlige Werte zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="6dd7a-116">In the MIDL compiler's default mode, you can assign integer values to enumerators.</span></span> <span data-ttu-id="6dd7a-117">(Diese Funktion ist nicht verfügbar, wenn Sie mit dem [**/OSF**](-osf.md) -Schalter kompilieren.) Wie bei C-Language-Enumeratoren müssen Enumeratornamen eindeutig sein, aber die Enumeratorwerte müssen nicht gleich sein.</span><span class="sxs-lookup"><span data-stu-id="6dd7a-117">(This feature is not available when you compile with the [**/osf**](-osf.md) switch.) As with C-language enumerators, enumerator names must be unique, but the enumerator values need not be.</span></span>

<span data-ttu-id="6dd7a-118">Wenn Zuweisungs Operatoren nicht bereitgestellt werden, werden Bezeichner von links nach rechts aufeinander folgende ganzzahlige Werte zugeordnet, beginnend mit 0 (null).</span><span class="sxs-lookup"><span data-stu-id="6dd7a-118">When assignment operators are not provided, identifiers are mapped to consecutive integers from left to right, starting with zero.</span></span> <span data-ttu-id="6dd7a-119">Wenn Zuweisungs Operatoren bereitgestellt werden, beginnen zugewiesene Werte mit dem zuletzt zugewiesenen Wert.</span><span class="sxs-lookup"><span data-stu-id="6dd7a-119">When assignment operators are provided, assigned values start from the most recently assigned value.</span></span>

<span data-ttu-id="6dd7a-120">Die maximale Anzahl von Bezeichner beträgt 65.535.</span><span class="sxs-lookup"><span data-stu-id="6dd7a-120">The maximum number of identifiers is 65,535.</span></span>

<span data-ttu-id="6dd7a-121">Objekte vom Typ " **Enumeration** " sind [**int**](int.md) -Typen, und ihre Größe ist System abhängig.</span><span class="sxs-lookup"><span data-stu-id="6dd7a-121">Objects of type **enum** are [**int**](int.md) types, and their size is system-dependent.</span></span> <span data-ttu-id="6dd7a-122">Standardmäßig werden Objekte von Enumerationstypen als 16-Bit- **Objekte vom Typ** [**Ganzzahl ohne Vorzeichen**](unsigned.md) [**Short**](short.md) behandelt, wenn Sie über ein Netzwerk übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="6dd7a-122">By default, objects of **enum** types are treated as 16-bit objects of type [**unsigned**](unsigned.md) [**short**](short.md) when transmitted over a network.</span></span> <span data-ttu-id="6dd7a-123">Werte außerhalb des Bereichs 0 bis 32.767 bewirken, dass der RPC X-Enumerationswert für die Lauf Zeit Ausnahme außerhalb \_ \_ des gültigen Bereichs liegt \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6dd7a-123">Values outside the range 0 - 32,767 cause the run-time exception RPC\_X\_ENUM\_VALUE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="6dd7a-124">Um Objekte als 32-Bit-Entitäten zu übertragen, wenden Sie das **\[** [**v1- \_ Enumeration**](v1-enum.md) - **\]** Attribut auf die **Enumeration** -typedef an.</span><span class="sxs-lookup"><span data-stu-id="6dd7a-124">To transmit objects as 32-bit entities, apply the **\[**[**v1\_enum**](v1-enum.md)**\]** attribute to the **enum** typedef.</span></span>

## <a name="examples"></a><span data-ttu-id="6dd7a-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6dd7a-125">Examples</span></span>

``` syntax
typedef enum {Monday=2, Tuesday, Wednesday, Thursday, Friday} workdays; 
 
typedef enum {Clemens=21, Palmer=22, Ryan=34} pitchers;
```

## <a name="see-also"></a><span data-ttu-id="6dd7a-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6dd7a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dd7a-127">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="6dd7a-127">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="6dd7a-128">**INT**</span><span class="sxs-lookup"><span data-stu-id="6dd7a-128">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="6dd7a-129">**short**</span><span class="sxs-lookup"><span data-stu-id="6dd7a-129">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="6dd7a-130">**typedef**</span><span class="sxs-lookup"><span data-stu-id="6dd7a-130">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="6dd7a-131">**Ganzzahl ohne Vorzeichen**</span><span class="sxs-lookup"><span data-stu-id="6dd7a-131">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="6dd7a-132">**v1-Aufzählung \_**</span><span class="sxs-lookup"><span data-stu-id="6dd7a-132">**v1\_enum**</span></span>](v1-enum.md)
</dt> </dl>

 

 




