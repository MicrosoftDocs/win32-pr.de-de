---
title: Async-Attribut
description: Das Attribut \ Async \ ACF definiert einen Remote Prozedur Aufrufvorgang als asynchronen Vorgang.
ms.assetid: 8002980a-94be-4d45-99d7-dfa4eae7f102
keywords:
- Async-Attribut, Mittel l
topic_type:
- apiref
api_name:
- async
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 562b157f26078c6f4d5b3cffe47417fa18fe608d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948659"
---
# <a name="async-attribute"></a><span data-ttu-id="db888-104">Async-Attribut</span><span class="sxs-lookup"><span data-stu-id="db888-104">async attribute</span></span>

<span data-ttu-id="db888-105">Das \[ **Async** - \] ACF-Attribut definiert einen Remote Prozedur Aufrufvorgang als asynchronen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="db888-105">The \[**async**\] ACF attribute defines a remote procedure call as an asynchronous operation.</span></span>

``` syntax
[async, opt-acf-attributes] function-name (param-list)
```

## <a name="parameters"></a><span data-ttu-id="db888-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="db888-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db888-107">*Opt-ACF-Attribute*</span><span class="sxs-lookup"><span data-stu-id="db888-107">*opt-acf-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="db888-108">Gibt optionale Anwendungs Konfigurations Attribute an.</span><span class="sxs-lookup"><span data-stu-id="db888-108">Specifies optional application configuration attributes.</span></span>

</dd> <dt>

<span data-ttu-id="db888-109">*function-name*</span><span class="sxs-lookup"><span data-stu-id="db888-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="db888-110">Gibt den Namen der Funktion in der IDL-Datei an.</span><span class="sxs-lookup"><span data-stu-id="db888-110">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="db888-111">*param-Liste*</span><span class="sxs-lookup"><span data-stu-id="db888-111">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="db888-112">Gibt eine optionale Parameterliste an.</span><span class="sxs-lookup"><span data-stu-id="db888-112">Specifies an optional parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db888-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db888-113">Remarks</span></span>

<span data-ttu-id="db888-114">Dieses Attribut ist in COM-Schnittstellen nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="db888-114">This attribute is not applicable in COM interfaces.</span></span>

<span data-ttu-id="db888-115">Um eine RPC-Funktion als asynchron zu deklarieren, deklarieren Sie zuerst die Funktion als Teil einer Schnittstellen Definition in einer IDL-Datei.</span><span class="sxs-lookup"><span data-stu-id="db888-115">To declare an RPC function as asynchronous, first declare the function as part of an interface definition in an IDL file.</span></span> <span data-ttu-id="db888-116">Ändern Sie dann die Funktionsdeklaration in der Anwendungs Konfigurationsdatei (ACF), indem Sie das \[ **Async** - \] Attribut anwenden.</span><span class="sxs-lookup"><span data-stu-id="db888-116">Then modify that function declaration, within the application configuration file (ACF), by applying the \[**async**\] attribute.</span></span> <span data-ttu-id="db888-117">Beachten Sie, dass die Funktionsdeklaration das asynchrone Handle nicht erwähnt und dass das Bindungs Handle der erste Parameter ist.</span><span class="sxs-lookup"><span data-stu-id="db888-117">Note that the function declaration makes no mention of the asynchronous handle and that the binding handle is the first parameter.</span></span> <span data-ttu-id="db888-118">\[Wenn Sie das **Async** - \] Attribut in der ACF-Datei anwenden, wird der entsprechende Code generiert, damit der asynchrone Server beim Aufrufen dieser Funktion erwartet, dass vor den anderen Parametern ein asynchrones handle empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="db888-118">Applying the \[**async**\] attribute in the ACF file generates the appropriate code so that when this function is called, the asynchronous server expects to receive an asynchronous handle before the other parameters.</span></span>

> [!Note]  
> <span data-ttu-id="db888-119">Das Async-Attribut kann nicht mit dem [**/OSF**](-osf.md) -Befehls Zeilenschalter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="db888-119">The async attribute cannot be used with the [**/osf**](-osf.md) command line switch.</span></span>

 

## <a name="examples"></a><span data-ttu-id="db888-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="db888-120">Examples</span></span>

``` syntax
//file:Xasync.idl
interface AsyncIface 
{
    HRESULT MyAsyncFunc (
        handle_t hBinding,
        [in] int a,
        [in] int b,
        [out] int *c) ;
//other interface definitions
}
//end XAsync.idl

// file: Xasync.acf
interface AsyncIface
{
    [async] MyAsyncFunc () ;
    //any other ACF definitions
}
//end Xasync.acf
```

## <a name="see-also"></a><span data-ttu-id="db888-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="db888-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db888-122">Anwendungs Konfigurationsdatei (ACF)</span><span class="sxs-lookup"><span data-stu-id="db888-122">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="db888-123">Asynchroner RPC</span><span class="sxs-lookup"><span data-stu-id="db888-123">Asynchronous RPC</span></span>](/windows/desktop/Rpc/asynchronous-rpc)
</dt> </dl>

 

 