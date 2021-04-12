---
description: Speichert die Schlüsselinformationen zu einer drahtlosen LAN-Schnittstelle, die vom drahtlos Konfigurations Dienst verwaltet wird.
ms.assetid: 5e689fd0-27d9-48eb-8983-96d7918be1cd
title: INTF_KEY_ENTRY Struktur (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_KEY_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: 91f25708e79be4f85c4200bd690404ff39f567d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343898"
---
# <a name="intf_key_entry-structure"></a><span data-ttu-id="8b7bd-103">INTF- \_ Schlüssel \_ Eintrags Struktur</span><span class="sxs-lookup"><span data-stu-id="8b7bd-103">INTF\_KEY\_ENTRY structure</span></span>

<span data-ttu-id="8b7bd-104">\[**INTF \_ Der Schlüssel \_ Eintrag** wird ab Windows Vista und Windows Server 2008 nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8b7bd-104">\[**INTF\_KEY\_ENTRY** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="8b7bd-105">Verwenden Sie stattdessen die [native WiFi-API](native-wifi-reference.md), die eine ähnliche Funktionalität bietet.</span><span class="sxs-lookup"><span data-stu-id="8b7bd-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="8b7bd-106">Weitere Informationen finden Sie unter Informationen zur [nativen WiFi-API](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="8b7bd-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="8b7bd-107">In der **INTF- \_ Schlüssel \_ Eintrags** Struktur werden die Schlüsselinformationen zu einer vom drahtlos Konfigurations Dienst verwalteten drahtlosen LAN-Schnittstelle gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8b7bd-107">The **INTF\_KEY\_ENTRY** structure stores the key information about a wireless LAN interface managed by the Wireless Configuration Service.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b7bd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b7bd-108">Syntax</span></span>


```C++
typedef struct {
  LPWSTR wszGuid;
} INTF_KEY_ENTRY, *PINTF_KEY_ENTRY;
```



## <a name="members"></a><span data-ttu-id="8b7bd-109">Member</span><span class="sxs-lookup"><span data-stu-id="8b7bd-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="8b7bd-110">**wszguid**</span><span class="sxs-lookup"><span data-stu-id="8b7bd-110">**wszGuid**</span></span>
</dt> <dd>

<span data-ttu-id="8b7bd-111">Ein Zeiger auf die GUID der Schnittstelle, die als Unicode-Zeichenfolge im folgenden Format dargestellt wird: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".</span><span class="sxs-lookup"><span data-stu-id="8b7bd-111">A pointer to the interface GUID represented as a Unicode string in the following format: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b7bd-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b7bd-112">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8b7bd-113">Die Header Datei " *wzcsapi. h* " ist im Windows SDK nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8b7bd-113">The *Wzcsapi.h* header file is not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8b7bd-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b7bd-114">Requirements</span></span>



| <span data-ttu-id="8b7bd-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b7bd-115">Requirement</span></span> | <span data-ttu-id="8b7bd-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8b7bd-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8b7bd-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b7bd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8b7bd-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b7bd-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8b7bd-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b7bd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8b7bd-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b7bd-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8b7bd-121">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="8b7bd-121">End of client support</span></span><br/>    | <span data-ttu-id="8b7bd-122">Windows XP mit SP3</span><span class="sxs-lookup"><span data-stu-id="8b7bd-122">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="8b7bd-123">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="8b7bd-123">End of server support</span></span><br/>    | <span data-ttu-id="8b7bd-124">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8b7bd-124">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="8b7bd-125">Header</span><span class="sxs-lookup"><span data-stu-id="8b7bd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b7bd-126"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b7bd-126"><dt>Wzcsapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b7bd-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b7bd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b7bd-128">**intfs- \_ Schlüssel \_ Tabelle**</span><span class="sxs-lookup"><span data-stu-id="8b7bd-128">**INTFS\_KEY\_TABLE**</span></span>](intfs-key-table.md)
</dt> <dt>

[<span data-ttu-id="8b7bd-129">**Wzcenumschlag-Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="8b7bd-129">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> </dl>

 

 




