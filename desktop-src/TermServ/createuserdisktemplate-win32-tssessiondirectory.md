---
title: Methode "kreateuserdisktemplate" der Win32_TSSessionDirectory-Klasse
description: Erstellt eine Vorlage für Benutzer Datenträger.
ms.assetid: 4036a418-b082-4376-a400-16f48b98f071
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "kreateuserdisktemplate"
- Methode Remotedesktopdienste der Methode "kreateuserdisktemplate", Win32_TSSessionDirectory Klasse
- Win32_TSSessionDirectory-Klasse Remotedesktopdienste, Methode "kreateuserdisktemplate"
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.CreateUserDiskTemplate
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c142834b4501639499cd0bcf102dadcc1b07d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103098"
---
# <a name="createuserdisktemplate-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="faee7-106">Methode "| ateuserdisktemplate" der Win32- \_ Klasse "tssessiondirectory"</span><span class="sxs-lookup"><span data-stu-id="faee7-106">CreateUserDiskTemplate method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="faee7-107">Erstellt eine Vorlage für Benutzer Datenträger.</span><span class="sxs-lookup"><span data-stu-id="faee7-107">Creates a user disk template.</span></span>

## <a name="syntax"></a><span data-ttu-id="faee7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="faee7-108">Syntax</span></span>


```mof
uint32 CreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a><span data-ttu-id="faee7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="faee7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="faee7-110">*Userdisksstorageurl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="faee7-110">*UserDisksStorageUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faee7-111">Der Speicherort der Freigabe, auf der alle Benutzer Datenträger gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="faee7-111">The location of the share where all user disks are stored.</span></span>

</dd> <dt>

<span data-ttu-id="faee7-112">*Userdiskmaxsizzugb* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="faee7-112">*UserDiskMaxSizeInGB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faee7-113">Die maximale Größe in Gigabyte für alle Benutzer Datenträger.</span><span class="sxs-lookup"><span data-stu-id="faee7-113">The maximum size in gigabytes, for all user disks.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="faee7-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="faee7-114">Requirements</span></span>



| <span data-ttu-id="faee7-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="faee7-115">Requirement</span></span> | <span data-ttu-id="faee7-116">Wert</span><span class="sxs-lookup"><span data-stu-id="faee7-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="faee7-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="faee7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="faee7-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="faee7-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="faee7-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="faee7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="faee7-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="faee7-120">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="faee7-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="faee7-121">Namespace</span></span><br/>                | <span data-ttu-id="faee7-122">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="faee7-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="faee7-123">MOF</span><span class="sxs-lookup"><span data-stu-id="faee7-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="faee7-124"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="faee7-124"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="faee7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="faee7-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="faee7-126"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="faee7-126"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faee7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="faee7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faee7-128">**Win32- \_ tssessiondirectory**</span><span class="sxs-lookup"><span data-stu-id="faee7-128">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

 





