---
title: implicit_handle-Attribut
description: Das Attribut \ implizites \_ handle \ ACF gibt das Handle an, das für Funktionen verwendet wird, die kein explizites Handle als Prozedur Parameter enthalten.
ms.assetid: 09c17473-87b5-4fd6-beb9-3d9b7bc82d8c
keywords:
- implicit_handle Attribut-Mittel l
topic_type:
- apiref
api_name:
- implicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22f410fa048a27e1f7626690e6308de4c1a31c2a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857228"
---
# <a name="implicit_handle-attribute"></a><span data-ttu-id="114cf-104">impliziertes \_ handle-Attribut</span><span class="sxs-lookup"><span data-stu-id="114cf-104">implicit\_handle attribute</span></span>

<span data-ttu-id="114cf-105">Das **\[ implizite \_ handle \]** -ACF-Attribut gibt das Handle an, das für Funktionen verwendet wird, die kein explizites Handle als Prozedur Parameter enthalten.</span><span class="sxs-lookup"><span data-stu-id="114cf-105">The **\[implicit\_handle\]** ACF attribute specifies the handle used for functions that do not include an explicit handle as a procedure parameter.</span></span>

``` syntax
implicit_handle(handle-type handle-name)
```

## <a name="parameters"></a><span data-ttu-id="114cf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="114cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="114cf-107">*Handle-Typ*</span><span class="sxs-lookup"><span data-stu-id="114cf-107">*handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="114cf-108">Gibt den Datentyp des Handles an, z. b. das Basistyp [**handle \_ t**](handle-t.md) oder einen benutzerdefinierten Handlertyp.</span><span class="sxs-lookup"><span data-stu-id="114cf-108">Specifies the handle data type, such as the base type [**handle\_t**](handle-t.md) or a user-defined handle type.</span></span>

</dd> <dt>

<span data-ttu-id="114cf-109">*Handle-Name*</span><span class="sxs-lookup"><span data-stu-id="114cf-109">*handle-name*</span></span> 
</dt> <dd>

<span data-ttu-id="114cf-110">Gibt den Namen des Handles an.</span><span class="sxs-lookup"><span data-stu-id="114cf-110">Specifies the name of the handle.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="114cf-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="114cf-111">Remarks</span></span>

<span data-ttu-id="114cf-112">Das vom **\[ impliziten \_ handle \]** angegebene Handle wird abhängig von der Art der Prozedur auf unterschiedliche Weise verwendet.</span><span class="sxs-lookup"><span data-stu-id="114cf-112">The handle specified by the **\[implicit\_handle\]** attribute is used in different ways depending on the nature of the procedure.</span></span> <span data-ttu-id="114cf-113">Wenn die Prozedur Remote ist, wird das Handle als Bindungs Handle für den Remote-Befehl verwendet.</span><span class="sxs-lookup"><span data-stu-id="114cf-113">If the procedure is remote, the handle will be used as the binding handle for the remote call.</span></span> <span data-ttu-id="114cf-114">Das implizite Handle kann auch verwendet werden, um eine anfängliche Bindung für eine Funktion einzurichten, die ein Kontext Handle verwendet.</span><span class="sxs-lookup"><span data-stu-id="114cf-114">The implicit handle may also be used to establish an initial binding for a function that uses a context handle.</span></span> <span data-ttu-id="114cf-115">Wenn es sich bei der Prozedur um eine Serialisierungsprozedur handelt, wird das Handle als serialisierungshandle verwendet, das den Vorgang steuert.</span><span class="sxs-lookup"><span data-stu-id="114cf-115">If the procedure is a serializing procedure, the handle is used as a serializing handle controlling the operation.</span></span> <span data-ttu-id="114cf-116">Bei der Typserialisierung wird das Handle als serialisierungshandle für alle serialisierten Typen verwendet.</span><span class="sxs-lookup"><span data-stu-id="114cf-116">In the case of type serialization, the handle is used as the serialization handle for all the serialized types.</span></span>

<span data-ttu-id="114cf-117">Das **\[ implizite \_ handle \]** -Attribut gibt eine globale Variable an, die ein Handle enthält, das von jeder Funktion verwendet wird, die implizite Handles benötigt.</span><span class="sxs-lookup"><span data-stu-id="114cf-117">The **\[implicit\_handle\]** attribute specifies a global variable that contains a handle used by any function needing implicit handles.</span></span>

<span data-ttu-id="114cf-118">Der Typ des impliziten Bindungs Handles muss entweder [**handle \_ t**](handle-t.md) (oder ein Typ, der auf **handle \_ t** basiert) oder ein benutzerdefinierter Handlertyp sein, der mit dem [**handle**](handle.md) -Attribut angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="114cf-118">The implicit binding handle type must be either [**handle\_t**](handle-t.md) (or a type based on **handle\_t**) or a user-defined handle type specified with the [**handle**](handle.md) attribute.</span></span> <span data-ttu-id="114cf-119">Der implizite serialisierungshandle muss ein Typ sein, der auf **handle \_ t** basiert.</span><span class="sxs-lookup"><span data-stu-id="114cf-119">The implicit serializing handle must be a type based on **handle\_t**.</span></span>

<span data-ttu-id="114cf-120">Wenn der implizite Handlertyp nicht in der IDL-Datei oder in Dateien definiert ist, die von der IDL-Datei für den mittleren Computer eingeschlossen und importiert werden, müssen Sie beim Kompilieren der Stubdateien die Datei angeben, die die Handle-Type-Definition enthält.</span><span class="sxs-lookup"><span data-stu-id="114cf-120">If the implicit handle type is not defined in the IDL file or in any files included and imported by the IDL file for the MIDL computer, you must supply the file containing the handle-type definition when you compile the stubs.</span></span> <span data-ttu-id="114cf-121">Verwenden Sie die ACF [**include**](include.md) -Anweisung, um die Datei einzufügen, die die Handle-Type-Definition enthält.</span><span class="sxs-lookup"><span data-stu-id="114cf-121">Use the ACF [**include**](include.md) statement to include the file containing the handle-type definition.</span></span>

<span data-ttu-id="114cf-122">Das **\[ implizite \_ handle \]** -Attribut kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="114cf-122">The **\[implicit\_handle\]** attribute can occur once, at most.</span></span> <span data-ttu-id="114cf-123">Das **\[ implizite \_ handle \]** -Attribut kann nur auftreten, wenn die Attribute des [**\[ automatischen \_ Handles \]**](auto-handle.md) und des [**\[ expliziten \_ Handles \]**](explicit-handle.md) nicht auftreten.</span><span class="sxs-lookup"><span data-stu-id="114cf-123">The **\[implicit\_handle\]** attribute can occur only if the [**\[auto\_handle\]**](auto-handle.md) and [**\[explicit\_handle\]**](explicit-handle.md) attributes do not occur.</span></span>

## <a name="examples"></a><span data-ttu-id="114cf-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="114cf-124">Examples</span></span>

``` syntax
/* ACF file */ 
[
    implicit_handle(handle_t hMyHandle)
] 
interface iface
{ 
    // Attribute configuration statements
}
```

## <a name="see-also"></a><span data-ttu-id="114cf-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="114cf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="114cf-126">Anwendungs Konfigurationsdatei (ACF)</span><span class="sxs-lookup"><span data-stu-id="114cf-126">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="114cf-127">**Automatisches \_ handle**</span><span class="sxs-lookup"><span data-stu-id="114cf-127">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="114cf-128">**explizites \_ handle**</span><span class="sxs-lookup"><span data-stu-id="114cf-128">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="114cf-129">**Handle \_ t**</span><span class="sxs-lookup"><span data-stu-id="114cf-129">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="114cf-130">**darunter**</span><span class="sxs-lookup"><span data-stu-id="114cf-130">**include**</span></span>](include.md)
</dt> </dl>

 

 




