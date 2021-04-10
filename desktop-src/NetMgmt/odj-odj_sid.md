---
title: ODJ_SID
description: ODJ_SID IDL-Definition
ms.assetid: 1d06f725-6cd4-42cf-b171-c78a095690cb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: dd51f2e8a54eaf5be566e5a25f013ca1d87b9341
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "104039797"
---
# <a name="odj_sid-structure"></a><span data-ttu-id="a9ba0-103">ODJ_SID Struktur</span><span class="sxs-lookup"><span data-stu-id="a9ba0-103">ODJ_SID structure</span></span>

<span data-ttu-id="a9ba0-104">Enthält eine Sicherheits-ID (SID).</span><span class="sxs-lookup"><span data-stu-id="a9ba0-104">Contains a Security Identifier (SID).</span></span>

## <a name="syntax"></a><span data-ttu-id="a9ba0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9ba0-105">Syntax</span></span>

```C++
typedef struct _ODJ_SID
{
    UCHAR Revision;
    UCHAR SubAuthorityCount;
    SID_IDENTIFIER_AUTHORITY IdentifierAuthority;
    [size_is(SubAuthorityCount)] ULONG SubAuthority[*];
}   ODJ_SID, *PODJ_SID;
```

## <a name="members"></a><span data-ttu-id="a9ba0-106">Member</span><span class="sxs-lookup"><span data-stu-id="a9ba0-106">Members</span></span>

### <a name="revision"></a><span data-ttu-id="a9ba0-107">Revision</span><span class="sxs-lookup"><span data-stu-id="a9ba0-107">Revision</span></span>

<span data-ttu-id="a9ba0-108">Muss auf die SID-Revision festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a9ba0-108">Must be set to the SID revision.</span></span>

### <a name="subauthoritycount"></a><span data-ttu-id="a9ba0-109">Subautoritycount</span><span class="sxs-lookup"><span data-stu-id="a9ba0-109">SubAuthorityCount</span></span>

<span data-ttu-id="a9ba0-110">Muss auf die Anzahl der Elemente in der untergeordneten Autorität festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a9ba0-110">Must be set to the number of elements in SubAuthority.</span></span>

### <a name="identifierauthority"></a><span data-ttu-id="a9ba0-111">Identifiziererautorität</span><span class="sxs-lookup"><span data-stu-id="a9ba0-111">IdentifierAuthority</span></span>

<span data-ttu-id="a9ba0-112">Muss auf den Bezeichner der SID-Autorität festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a9ba0-112">Must be set to the SID authority identifier.</span></span>

### <a name="subauthority"></a><span data-ttu-id="a9ba0-113">Untergeordnete Autorität</span><span class="sxs-lookup"><span data-stu-id="a9ba0-113">SubAuthority</span></span>

<span data-ttu-id="a9ba0-114">Muss ein Array von sid-untergeordneten Autoritäten enthalten.</span><span class="sxs-lookup"><span data-stu-id="a9ba0-114">Must contain an array of SID sub authorities.</span></span>

## <a name="see-also"></a><span data-ttu-id="a9ba0-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9ba0-115">See also</span></span>

[<span data-ttu-id="a9ba0-116">**IDL-Definitionen im Offline-Domänen Beitritt**</span><span class="sxs-lookup"><span data-stu-id="a9ba0-116">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="a9ba0-117">**ODJ- \_ sid- \_ \_ Bezeichnerautorität**</span><span class="sxs-lookup"><span data-stu-id="a9ba0-117">**ODJ\_SID\_IDENTIFIER\_AUTHORITY**</span></span>](odj-sid_identifier_authority.md)
