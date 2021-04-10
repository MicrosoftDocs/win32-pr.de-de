---
title: Attribut codieren
description: Das Attribut "\ Encode \ ACF" gibt an, dass für eine Prozedur oder einen Datentyp eine Serialisierungsunterstützung erforderlich ist.
ms.assetid: 2661021d-8a26-4216-935b-ca40b6f8b9ec
keywords:
- Codieren von Attributen in der Mitte
topic_type:
- apiref
api_name:
- encode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2a35c6d6910229a9e14026f6727db5c3176050
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948621"
---
# <a name="encode-attribute"></a><span data-ttu-id="d1c73-104">Attribut codieren</span><span class="sxs-lookup"><span data-stu-id="d1c73-104">encode attribute</span></span>

<span data-ttu-id="d1c73-105">Das **\[ COF \] -Attribut codieren** gibt an, dass für eine Prozedur oder einen Datentyp eine Serialisierungsunterstützung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d1c73-105">The **\[encode\]** ACF attribute specifies that a procedure or a data type needs serialization support.</span></span>

``` syntax
[ 
    encode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ encode [ , op-attribute-list] ] proc-name

typedef [encode [ , type-attribute-list] ] type-name
```

## <a name="parameters"></a><span data-ttu-id="d1c73-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1c73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1c73-107">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="d1c73-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d1c73-108">Gibt andere Attribute an, die auf die gesamte Schnittstelle angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1c73-108">Specifies other attributes that apply to the interface as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="d1c73-109">*Schnittstellen Name*</span><span class="sxs-lookup"><span data-stu-id="d1c73-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d1c73-110">Gibt den Namen der Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="d1c73-110">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="d1c73-111">*Schnittstellen Definition*</span><span class="sxs-lookup"><span data-stu-id="d1c73-111">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="d1c73-112">Gibt IDL-Anweisungen an, die die Definition der-Schnittstelle bilden.</span><span class="sxs-lookup"><span data-stu-id="d1c73-112">Specifies IDL statements which form the definition of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="d1c73-113">*OP-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="d1c73-113">*op-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d1c73-114">Gibt andere operative Attribute an, die für die Prozedur (z **\[** . b. [**Decodierung**](decode.md)) gelten **\]** .</span><span class="sxs-lookup"><span data-stu-id="d1c73-114">Specifies other operational attributes that apply to the procedure such as **\[**[**decode**](decode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="d1c73-115">*proc-Name*</span><span class="sxs-lookup"><span data-stu-id="d1c73-115">*proc-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d1c73-116">Gibt den Namen der Prozedur an.</span><span class="sxs-lookup"><span data-stu-id="d1c73-116">Specifies the name of the procedure.</span></span>

</dd> <dt>

<span data-ttu-id="d1c73-117">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="d1c73-117">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d1c73-118">Gibt andere Attribute an, die auf den Typ angewendet werden, z **\[** . b. [**decodieren**](decode.md) **\]** und **\[** [**zuordnen**](allocate.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="d1c73-118">Specifies other attributes that apply to the type such as **\[**[**decode**](decode.md)**\]** and **\[**[**allocate**](allocate.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="d1c73-119">*Typname*</span><span class="sxs-lookup"><span data-stu-id="d1c73-119">*type-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d1c73-120">Gibt einen Typ an, der in der IDL-Datei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d1c73-120">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1c73-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1c73-121">Remarks</span></span>

<span data-ttu-id="d1c73-122">Das **\[ Codieren \]** -Attribut bewirkt, dass der mittlerer l-Compiler Code generiert, der von einer Anwendung zum Serialisieren von Daten in einen Puffer verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d1c73-122">The **\[encode\]** attribute causes the MIDL compiler to generate code that an application can use to serialize data into a buffer.</span></span> <span data-ttu-id="d1c73-123">Das **\[** [**decodieren**](decode.md) - **\]** Attribut generiert den Code zum Zurücksetzen von Daten aus einem Puffer.</span><span class="sxs-lookup"><span data-stu-id="d1c73-123">The **\[**[**decode**](decode.md)**\]** attribute generates the code for unmarshaling data from a buffer.</span></span>

<span data-ttu-id="d1c73-124">Verwenden Sie die Attribute **\[ Codieren \]** und **\[** [**decodieren**](decode.md) **\]** in einer ACF, um Serialisierungscode für Prozeduren oder Typen zu generieren, die in der IDL-Datei einer Schnittstelle definiert sind.</span><span class="sxs-lookup"><span data-stu-id="d1c73-124">Use the **\[encode\]** and **\[**[**decode**](decode.md)**\]** attributes in an ACF to generate serialization code for procedures or types defined in the IDL file of an interface.</span></span> <span data-ttu-id="d1c73-125">Bei Verwendung als Schnittstellen Attribut gilt die **\[ Codierung \]** für alle Typen und Prozeduren, die in der IDL-Datei definiert sind.</span><span class="sxs-lookup"><span data-stu-id="d1c73-125">When used as an interface attribute, **\[encode\]** applies to all the types and procedures defined in the IDL file.</span></span> <span data-ttu-id="d1c73-126">Wenn die **\[ Codierung \]** als Betriebs Attribut verwendet wird, gilt sie nur für die angegebene Prozedur.</span><span class="sxs-lookup"><span data-stu-id="d1c73-126">When used as an operational attribute, **\[encode\]** applies only to the specified procedure.</span></span> <span data-ttu-id="d1c73-127">Wenn die **\[ Codierung \]** als Type-Attribut verwendet wird, gilt sie nur für den angegebenen Typ.</span><span class="sxs-lookup"><span data-stu-id="d1c73-127">When used as a type attribute, **\[encode\]** applies only to the specified type.</span></span>

<span data-ttu-id="d1c73-128">Wenn das Attribut **\[ Codieren \]** oder **\[** [**decodieren**](decode.md) **\]** auf eine Prozedur angewendet wird, generiert der mittlerer l-Compiler einen serialisierungsstub in ähnlicher Weise, wie remotestubs für Remote Routinen generiert werden.</span><span class="sxs-lookup"><span data-stu-id="d1c73-128">When the **\[encode\]** or **\[**[**decode**](decode.md)**\]** attribute is applied to a procedure, the MIDL compiler generates a serialization stub in a similar fashion as remote stubs are generated for remote routines.</span></span> <span data-ttu-id="d1c73-129">Eine Prozedur kann entweder eine Remote-oder eine Serialisierungsprozedur sein, aber nicht beides.</span><span class="sxs-lookup"><span data-stu-id="d1c73-129">A procedure can be either a remote or a serializing procedure, but it cannot be both.</span></span> <span data-ttu-id="d1c73-130">Der Prototyp der generierten Routine wird an den Stub gesendet. H-Datei, während der Stub selbst in die Stub- \_ c. c-Datei übergeht.</span><span class="sxs-lookup"><span data-stu-id="d1c73-130">The prototype of the generated routine is sent to the STUB.H file while the stub itself goes into the STUB\_C.C file.</span></span>

<span data-ttu-id="d1c73-131">Der-compilercompiler generiert zwei Funktionen für jeden Typ, auf den das **\[ Codieren \]** -Attribut angewendet wird, und eine zusätzliche Funktion für jeden Typ, auf den das Attribut " **\[** [**Decodierung**](decode.md) " **\]** angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="d1c73-131">The MIDL compiler generates two functions for each type the **\[encode\]** attribute applies to, and one additional function for each type the **\[**[**decode**](decode.md)**\]** attribute applies to.</span></span> <span data-ttu-id="d1c73-132">Für einen benutzerdefinierten Typ mit dem Namen "MyType" generiert der Compiler z. b. Code für die Funktionen "MyType \_ encode", "MyType \_ Decode" und "MyType \_ alignsize".</span><span class="sxs-lookup"><span data-stu-id="d1c73-132">For example, for a user-defined type named MyType, the compiler generates code for the MyType\_Encode, MyType\_Decode, and MyType\_AlignSize functions.</span></span> <span data-ttu-id="d1c73-133">Für diese Funktionen schreibt der Compiler Prototypen in den Stub. H und Quellcode zu Stub \_ C.C.</span><span class="sxs-lookup"><span data-stu-id="d1c73-133">For these functions, the compiler writes prototypes to STUB.H and source code to STUB\_C.C.</span></span>

<span data-ttu-id="d1c73-134">Weitere Informationen zu serialisierungshandles und zum Codieren oder Decodieren von Daten finden Sie unter [Serialisierung Services](/windows/desktop/Rpc/serialization-services).</span><span class="sxs-lookup"><span data-stu-id="d1c73-134">For additional information about serialization handles and encoding or decoding data, see [Serialization Services](/windows/desktop/Rpc/serialization-services).</span></span>

## <a name="examples"></a><span data-ttu-id="d1c73-135">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1c73-135">Examples</span></span>

``` syntax
/* 
    ACF file example; 
    Assumes MyType1, MyType2, MyType3, MyProc1, MyProc2, MyProc3 defined 
    in IDL file  
    MyType1, MyType2, MyProc1, MyProc2 have encode and decode 
    serialization support 
    MyType3 and MyProc3 have encode serialization support only 
*/ 
[ 
    encode, 
    implicit_handle(handle_t bh) 
]    
interface regress 
{ 
    typedef [ decode ] MyType1; 
    typedef [ encode, decode ] MyType2; 
    [ decode ] MyProcc1(); 
    [ encode ] MyProc2(); 
}
```

## <a name="see-also"></a><span data-ttu-id="d1c73-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d1c73-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1c73-137">Anwendungs Konfigurationsdatei (ACF)</span><span class="sxs-lookup"><span data-stu-id="d1c73-137">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="d1c73-138">**allocate**</span><span class="sxs-lookup"><span data-stu-id="d1c73-138">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="d1c73-139">**Decodieren**</span><span class="sxs-lookup"><span data-stu-id="d1c73-139">**decode**</span></span>](decode.md)
</dt> </dl>

 

 