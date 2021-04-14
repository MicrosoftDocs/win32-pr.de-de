---
title: Provisioningjobexecute-Methode der Win32_RDMSVirtualDesktopCollection-Klasse
description: Führt einen Bereitstellungs Auftrag für virtuelle Desktops aus.
ms.assetid: 69f0cc6a-7eef-4cd9-94ac-f0c7e52d02d8
ms.tgt_platform: multiple
keywords:
- Provisioningjobexecute-Methode Remotedesktopdienste
- Provisioningjobexecute-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktopCollection-Klasse
- Win32_RDMSVirtualDesktopCollection-Klasse Remotedesktopdienste, provisioningjobexecute-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobExecute
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c632a6bdc5fc5c4a128941d8a6c8b4379ddf9629
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478870"
---
# <a name="provisioningjobexecute-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="5ef2f-106">Provisioningjobexecute-Methode der Win32 \_ rdmsvirtualdesktopcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="5ef2f-106">ProvisioningJobExecute method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="5ef2f-107">Führt einen Bereitstellungs Auftrag für virtuelle Desktops aus.</span><span class="sxs-lookup"><span data-stu-id="5ef2f-107">Runs a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ef2f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ef2f-108">Syntax</span></span>


```mof
uint32 ProvisioningJobExecute(
  [in]  string JobInputXml,
  [out] string JobGuid
);
```



## <a name="parameters"></a><span data-ttu-id="5ef2f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ef2f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ef2f-110">*Jobinputxml* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ef2f-110">*JobInputXml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ef2f-111">Eine Zeichenfolge, die die Bereitstellungs Informationen im XML-Format enthält.</span><span class="sxs-lookup"><span data-stu-id="5ef2f-111">A string that contains the provisioning information in XML format.</span></span>

</dd> <dt>

<span data-ttu-id="5ef2f-112">*Jobguid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5ef2f-112">*JobGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ef2f-113">Die **GUID** , die den zu testender Bereitstellungs Auftrag eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5ef2f-113">The **GUID** that uniquely identifies the provisioning job to run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ef2f-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ef2f-114">Return value</span></span>

<span data-ttu-id="5ef2f-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5ef2f-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ef2f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ef2f-116">Requirements</span></span>



| <span data-ttu-id="5ef2f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ef2f-117">Requirement</span></span> | <span data-ttu-id="5ef2f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="5ef2f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ef2f-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ef2f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5ef2f-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5ef2f-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="5ef2f-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ef2f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5ef2f-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ef2f-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="5ef2f-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ef2f-123">Namespace</span></span><br/>                | <span data-ttu-id="5ef2f-124">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="5ef2f-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="5ef2f-125">MOF</span><span class="sxs-lookup"><span data-stu-id="5ef2f-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ef2f-126"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5ef2f-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ef2f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="5ef2f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ef2f-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ef2f-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="5ef2f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ef2f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ef2f-130">**Win32 \_ rdmsvirtualdesktopcollection**</span><span class="sxs-lookup"><span data-stu-id="5ef2f-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





