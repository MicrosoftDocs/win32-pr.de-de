---
title: Handle-Attribut
description: Das \ handle \-Attribut gibt eine benutzerdefinierte oder \ 0034; angepasste \ 0034; an. behandlertyp.
ms.assetid: db5c6ea6-6081-4cea-9265-5e2f67fd8c14
keywords:
- Handle-Attribut-Mittel l
topic_type:
- apiref
api_name:
- handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d4560de53bf3f24238e9ff96e01c74716729749
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858252"
---
# <a name="handle-attribute"></a><span data-ttu-id="d50d8-104">Handle-Attribut</span><span class="sxs-lookup"><span data-stu-id="d50d8-104">handle attribute</span></span>

<span data-ttu-id="d50d8-105">Das \[ **handle** - \] Attribut gibt einen benutzerdefinierten oder "angepassten" Handlertyp an.</span><span class="sxs-lookup"><span data-stu-id="d50d8-105">The \[**handle**\] attribute specifies a user-defined or "customized" handle type.</span></span>

``` syntax
typedef [handle] typename;  
handle_t __RPC_USER typename_bind (typename);
void __RPC_USER typename_unbind (typename, handle_t);
```

## <a name="parameters"></a><span data-ttu-id="d50d8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d50d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d50d8-107">*typeName*</span><span class="sxs-lookup"><span data-stu-id="d50d8-107">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="d50d8-108">Gibt den Namen des benutzerdefinierten Bindungs Handle Typs an.</span><span class="sxs-lookup"><span data-stu-id="d50d8-108">Specifies the name of the user-defined binding-handle type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d50d8-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d50d8-109">Remarks</span></span>

<span data-ttu-id="d50d8-110">Benutzerdefinierte Handles ermöglichen Entwicklern das Entwerfen von Handles, die für die Anwendung von Bedeutung sind.</span><span class="sxs-lookup"><span data-stu-id="d50d8-110">User-defined handles permit developers to design handles that are meaningful to the application.</span></span> <span data-ttu-id="d50d8-111">Ein benutzerdefiniertes Handle kann nur in einer Typdeklaration definiert werden, nicht in einem funktionsdeklarator.</span><span class="sxs-lookup"><span data-stu-id="d50d8-111">A user-defined handle can only be defined in a type declaration, not in a function declarator.</span></span>

<span data-ttu-id="d50d8-112">Ein Parameter eines Typs, der durch das \[ **handle** \] -Attribut definiert wird, wird verwendet, um die Bindung für den Aufruf zu bestimmen und wird an die aufgerufene Prozedur übertragen.</span><span class="sxs-lookup"><span data-stu-id="d50d8-112">A parameter of a type defined by the \[**handle**\] attribute is used to determine the binding for the call and is transmitted to the called procedure.</span></span>

<span data-ttu-id="d50d8-113">Der Benutzer muss Bindungs-und unbindungs Routinen bereitstellen, um zwischen primitiven und benutzerdefinierten handle-Typen zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="d50d8-113">The user must provide binding and unbinding routines to convert between primitive and user-defined handle types.</span></span> <span data-ttu-id="d50d8-114">Wenn ein benutzerdefiniertes Handle des Typs *Typname* angegeben ist, muss der Benutzer die Routinen *tykame* \_ **Bind** und *tykame* \_ **Bindung** angeben.</span><span class="sxs-lookup"><span data-stu-id="d50d8-114">Given a user-defined handle of type *typename*, the user must supply the routines *typename*\_**bind** and *typename*\_**unbind**.</span></span> <span data-ttu-id="d50d8-115">Wenn z. b. der benutzerdefinierte Handlertyp myhandle lautet, werden die Routinen mit myhandle \_ **Bind** und myhandle \_ **Bindung** benannt.</span><span class="sxs-lookup"><span data-stu-id="d50d8-115">For example, if the user-defined handle type is named MYHANDLE, the routines are named MYHANDLE\_**bind** and MYHANDLE\_**unbind**.</span></span>

<span data-ttu-id="d50d8-116">Wenn der Vorgang erfolgreich ist, sollte die Bindungs Routine *Typname* \_  ein gültiges Primitives Bindungs Handle zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d50d8-116">If successful, the *typename*\_**bind** routine should return a valid primitive binding handle.</span></span> <span data-ttu-id="d50d8-117">Wenn nicht erfolgreich, sollte die Routine einen **null**-Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d50d8-117">If unsuccessful, the routine should return a **NULL**.</span></span> <span data-ttu-id="d50d8-118">Wenn die Routine **null** zurückgibt, wird die Bindung-Routine von *typame* \_  nicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="d50d8-118">If the routine returns **NULL**, the *typename*\_**unbind** routine will not be called.</span></span> <span data-ttu-id="d50d8-119">Wenn die Bindungs Routine ein ungültiges Bindungs handle zurückgibt, das nicht **null** ist, ist das stubverhalten nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="d50d8-119">If the binding routine returns an invalid binding handle different from **NULL**, the stub behavior is undefined.</span></span>

<span data-ttu-id="d50d8-120">Wenn die Remote Prozedur ein benutzerdefiniertes Handle als Parameter oder als implizites handle aufweist, rufen die Client-stubdie Bindungs Routine auf, bevor Sie die Remote Prozedur aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d50d8-120">When the remote procedure has a user-defined handle as a parameter or as an implicit handle, the client stubs call the binding routine before calling the remote procedure.</span></span> <span data-ttu-id="d50d8-121">Die Client-stubzeichen nennen die aufheben-Routine nach dem Remote-Befehl.</span><span class="sxs-lookup"><span data-stu-id="d50d8-121">The client stubs call the unbinding routine after the remote call.</span></span>

<span data-ttu-id="d50d8-122">In DCE IDL muss ein Parameter mit dem \[ **handle** - \] Attribut als erster Parameter in der Liste der Remote Prozedur Argumente angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d50d8-122">In DCE IDL, a parameter with the \[**handle**\] attribute must appear as the first parameter in the remote procedure argument list.</span></span> <span data-ttu-id="d50d8-123">Nachfolgende Parameter, einschließlich anderer \[ **handle** - \] Attribute, werden als normale Parameter behandelt.</span><span class="sxs-lookup"><span data-stu-id="d50d8-123">Subsequent parameters, including other \[**handle**\] attributes, are treated as ordinary parameters.</span></span> <span data-ttu-id="d50d8-124">Microsoft unterstützt eine Erweiterung der DCE-IDL, die es ermöglicht, dass der benutzerdefinierte \[ **handle** - \] Parameter in anderen Positionen als dem ersten Parameter angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d50d8-124">Microsoft supports an extension to DCE IDL that allows the user-defined \[**handle**\] parameter to appear in positions other than the first parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="d50d8-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d50d8-125">Examples</span></span>

``` syntax
typedef [handle] struct 
{ 
    char machine[8]; 
    char nmpipe[256]; 
} h_service; 
 
handle_t __RPC_USER h_service_bind(h_service); 
void __RPC_USER h_service_unbind(h_service, handle_t);
```

## <a name="see-also"></a><span data-ttu-id="d50d8-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d50d8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d50d8-127">Bindung und Handles</span><span class="sxs-lookup"><span data-stu-id="d50d8-127">Binding and Handles</span></span>](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[<span data-ttu-id="d50d8-128">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="d50d8-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="d50d8-129">**implizites \_ handle**</span><span class="sxs-lookup"><span data-stu-id="d50d8-129">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="d50d8-130">**typedef**</span><span class="sxs-lookup"><span data-stu-id="d50d8-130">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 