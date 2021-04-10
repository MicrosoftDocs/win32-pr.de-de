---
description: Eine-Struktur, die den zu bewertenden Host und die Quelldatei identifiziert.
ms.assetid: 547EF59E-7DE5-45E4-948F-109547FAAEE7
title: WLDP_HOST_INFORMATION Struktur (wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_INFORMATION
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: ad20be7fa5887e42c09248d04e14f5ff8cffcd54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041341"
---
# <a name="wldp_host_information-structure"></a><span data-ttu-id="7b8be-103">Wldp- \_ Host \_ Informationsstruktur</span><span class="sxs-lookup"><span data-stu-id="7b8be-103">WLDP\_HOST\_INFORMATION structure</span></span>

<span data-ttu-id="7b8be-104">Eine-Struktur, die den zu bewertenden Host und die Quelldatei identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7b8be-104">A structure identifying the host and source file to be evaluated.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b8be-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b8be-105">Syntax</span></span>


```C++
typedef struct _WLDP_HOST_INFORMATION {
  DWORD        dwRevision;
  WLDP_HOST_ID dwHostId;
  PCWSTR       szSource;
  HANDLE       hSource;
} WLDP_HOST_INFORMATION, *PWLDP_HOST_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="7b8be-106">Member</span><span class="sxs-lookup"><span data-stu-id="7b8be-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7b8be-107">**dwrevision**</span><span class="sxs-lookup"><span data-stu-id="7b8be-107">**dwRevision**</span></span>
</dt> <dd>

<span data-ttu-id="7b8be-108">Muss eine **wldp- \_ Host \_ Informations \_ Revision** sein.</span><span class="sxs-lookup"><span data-stu-id="7b8be-108">Must be **WLDP\_HOST\_INFORMATION\_REVISION**.</span></span>

</dd> <dt>

<span data-ttu-id="7b8be-109">**dwhostid**</span><span class="sxs-lookup"><span data-stu-id="7b8be-109">**dwHostId**</span></span>
</dt> <dd>

<span data-ttu-id="7b8be-110">Enumerationswert aus der [**wldp- \_ Host- \_ ID**](wldp-host-id.md) , die die Host-ID beschreibt.</span><span class="sxs-lookup"><span data-stu-id="7b8be-110">Enumeration value from [**WLDP\_HOST\_ID**](wldp-host-id.md) that describes the host ID.</span></span>

</dd> <dt>

<span data-ttu-id="7b8be-111">**szsource**</span><span class="sxs-lookup"><span data-stu-id="7b8be-111">**szSource**</span></span>
</dt> <dd>

<span data-ttu-id="7b8be-112">Vollständiger Pfad-und Skript Name mit der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="7b8be-112">Full path and script name with the extension.</span></span> <span data-ttu-id="7b8be-113">NULL für die **globale wldp- \_ Host- \_ ID \_** oder die manuelle Skriptausführung.</span><span class="sxs-lookup"><span data-stu-id="7b8be-113">NULL for **WLDP\_HOST\_ID\_GLOBAL**, or manual script execution.</span></span>

</dd> <dt>

<span data-ttu-id="7b8be-114">**hsource**</span><span class="sxs-lookup"><span data-stu-id="7b8be-114">**hSource**</span></span>
</dt> <dd>

<span data-ttu-id="7b8be-115">Zusätzlich zum Namen kann der Aufrufer ein Handle für die Datei angeben, die für die Validierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7b8be-115">In addition to the name, the caller can specify a handle to the file used for validation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b8be-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b8be-116">Requirements</span></span>



| <span data-ttu-id="7b8be-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b8be-117">Requirement</span></span> | <span data-ttu-id="7b8be-118">Wert</span><span class="sxs-lookup"><span data-stu-id="7b8be-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7b8be-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b8be-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7b8be-120">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b8be-120">Windows 8 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7b8be-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b8be-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7b8be-122">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b8be-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7b8be-123">Header</span><span class="sxs-lookup"><span data-stu-id="7b8be-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b8be-124"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b8be-124"><dt>Wldp.h</dt></span></span> </dl> |



 

 




