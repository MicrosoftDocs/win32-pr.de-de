---
title: OP_PACKAGE_PART
description: OP_PACKAGE_PART IDL-Definition
ms.assetid: 8f13aa71-a7b2-41ee-ad1e-4953f49a391a
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 74f299c58b9bf417a94119cd7520b7c0a364f73a
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "104213076"
---
# <a name="op_package_part-structure"></a><span data-ttu-id="62edc-103">OP_PACKAGE_PART Struktur</span><span class="sxs-lookup"><span data-stu-id="62edc-103">OP_PACKAGE_PART structure</span></span>

<span data-ttu-id="62edc-104">Definiert eine-Struktur, die ein DataSet enthält, das durch eine GUID identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="62edc-104">Defines a structure that contains a data set identified by a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="62edc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="62edc-105">Syntax</span></span>

```C++
typedef struct _OP_PACKAGE_PART
{
    GUID    PartType;
    ULONG   ulFlags;
    OP_BLOB Part;
    OP_BLOB Extension;
} OP_PACKAGE_PART, *POP_PACKAGE_PART;
```

## <a name="members"></a><span data-ttu-id="62edc-106">Member</span><span class="sxs-lookup"><span data-stu-id="62edc-106">Members</span></span>

### <a name="parttype"></a><span data-ttu-id="62edc-107">Paramettype</span><span class="sxs-lookup"><span data-stu-id="62edc-107">PartType</span></span>

<span data-ttu-id="62edc-108">Identifiziert die serialisierte Struktur, die in einem Teil der folgenden Tabelle enthalten ist:</span><span class="sxs-lookup"><span data-stu-id="62edc-108">Identifies the serialized structure contained in Part per the following table:</span></span>

|<span data-ttu-id="62edc-109">Paramettype</span><span class="sxs-lookup"><span data-stu-id="62edc-109">PartType</span></span>|<span data-ttu-id="62edc-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="62edc-110">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="62edc-111">GUID_JOIN_PROVIDER {631c7621-5289-4321-bc9e-80F 843f 868c3}</span><span class="sxs-lookup"><span data-stu-id="62edc-111">GUID_JOIN_PROVIDER {631c7621-5289-4321-bc9e-80f843f868c3}</span></span>|<span data-ttu-id="62edc-112">Enthält eine serialisierte ODJ_WIN7_BLOB Struktur.</span><span class="sxs-lookup"><span data-stu-id="62edc-112">Contains a serialized ODJ_WIN7_BLOB structure.</span></span>|
|<span data-ttu-id="62edc-113">GUID_JOIN_PROVIDER2 {57bfc56b-52b f 9-480c-adcb-91b3f 8a82317}</span><span class="sxs-lookup"><span data-stu-id="62edc-113">GUID_JOIN_PROVIDER2 {57BFC56B-52F9-480C-ADCB-91B3F8A82317}</span></span>|<span data-ttu-id="62edc-114">Enthält eine serialisierte OP_JOIN_PROV2_PART Struktur.</span><span class="sxs-lookup"><span data-stu-id="62edc-114">Contains a serialized OP_JOIN_PROV2_PART structure.</span></span>|
|<span data-ttu-id="62edc-115">GUID_JOIN_PROVIDER3 {FC0CCF25-7FFA-474A-8611-69FFE269645F}</span><span class="sxs-lookup"><span data-stu-id="62edc-115">GUID_JOIN_PROVIDER3 {FC0CCF25-7FFA-474A-8611-69FFE269645F}</span></span>|<span data-ttu-id="62edc-116">Enthält eine serialisierte OP_JOIN_PROV3_PART Struktur.</span><span class="sxs-lookup"><span data-stu-id="62edc-116">Contains a serialized OP_JOIN_PROV3_PART structure.</span></span>|
|<span data-ttu-id="62edc-117">GUID_CERT_PROVIDER {9c0971e9-832b-4873-8e87-ef1419d4781e}</span><span class="sxs-lookup"><span data-stu-id="62edc-117">GUID_CERT_PROVIDER {9c0971e9-832f-4873-8e87-ef1419d4781e}</span></span>|<span data-ttu-id="62edc-118">Enthält eine serialisierte OP_CERT_PART Struktur.</span><span class="sxs-lookup"><span data-stu-id="62edc-118">Contains a serialized OP_CERT_PART structure.</span></span>|
|<span data-ttu-id="62edc-119">GUID_POLICY_PROVIDER {68b602a-0c09-48ce-b75f -07b7bd58f EC}</span><span class="sxs-lookup"><span data-stu-id="62edc-119">GUID_POLICY_PROVIDER {68fb602a-0c09-48ce-b75f-07b7bd58f7ec}</span></span>|<span data-ttu-id="62edc-120">Enthält eine serialisierte OP_POLICY_PART Struktur.</span><span class="sxs-lookup"><span data-stu-id="62edc-120">Contains a serialized OP_POLICY_PART structure.</span></span>|

### <a name="ulflags"></a><span data-ttu-id="62edc-121">ulFlags</span><span class="sxs-lookup"><span data-stu-id="62edc-121">ulFlags</span></span>

<span data-ttu-id="62edc-122">Muss auf 0 (null) oder mehrere der folgenden Flags festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="62edc-122">Must be set to zero or more of the following flags:</span></span>

|<span data-ttu-id="62edc-123">Wert</span><span class="sxs-lookup"><span data-stu-id="62edc-123">Value</span></span>|<span data-ttu-id="62edc-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="62edc-124">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="62edc-125">OPSPI_PACKAGE_PART_ESSENTIAL (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="62edc-125">OPSPI_PACKAGE_PART_ESSENTIAL (0x00000001)</span></span>|<span data-ttu-id="62edc-126">Dieser Paketteil ist als unverzichtbar anzusehen.</span><span class="sxs-lookup"><span data-stu-id="62edc-126">This package part is considered essential.</span></span> <span data-ttu-id="62edc-127">Wenn der Consumer dieses Paketteil nicht erkennt oder nicht erfolgreich verarbeitet werden kann, muss der gesamte Vorgang fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="62edc-127">If the consumer does not recognize this package part or fails to successfully process it, the overall operation must fail.</span></span>|

### <a name="part"></a><span data-ttu-id="62edc-128">Teil</span><span class="sxs-lookup"><span data-stu-id="62edc-128">Part</span></span>

<span data-ttu-id="62edc-129">Enthält eine serialisierte Struktur in einer OP_BLOB-Struktur.</span><span class="sxs-lookup"><span data-stu-id="62edc-129">Contains a serialized structure in an OP_BLOB structure.</span></span> <span data-ttu-id="62edc-130">Die jeweilige Struktur wird durch einen "paramettype" bestimmt.</span><span class="sxs-lookup"><span data-stu-id="62edc-130">The specific structure is determined by PartType.</span></span>

### <a name="extension"></a><span data-ttu-id="62edc-131">Durchwahl</span><span class="sxs-lookup"><span data-stu-id="62edc-131">Extension</span></span>

<span data-ttu-id="62edc-132">Für zukünftige Verwendung reserviert und muss auf alle Nullen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="62edc-132">Reserved for future use and MUST be set to all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="62edc-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62edc-133">See also</span></span>

[<span data-ttu-id="62edc-134">**IDL-Definitionen im Offline-Domänen Beitritt**</span><span class="sxs-lookup"><span data-stu-id="62edc-134">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="62edc-135">**OP- \_ BLOB**</span><span class="sxs-lookup"><span data-stu-id="62edc-135">**OP\_BLOB**</span></span>](odj-op_blob.md)
