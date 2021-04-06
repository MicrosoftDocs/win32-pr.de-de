---
title: Rdvkreateuserdisktemplate-Methode der Win32_RdvhManagement-Klasse
description: Erstellt eine Vorlage für einen Benutzer Datenträger mit der angegebenen maximalen Größe an der angegebenen Position.
ms.assetid: b8ca8b8c-58fd-44fc-9a88-5d7d41ef96a2
ms.tgt_platform: multiple
keywords:
- Rdvkreateuserdisktemplate-Methode Remotedesktopdienste
- Rdvkreateuserdisktemplate-Methode Remotedesktopdienste, Win32_RdvhManagement-Klasse
- Win32_RdvhManagement-Klasse Remotedesktopdienste, rdvkreateuserdisktemplate-Methode
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvCreateUserDiskTemplate
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cdc7fec869fa4ffde9ac0a5a724f73b04b84351
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743288"
---
# <a name="rdvcreateuserdisktemplate-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="af9dc-106">Rdvkreateuserdisktemplate-Methode der Win32 \_ rdvhmanagement-Klasse</span><span class="sxs-lookup"><span data-stu-id="af9dc-106">RdvCreateUserDiskTemplate method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="af9dc-107">Erstellt eine Vorlage für einen Benutzer Datenträger mit der angegebenen maximalen Größe an der angegebenen Position.</span><span class="sxs-lookup"><span data-stu-id="af9dc-107">Creates a user disk template, with the specified maximum size, at the specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="af9dc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="af9dc-108">Syntax</span></span>


```mof
uint32 RdvCreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a><span data-ttu-id="af9dc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="af9dc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af9dc-110">*Userdisksstorageurl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af9dc-110">*UserDisksStorageUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af9dc-111">Speicherort des Benutzer Festplatten Speichers.</span><span class="sxs-lookup"><span data-stu-id="af9dc-111">Location of the user disk storage.</span></span>

</dd> <dt>

<span data-ttu-id="af9dc-112">*Userdiskmaxsizzugb* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af9dc-112">*UserDiskMaxSizeInGB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af9dc-113">Maximale Größe des Benutzer Datenträgers in GB.</span><span class="sxs-lookup"><span data-stu-id="af9dc-113">Maximum size of the user disk, in GB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af9dc-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="af9dc-114">Return value</span></span>

<span data-ttu-id="af9dc-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="af9dc-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="af9dc-116">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="af9dc-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="af9dc-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af9dc-117">Remarks</span></span>

<span data-ttu-id="af9dc-118">Alle Benutzer Datenträger, die mit dieser Vorlage erstellt werden, haben dieselbe maximale Größe wie die Vorlage.</span><span class="sxs-lookup"><span data-stu-id="af9dc-118">All user disks created using this template will have the same maximum size as the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="af9dc-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af9dc-119">Requirements</span></span>



| <span data-ttu-id="af9dc-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af9dc-120">Requirement</span></span> | <span data-ttu-id="af9dc-121">Wert</span><span class="sxs-lookup"><span data-stu-id="af9dc-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="af9dc-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="af9dc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="af9dc-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="af9dc-123">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="af9dc-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="af9dc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="af9dc-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="af9dc-125">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="af9dc-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="af9dc-126">Namespace</span></span><br/>                | <span data-ttu-id="af9dc-127">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="af9dc-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="af9dc-128">MOF</span><span class="sxs-lookup"><span data-stu-id="af9dc-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af9dc-129"><dt>"Zvmhost. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="af9dc-129"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="af9dc-130">DLL</span><span class="sxs-lookup"><span data-stu-id="af9dc-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af9dc-131"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af9dc-131"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af9dc-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af9dc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af9dc-133">**Win32- \_ rdvhmanagement**</span><span class="sxs-lookup"><span data-stu-id="af9dc-133">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





