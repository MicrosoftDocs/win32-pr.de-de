---
title: MPCOMPONENT_VERSION Struktur (mpclient. h)
description: Versions-und Aktualisierungszeit für eine einzelne Komponente.
ms.assetid: 43468230-EE13-4630-8C09-F8DF983EF748
keywords:
- MPCOMPONENT_VERSION Struktur Funktionen der Legacy-Windows-Umgebung
- PMPCOMPONENT_VERSION Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPCOMPONENT_VERSION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a1d4b5011bb185dc8ca0892e0a0e65bc4a7d8b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949824"
---
# <a name="mpcomponent_version-structure"></a><span data-ttu-id="04cd9-105">Mpcomponent- \_ Versions Struktur</span><span class="sxs-lookup"><span data-stu-id="04cd9-105">MPCOMPONENT\_VERSION structure</span></span>

<span data-ttu-id="04cd9-106">Versions-und Aktualisierungszeit für eine einzelne Komponente.</span><span class="sxs-lookup"><span data-stu-id="04cd9-106">Version and update time for an individual component.</span></span>

## <a name="syntax"></a><span data-ttu-id="04cd9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="04cd9-107">Syntax</span></span>


```C++
typedef struct tagMPCOMPONENT_VERSION {
  ULONGLONG      Version;
  ULARGE_INTEGER UpdateTime;
} MPCOMPONENT_VERSION, *PMPCOMPONENT_VERSION;
```



## <a name="members"></a><span data-ttu-id="04cd9-108">Member</span><span class="sxs-lookup"><span data-stu-id="04cd9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="04cd9-109">**Version**</span><span class="sxs-lookup"><span data-stu-id="04cd9-109">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="04cd9-110">Typ: **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="04cd9-110">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="04cd9-111">Versions Feld.</span><span class="sxs-lookup"><span data-stu-id="04cd9-111">Version field.</span></span> <span data-ttu-id="04cd9-112">Jedes **Wort** stellt die Haupt-, neben Version, Build und Revision dar.</span><span class="sxs-lookup"><span data-stu-id="04cd9-112">Each **WORD** represents major, minor, build, and revision.</span></span>

</dd> <dt>

<span data-ttu-id="04cd9-113">**Update time**</span><span class="sxs-lookup"><span data-stu-id="04cd9-113">**UpdateTime**</span></span>
</dt> <dd>

<span data-ttu-id="04cd9-114">Typ: **ularge \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="04cd9-114">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="04cd9-115">Der Zeitpunkt der letzten Aktualisierung der Komponente im **FILETIME** -Format.</span><span class="sxs-lookup"><span data-stu-id="04cd9-115">Last update time of the component, in **FILETIME** format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="04cd9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04cd9-116">Requirements</span></span>



| <span data-ttu-id="04cd9-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04cd9-117">Requirement</span></span> | <span data-ttu-id="04cd9-118">Wert</span><span class="sxs-lookup"><span data-stu-id="04cd9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04cd9-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="04cd9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="04cd9-120">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04cd9-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="04cd9-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="04cd9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="04cd9-122">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04cd9-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="04cd9-123">Header</span><span class="sxs-lookup"><span data-stu-id="04cd9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="04cd9-124"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="04cd9-124"><dt>MpClient.h</dt></span></span> </dl> |



 

 





