---
description: Bei der componentcurrentstate-Eigenschaft des Session-Objekts handelt es sich um eine schreibgeschützte Eigenschaft, die den aktuell installierten Zustand der angegebenen Komponente zurückgibt. Informationen zu Zustands Werten finden Sie unter der componentrequeststate-Eigenschaft.
ms.assetid: c8343e90-8867-462d-9844-e547341a590c
title: Session. componentcurrentstate-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8c556dd9656ebced155ef90fe96abd394a32ff1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368474"
---
# <a name="sessioncomponentcurrentstate-property"></a><span data-ttu-id="0127c-104">Session. componentcurrentstate-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0127c-104">Session.ComponentCurrentState property</span></span>

<span data-ttu-id="0127c-105">Bei der **componentcurrentstate** -Eigenschaft des [**Session**](session-object.md) -Objekts handelt es sich um eine schreibgeschützte Eigenschaft, die den aktuell installierten Zustand der angegebenen Komponente zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="0127c-105">The **ComponentCurrentState** property of the [**Session**](session-object.md) object is a read-only property that returns the current installed state of the designated component.</span></span> <span data-ttu-id="0127c-106">Informationen zu Zustands Werten finden Sie unter der [**componentrequeststate**](session-componentrequeststate.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0127c-106">For state values, see the [**ComponentRequestState**](session-componentrequeststate.md) property.</span></span>

<span data-ttu-id="0127c-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0127c-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0127c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0127c-108">Syntax</span></span>


```JScript
propVal = Session.ComponentCurrentState
```



## <a name="property-value"></a><span data-ttu-id="0127c-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0127c-109">Property value</span></span>

<span data-ttu-id="0127c-110">Erforderlicher Zeichen folgen Name der angeforderten Komponente, Primärschlüssel in der Komponenten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0127c-110">Required string name of the requested component, primary key into the Component table.</span></span>

## <a name="remarks"></a><span data-ttu-id="0127c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0127c-111">Remarks</span></span>

<span data-ttu-id="0127c-112">Wenn die Eigenschaft fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="0127c-112">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0127c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0127c-113">Requirements</span></span>



| <span data-ttu-id="0127c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0127c-114">Requirement</span></span> | <span data-ttu-id="0127c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="0127c-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0127c-116">Version</span><span class="sxs-lookup"><span data-stu-id="0127c-116">Version</span></span><br/> | <span data-ttu-id="0127c-117">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0127c-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0127c-118">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0127c-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0127c-119">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="0127c-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0127c-120">DLL</span><span class="sxs-lookup"><span data-stu-id="0127c-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="0127c-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0127c-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0127c-122">IID</span><span class="sxs-lookup"><span data-stu-id="0127c-122">IID</span></span><br/>     | <span data-ttu-id="0127c-123">IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0127c-123">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="0127c-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0127c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0127c-125">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="0127c-125">**Session**</span></span>](session-object.md)
</dt> <dt>

[<span data-ttu-id="0127c-126">**Componentrequeststate (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="0127c-126">**ComponentRequestState property**</span></span>](session-componentrequeststate.md)
</dt> </dl>

 

 




