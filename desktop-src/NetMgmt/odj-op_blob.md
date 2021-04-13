---
title: OP_BLOB
description: OP_BLOB IDL-Definition
ms.assetid: c215c793-5fad-4baa-97c0-c809040dda1e
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: fab6df11be3bf719f787c40a41a50d948a865474
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "104391173"
---
# <a name="op_blob-structure"></a><span data-ttu-id="aff0c-103">OP_BLOB Struktur</span><span class="sxs-lookup"><span data-stu-id="aff0c-103">OP_BLOB structure</span></span>

<span data-ttu-id="aff0c-104">Enthält einen nicht transparenten Byte Puffer.</span><span class="sxs-lookup"><span data-stu-id="aff0c-104">Contains an opaque byte buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="aff0c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aff0c-105">Syntax</span></span>

```C++
typedef struct _OP_BLOB
{
    ULONG                       cbBlob;
    [size_is(cbBlob)]   PBYTE   pBlob;
} OP_BLOB, *POP_BLOB;
```

## <a name="members"></a><span data-ttu-id="aff0c-106">Member</span><span class="sxs-lookup"><span data-stu-id="aff0c-106">Members</span></span>

### <a name="cbblob"></a><span data-ttu-id="aff0c-107">cbblob</span><span class="sxs-lookup"><span data-stu-id="aff0c-107">cbBlob</span></span>

<span data-ttu-id="aff0c-108">Gibt die Größe des pBlob in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="aff0c-108">Specifies the the size of pBlob in bytes.</span></span>

### <a name="pblob"></a><span data-ttu-id="aff0c-109">pBlob</span><span class="sxs-lookup"><span data-stu-id="aff0c-109">pBlob</span></span>

<span data-ttu-id="aff0c-110">Verweist auf einen Byte Puffer.</span><span class="sxs-lookup"><span data-stu-id="aff0c-110">Points to a byte buffer.</span></span>

## <a name="see-also"></a><span data-ttu-id="aff0c-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aff0c-111">See also</span></span>

[<span data-ttu-id="aff0c-112">**IDL-Definitionen im Offline-Domänen Beitritt**</span><span class="sxs-lookup"><span data-stu-id="aff0c-112">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
