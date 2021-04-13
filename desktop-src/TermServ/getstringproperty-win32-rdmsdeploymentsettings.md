---
title: GetStringProperty-Methode der Win32_RDMSDeploymentSettings-Klasse
description: Ruft eine Zeichen folgen Eigenschaft für die Bereitstellungs Einstellungen einer Sammlung virtueller Desktops ab.
ms.assetid: 468ffdea-57a9-4478-adae-3629e4522762
ms.tgt_platform: multiple
keywords:
- GetStringProperty-Methode Remotedesktopdienste
- GetStringProperty-Methode Remotedesktopdienste, Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste, GetStringProperty-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f26a570becbbae6b0d768c399acd3dd2954ecdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391746"
---
# <a name="getstringproperty-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="706e7-106">GetStringProperty-Methode der Win32 \_ rdmsdeploymentsettings-Klasse</span><span class="sxs-lookup"><span data-stu-id="706e7-106">GetStringProperty method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="706e7-107">Ruft eine Zeichen folgen Eigenschaft für die Bereitstellungs Einstellungen einer Sammlung virtueller Desktops ab.</span><span class="sxs-lookup"><span data-stu-id="706e7-107">Retrieves a string property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="706e7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="706e7-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="706e7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="706e7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="706e7-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="706e7-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="706e7-111">Der Alias für die Sammlung virtueller Desktops.</span><span class="sxs-lookup"><span data-stu-id="706e7-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="706e7-112">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="706e7-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="706e7-113">Eine Zeichenfolge, die den abgerufenen Wert empfängt.</span><span class="sxs-lookup"><span data-stu-id="706e7-113">A string that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="706e7-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="706e7-114">Requirements</span></span>



| <span data-ttu-id="706e7-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="706e7-115">Requirement</span></span> | <span data-ttu-id="706e7-116">Wert</span><span class="sxs-lookup"><span data-stu-id="706e7-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="706e7-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="706e7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="706e7-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="706e7-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="706e7-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="706e7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="706e7-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="706e7-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="706e7-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="706e7-121">Namespace</span></span><br/>                | <span data-ttu-id="706e7-122">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="706e7-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="706e7-123">MOF</span><span class="sxs-lookup"><span data-stu-id="706e7-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="706e7-124"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="706e7-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="706e7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="706e7-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="706e7-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="706e7-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="706e7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="706e7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="706e7-128">**Win32 \_ rdmsdeploymentsettings**</span><span class="sxs-lookup"><span data-stu-id="706e7-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





