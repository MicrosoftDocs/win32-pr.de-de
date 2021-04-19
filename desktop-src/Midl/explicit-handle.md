---
title: explicit_handle-Attribut
description: Das \ explizite \_ handle \ ACF-Attribut gibt an, dass jede Prozedur als ersten Parameter ein Primitives handle, z. b. ein Handle t-Typ, aufweist \_ .
ms.assetid: c95d005e-dcc7-4d83-885d-91c0773c0ed8
keywords:
- explicit_handle Attribut-Mittel l
topic_type:
- apiref
api_name:
- explicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4fa677f1bb5a3414e6cf6dc761b83414c2d68b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106341894"
---
# <a name="explicit_handle-attribute"></a><span data-ttu-id="594ff-104">explizites \_ handle</span><span class="sxs-lookup"><span data-stu-id="594ff-104">explicit\_handle attribute</span></span>

<span data-ttu-id="594ff-105">Das \[ **explizite \_ handle** - \] ACF-Attribut gibt an, dass jede Prozedur als ersten Parameter ein Primitives handle, z. b. ein [**handle \_ t**](handle-t.md) -Typ, aufweist.</span><span class="sxs-lookup"><span data-stu-id="594ff-105">The \[**explicit\_handle**\] ACF attribute specifies that each procedure has, as its first parameter, a primitive handle, such as a [**handle\_t**](handle-t.md) type.</span></span>

``` syntax
[
    explicit_handle
] 
interface interface-name
{
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="594ff-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="594ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="594ff-107">*Schnittstellen Name*</span><span class="sxs-lookup"><span data-stu-id="594ff-107">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="594ff-108">Gibt den Namen der Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="594ff-108">Specifies the name of the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="594ff-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="594ff-109">Remarks</span></span>

<span data-ttu-id="594ff-110">Wenn Sie das **\[ explizite \_ handle \]** -Attribut verwenden, verfügt jede Prozedur über ein Primitives Handle als ersten Parameter, auch wenn die IDL-Datei dieses Handle nicht in der Parameterliste enthält.</span><span class="sxs-lookup"><span data-stu-id="594ff-110">When you use the **\[explicit\_handle\]** attribute, each procedure has a primitive handle as its first parameter even if the IDL file does not contain this handle in its parameter list.</span></span> <span data-ttu-id="594ff-111">Die Prototypen, die an die Header Datei und die Stub-Routinen ausgegeben werden, enthalten den zusätzlichen Parameter, und dieser Parameter wird als Handle zum Weiterleiten des Remote Aufrufes verwendet.</span><span class="sxs-lookup"><span data-stu-id="594ff-111">The prototypes emitted to the header file and stub routines contain the additional parameter, and that parameter is used as the handle for directing the remote call.</span></span>

<span data-ttu-id="594ff-112">Das **\[ explizite \_ handle \]** -Attribut wirkt sich auf Remote Prozeduren und Serialisierungsprozesse aus</span><span class="sxs-lookup"><span data-stu-id="594ff-112">The **\[explicit\_handle\]** attribute affects both remote procedures and serialization procedures.</span></span> <span data-ttu-id="594ff-113">Bei der Typserialisierung werden die Unterstützungs Routinen mit dem anfänglichen Parameter als explizites (Serialisierungs-) handle generiert.</span><span class="sxs-lookup"><span data-stu-id="594ff-113">For type serialization, the support routines are generated with the initial parameter as an explicit (serialization) handle.</span></span> <span data-ttu-id="594ff-114">Wenn das **\[ explizite \_ handle \]** -Attribut nicht verwendet wird, kann die Anwendung immer noch angeben, dass ein Vorgang über ein explizites handle (Bindung oder Serialisierung) verfügt, das den-Befehl umleitet.</span><span class="sxs-lookup"><span data-stu-id="594ff-114">If the **\[explicit\_handle\]** attribute is not used, the application can still specify that an operation have an explicit handle (binding or serialization) directing the call.</span></span> <span data-ttu-id="594ff-115">Zu diesem Zweck wird ein Prototyp mit einem Argument, das einen Handles-Typ enthält, für die IDL-Datei bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="594ff-115">To do this, a prototype with an argument containing a handle type is supplied to the IDL file.</span></span> <span data-ttu-id="594ff-116">Beachten Sie, dass im Standardmodus ein Argument, das nicht zuerst angezeigt wird, auch als Handle verwendet werden kann, das den-Befehl anleitet.</span><span class="sxs-lookup"><span data-stu-id="594ff-116">Note that in default mode, an argument that does not appear first can also be used as a handle directing the call.</span></span>

<span data-ttu-id="594ff-117">Obwohl das **\[ explizite \_ handle \]** -Attribut eine Möglichkeit ist, dem IDL-Prototyp ein Primitives **\[ explizites \_ handle \]** -Attribut zuzuweisen, ist es nicht unbedingt erforderlich, eine Änderung an der IDL-Datei durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="594ff-117">Therefore, while the **\[explicit\_handle\]** attribute is a way of giving the IDL prototype a primitive **\[explicit\_handle\]** attribute, it does not necessarily require a change to the IDL file.</span></span> <span data-ttu-id="594ff-118">Im [**/OSF**](-osf.md) -Modus kann nur das erste Argument als expliziter Handlertyp verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="594ff-118">In [**/osf**](-osf.md) mode only the first argument can be used as an explicit handle type.</span></span>

<span data-ttu-id="594ff-119">Das **\[ explizite \_ handle \]** -Attribut kann entweder als Schnittstellen Attribut oder als Vorgangs Attribut verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="594ff-119">The **\[explicit\_handle\]** attribute can be used as either an interface attribute or an operation attribute.</span></span> <span data-ttu-id="594ff-120">Als Schnittstellen Attribut wirkt sich dies auf alle Vorgänge in der-Schnittstelle und alle Typen aus, die die Serialisierungsunterstützung benötigen.</span><span class="sxs-lookup"><span data-stu-id="594ff-120">As an interface attribute, it affects all the operations in the interface and all the types that require serialization support.</span></span> <span data-ttu-id="594ff-121">Wenn Sie jedoch als Vorgangs Attribut verwendet wird, wirkt sich dies nur auf den jeweiligen Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="594ff-121">If, however, it is used as an operation attribute, it affects only that particular operation.</span></span> <span data-ttu-id="594ff-122">Wenn eine Methode mindestens ein in- \[ \] Kontext Handle enthält, wird das am weitesten links \[ \] verwendete Kontext Handle als Bindungs Handle verwendet, und es wird kein zusätzliches explizites Handle erstellt.</span><span class="sxs-lookup"><span data-stu-id="594ff-122">If a method contains one or more \[in\] context handles, the left most \[in\] context handle is used as the binding handle, and no additional explicit handle is created.</span></span>

## <a name="examples"></a><span data-ttu-id="594ff-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="594ff-123">Examples</span></span>

``` syntax
/* ACF File */ 
[
    explicit_handle
] 
interface iface
{ 
    // Interface definition statements.
};
```

## <a name="see-also"></a><span data-ttu-id="594ff-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="594ff-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="594ff-125">Anwendungs Konfigurationsdatei (ACF)</span><span class="sxs-lookup"><span data-stu-id="594ff-125">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="594ff-126">**Automatisches \_ handle**</span><span class="sxs-lookup"><span data-stu-id="594ff-126">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="594ff-127">**implizites \_ handle**</span><span class="sxs-lookup"><span data-stu-id="594ff-127">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="594ff-128">**/osf**</span><span class="sxs-lookup"><span data-stu-id="594ff-128">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 




