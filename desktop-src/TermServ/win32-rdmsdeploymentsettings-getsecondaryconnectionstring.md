---
title: Getsecondaryconnectionstring-Methode der Win32_RDMSDeploymentSettings-Klasse
description: Ruft die sekundäre Daten bankverbindungs Zeichenfolge auf Bereitstellungs Ebene ab, die zur Unterstützung des Kenn Wort Ablaufs verwendet werden kann.
ms.assetid: 0de02752-6cbf-4c21-b752-a57ed58aeef1
ms.tgt_platform: multiple
keywords:
- Getsecondaryconnectionstring-Methode Remotedesktopdienste
- Getsecondaryconnectionstring-Methode Remotedesktopdienste, Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste, getsecondaryconnectionstring-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetSecondaryConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2c09f4fcacabbe928fcda00447e252077bd8a51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340638"
---
# <a name="getsecondaryconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="0a45b-106">Getsecondaryconnectionstring-Methode der Win32 \_ rdmsdeploymentsettings-Klasse</span><span class="sxs-lookup"><span data-stu-id="0a45b-106">GetSecondaryConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="0a45b-107">Ruft die sekundäre Daten bankverbindungs Zeichenfolge auf Bereitstellungs Ebene ab, die zur Unterstützung des Kenn Wort Ablaufs verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0a45b-107">Retrieves the deployment-level database secondary connection string, which may be used to support password expiration.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a45b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a45b-108">Syntax</span></span>


```mof
uint32 GetSecondaryConnectionString(
  [out] string SecondaryConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="0a45b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a45b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a45b-110">*Secondaryconnectionstring* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0a45b-110">*SecondaryConnectionString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a45b-111">Abzurufende Verbindungs Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0a45b-111">The connection string to retrieve</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a45b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0a45b-112">Return value</span></span>

<span data-ttu-id="0a45b-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0a45b-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a45b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a45b-114">Requirements</span></span>



| <span data-ttu-id="0a45b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a45b-115">Requirement</span></span> | <span data-ttu-id="0a45b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0a45b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a45b-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0a45b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0a45b-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0a45b-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="0a45b-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0a45b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0a45b-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0a45b-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="0a45b-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="0a45b-121">Namespace</span></span><br/>                | <span data-ttu-id="0a45b-122">Root \\ CIMV2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="0a45b-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="0a45b-123">MOF</span><span class="sxs-lookup"><span data-stu-id="0a45b-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a45b-124"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0a45b-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a45b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0a45b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a45b-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a45b-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="0a45b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a45b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a45b-128">**Win32 \_ rdmsdeploymentsettings**</span><span class="sxs-lookup"><span data-stu-id="0a45b-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





