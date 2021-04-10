---
title: Testandsetstate-Methode der Win32_RDSHServer-Klasse
description: Vergleicht den aktuellen Zustand mit dem angegebenen comparand. Wenn die beiden Stimmen, wird der Zustand auf einen neuen Wert festgelegt. Unabhängig von der Übereinstimmung wird der aktuelle Zustand ebenfalls zurückgegeben.
ms.assetid: f1bb0076-251b-4c0d-92f9-1c460e1b26bb
ms.tgt_platform: multiple
keywords:
- Testandsetstate-Methode Remotedesktopdienste
- Testandsetstate-Methode Remotedesktopdienste, Win32_RDSHServer-Klasse
- Win32_RDSHServer-Klasse Remotedesktopdienste, testandsetstate-Methode
topic_type:
- apiref
api_name:
- Win32_RDSHServer.TestAndSetState
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff4c9b616c2a288f5f39b240d71b2611e25d45f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103983"
---
# <a name="testandsetstate-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="dc070-107">Testandsetstate-Methode der Win32 \_ rdshserver-Klasse</span><span class="sxs-lookup"><span data-stu-id="dc070-107">TestAndSetState method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="dc070-108">Vergleicht den aktuellen Zustand mit dem angegebenen comparand. Wenn die beiden Stimmen, wird der Zustand auf einen neuen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dc070-108">Compares the current state to the specified comparand; if the two match, the state is set to a new value.</span></span> <span data-ttu-id="dc070-109">Unabhängig von der Übereinstimmung wird der aktuelle Zustand ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dc070-109">Regardless of the match, the current state is also returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc070-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc070-110">Syntax</span></span>


```mof
uint32 TestAndSetState(
  [in]  uint32 Comparand,
  [in]  uint32 NewState,
  [out] uint32 InitState
);
```



## <a name="parameters"></a><span data-ttu-id="dc070-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc070-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc070-112">*Comparand* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc070-112">*Comparand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc070-113">Ein Wert, der mit dem aktuellen Zustand verglichen werden soll. Wenn die beiden Werte stimmen, wird der Zustand auf *newState* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dc070-113">A value to compare to the current state; if the two values match, the state is set to *NewState*.</span></span>

</dd> <dt>

<span data-ttu-id="dc070-114">*NewState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc070-114">*NewState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc070-115">Der neue Wert des Zustands.</span><span class="sxs-lookup"><span data-stu-id="dc070-115">The new value of the state.</span></span>

</dd> <dt>

<span data-ttu-id="dc070-116">*Initstate* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dc070-116">*InitState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc070-117">Bei Erfolg oder Fehler gibt den aktuellen Status zurück.</span><span class="sxs-lookup"><span data-stu-id="dc070-117">On success or failure, returns the current state.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc070-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc070-118">Requirements</span></span>



| <span data-ttu-id="dc070-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc070-119">Requirement</span></span> | <span data-ttu-id="dc070-120">Wert</span><span class="sxs-lookup"><span data-stu-id="dc070-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc070-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dc070-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dc070-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="dc070-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="dc070-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dc070-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dc070-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="dc070-124">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="dc070-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="dc070-125">Namespace</span></span><br/>                | <span data-ttu-id="dc070-126">Root \\ CIMV2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="dc070-126">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="dc070-127">MOF</span><span class="sxs-lookup"><span data-stu-id="dc070-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc070-128"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dc070-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc070-129">DLL</span><span class="sxs-lookup"><span data-stu-id="dc070-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc070-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc070-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="dc070-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc070-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc070-132">**Win32- \_ rdshserver**</span><span class="sxs-lookup"><span data-stu-id="dc070-132">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





