---
title: Keyvalueget-Methode der Win32_RDSHCollection-Klasse
description: Ruft den Wert ab, der dem angegebenen Schlüssel in der Auflistung zugeordnet ist.
ms.assetid: 69d309a4-b32e-4dbc-bd28-be79d395ac26
ms.tgt_platform: multiple
keywords:
- Keyvalueget-Methode Remotedesktopdienste
- Keyvalueget-Methode Remotedesktopdienste, Win32_RDSHCollection-Klasse
- Win32_RDSHCollection-Klasse Remotedesktopdienste, keyvalueget-Methode
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueGet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5304cca379106094d4d00b9a0b5506c8df7075a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858804"
---
# <a name="keyvalueget-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="834d0-106">Keyvalueget-Methode der Win32 \_ rdshcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="834d0-106">KeyValueGet method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="834d0-107">Ruft den Wert ab, der dem angegebenen Schlüssel in der Auflistung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="834d0-107">Retrieves the value associated with the specified key in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="834d0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="834d0-108">Syntax</span></span>


```mof
uint32 KeyValueGet(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="834d0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="834d0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="834d0-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="834d0-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="834d0-111">Der Schlüssel, der den Wert identifiziert, den Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="834d0-111">The key that identifies the value you wish to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="834d0-112">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="834d0-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="834d0-113">Bei Erfolg wird der Wert zurückgegeben, der dem angegebenen Schlüssel zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="834d0-113">On success, returns the value associated with the specified key.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="834d0-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="834d0-114">Requirements</span></span>



| <span data-ttu-id="834d0-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="834d0-115">Requirement</span></span> | <span data-ttu-id="834d0-116">Wert</span><span class="sxs-lookup"><span data-stu-id="834d0-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="834d0-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="834d0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="834d0-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="834d0-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="834d0-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="834d0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="834d0-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="834d0-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="834d0-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="834d0-121">Namespace</span></span><br/>                | <span data-ttu-id="834d0-122">Root \\ CIMV2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="834d0-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="834d0-123">MOF</span><span class="sxs-lookup"><span data-stu-id="834d0-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="834d0-124"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="834d0-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="834d0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="834d0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="834d0-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="834d0-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="834d0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="834d0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="834d0-128">**Win32- \_ rdshcollection**</span><span class="sxs-lookup"><span data-stu-id="834d0-128">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





