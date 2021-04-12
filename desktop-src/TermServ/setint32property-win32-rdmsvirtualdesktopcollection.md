---
title: SetInt32Property-Methode der Win32_RDMSVirtualDesktopCollection-Klasse
description: Aktualisiert eine ganzzahlige Eigenschaft einer Sammlung virtueller Desktops.
ms.assetid: 2ea27385-5100-4e88-ad11-df5e439d0815
ms.tgt_platform: multiple
keywords:
- SetInt32Property-Methode Remotedesktopdienste
- SetInt32Property-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktopCollection-Klasse
- Win32_RDMSVirtualDesktopCollection-Klasse Remotedesktopdienste, SetInt32Property-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c2a93a52ce79bc185cd37dd9ac93e5b420b5d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105843"
---
# <a name="setint32property-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="8d316-106">SetInt32Property-Methode der Win32 \_ rdmsvirtualdesktopcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="8d316-106">SetInt32Property method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="8d316-107">Aktualisiert eine ganzzahlige Eigenschaft einer Sammlung virtueller Desktops.</span><span class="sxs-lookup"><span data-stu-id="8d316-107">Updates an integer property of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d316-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d316-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="8d316-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d316-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d316-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d316-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d316-111">Ein Schlüssel, der die zu Aktualisier enswerte Eigenschaft identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8d316-111">A key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="8d316-112">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d316-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d316-113">Der neue Eigenschaftswert.</span><span class="sxs-lookup"><span data-stu-id="8d316-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d316-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8d316-114">Return value</span></span>

<span data-ttu-id="8d316-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8d316-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d316-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d316-116">Requirements</span></span>



| <span data-ttu-id="8d316-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d316-117">Requirement</span></span> | <span data-ttu-id="8d316-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8d316-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d316-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8d316-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8d316-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8d316-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="8d316-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8d316-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8d316-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8d316-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="8d316-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="8d316-123">Namespace</span></span><br/>                | <span data-ttu-id="8d316-124">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="8d316-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="8d316-125">MOF</span><span class="sxs-lookup"><span data-stu-id="8d316-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d316-126"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8d316-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d316-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8d316-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d316-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d316-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="8d316-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d316-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d316-130">**Win32 \_ rdmsvirtualdesktopcollection**</span><span class="sxs-lookup"><span data-stu-id="8d316-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





