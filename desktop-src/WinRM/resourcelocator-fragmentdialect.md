---
title: ResourceLocator. Fragmentdialekt-Eigenschaft (WSManDisp. h)
description: Ruft den sprach Dialekt für einen Ressourcen Fragment-Dialekt ab, wenn ResourceLocator in Sitzungs Objekt Vorgängen wie "Session. Get", "Session. Put" oder "Session. Enumerate" verwendet wird, oder legt ihn fest.
ms.assetid: 60b08084-f4b9-4049-b0cd-a7420fcffd7c
ms.tgt_platform: multiple
keywords:
- Fragmentdialekt-Eigenschaft Windows-Remoteverwaltung
- Fragmentdialekt-Eigenschaft Windows-Remoteverwaltung, ResourceLocator-Objekt
- ResourceLocator-Objekt Windows-Remoteverwaltung, Fragmentdialekt (Eigenschaft)
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentDialect
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1fe42c2bbe15c75d5f38ea47119f9649e678931
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478783"
---
# <a name="resourcelocatorfragmentdialect-property"></a><span data-ttu-id="de084-106">ResourceLocator. Fragmentdialekt (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="de084-106">ResourceLocator.FragmentDialect property</span></span>

<span data-ttu-id="de084-107">Ruft den sprach Dialekt für einen [*Ressourcen*](windows-remote-management-glossary.md) [*Fragment*](windows-remote-management-glossary.md) - *Dialekt* ab, wenn [**ResourceLocator**](resourcelocator.md) in [**Sitzungs**](session.md) Objekt Vorgängen wie " [**Session. Get**](session-get.md)", " [**Session. Put**](session-put.md)" oder " [**Session. Enumerate**](session-enumerate.md)" verwendet wird, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="de084-107">Gets or sets the language dialect for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md) *dialect* when [**ResourceLocator**](resourcelocator.md) is used in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="de084-108">Ein Fragment stellt eine Eigenschaft oder einen Teil einer Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="de084-108">A fragment represents one property or part of a resource.</span></span> <span data-ttu-id="de084-109">Sie können ein [**ResourceLocator**](resourcelocator.md) -Objekt bereitstellen, anstatt einen Ressourcen-URI in [**Sitzungs**](session.md) Objekt Vorgängen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="de084-109">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations.</span></span> <span data-ttu-id="de084-110">Der Dialekt gibt an, welche XML-Sprache das Fragment für den Dienst beschreibt, der die [WS-Management-Protokoll](ws-management-protocol.md) implementiert und die Anforderung empfängt.</span><span class="sxs-lookup"><span data-stu-id="de084-110">The dialect indicates what XML language describes the fragment to the service that implements the [WS-Management Protocol](ws-management-protocol.md) and receives the request.</span></span>

<span data-ttu-id="de084-111">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="de084-111">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="de084-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="de084-112">Syntax</span></span>


```VB
ResourceLocator.FragmentDialect As string
```



## <a name="property-value"></a><span data-ttu-id="de084-113">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="de084-113">Property value</span></span>

<span data-ttu-id="de084-114">Eine XML-Zeichenfolge, die die Sprache angibt, die in der [**fragmentpath**](resourcelocator-fragmentpath.md) -Eigenschaft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="de084-114">An XML string that identifies the language used in the [**FragmentPath**](resourcelocator-fragmentpath.md) property.</span></span> <span data-ttu-id="de084-115">Die Dialekt Zeichenfolge ist standardmäßig die XPath 1,0-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="de084-115">The dialect string defaults to the XPath 1.0 specification.</span></span> <span data-ttu-id="de084-116">Weitere Informationen finden Sie unter [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span><span class="sxs-lookup"><span data-stu-id="de084-116">For more information, see [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span></span>

## <a name="remarks"></a><span data-ttu-id="de084-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de084-117">Remarks</span></span>

<span data-ttu-id="de084-118">[**Iwsmanresourcelocator:: Fragmentdialekt**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect) ist die entsprechende C++-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="de084-118">[**IWSManResourceLocator::FragmentDialect**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect) is the corresponding C++ property.</span></span>

## <a name="requirements"></a><span data-ttu-id="de084-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de084-119">Requirements</span></span>



| <span data-ttu-id="de084-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de084-120">Requirement</span></span> | <span data-ttu-id="de084-121">Wert</span><span class="sxs-lookup"><span data-stu-id="de084-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="de084-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de084-122">Minimum supported client</span></span><br/> | <span data-ttu-id="de084-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de084-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="de084-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de084-124">Minimum supported server</span></span><br/> | <span data-ttu-id="de084-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de084-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="de084-126">Header</span><span class="sxs-lookup"><span data-stu-id="de084-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="de084-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="de084-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="de084-128">IDL</span><span class="sxs-lookup"><span data-stu-id="de084-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="de084-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="de084-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="de084-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="de084-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="de084-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="de084-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="de084-132">DLL</span><span class="sxs-lookup"><span data-stu-id="de084-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de084-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de084-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="de084-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de084-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de084-135">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="de084-135">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





