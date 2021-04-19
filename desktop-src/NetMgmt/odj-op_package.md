---
title: OP_PACKAGE
description: OP_PACKAGE IDL-Definition
ms.assetid: 065266a6-6db5-4113-bd2b-22ac6063236d
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 6220b3815ad6ff360af7255a91fc34d71125f38c
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "106339521"
---
# <a name="op_package-structure"></a><span data-ttu-id="e3c2a-103">OP_PACKAGE Struktur</span><span class="sxs-lookup"><span data-stu-id="e3c2a-103">OP_PACKAGE structure</span></span>

<span data-ttu-id="e3c2a-104">Enthält eine-Struktur, die eine serialisierte OP_PACKAGE_COLLECTION enthält.</span><span class="sxs-lookup"><span data-stu-id="e3c2a-104">Contains a structure that contains a serialized OP_PACKAGE_COLLECTION.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3c2a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3c2a-105">Syntax</span></span>

```C++
typedef struct _OP_PACKAGE
{
    GUID    EncryptionType;
    OP_BLOB EncryptionContext;
    OP_BLOB WrappedPartCollection;
    ULONG   cbDecryptedPartCollection;
    OP_BLOB Extension;
} OP_PACKAGE, *POP_PACKAGE;
```

## <a name="members"></a><span data-ttu-id="e3c2a-106">Member</span><span class="sxs-lookup"><span data-stu-id="e3c2a-106">Members</span></span>

### <a name="encryptiontype"></a><span data-ttu-id="e3c2a-107">EncryptionType</span><span class="sxs-lookup"><span data-stu-id="e3c2a-107">EncryptionType</span></span>

<span data-ttu-id="e3c2a-108">Für zukünftige Verwendung reserviert und muss auf GUID_NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e3c2a-108">Reserved for future use and MUST be set to GUID_NULL.</span></span>

### <a name="encryptioncontext"></a><span data-ttu-id="e3c2a-109">Verschlüsselungs Kontext</span><span class="sxs-lookup"><span data-stu-id="e3c2a-109">EncryptionContext</span></span>

<span data-ttu-id="e3c2a-110">Für zukünftige Verwendung reserviert und muss auf alle Nullen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e3c2a-110">Reserved for future use and MUST be set to all zeros.</span></span>

### <a name="wrappedpartcollection"></a><span data-ttu-id="e3c2a-111">Wrappedpartcollection</span><span class="sxs-lookup"><span data-stu-id="e3c2a-111">WrappedPartCollection</span></span>

<span data-ttu-id="e3c2a-112">Eine OP_BLOB-Struktur, die eine serialisierte OP_PACKAGE_COLLECTION Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="e3c2a-112">An OP_BLOB structure that contains a serialized OP_PACKAGE_COLLECTION structure.</span></span>

### <a name="cbdecryptedpartcollection"></a><span data-ttu-id="e3c2a-113">cbdecryptedpartcollection</span><span class="sxs-lookup"><span data-stu-id="e3c2a-113">cbDecryptedPartCollection</span></span>

<span data-ttu-id="e3c2a-114">Für zukünftige Verwendung reserviert und muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e3c2a-114">Reserved for future use and MUST be set to zero.</span></span>

### <a name="extension"></a><span data-ttu-id="e3c2a-115">Durchwahl</span><span class="sxs-lookup"><span data-stu-id="e3c2a-115">Extension</span></span>

<span data-ttu-id="e3c2a-116">Für zukünftige Verwendung reserviert und muss auf alle Nullen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e3c2a-116">Reserved for future use and MUST be set to all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="e3c2a-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3c2a-117">See also</span></span>

[<span data-ttu-id="e3c2a-118">**IDL-Definitionen im Offline-Domänen Beitritt**</span><span class="sxs-lookup"><span data-stu-id="e3c2a-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="e3c2a-119">**OP- \_ BLOB**</span><span class="sxs-lookup"><span data-stu-id="e3c2a-119">**OP\_BLOB**</span></span>](odj-op_blob.md)

[<span data-ttu-id="e3c2a-120">**\_Paket \_ Sammlung (OP)**</span><span class="sxs-lookup"><span data-stu-id="e3c2a-120">**OP\_PACKAGE\_COLLECTION**</span></span>](odj-op_package_collection.md)
