---
title: enable_allocate-Attribut
description: Das Attribut \ enable \_ attributs\acf gibt an, dass der Serverstub-Code die Stub-Speicher Verwaltungs Umgebung aktivieren soll.
ms.assetid: 3a232a82-f114-4d8c-8b71-cf8860c77db3
keywords:
- enable_allocate Attribut-Mittel l
topic_type:
- apiref
api_name:
- enable_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f43e8c10592fcf99ea294327c400c579ce45bf6b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101506"
---
# <a name="enable_allocate-attribute"></a><span data-ttu-id="9cea9-104">\_Attribut zuweisen aktivieren</span><span class="sxs-lookup"><span data-stu-id="9cea9-104">enable\_allocate attribute</span></span>

<span data-ttu-id="9cea9-105">Das Attribut "Zuordnungs-ACF **\[ aktivieren \_ \]** " gibt an, dass der serverstubcode die Stub-Speicher Verwaltungs Umgebung aktivieren soll.</span><span class="sxs-lookup"><span data-stu-id="9cea9-105">The **\[enable\_allocate\]** ACF attribute specifies that the server stub code should enable the stub memory management environment.</span></span>

> [!Note]  
> <span data-ttu-id="9cea9-106">Das Attribut " **\[ \_ zuordnen \]** " ist veraltet und wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9cea9-106">The **\[enable\_allocate\]** attribute is obsolete and is no longer supported.</span></span>

 

``` syntax
[
    enable_allocate
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a><span data-ttu-id="9cea9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9cea9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cea9-108">*optional-Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="9cea9-108">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9cea9-109">Gibt eine Liste von 0 (null) oder mehr zusätzlichen Mittelwert Attributen an.</span><span class="sxs-lookup"><span data-stu-id="9cea9-109">Specifies a list of zero or more additional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="9cea9-110">*Schnittstellen Name*</span><span class="sxs-lookup"><span data-stu-id="9cea9-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9cea9-111">Der Name der Schnittstelle, auf die das **\[ enable \_ allcoate \]** -Attribut angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="9cea9-111">The name of the interface to which the **\[enable\_allcoate\]** attribute will be applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9cea9-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9cea9-112">Remarks</span></span>

<span data-ttu-id="9cea9-113">Im Standardmodus aktiviert der Serverstub die Arbeitsspeicher Umgebung nur, wenn das Attribut " **\[ \_ zuordnen \]** " verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9cea9-113">In default mode, the server stub enables the memory environment only when the **\[enable\_allocate\]** attribute is used.</span></span> <span data-ttu-id="9cea9-114">Die Speicher Verwaltungs Umgebung muss aktiviert werden, damit der Arbeitsspeicher mithilfe von [**rpcsmallozugewiesen**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate)werden kann.</span><span class="sxs-lookup"><span data-stu-id="9cea9-114">The memory management environment must be enabled before memory can be allocated using [**RpcSmAllocate**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate).</span></span> <span data-ttu-id="9cea9-115">Im **eines Zertifikats** -Modus (bei der Kompilierung mithilfe des [**/OSF**](-osf.md) -Schalters) aktiviert der Stub diese Umgebung automatisch oder bei einer Anforderung, wenn das Attribut " **\[ \_ zuordnen \]** " verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9cea9-115">In **osf** mode (when you compile using the [**/osf**](-osf.md) switch), the stub enables this environment automatically, or on request when the **\[enable\_allocate\]** attribute is used.</span></span>

<span data-ttu-id="9cea9-116">Der Client seitige Stub kann für die **RPCSS** -Speicher Verwaltungs Umgebung empfindlich sein.</span><span class="sxs-lookup"><span data-stu-id="9cea9-116">The client side stub may be sensitive to the **Rpcss** memory management environment.</span></span> <span data-ttu-id="9cea9-117">Wenn ein sensibler Clientstub ausgeführt wird, wenn das **RPCSS** -Paket deaktiviert ist, werden die standardmäßigen benutzerallokator/-deallocators aufgerufen (z. b. " [Mittel l Benutzer", wenn Sie den \_ \_](/windows/desktop/Rpc/the-midl-user-allocate-function) /  [ \_ Benutzer \_ kostenlos](/windows/desktop/Rpc/the-midl-user-free-function)zuweisen).</span><span class="sxs-lookup"><span data-stu-id="9cea9-117">If a sensitive client stub is executed when the **Rpcss** package is disabled, the default user allocator/deallocators are called (for example, [midl\_user\_allocate](/windows/desktop/Rpc/the-midl-user-allocate-function)/ [midl\_user\_free](/windows/desktop/Rpc/the-midl-user-free-function)).</span></span> <span data-ttu-id="9cea9-118">Wenn diese Option aktiviert ist, verwendet das **RPCSS** -Paket das zuordnerpaar/das dezuordnerpaar aus dem Paket.</span><span class="sxs-lookup"><span data-stu-id="9cea9-118">When enabled, the **Rpcss** package uses the allocator/deallocator pair from the package.</span></span> <span data-ttu-id="9cea9-119">Im Standardmodus ist der Client nur dann sensibel, wenn das Attribut " **\[ \_ zuordnen \]** " verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9cea9-119">In the default mode, the client is sensitive only when the **\[enable\_allocate\]** attribute is used.</span></span> <span data-ttu-id="9cea9-120">In der Regel arbeitet der Client seitige Stub in der deaktivierten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="9cea9-120">Typically, the client side stub operates in the disabled environment.</span></span> <span data-ttu-id="9cea9-121">Im **eines Zertifikats** -Modus (bei der Kompilierung mithilfe des [**/OSF**](-osf.md) -Schalters) ist der Client immer für die **RPCSS** -Speicher Verwaltungs Umgebung sensibel. Daher wirkt sich das Attribut " **\[ \_ zuordnen \]** " nicht auf die Clientstub aus.</span><span class="sxs-lookup"><span data-stu-id="9cea9-121">In **osf** mode (when you compile using the [**/osf**](-osf.md) switch), the client is always sensitive to the **Rpcss** memory management environment and, therefore, the **\[enable\_allocate\]** attribute will not affect the client stubs.</span></span>

## <a name="see-also"></a><span data-ttu-id="9cea9-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9cea9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cea9-123">Anwendungs Konfigurationsdatei (ACF)</span><span class="sxs-lookup"><span data-stu-id="9cea9-123">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="9cea9-124">mittlere Benutzer Zuordnungen \_ \_</span><span class="sxs-lookup"><span data-stu-id="9cea9-124">midl\_user\_allocate</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="9cea9-125">mittlerer l- \_ Benutzer \_ kostenlos</span><span class="sxs-lookup"><span data-stu-id="9cea9-125">midl\_user\_free</span></span>](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[<span data-ttu-id="9cea9-126">**/osf**</span><span class="sxs-lookup"><span data-stu-id="9cea9-126">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="9cea9-127">Rpcsmdisablezuordnen</span><span class="sxs-lookup"><span data-stu-id="9cea9-127">RpcSmDisableAllocate</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmdisableallocate)
</dt> <dt>

[<span data-ttu-id="9cea9-128">Rpcsmenablezuordnen</span><span class="sxs-lookup"><span data-stu-id="9cea9-128">RpcSmEnableAllocate</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmenableallocate)
</dt> <dt>

[<span data-ttu-id="9cea9-129">Rpcsmfree</span><span class="sxs-lookup"><span data-stu-id="9cea9-129">RpcSmFree</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree)
</dt> </dl>

 

 