---
title: GetStringProperty-Methode der Win32_RDSHServer-Klasse
description: Ruft den Wert der Zeichen folgen Eigenschaft eines Win32- \_ rdshserver-Objekts ab.
ms.assetid: 136cd213-86a6-472a-8853-8d05f992309a
ms.tgt_platform: multiple
keywords:
- GetStringProperty-Methode Remotedesktopdienste
- GetStringProperty-Methode Remotedesktopdienste, Win32_RDSHServer-Klasse
- Win32_RDSHServer-Klasse Remotedesktopdienste, GetStringProperty-Methode
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 619a034e0a2f89270d21bf0c4fc297b4248cef59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479116"
---
# <a name="getstringproperty-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="2777f-106">GetStringProperty-Methode der Win32 \_ rdshserver-Klasse</span><span class="sxs-lookup"><span data-stu-id="2777f-106">GetStringProperty method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="2777f-107">Ruft den Wert der Zeichen folgen Eigenschaft eines [**Win32- \_ rdshserver**](win32-rdshserver.md) -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="2777f-107">Retrieves a string property value of a [**Win32\_RDSHServer**](win32-rdshserver.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2777f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2777f-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="2777f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2777f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2777f-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2777f-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2777f-111">Der Schlüssel, der die abzurufende Eigenschaft identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2777f-111">The key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="2777f-112">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2777f-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2777f-113">Empfängt den abgerufenen Eigenschafts Wert.</span><span class="sxs-lookup"><span data-stu-id="2777f-113">Receives the retrieved property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2777f-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2777f-114">Return value</span></span>

<span data-ttu-id="2777f-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2777f-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2777f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2777f-116">Requirements</span></span>



| <span data-ttu-id="2777f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2777f-117">Requirement</span></span> | <span data-ttu-id="2777f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="2777f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2777f-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2777f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2777f-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2777f-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="2777f-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2777f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2777f-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2777f-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="2777f-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="2777f-123">Namespace</span></span><br/>                | <span data-ttu-id="2777f-124">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="2777f-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="2777f-125">MOF</span><span class="sxs-lookup"><span data-stu-id="2777f-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2777f-126"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2777f-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="2777f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2777f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2777f-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2777f-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="2777f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2777f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2777f-130">**Win32- \_ rdshserver**</span><span class="sxs-lookup"><span data-stu-id="2777f-130">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





