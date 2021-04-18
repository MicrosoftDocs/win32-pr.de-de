---
title: Provisioningjobgetreport-Methode der Win32_RDMSVirtualDesktopCollection-Klasse
description: Ruft einen Bericht zum Status eines virtuellen Desktop Bereitstellungs Auftrags ab.
ms.assetid: 8fc03fed-0838-4530-9b0f-0f561d76769d
ms.tgt_platform: multiple
keywords:
- Provisioningjobgetreport-Methode Remotedesktopdienste
- Provisioningjobgetreport-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktopCollection-Klasse
- Win32_RDMSVirtualDesktopCollection-Klasse Remotedesktopdienste, provisioningjobgetreport-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobGetReport
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6605402c6ed6c0269b9971922bdefd48f265c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344068"
---
# <a name="provisioningjobgetreport-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="dcd07-106">Provisioningjobgetreport-Methode der Win32 \_ rdmsvirtualdesktopcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="dcd07-106">ProvisioningJobGetReport method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="dcd07-107">Ruft einen Bericht zum Status eines virtuellen Desktop Bereitstellungs Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="dcd07-107">Gets a report about the status of a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcd07-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="dcd07-108">Syntax</span></span>


```mof
uint32 ProvisioningJobGetReport(
  [in]  string JobGuid,
  [out] string JobReportXml
);
```



## <a name="parameters"></a><span data-ttu-id="dcd07-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="dcd07-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcd07-110">*Jobguid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcd07-110">*JobGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcd07-111">Die **GUID** , die den Bereitstellungs Auftrag eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="dcd07-111">The **GUID** that uniquely identifies the provisioning job.</span></span>

</dd> <dt>

<span data-ttu-id="dcd07-112">*Jobreportxml* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dcd07-112">*JobReportXml* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcd07-113">Eine Zeichenfolge, die den Bericht im XML-Format enthält.</span><span class="sxs-lookup"><span data-stu-id="dcd07-113">A string that contains the report in XML format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcd07-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dcd07-114">Return value</span></span>

<span data-ttu-id="dcd07-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dcd07-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcd07-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dcd07-116">Requirements</span></span>



| <span data-ttu-id="dcd07-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dcd07-117">Requirement</span></span> | <span data-ttu-id="dcd07-118">Wert</span><span class="sxs-lookup"><span data-stu-id="dcd07-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcd07-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dcd07-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dcd07-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="dcd07-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="dcd07-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dcd07-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dcd07-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dcd07-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="dcd07-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="dcd07-123">Namespace</span></span><br/>                | <span data-ttu-id="dcd07-124">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="dcd07-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="dcd07-125">MOF</span><span class="sxs-lookup"><span data-stu-id="dcd07-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dcd07-126"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dcd07-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="dcd07-127">DLL</span><span class="sxs-lookup"><span data-stu-id="dcd07-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcd07-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcd07-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="dcd07-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dcd07-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcd07-130">**Win32 \_ rdmsvirtualdesktopcollection**</span><span class="sxs-lookup"><span data-stu-id="dcd07-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





