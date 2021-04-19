---
description: Enthält eine Liste von Basic-Service Set-Bezeichner (BSS).
ms.assetid: 22907f94-1ae8-4938-a816-b406656256c0
title: DOT11_BSSID_LIST-Struktur (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_BSSID_LIST
api_type:
- HeaderDef
api_location:
- windot11.h
ms.openlocfilehash: 345053a8d39ea37bea2fa2350dcc426420aed422
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349481"
---
# <a name="dot11_bssid_list-structure"></a><span data-ttu-id="6967f-103">DOT11 \_ BSSID- \_ Listenstruktur</span><span class="sxs-lookup"><span data-stu-id="6967f-103">DOT11\_BSSID\_LIST structure</span></span>

<span data-ttu-id="6967f-104">Die **DOT11 \_ BSSID- \_ Listen** Struktur enthält eine Liste von Basic-Service Set-bezeichern (BSS).</span><span class="sxs-lookup"><span data-stu-id="6967f-104">The **DOT11\_BSSID\_LIST** structure contains a list of basic service set (BSS) identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="6967f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6967f-105">Syntax</span></span>


```C++
typedef struct _DOT11_BSSID_LIST {
  NDIS_OBJECT_HEADER Header;
  ULONG              uNumOfEntries;
  ULONG              uTotalNumOfEntries;
  DOT11_MAC_ADDRESS  BSSIDs[1];
} DOT11_BSSID_LIST, *PDOT11_BSSID_LIST;
```



## <a name="members"></a><span data-ttu-id="6967f-106">Member</span><span class="sxs-lookup"><span data-stu-id="6967f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6967f-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="6967f-107">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="6967f-108">Eine [**NDIS- \_ Objekt \_ Header**](ndis-object-header.md) Struktur, die den Typ, die Version und die Größen Informationen einer NDIS-Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="6967f-108">An [**NDIS\_OBJECT\_HEADER**](ndis-object-header.md) structure that contains the type, version, and, size information of an NDIS structure.</span></span> <span data-ttu-id="6967f-109">Legen Sie für die meisten **DOT11 \_ -BSSID- \_ Listen** Strukturen das **Typelement** auf den **NDIS- \_ \_ Objekttyp \_ default** fest, legen Sie das **Revisions** Element auf **DOT11 \_ BSSID \_ List \_ Revision \_ 1** fest, und legen Sie den **size** -Member auf **sizeof (DOT11 \_ BSSID \_ List)** fest.</span><span class="sxs-lookup"><span data-stu-id="6967f-109">For most **DOT11\_BSSID\_LIST** structures, set the **Type** member to **NDIS\_OBJECT\_TYPE\_DEFAULT**, set the **Revision** member to **DOT11\_BSSID\_LIST\_REVISION\_1**, and set the **Size** member to **sizeof(DOT11\_BSSID\_LIST)**.</span></span>

</dd> <dt>

<span data-ttu-id="6967f-110">**unumamaentries**</span><span class="sxs-lookup"><span data-stu-id="6967f-110">**uNumOfEntries**</span></span>
</dt> <dd>

<span data-ttu-id="6967f-111">Die Anzahl der Einträge in dieser-Struktur.</span><span class="sxs-lookup"><span data-stu-id="6967f-111">The number of entries in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="6967f-112">**utotalnumuf-Einträge**</span><span class="sxs-lookup"><span data-stu-id="6967f-112">**uTotalNumOfEntries**</span></span>
</dt> <dd>

<span data-ttu-id="6967f-113">Die Gesamtanzahl unterstützter Einträge.</span><span class="sxs-lookup"><span data-stu-id="6967f-113">The total number of entries supported.</span></span>

</dd> <dt>

<span data-ttu-id="6967f-114">**BSSIDs**</span><span class="sxs-lookup"><span data-stu-id="6967f-114">**BSSIDs**</span></span>
</dt> <dd>

<span data-ttu-id="6967f-115">Eine Liste von BSS-bezeichgern.</span><span class="sxs-lookup"><span data-stu-id="6967f-115">A list of BSS identifiers.</span></span> <span data-ttu-id="6967f-116">Ein BSS-Bezeichner wird als [**DOT11 \_ Mac \_**](dot11-mac-address-type.md) -Adresstyp gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6967f-116">A BSS identifier is stored as a [**DOT11\_MAC\_ADDRESS**](dot11-mac-address-type.md) type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6967f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6967f-117">Requirements</span></span>



| <span data-ttu-id="6967f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6967f-118">Requirement</span></span> | <span data-ttu-id="6967f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="6967f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6967f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6967f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6967f-121">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6967f-121">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6967f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6967f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6967f-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6967f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6967f-124">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="6967f-124">Redistributable</span></span><br/>          | <span data-ttu-id="6967f-125">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="6967f-125">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="6967f-126">Header</span><span class="sxs-lookup"><span data-stu-id="6967f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6967f-127"><dt>Windot11. h (Include Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6967f-127"><dt>Windot11.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6967f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6967f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6967f-129">**WLAN- \_ Verbindungs \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="6967f-129">**WLAN\_CONNECTION\_PARAMETERS**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> </dl>

 

 




