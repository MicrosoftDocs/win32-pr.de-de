---
description: Die FeatureInfo-Methode des Session-Objekts gibt ein FeatureInfo-Objekt zurück, das beschreibende Informationen für die angegebene Funktion enthält.
ms.assetid: f5391fd4-984e-44cc-8b6c-fd97834e0674
title: Session. FeatureInfo-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6cb2acd17dd7d07024e0b490beb6d13ad2bafd6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369175"
---
# <a name="sessionfeatureinfo-method"></a><span data-ttu-id="7a8de-103">Session. FeatureInfo-Methode</span><span class="sxs-lookup"><span data-stu-id="7a8de-103">Session.FeatureInfo method</span></span>

<span data-ttu-id="7a8de-104">Die **FeatureInfo** -Methode des [**Session**](session-object.md) -Objekts gibt ein **FeatureInfo** -Objekt zurück, das beschreibende Informationen für die angegebene Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="7a8de-104">The **FeatureInfo** method of the [**Session**](session-object.md) object returns a **FeatureInfo** object containing descriptive information for the specified feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a8de-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a8de-105">Syntax</span></span>


```JScript
Session.FeatureInfo(
  Feature
)
```



## <a name="parameters"></a><span data-ttu-id="7a8de-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a8de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a8de-107">*Feature*</span><span class="sxs-lookup"><span data-stu-id="7a8de-107">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="7a8de-108">Identifiziert das relevante Feature.</span><span class="sxs-lookup"><span data-stu-id="7a8de-108">Identifies the feature of interest.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a8de-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a8de-109">Return value</span></span>

<span data-ttu-id="7a8de-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7a8de-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a8de-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a8de-111">Requirements</span></span>



| <span data-ttu-id="7a8de-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a8de-112">Requirement</span></span> | <span data-ttu-id="7a8de-113">Wert</span><span class="sxs-lookup"><span data-stu-id="7a8de-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a8de-114">Version</span><span class="sxs-lookup"><span data-stu-id="7a8de-114">Version</span></span><br/> | <span data-ttu-id="7a8de-115">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7a8de-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7a8de-116">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7a8de-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7a8de-117">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="7a8de-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="7a8de-118">DLL</span><span class="sxs-lookup"><span data-stu-id="7a8de-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="7a8de-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a8de-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="7a8de-120">IID</span><span class="sxs-lookup"><span data-stu-id="7a8de-120">IID</span></span><br/>     | <span data-ttu-id="7a8de-121">IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7a8de-121">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="7a8de-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a8de-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a8de-123">**Msigetfeatureinfo**</span><span class="sxs-lookup"><span data-stu-id="7a8de-123">**MsiGetFeatureInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)
</dt> </dl>

 

 




