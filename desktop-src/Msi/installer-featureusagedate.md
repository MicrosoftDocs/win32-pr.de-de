---
description: Die featureusagedate-Eigenschaft ist eine schreibgeschützte Eigenschaft, die das Datum zurückgibt, an dem die angegebene Funktion zuletzt verwendet wurde.
ms.assetid: 444e54b2-94e7-44ea-8d7b-eeac984e3715
title: Installer. featureusagedate (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageDate
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b393f9a24b9d1ebeb82de86d26483f703d7854c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365910"
---
# <a name="installerfeatureusagedate-property"></a><span data-ttu-id="80c99-103">Installer. featureusagedate (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="80c99-103">Installer.FeatureUsageDate property</span></span>

<span data-ttu-id="80c99-104">Die **featureusagedate** -Eigenschaft ist eine schreibgeschützte Eigenschaft, die das Datum zurückgibt, an dem die angegebene Funktion zuletzt verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="80c99-104">The **FeatureUsageDate** property is a read-only property that returns the date the specified feature was last used.</span></span>

<span data-ttu-id="80c99-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="80c99-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="80c99-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="80c99-106">Syntax</span></span>


```JScript
propVal = Installer.FeatureUsageDate
```



## <a name="property-value"></a><span data-ttu-id="80c99-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="80c99-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="80c99-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80c99-108">Remarks</span></span>

<span data-ttu-id="80c99-109">Diese Eigenschaft wird von der Verwendung der [**Funktionen usefeature**](installer-usefeature.md), [**providecomponent**](installer-providecomponent.md) oder [**providequalifiedcomponent**](installer-providequalifiedcomponent.md) oder ihrer API-Entsprechungen für die angegebene Funktion festgelegt.</span><span class="sxs-lookup"><span data-stu-id="80c99-109">Use of the [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) or [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) methods or their API equivalents on the specified feature sets this property.</span></span>

<span data-ttu-id="80c99-110">Das Datum liegt im MS-DOS-Datumsformat vor, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="80c99-110">The date is in the MS-DOS date format as shown in the following table.</span></span>



| <span data-ttu-id="80c99-111">Bits</span><span class="sxs-lookup"><span data-stu-id="80c99-111">Bits</span></span> | <span data-ttu-id="80c99-112">Inhalte</span><span class="sxs-lookup"><span data-stu-id="80c99-112">Contents</span></span>                                            |
|------|-----------------------------------------------------|
| <span data-ttu-id="80c99-113">0–4</span><span class="sxs-lookup"><span data-stu-id="80c99-113">0-4</span></span>  | <span data-ttu-id="80c99-114">Tag des Monats (1-31)</span><span class="sxs-lookup"><span data-stu-id="80c99-114">Day of the month (1-31)</span></span>                             |
| <span data-ttu-id="80c99-115">5-8</span><span class="sxs-lookup"><span data-stu-id="80c99-115">5-8</span></span>  | <span data-ttu-id="80c99-116">Monat (1 = Januar, 2 = Februar usw.)</span><span class="sxs-lookup"><span data-stu-id="80c99-116">Month (1 = January, 2 = February, and so on)</span></span>        |
| <span data-ttu-id="80c99-117">9-15</span><span class="sxs-lookup"><span data-stu-id="80c99-117">9-15</span></span> | <span data-ttu-id="80c99-118">Jahr Offset von 1980 (Hinzufügen von 1980, um das tatsächliche Jahr zu erhalten)</span><span class="sxs-lookup"><span data-stu-id="80c99-118">Year offset from 1980 (add 1980 to get actual year)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="80c99-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80c99-119">Requirements</span></span>



| <span data-ttu-id="80c99-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80c99-120">Requirement</span></span> | <span data-ttu-id="80c99-121">Wert</span><span class="sxs-lookup"><span data-stu-id="80c99-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80c99-122">Version</span><span class="sxs-lookup"><span data-stu-id="80c99-122">Version</span></span><br/> | <span data-ttu-id="80c99-123">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="80c99-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="80c99-124">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="80c99-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="80c99-125">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="80c99-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="80c99-126">DLL</span><span class="sxs-lookup"><span data-stu-id="80c99-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="80c99-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80c99-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="80c99-128">IID</span><span class="sxs-lookup"><span data-stu-id="80c99-128">IID</span></span><br/>     | <span data-ttu-id="80c99-129">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="80c99-129">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="80c99-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80c99-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80c99-131">**Msigetfeatureusage**</span><span class="sxs-lookup"><span data-stu-id="80c99-131">**MsiGetFeatureUsage**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




