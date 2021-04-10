---
title: Registeredtask. getsecuritydescriptor-Methode
description: Ruft bei der Skripterstellung die Sicherheits Beschreibung ab, die als Anmelde Informationen für die registrierte Aufgabe verwendet wird.
ms.assetid: 9b5985c5-c01a-4104-940f-1e0e79f18bb7
keywords:
- Getsecuritydescriptor-Methode Taskplaner
- Getsecuritydescriptor-Methode Taskplaner, registeredtask-Objekt
- Registeredtask-Objekt Taskplaner, getsecuritydescriptor-Methode
topic_type:
- apiref
api_name:
- RegisteredTask.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85c7c0e6125bc848b361e4cc2d4515c32d797c57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956928"
---
# <a name="registeredtaskgetsecuritydescriptor-method"></a><span data-ttu-id="4d8a3-106">Registeredtask. getsecuritydescriptor-Methode</span><span class="sxs-lookup"><span data-stu-id="4d8a3-106">RegisteredTask.GetSecurityDescriptor method</span></span>

<span data-ttu-id="4d8a3-107">Ruft bei der Skripterstellung die Sicherheits Beschreibung ab, die als Anmelde Informationen für die registrierte Aufgabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4d8a3-107">For scripting, gets the security descriptor that is used as credentials for the registered task.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d8a3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d8a3-108">Syntax</span></span>


```VB
sddl = .GetSecurityDescriptor( _
  ByVal securityInformation _
)
```



## <a name="parameters"></a><span data-ttu-id="4d8a3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d8a3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d8a3-110">*securityinformation*</span><span class="sxs-lookup"><span data-stu-id="4d8a3-110">*securityInformation*</span></span> 
</dt> <dd>

<span data-ttu-id="4d8a3-111">Die Sicherheitsinformationen aus [**Sicherheits \_ Informationen**](/windows/desktop/SecAuthZ/security-information).</span><span class="sxs-lookup"><span data-stu-id="4d8a3-111">The security information from [**SECURITY\_INFORMATION**](/windows/desktop/SecAuthZ/security-information).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d8a3-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d8a3-112">Return value</span></span>

<span data-ttu-id="4d8a3-113">Die Sicherheits Beschreibung für den registrierten Task.</span><span class="sxs-lookup"><span data-stu-id="4d8a3-113">The security descriptor for the registered task.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d8a3-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d8a3-114">Requirements</span></span>



| <span data-ttu-id="4d8a3-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d8a3-115">Requirement</span></span> | <span data-ttu-id="4d8a3-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4d8a3-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d8a3-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4d8a3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4d8a3-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4d8a3-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4d8a3-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4d8a3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4d8a3-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4d8a3-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4d8a3-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="4d8a3-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="4d8a3-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4d8a3-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4d8a3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4d8a3-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d8a3-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d8a3-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d8a3-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d8a3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d8a3-126">**Registeredtask**</span><span class="sxs-lookup"><span data-stu-id="4d8a3-126">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="4d8a3-127">**Taskfolder. getsecuritydescriptor**</span><span class="sxs-lookup"><span data-stu-id="4d8a3-127">**TaskFolder.GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="4d8a3-128">**Registeredtask. SETSECURITYDESCRIPTOR**</span><span class="sxs-lookup"><span data-stu-id="4d8a3-128">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

