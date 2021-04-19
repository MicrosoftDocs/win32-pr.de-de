---
description: Enthält die Tabelle mit Schlüsselinformationen für alle drahtlosen LAN-Schnittstellen, die vom drahtlos Konfigurations Dienst verwaltet werden.
ms.assetid: 5d5fe222-6ca1-4778-9f64-1c6a63467a6c
title: INTFS_KEY_TABLE Struktur (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTFS_KEY_TABLE
api_type:
- HeaderDef
api_location:
- Wzcsapi.h
ms.openlocfilehash: 4ef38f2317c763eaa6c7e0379be5c8b00c0ed6b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350473"
---
# <a name="intfs_key_table-structure"></a><span data-ttu-id="9c18c-103">Intfs- \_ Schlüssel \_ Tabellenstruktur</span><span class="sxs-lookup"><span data-stu-id="9c18c-103">INTFS\_KEY\_TABLE structure</span></span>

<span data-ttu-id="9c18c-104">\[**Intfs \_ Die Schlüssel \_ Tabelle** wird ab Windows Vista und Windows Server 2008 nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9c18c-104">\[**INTFS\_KEY\_TABLE** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="9c18c-105">Verwenden Sie stattdessen die [native WiFi-API](native-wifi-reference.md), die eine ähnliche Funktionalität bietet.</span><span class="sxs-lookup"><span data-stu-id="9c18c-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="9c18c-106">Weitere Informationen finden Sie unter Informationen zur [nativen WiFi-API](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="9c18c-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="9c18c-107">Die **intfs- \_ Schlüssel \_ Tabellen** Struktur enthält die Tabelle mit Schlüsselinformationen für alle drahtlosen LAN-Schnittstellen, die vom drahtlos Konfigurations Dienst verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="9c18c-107">The **INTFS\_KEY\_TABLE** structure contains the table of key information for all wireless LAN interfaces managed by the Wireless Configuration Service.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c18c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c18c-108">Syntax</span></span>


```C++
typedef struct {
  DWORD           dwNumIntfs;
  PINTF_KEY_ENTRY pIntfs;
} INTFS_KEY_TABLE, *PINTFS_KEY_TABLE;
```



## <a name="members"></a><span data-ttu-id="9c18c-109">Member</span><span class="sxs-lookup"><span data-stu-id="9c18c-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="9c18c-110">**dwnumintfs**</span><span class="sxs-lookup"><span data-stu-id="9c18c-110">**dwNumIntfs**</span></span>
</dt> <dd>

<span data-ttu-id="9c18c-111">Die Gesamtanzahl der Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="9c18c-111">Total number of interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="9c18c-112">**pintfs**</span><span class="sxs-lookup"><span data-stu-id="9c18c-112">**pIntfs**</span></span>
</dt> <dd>

<span data-ttu-id="9c18c-113">Ein Zeiger auf die [**INTF- \_ Schlüssel \_ Eintrags**](intf-key-entry.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="9c18c-113">Pointer to the [**INTF\_KEY\_ENTRY**](intf-key-entry.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c18c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c18c-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9c18c-115">Die Header Datei " *wzcsapi. h* " ist im Windows SDK nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9c18c-115">The *Wzcsapi.h* header file is not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9c18c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c18c-116">Requirements</span></span>



| <span data-ttu-id="9c18c-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c18c-117">Requirement</span></span> | <span data-ttu-id="9c18c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9c18c-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9c18c-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9c18c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9c18c-120">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c18c-120">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9c18c-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9c18c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9c18c-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c18c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9c18c-123">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="9c18c-123">End of client support</span></span><br/>    | <span data-ttu-id="9c18c-124">Windows XP mit SP3</span><span class="sxs-lookup"><span data-stu-id="9c18c-124">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="9c18c-125">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="9c18c-125">End of server support</span></span><br/>    | <span data-ttu-id="9c18c-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9c18c-126">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="9c18c-127">Header</span><span class="sxs-lookup"><span data-stu-id="9c18c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c18c-128"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c18c-128"><dt>Wzcsapi.h</dt></span></span> </dl> |



 

 




