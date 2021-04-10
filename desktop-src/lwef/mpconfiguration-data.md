---
title: MPCONFIGURATION_DATA Struktur (mpclient. h)
description: Enthält Daten zu Konfigurationsänderungen, einschließlich der alten und neuen Werte.
ms.assetid: AB70B1C0-C148-44BC-8C0E-CC5D2A66BCA5
keywords:
- MPCONFIGURATION_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPCONFIGURATION_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPCONFIGURATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb54ae4e323f2144dd25c52005d8484b0a207e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040459"
---
# <a name="mpconfiguration_data-structure"></a><span data-ttu-id="9ba92-105">Mpconfiguration- \_ Datenstruktur</span><span class="sxs-lookup"><span data-stu-id="9ba92-105">MPCONFIGURATION\_DATA structure</span></span>

<span data-ttu-id="9ba92-106">Enthält Daten zu Konfigurationsänderungen, einschließlich der alten und neuen Werte.</span><span class="sxs-lookup"><span data-stu-id="9ba92-106">Contains data about configuration changes, including the old and new values.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ba92-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ba92-107">Syntax</span></span>


```C++
typedef struct tagMPCONFIGURATION_DATA {
  MP_MIDL_STRING LPWSTR ConfigurationName;
  DWORD                 DataType;
  DWORD                 PreviousDataSize;
  BYTE                  *pPreviousData;
  DWORD                 CurrentDataSize;
  BYTE                  *pCurrentData;
} MPCONFIGURATION_DATA, *PMPCONFIGURATION_DATA;
```



## <a name="members"></a><span data-ttu-id="9ba92-108">Member</span><span class="sxs-lookup"><span data-stu-id="9ba92-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="9ba92-109">**ConfigurationName**</span><span class="sxs-lookup"><span data-stu-id="9ba92-109">**ConfigurationName**</span></span>
</dt> <dd>

<span data-ttu-id="9ba92-110">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="9ba92-110">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="9ba92-111">Der Name der geänderten Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9ba92-111">Name of the configuration that changed.</span></span>

</dd> <dt>

<span data-ttu-id="9ba92-112">**DataType**</span><span class="sxs-lookup"><span data-stu-id="9ba92-112">**DataType**</span></span>
</dt> <dd>

<span data-ttu-id="9ba92-113">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="9ba92-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="9ba92-114">Der Typ der verwendeten Daten.</span><span class="sxs-lookup"><span data-stu-id="9ba92-114">The type of data used.</span></span>

</dd> <dt>

<span data-ttu-id="9ba92-115">**Previousdatasize**</span><span class="sxs-lookup"><span data-stu-id="9ba92-115">**PreviousDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="9ba92-116">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="9ba92-116">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="9ba92-117">Größe der vorherigen Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="9ba92-117">Size of previous data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9ba92-118">**ppreviousdata**</span><span class="sxs-lookup"><span data-stu-id="9ba92-118">**pPreviousData**</span></span>
</dt> <dd>

<span data-ttu-id="9ba92-119">Typ: \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="9ba92-119">Type: \**BYTE\** _</span></span>

</dd> <dd>

<span data-ttu-id="9ba92-120">Zeiger auf vorherige Daten.</span><span class="sxs-lookup"><span data-stu-id="9ba92-120">Pointer to previous data.</span></span>

</dd> <dt>

<span data-ttu-id="9ba92-121">_ *Currentdatasize*\*</span><span class="sxs-lookup"><span data-stu-id="9ba92-121">_ *CurrentDataSize*\*</span></span>
</dt> <dd>

<span data-ttu-id="9ba92-122">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="9ba92-122">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="9ba92-123">Größe der neuen Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="9ba92-123">Size of new data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9ba92-124">**pcurrentdata**</span><span class="sxs-lookup"><span data-stu-id="9ba92-124">**pCurrentData**</span></span>
</dt> <dd>

<span data-ttu-id="9ba92-125">Type: **Byte \***</span><span class="sxs-lookup"><span data-stu-id="9ba92-125">Type: **BYTE\***</span></span>

</dd> <dd>

<span data-ttu-id="9ba92-126">Zeiger auf neue Daten.</span><span class="sxs-lookup"><span data-stu-id="9ba92-126">Pointer to new data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ba92-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ba92-127">Requirements</span></span>



| <span data-ttu-id="9ba92-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ba92-128">Requirement</span></span> | <span data-ttu-id="9ba92-129">Wert</span><span class="sxs-lookup"><span data-stu-id="9ba92-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ba92-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ba92-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9ba92-131">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ba92-131">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9ba92-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ba92-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9ba92-133">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ba92-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9ba92-134">Header</span><span class="sxs-lookup"><span data-stu-id="9ba92-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ba92-135"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ba92-135"><dt>MpClient.h</dt></span></span> </dl> |



 

 





