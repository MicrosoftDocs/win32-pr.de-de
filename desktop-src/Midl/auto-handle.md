---
title: auto_handle-Attribut
description: Das Attribut \ Auto \_ handle \ ACF weist den Stub an, automatisch die Bindung für eine Funktion zu erstellen, die keinen expliziten Bindungs handle-Parameter hat. Beachten Sie, dass dieses Attribut veraltet ist und nicht mehr unterstützt wird.
ms.assetid: a402b933-f69b-4dfe-b0c5-b034d65d4a84
keywords:
- auto_handle Attribut-Mittel l
topic_type:
- apiref
api_name:
- auto_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e9a4c91fac8553867536f4f5a8c3094e0f0ff9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104471909"
---
# <a name="auto_handle-attribute"></a><span data-ttu-id="32906-104">Attribut für automatisches \_ handle</span><span class="sxs-lookup"><span data-stu-id="32906-104">auto\_handle attribute</span></span>

<span data-ttu-id="32906-105">Das ACF-Attribut für **\[ automatische \_ Handles \]** weist den Stub an, automatisch die Bindung für eine Funktion einzurichten, die über keinen expliziten Bindungs handle-Parameter verfügt.</span><span class="sxs-lookup"><span data-stu-id="32906-105">The **\[auto\_handle\]** ACF attribute directs the stub to automatically establish the binding for a function that does not have an explicit binding-handle parameter.</span></span>

> [!Note]  
> <span data-ttu-id="32906-106">Dieses Attribut ist veraltet und wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="32906-106">This attribute is obsolete and no longer supported.</span></span> <span data-ttu-id="32906-107">Die Verwendung des [**/robust**](-robust.md) -Schalters wird empfohlen.</span><span class="sxs-lookup"><span data-stu-id="32906-107">Use of the [**/robust**](-robust.md) switch is recommended.</span></span>

 

``` syntax
[ 
    auto_handle [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}
```

## <a name="parameters"></a><span data-ttu-id="32906-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="32906-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32906-109">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="32906-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="32906-110">Gibt 0 (null) oder mehr Attribute an, die auf die gesamte Schnittstelle angewendet werden, z. b. [**Code**](code.md) oder [**NoCode**](nocode.md).</span><span class="sxs-lookup"><span data-stu-id="32906-110">Specifies zero or more attributes that apply to the interface as a whole, such as [**code**](code.md) or [**nocode**](nocode.md).</span></span> <span data-ttu-id="32906-111">Trennen Sie Schnittstellen Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="32906-111">Separate interface attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="32906-112">*Schnittstellen Name*</span><span class="sxs-lookup"><span data-stu-id="32906-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="32906-113">Gibt den Namen der Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="32906-113">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="32906-114">*Schnittstellen Definition*</span><span class="sxs-lookup"><span data-stu-id="32906-114">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="32906-115">Gibt IDL-Anweisungen an, die die Definition der-Schnittstelle bilden.</span><span class="sxs-lookup"><span data-stu-id="32906-115">Specifies IDL statements that form the definition of the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32906-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32906-116">Remarks</span></span>

<span data-ttu-id="32906-117">Das Attribut für **\[ Automatisches \_ handle \]** wird im Schnittstellen Header der ACF angezeigt.</span><span class="sxs-lookup"><span data-stu-id="32906-117">The **\[auto\_handle\]** attribute appears in the interface header of the ACF.</span></span> <span data-ttu-id="32906-118">Sie wird auch im Schnittstellen Header der IDL-Datei angezeigt, wenn Sie den Mittelwert Compiler Switch [**/App \_ config**](-app-config.md)angeben.</span><span class="sxs-lookup"><span data-stu-id="32906-118">It also appears in the interface header of the IDL file when you specify the MIDL compiler switch [**/app\_config**](-app-config.md).</span></span>

<span data-ttu-id="32906-119">Wenn der Client eine Funktion aufruft, die die automatische Bindung verwendet, und keine Bindung an einen Server vorhanden ist, richtet der Stub automatisch die Bindung ein.</span><span class="sxs-lookup"><span data-stu-id="32906-119">When the client calls a function that uses automatic binding and no binding to a server exists, the stub automatically establishes the binding.</span></span> <span data-ttu-id="32906-120">Die Bindung wird für nachfolgende Aufrufe anderer Funktionen in der-Schnittstelle wieder verwendet, die die automatische Bindung verwenden.</span><span class="sxs-lookup"><span data-stu-id="32906-120">The binding is reused for subsequent calls to other functions in the interface that use automatic binding.</span></span> <span data-ttu-id="32906-121">Das Client Anwendungsprogramm muss keine Verarbeitung in Bezug auf das Bindungs handle deklarieren oder ausführen.</span><span class="sxs-lookup"><span data-stu-id="32906-121">The client application program does not have to declare or perform any processing relating to the binding handle.</span></span>

<span data-ttu-id="32906-122">Wenn die ACF nicht vorhanden ist oder das [**\[ implizite \_ handle \]**](implicit-handle.md) -Attribut nicht enthält, verwendet der Mittell-Compiler das **\[ automatische \_ handle \]** und gibt eine Informations Meldung aus.</span><span class="sxs-lookup"><span data-stu-id="32906-122">When the ACF is not present or does not include the [**\[implicit\_handle\]**](implicit-handle.md) attribute, the MIDL compiler uses **\[auto\_handle\]** and issues an informational message.</span></span> <span data-ttu-id="32906-123">Der mittlerer l-Compiler verwendet bei Bedarf auch das **\[ automatische \_ handle \]**, um die anfängliche Bindung für ein [**\[ Kontext \_ handle \]**](context-handle.md)herzustellen.</span><span class="sxs-lookup"><span data-stu-id="32906-123">The MIDL compiler also uses **\[auto\_handle\]**, if needed, to establish the initial binding for a [**\[context\_handle\]**](context-handle.md).</span></span>

<span data-ttu-id="32906-124">Das Attribut für **\[ Automatisches \_ handle \]** kann nur auftreten, wenn das [**\[ implizite \_ handle \]**](implicit-handle.md) oder das [**\[ explizite \_ handle \]**](explicit-handle.md) nicht auftritt.</span><span class="sxs-lookup"><span data-stu-id="32906-124">The **\[auto\_handle\]** attribute can occur only if the [**\[implicit\_handle\]**](implicit-handle.md) or [**\[explicit\_handle\]**](explicit-handle.md) attribute does not occur.</span></span> <span data-ttu-id="32906-125">Das Attribut für **\[ Automatisches \_ handle \]** kann höchstens einmal im ACF-oder IDL-Schnittstellen Header auftreten.</span><span class="sxs-lookup"><span data-stu-id="32906-125">The **\[auto\_handle\]** attribute can occur in the ACF or IDL interface header at most once.</span></span>

> [!Note]  
> <span data-ttu-id="32906-126">Wenn Sie Daten über Pipes verarbeiten, können Sie keine automatische Bindung verwenden (entweder mit dem Attribut "Automatisches **\[ \_ handle \]** " oder standardmäßig).</span><span class="sxs-lookup"><span data-stu-id="32906-126">You cannot use automatic binding (either with the **\[auto\_handle\]** attribute, or by default) if you are processing data through pipes.</span></span>

 

## <a name="examples"></a><span data-ttu-id="32906-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="32906-127">Examples</span></span>

``` syntax
[
    auto_handle
] 
interface MyInterface 
{ 
    /* Interface definition goes here*/
} 
[
    auto_handle, 
    code
] 
interface MyInterface
{ 
    /* Interface definition goes here*/
}
```

## <a name="see-also"></a><span data-ttu-id="32906-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="32906-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32906-129">Anwendungs Konfigurationsdatei (ACF)</span><span class="sxs-lookup"><span data-stu-id="32906-129">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="32906-130">**/APP- \_ Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="32906-130">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="32906-131">**Ordnung**</span><span class="sxs-lookup"><span data-stu-id="32906-131">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="32906-132">**explizites \_ handle**</span><span class="sxs-lookup"><span data-stu-id="32906-132">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="32906-133">**Kontext \_ handle**</span><span class="sxs-lookup"><span data-stu-id="32906-133">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="32906-134">**implizites \_ handle**</span><span class="sxs-lookup"><span data-stu-id="32906-134">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="32906-135">**NoCode**</span><span class="sxs-lookup"><span data-stu-id="32906-135">**nocode**</span></span>](nocode.md)
</dt> </dl>

 

 




