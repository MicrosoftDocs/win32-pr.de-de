---
title: ODJ_BLOB
description: ODJ_BLOB IDL-Definition
ms.assetid: ada2c597-9ab9-4cc0-b5ba-4b533eec5502
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 079ea531b0cb392539679c10574c0cc0f1601318
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "104474590"
---
# <a name="odj_blob-structure"></a><span data-ttu-id="df65f-103">ODJ_BLOB Struktur</span><span class="sxs-lookup"><span data-stu-id="df65f-103">ODJ_BLOB structure</span></span>

<span data-ttu-id="df65f-104">Gibt eine-Struktur an, die entweder eine serialisierte ODJ_WIN7BLOB Struktur oder eine serialisierte OP_PACKAGE Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="df65f-104">Specifies a structure containing either a serialized ODJ_WIN7BLOB structure or a serialized OP_PACKAGE structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="df65f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="df65f-105">Syntax</span></span>

```c++
typedef struct _ODJ_BLOB
{
    ULONG ulODJFormat;
    ULONG cbBlob;
    [size_is(cbBlob)] PBYTE pBlob;
} ODJ_BLOB, *PODJ_BLOB;

```

## <a name="members"></a><span data-ttu-id="df65f-106">Member</span><span class="sxs-lookup"><span data-stu-id="df65f-106">Members</span></span>

### <a name="ulodjformat"></a><span data-ttu-id="df65f-107">ulodjformat</span><span class="sxs-lookup"><span data-stu-id="df65f-107">ulODJFormat</span></span>

<span data-ttu-id="df65f-108">Gibt die logische Version der Struktur an und muss auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="df65f-108">Specifies the logical version of the structure and must be set to one of the following values:</span></span>

|<span data-ttu-id="df65f-109">Wert</span><span class="sxs-lookup"><span data-stu-id="df65f-109">Value</span></span>|<span data-ttu-id="df65f-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="df65f-110">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="df65f-111">ODJ_WIN7_FORMAT (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="df65f-111">ODJ_WIN7_FORMAT (0x00000001)</span></span>|<span data-ttu-id="df65f-112">Die in pBlob enthaltenen Bytes müssen eine serialisierte ODJ_WIN7_BLOB Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="df65f-112">The bytes contained in pBlob must contain a serialized ODJ_WIN7_BLOB structure.</span></span>|
|<span data-ttu-id="df65f-113">ODJ_WIN8_FORMAT (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="df65f-113">ODJ_WIN8_FORMAT (0x00000002)</span></span>|<span data-ttu-id="df65f-114">Die in pBlob enthaltenen Bytes müssen eine serialisierte OP_PACKAGE Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="df65f-114">The bytes contained in pBlob must contain a serialized OP_PACKAGE structure.</span></span>|

### <a name="cbblob"></a><span data-ttu-id="df65f-115">cbblob</span><span class="sxs-lookup"><span data-stu-id="df65f-115">cbBlob</span></span>

<span data-ttu-id="df65f-116">Dieser Wert muss auf die Anzahl der Bytes im pBlob-Array festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="df65f-116">This must be set to the number of bytes in the pBlob array.</span></span>

### <a name="pblob"></a><span data-ttu-id="df65f-117">pBlob</span><span class="sxs-lookup"><span data-stu-id="df65f-117">pBlob</span></span>

<span data-ttu-id="df65f-118">Verweist auf einen Byte Puffer, der eine serialisierte Struktur enthält, wie von dem oben genannten "ulodjformat" angegeben.</span><span class="sxs-lookup"><span data-stu-id="df65f-118">Points to a byte buffer containing a serialized structure as specified by ulODJFormat above.</span></span>

## <a name="see-also"></a><span data-ttu-id="df65f-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df65f-119">See also</span></span>

[<span data-ttu-id="df65f-120">**IDL-Definitionen im Offline-Domänen Beitritt**</span><span class="sxs-lookup"><span data-stu-id="df65f-120">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

