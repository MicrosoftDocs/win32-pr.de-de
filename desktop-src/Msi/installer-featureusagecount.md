---
description: Die featureusagecount-Eigenschaft ist eine schreibgeschützte Eigenschaft, die zurückgibt, wie oft die Funktion verwendet wurde.
ms.assetid: 70171e22-d73a-4718-a360-df9d1722761b
title: Installer. featureusagecount-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageCount
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fbacb6b6fd5dc4d31d7c727d719e1253969c0d43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367443"
---
# <a name="installerfeatureusagecount-property"></a><span data-ttu-id="e7ab1-103">Installer. featureusagecount-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e7ab1-103">Installer.FeatureUsageCount property</span></span>

<span data-ttu-id="e7ab1-104">Die **featureusagecount** -Eigenschaft ist eine schreibgeschützte Eigenschaft, die zurückgibt, wie oft die Funktion verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e7ab1-104">The **FeatureUsageCount** property is a read-only property that returns the number of times the feature has been used.</span></span>

<span data-ttu-id="e7ab1-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e7ab1-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7ab1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7ab1-106">Syntax</span></span>


```JScript
propVal = Installer.FeatureUsageCount
```



## <a name="property-value"></a><span data-ttu-id="e7ab1-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e7ab1-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="e7ab1-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7ab1-108">Remarks</span></span>

<span data-ttu-id="e7ab1-109">Die Verwendung der [**Funktionen usefeature**](installer-usefeature.md), [**providecomponent**](installer-providecomponent.md) oder [**providequalifiedcomponent**](installer-providequalifiedcomponent.md) oder ihrer API-Entsprechungen für die angegebene Funktion erhöht diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e7ab1-109">Use of the [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) or [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) methods or their API equivalents on the specified feature increments this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7ab1-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7ab1-110">Requirements</span></span>



| <span data-ttu-id="e7ab1-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7ab1-111">Requirement</span></span> | <span data-ttu-id="e7ab1-112">Wert</span><span class="sxs-lookup"><span data-stu-id="e7ab1-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7ab1-113">Version</span><span class="sxs-lookup"><span data-stu-id="e7ab1-113">Version</span></span><br/> | <span data-ttu-id="e7ab1-114">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e7ab1-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e7ab1-115">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e7ab1-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e7ab1-116">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="e7ab1-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e7ab1-117">DLL</span><span class="sxs-lookup"><span data-stu-id="e7ab1-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="e7ab1-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7ab1-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e7ab1-119">IID</span><span class="sxs-lookup"><span data-stu-id="e7ab1-119">IID</span></span><br/>     | <span data-ttu-id="e7ab1-120">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e7ab1-120">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="e7ab1-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7ab1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7ab1-122">**Msigetfeatureusage**</span><span class="sxs-lookup"><span data-stu-id="e7ab1-122">**MsiGetFeatureUsage**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




