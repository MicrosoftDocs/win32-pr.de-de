---
description: Enthält ein Array von BLOB.
ms.assetid: e87f493b-f160-4316-b369-75d20c735213
title: BLOB_TABLE Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BLOB_TABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 32bacc925381f1c7ed30aa66247671b67e31b7e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215893"
---
# <a name="blob_table-structure"></a><span data-ttu-id="47f8c-103">BLOB- \_ Tabellenstruktur</span><span class="sxs-lookup"><span data-stu-id="47f8c-103">BLOB\_TABLE structure</span></span>

<span data-ttu-id="47f8c-104">Die **BLOB- \_ Tabellen** Struktur enthält ein Array von BLOBs.</span><span class="sxs-lookup"><span data-stu-id="47f8c-104">The **BLOB\_TABLE** structure contains an array of BLOBs.</span></span>

## <a name="syntax"></a><span data-ttu-id="47f8c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="47f8c-105">Syntax</span></span>


```C++
typedef struct {
  DWORD dwNumBlobs;
  HBLOB hBlobs[];
} BLOB_TABLE, *PBLOB_TABLE;
```



## <a name="members"></a><span data-ttu-id="47f8c-106">Member</span><span class="sxs-lookup"><span data-stu-id="47f8c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="47f8c-107">**dwnumblosb**</span><span class="sxs-lookup"><span data-stu-id="47f8c-107">**dwNumBlobs**</span></span>
</dt> <dd>

<span data-ttu-id="47f8c-108">Indikator, dem viele blobdie folgen.</span><span class="sxs-lookup"><span data-stu-id="47f8c-108">Indicator that many BLOBs follow.</span></span>

</dd> <dt>

<span data-ttu-id="47f8c-109">**hblob**</span><span class="sxs-lookup"><span data-stu-id="47f8c-109">**hBlobs**</span></span>
</dt> <dd>

<span data-ttu-id="47f8c-110">Handle für das BLOB-Array.</span><span class="sxs-lookup"><span data-stu-id="47f8c-110">Handle to the BLOB array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="47f8c-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47f8c-111">Requirements</span></span>



| <span data-ttu-id="47f8c-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47f8c-112">Requirement</span></span> | <span data-ttu-id="47f8c-113">Wert</span><span class="sxs-lookup"><span data-stu-id="47f8c-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="47f8c-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="47f8c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="47f8c-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47f8c-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="47f8c-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="47f8c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="47f8c-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47f8c-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="47f8c-118">Header</span><span class="sxs-lookup"><span data-stu-id="47f8c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="47f8c-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="47f8c-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




