---
title: Keyvaluedelete-Methode der Win32_RDSHCollection-Klasse
description: Löscht den angegebenen Schlüssel (und zugeordneten Wert) aus der Auflistung.
ms.assetid: 968d6744-7b4a-45e5-87fb-90c408dbc771
ms.tgt_platform: multiple
keywords:
- Keyvaluedelete-Methode Remotedesktopdienste
- Keyvaluedelete-Methode Remotedesktopdienste, Win32_RDSHCollection-Klasse
- Win32_RDSHCollection-Klasse Remotedesktopdienste, keyvaluedelete-Methode
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueDelete
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1b4b29aea7890817c8d3cd8599f6effceb53c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949737"
---
# <a name="keyvaluedelete-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="95089-106">Keyvaluedelete-Methode der Win32 \_ rdshcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="95089-106">KeyValueDelete method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="95089-107">Löscht den angegebenen Schlüssel (und zugeordneten Wert) aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="95089-107">Deletes the specified key (and associated value) from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="95089-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="95089-108">Syntax</span></span>


```mof
uint32 KeyValueDelete(
  [in] string Key
);
```



## <a name="parameters"></a><span data-ttu-id="95089-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="95089-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95089-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95089-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95089-111">Der zu löschende Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="95089-111">The key to delete.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="95089-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95089-112">Requirements</span></span>



| <span data-ttu-id="95089-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95089-113">Requirement</span></span> | <span data-ttu-id="95089-114">Wert</span><span class="sxs-lookup"><span data-stu-id="95089-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="95089-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95089-115">Minimum supported client</span></span><br/> | <span data-ttu-id="95089-116">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="95089-116">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="95089-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95089-117">Minimum supported server</span></span><br/> | <span data-ttu-id="95089-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="95089-118">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="95089-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="95089-119">Namespace</span></span><br/>                | <span data-ttu-id="95089-120">Root \\ CIMV2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="95089-120">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="95089-121">MOF</span><span class="sxs-lookup"><span data-stu-id="95089-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95089-122"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="95089-122"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="95089-123">DLL</span><span class="sxs-lookup"><span data-stu-id="95089-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95089-124"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95089-124"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="95089-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95089-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95089-126">**Win32- \_ rdshcollection**</span><span class="sxs-lookup"><span data-stu-id="95089-126">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





