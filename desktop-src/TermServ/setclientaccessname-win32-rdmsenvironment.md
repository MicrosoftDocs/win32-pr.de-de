---
title: Setclientaccessname-Methode der Win32_RDMSEnvironment-Klasse
description: Aktualisiert den Namen der Domain Name System (DNS) Resource Record (RR) einer Remotedesktop Verwaltungsdienste-Umgebung (RDMs).
ms.assetid: bbce3fc1-d2c5-4874-bdd0-be27fb5981d1
ms.tgt_platform: multiple
keywords:
- Setclientaccessname-Methode Remotedesktopdienste
- Setclientaccessname-Methode Remotedesktopdienste, Win32_RDMSEnvironment-Klasse
- Win32_RDMSEnvironment-Klasse Remotedesktopdienste, setclientaccessname-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13f9087fe2c2139833baeb21bc62da508c6e5989
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344506"
---
# <a name="setclientaccessname-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="0c195-106">Setclientaccessname-Methode der Win32- \_ Klasse "rdmsenvironment"</span><span class="sxs-lookup"><span data-stu-id="0c195-106">SetClientAccessName method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="0c195-107">Aktualisiert den Namen der Domain Name System (DNS) Resource Record (RR) einer Remotedesktop Verwaltungsdienste-Umgebung (RDMs).</span><span class="sxs-lookup"><span data-stu-id="0c195-107">Updates the Domain Name System (DNS) resource record (RR) name of an Remote Desktop Management Services (RDMS) environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c195-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c195-108">Syntax</span></span>


```mof
uint32 SetClientAccessName(
  [in] string ClientAccessName
);
```



## <a name="parameters"></a><span data-ttu-id="0c195-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c195-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c195-110">*Clientaccessname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c195-110">*ClientAccessName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c195-111">Der neue RR-Name.</span><span class="sxs-lookup"><span data-stu-id="0c195-111">The new RR name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c195-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c195-112">Return value</span></span>

<span data-ttu-id="0c195-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0c195-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c195-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c195-114">Requirements</span></span>



| <span data-ttu-id="0c195-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c195-115">Requirement</span></span> | <span data-ttu-id="0c195-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0c195-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c195-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0c195-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0c195-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0c195-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="0c195-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0c195-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0c195-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0c195-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="0c195-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="0c195-121">Namespace</span></span><br/>                | <span data-ttu-id="0c195-122">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="0c195-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="0c195-123">MOF</span><span class="sxs-lookup"><span data-stu-id="0c195-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c195-124"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0c195-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c195-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0c195-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c195-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c195-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="0c195-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c195-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c195-128">**Win32- \_ rdmsenvironment**</span><span class="sxs-lookup"><span data-stu-id="0c195-128">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





