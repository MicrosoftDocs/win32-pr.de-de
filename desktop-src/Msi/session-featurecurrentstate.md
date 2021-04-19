---
description: Die featurecurrentstate-Eigenschaft des Session-Objekts ist eine schreibgeschützte Eigenschaft, die den aktuell installierten Zustand der angegebenen Funktion zurückgibt. Informationen zu Zustands Werten finden Sie unter der Eigenschaft "featurerequeststate".
ms.assetid: c4c325dc-6e7e-4009-8707-952c04574170
title: Session. featurecurrentstate (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 47c834571dd211dd085ed94e9d8c1ff9d5516c9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359411"
---
# <a name="sessionfeaturecurrentstate-property"></a><span data-ttu-id="ca397-104">Session. featurecurrentstate (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ca397-104">Session.FeatureCurrentState property</span></span>

<span data-ttu-id="ca397-105">Die **featurecurrentstate** -Eigenschaft des [**Session**](session-object.md) -Objekts ist eine schreibgeschützte Eigenschaft, die den aktuell installierten Zustand der angegebenen Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ca397-105">The **FeatureCurrentState** property of the [**Session**](session-object.md) object is a read-only property that returns the current installed state of the designated feature.</span></span> <span data-ttu-id="ca397-106">Informationen zu Zustands Werten finden Sie unter der Eigenschaft " [**featurerequeststate**](session-featurerequeststate.md) ".</span><span class="sxs-lookup"><span data-stu-id="ca397-106">For state values, see the [**FeatureRequestState**](session-featurerequeststate.md) property.</span></span>

<span data-ttu-id="ca397-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ca397-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca397-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca397-108">Syntax</span></span>


```JScript
propVal = Session.FeatureCurrentState
```



## <a name="property-value"></a><span data-ttu-id="ca397-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ca397-109">Property value</span></span>

<span data-ttu-id="ca397-110">Erforderlicher Zeichen folgen Name der angeforderten Funktion und ein Primärschlüssel in der [Featuretabelle](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="ca397-110">Required string name of the requested feature, and a primary key into the [Feature table](feature-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ca397-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca397-111">Remarks</span></span>

<span data-ttu-id="ca397-112">Wenn die Eigenschaft fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="ca397-112">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca397-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca397-113">Requirements</span></span>



| <span data-ttu-id="ca397-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca397-114">Requirement</span></span> | <span data-ttu-id="ca397-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ca397-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca397-116">Version</span><span class="sxs-lookup"><span data-stu-id="ca397-116">Version</span></span><br/> | <span data-ttu-id="ca397-117">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ca397-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ca397-118">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ca397-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ca397-119">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="ca397-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="ca397-120">DLL</span><span class="sxs-lookup"><span data-stu-id="ca397-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="ca397-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca397-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="ca397-122">IID</span><span class="sxs-lookup"><span data-stu-id="ca397-122">IID</span></span><br/>     | <span data-ttu-id="ca397-123">IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ca397-123">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="ca397-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca397-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca397-125">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="ca397-125">**Session**</span></span>](session-object.md)
</dt> <dt>

[<span data-ttu-id="ca397-126">**Featurerequeststate (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="ca397-126">**FeatureRequestState property**</span></span>](session-featurerequeststate.md)
</dt> </dl>

 

 




