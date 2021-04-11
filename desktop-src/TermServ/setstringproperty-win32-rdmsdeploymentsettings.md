---
title: SetStringProperty-Methode der Win32_RDMSDeploymentSettings-Klasse (CertEnroll. h)
description: Aktualisiert eine Zeichen folgen Eigenschaft für die Bereitstellungs Einstellungen einer Sammlung virtueller Desktops.
ms.assetid: 500ab1cb-7336-47a8-adee-790976ea30fe
ms.tgt_platform: multiple
keywords:
- SetStringProperty-Methode Remotedesktopdienste
- SetStringProperty-Methode Remotedesktopdienste, Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste, setStringProperty-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 138f6d91ed428caabf8da69e3d958675f879dd15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104606"
---
# <a name="setstringproperty-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="5ca3f-106">SetStringProperty-Methode der Win32 \_ rdmsdeploymentsettings-Klasse</span><span class="sxs-lookup"><span data-stu-id="5ca3f-106">SetStringProperty method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="5ca3f-107">Aktualisiert eine Zeichen folgen Eigenschaft für die Bereitstellungs Einstellungen einer Sammlung virtueller Desktops.</span><span class="sxs-lookup"><span data-stu-id="5ca3f-107">Updates a string property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ca3f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ca3f-108">Syntax</span></span>


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="5ca3f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ca3f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ca3f-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ca3f-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca3f-111">Der Alias für die Sammlung virtueller Desktops.</span><span class="sxs-lookup"><span data-stu-id="5ca3f-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="5ca3f-112">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ca3f-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca3f-113">Der neue Eigenschaftswert.</span><span class="sxs-lookup"><span data-stu-id="5ca3f-113">The new property value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ca3f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ca3f-114">Requirements</span></span>



| <span data-ttu-id="5ca3f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ca3f-115">Requirement</span></span> | <span data-ttu-id="5ca3f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5ca3f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ca3f-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ca3f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5ca3f-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5ca3f-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="5ca3f-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ca3f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5ca3f-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ca3f-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="5ca3f-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ca3f-121">Namespace</span></span><br/>                | <span data-ttu-id="5ca3f-122">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="5ca3f-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="5ca3f-123">Header</span><span class="sxs-lookup"><span data-stu-id="5ca3f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ca3f-124"><dt>CertEnroll. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ca3f-124"><dt>Certenroll.h</dt></span></span> </dl>     |
| <span data-ttu-id="5ca3f-125">MOF</span><span class="sxs-lookup"><span data-stu-id="5ca3f-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ca3f-126"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5ca3f-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ca3f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="5ca3f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ca3f-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ca3f-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="5ca3f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ca3f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ca3f-130">**Win32 \_ rdmsdeploymentsettings**</span><span class="sxs-lookup"><span data-stu-id="5ca3f-130">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





