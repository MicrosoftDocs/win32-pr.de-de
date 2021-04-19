---
description: Legt die Parameter der freigegebenen Ressource fest.
ms.assetid: 592d0fa6-c865-4f70-89c3-b58204a8c5a6
ms.tgt_platform: multiple
title: Setshareingefo-Methode der Win32_ClusterShare-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bda6fe36d1168045ea9f8d331ff334920ed1dd19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346037"
---
# <a name="setshareinfo-method-of-the-win32_clustershare-class"></a><span data-ttu-id="4ebda-103">Setshareingefo-Methode der Win32 \_ clustershare-Klasse</span><span class="sxs-lookup"><span data-stu-id="4ebda-103">SetShareInfo method of the Win32\_ClusterShare class</span></span>

<span data-ttu-id="4ebda-104">Legt die Parameter der freigegebenen Ressource fest.</span><span class="sxs-lookup"><span data-stu-id="4ebda-104">Sets the parameters of the shared resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ebda-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ebda-105">Syntax</span></span>


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="4ebda-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ebda-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ebda-107">*MaximumAllowed* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="4ebda-107">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebda-108">Limit für die maximale Anzahl von Benutzern, die diese Ressource gleichzeitig verwenden dürfen.</span><span class="sxs-lookup"><span data-stu-id="4ebda-108">Limit on the maximum number of users allowed to use this resource concurrently.</span></span>

</dd> <dt>

<span data-ttu-id="4ebda-109">*Beschreibung* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="4ebda-109">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebda-110">Beschreibt die freigegebene Ressource.</span><span class="sxs-lookup"><span data-stu-id="4ebda-110">Describes the resource being shared.</span></span>

</dd> <dt>

<span data-ttu-id="4ebda-111">*Zugriff* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="4ebda-111">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebda-112">Sicherheits Beschreibung für Berechtigungen auf Benutzerebene.</span><span class="sxs-lookup"><span data-stu-id="4ebda-112">Security descriptor for user-level permissions.</span></span> <span data-ttu-id="4ebda-113">Eine Sicherheits Beschreibung enthält Informationen zu den Berechtigungen, den Besitzern und den Zugriffs Funktionen der Ressource.</span><span class="sxs-lookup"><span data-stu-id="4ebda-113">A security descriptor contains information about the permission, owner, and access capabilities of the resource.</span></span> <span data-ttu-id="4ebda-114">Weitere Informationen finden Sie unter [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="4ebda-114">For more information, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4ebda-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ebda-115">Requirements</span></span>



| <span data-ttu-id="4ebda-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ebda-116">Requirement</span></span> | <span data-ttu-id="4ebda-117">Wert</span><span class="sxs-lookup"><span data-stu-id="4ebda-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ebda-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4ebda-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4ebda-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4ebda-119">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="4ebda-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4ebda-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4ebda-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4ebda-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="4ebda-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ebda-122">Namespace</span></span><br/>                | <span data-ttu-id="4ebda-123">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4ebda-123">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4ebda-124">MOF</span><span class="sxs-lookup"><span data-stu-id="4ebda-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ebda-125"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4ebda-125"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ebda-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4ebda-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ebda-127"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ebda-127"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ebda-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ebda-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ebda-129">**Win32- \_ clustershare**</span><span class="sxs-lookup"><span data-stu-id="4ebda-129">**Win32\_ClusterShare**</span></span>](win32-clustershare.md)
</dt> </dl>

 

