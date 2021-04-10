---
title: SID_IDENTIFIER_AUTHORITY
description: SID_IDENTIFIER_AUTHORITY IDL-Definition
ms.assetid: 88fe41f4-1c67-4290-ac21-fd43ff12d825
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: d9a80ed0717a279f39ac7a105a95807911232c82
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "104102526"
---
# <a name="sid_identifier_authority-structure"></a><span data-ttu-id="f1fec-103">SID_IDENTIFIER_AUTHORITY Struktur</span><span class="sxs-lookup"><span data-stu-id="f1fec-103">SID_IDENTIFIER_AUTHORITY structure</span></span>

<span data-ttu-id="f1fec-104">Enthält eine SID-Bezeichnerautorität.</span><span class="sxs-lookup"><span data-stu-id="f1fec-104">Contains a SID identifier authority.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1fec-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1fec-105">Syntax</span></span>

```C++
typedef struct _SID_IDENTIFIER_AUTHORITY
{
    UCHAR Value[6];
} SID_IDENTIFIER_AUTHORITY, *PSID_IDENTIFIER_AUTHORITY;
```

## <a name="members"></a><span data-ttu-id="f1fec-106">Member</span><span class="sxs-lookup"><span data-stu-id="f1fec-106">Members</span></span>

### <a name="value"></a><span data-ttu-id="f1fec-107">Wert</span><span class="sxs-lookup"><span data-stu-id="f1fec-107">Value</span></span>

<span data-ttu-id="f1fec-108">Muss auf die sechs Bytes der SID-Bezeichnerautorität festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f1fec-108">Must be set to the six bytes of the SID identifier authority.</span></span>

## <a name="see-also"></a><span data-ttu-id="f1fec-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1fec-109">See also</span></span>

[<span data-ttu-id="f1fec-110">**IDL-Definitionen im Offline-Domänen Beitritt**</span><span class="sxs-lookup"><span data-stu-id="f1fec-110">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)