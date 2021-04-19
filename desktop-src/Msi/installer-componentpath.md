---
description: Die componentpath-Eigenschaft ist eine schreibgeschützte Eigenschaft, die den vollständigen Pfad zu einer installierten Komponente zurückgibt. Wenn der Schlüssel Pfad für die Komponente ein Registrierungsschlüssel ist, wird der Registrierungsschlüssel zurückgegeben.
ms.assetid: 6e53419d-f28a-45cd-abc8-0f451177f3fc
title: Installer. componentpath (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e249290af2477d2dfcbc73f80f80b439f1dd3663
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361961"
---
# <a name="installercomponentpath-property"></a><span data-ttu-id="95b24-104">Installer. componentpath (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="95b24-104">Installer.ComponentPath property</span></span>

<span data-ttu-id="95b24-105">Die **componentpath** -Eigenschaft ist eine schreibgeschützte Eigenschaft, die den vollständigen Pfad zu einer installierten Komponente zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="95b24-105">The **ComponentPath** property is a read-only property that returns the full path to an installed component.</span></span> <span data-ttu-id="95b24-106">Wenn der Schlüssel Pfad für die Komponente ein Registrierungsschlüssel ist, wird der Registrierungsschlüssel zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="95b24-106">If the key path for the component is a registry key then the registry key is returned.</span></span>

<span data-ttu-id="95b24-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="95b24-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="95b24-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="95b24-108">Syntax</span></span>


```JScript
propVal = Installer.ComponentPath
```



## <a name="property-value"></a><span data-ttu-id="95b24-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="95b24-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="95b24-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95b24-110">Remarks</span></span>

<span data-ttu-id="95b24-111">Wenn es sich bei der Komponente um einen Registrierungsschlüssel handelt, werden die Registrierungs Stämme numerisch dargestellt.</span><span class="sxs-lookup"><span data-stu-id="95b24-111">If the component is a registry key, the registry roots are represented numerically.</span></span> <span data-ttu-id="95b24-112">Beispielsweise würde der Registrierungs Pfad "HKEY \_ Current \_ User \\ Software \\ Microsoft" als "01: \\ Software Microsoft" zurückgegeben werden \\ .</span><span class="sxs-lookup"><span data-stu-id="95b24-112">For example, a registry path of "HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft" would be returned as "01:\\SOFTWARE\\Microsoft".</span></span> <span data-ttu-id="95b24-113">Die zurückgegebenen Registrierungs Stämme werden wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="95b24-113">The registry roots returned are defined as follows:</span></span>



| <span data-ttu-id="95b24-114">Root</span><span class="sxs-lookup"><span data-stu-id="95b24-114">Root</span></span>                    | <span data-ttu-id="95b24-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95b24-115">Returned value</span></span> |
|-------------------------|----------------|
| <span data-ttu-id="95b24-116">HKEY- \_ Klassen Stamm \_</span><span class="sxs-lookup"><span data-stu-id="95b24-116">HKEY\_CLASSES\_ROOT</span></span>     | <span data-ttu-id="95b24-117">00</span><span class="sxs-lookup"><span data-stu-id="95b24-117">00</span></span>             |
| <span data-ttu-id="95b24-118">Aktueller HKEY- \_ \_ Benutzer</span><span class="sxs-lookup"><span data-stu-id="95b24-118">HKEY\_CURRENT\_USER</span></span>     | <span data-ttu-id="95b24-119">01</span><span class="sxs-lookup"><span data-stu-id="95b24-119">01</span></span>             |
| <span data-ttu-id="95b24-120">lokaler HKEY- \_ \_ Computer</span><span class="sxs-lookup"><span data-stu-id="95b24-120">HKEY\_LOCAL\_MACHINE</span></span>    | <span data-ttu-id="95b24-121">02</span><span class="sxs-lookup"><span data-stu-id="95b24-121">02</span></span>             |
| <span data-ttu-id="95b24-122">HKEY- \_ Benutzer</span><span class="sxs-lookup"><span data-stu-id="95b24-122">HKEY\_USERS</span></span>             | <span data-ttu-id="95b24-123">03</span><span class="sxs-lookup"><span data-stu-id="95b24-123">03</span></span>             |
| <span data-ttu-id="95b24-124">HKEY- \_ Leistungs \_ Daten</span><span class="sxs-lookup"><span data-stu-id="95b24-124">HKEY\_PERFORMANCE\_DATA</span></span> | <span data-ttu-id="95b24-125">04</span><span class="sxs-lookup"><span data-stu-id="95b24-125">04</span></span>             |



 

## <a name="requirements"></a><span data-ttu-id="95b24-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95b24-126">Requirements</span></span>



| <span data-ttu-id="95b24-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95b24-127">Requirement</span></span> | <span data-ttu-id="95b24-128">Wert</span><span class="sxs-lookup"><span data-stu-id="95b24-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95b24-129">Version</span><span class="sxs-lookup"><span data-stu-id="95b24-129">Version</span></span><br/> | <span data-ttu-id="95b24-130">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="95b24-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="95b24-131">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="95b24-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="95b24-132">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="95b24-132">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="95b24-133">DLL</span><span class="sxs-lookup"><span data-stu-id="95b24-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="95b24-134"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95b24-134"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="95b24-135">IID</span><span class="sxs-lookup"><span data-stu-id="95b24-135">IID</span></span><br/>     | <span data-ttu-id="95b24-136">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="95b24-136">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="95b24-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95b24-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95b24-138">**MsiGetComponentPath**</span><span class="sxs-lookup"><span data-stu-id="95b24-138">**MsiGetComponentPath**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)
</dt> </dl>

 

 




