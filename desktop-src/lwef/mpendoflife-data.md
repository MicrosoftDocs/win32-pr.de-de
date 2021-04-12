---
title: MPENDOFLIFE_DATA Struktur (mpclient. h)
description: '\ 0034; Ende des Lebenszyklus \ 0034; Benachrichtigungs Daten.'
ms.assetid: 00C2E707-9034-4BBC-99CF-3DFA4B8C08D9
keywords:
- MPENDOFLIFE_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPENDOFLIFE_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPENDOFLIFE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e209b9b35a089523815c353e8a750152bf4af75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104852"
---
# <a name="mpendoflife_data-structure"></a><span data-ttu-id="0dab0-105">\_Mpendomelife-Datenstruktur</span><span class="sxs-lookup"><span data-stu-id="0dab0-105">MPENDOFLIFE\_DATA structure</span></span>

<span data-ttu-id="0dab0-106">"Lebensdauer"-Benachrichtigungs Daten.</span><span class="sxs-lookup"><span data-stu-id="0dab0-106">"End of life" notification data.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dab0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0dab0-107">Syntax</span></span>


```C++
typedef struct tagMPENDOFLIFE_DATA {
  FILETIME ftSignatureExpiry;
  FILETIME ftPlatformExpiry;
  BOOL     fAdminControlled;
  BOOL     fEndOfLifeImpendingOrPast;
} MPENDOFLIFE_DATA, *PMPENDOFLIFE_DATA;
```



## <a name="members"></a><span data-ttu-id="0dab0-108">Member</span><span class="sxs-lookup"><span data-stu-id="0dab0-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0dab0-109">**ftsignatureablauf**</span><span class="sxs-lookup"><span data-stu-id="0dab0-109">**ftSignatureExpiry**</span></span>
</dt> <dd>

<span data-ttu-id="0dab0-110">Typ: **FILETIME**</span><span class="sxs-lookup"><span data-stu-id="0dab0-110">Type: **FILETIME**</span></span>

</dd> <dd>

<span data-ttu-id="0dab0-111">Zeitpunkt, zu dem die Signatur abläuft.</span><span class="sxs-lookup"><span data-stu-id="0dab0-111">Time when the signature expires.</span></span>

</dd> <dt>

<span data-ttu-id="0dab0-112">**ftplatformexpiry**</span><span class="sxs-lookup"><span data-stu-id="0dab0-112">**ftPlatformExpiry**</span></span>
</dt> <dd>

<span data-ttu-id="0dab0-113">Typ: **FILETIME**</span><span class="sxs-lookup"><span data-stu-id="0dab0-113">Type: **FILETIME**</span></span>

</dd> <dd>

<span data-ttu-id="0dab0-114">Uhrzeit, zu der die Plattform abläuft.</span><span class="sxs-lookup"><span data-stu-id="0dab0-114">Time when the platform expires.</span></span>

</dd> <dt>

<span data-ttu-id="0dab0-115">**fadminkontrollierten**</span><span class="sxs-lookup"><span data-stu-id="0dab0-115">**fAdminControlled**</span></span>
</dt> <dd>

<span data-ttu-id="0dab0-116">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="0dab0-116">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="0dab0-117">True, wenn der Administrator die Richtlinie zur Anzeige der Benachrichtigung steuert.</span><span class="sxs-lookup"><span data-stu-id="0dab0-117">True if the administrator controlling the policy for showing the notification.</span></span> <span data-ttu-id="0dab0-118">Wenn dieser Wert festgelegt ist, weist die Benutzeroberfläche an, die EOL-Benachrichtigung nicht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0dab0-118">If set, this tells the UI to not show the EOL notification.</span></span>

</dd> <dt>

<span data-ttu-id="0dab0-119">**fendoflifeimpumdingorpast**</span><span class="sxs-lookup"><span data-stu-id="0dab0-119">**fEndOfLifeImpendingOrPast**</span></span>
</dt> <dd>

<span data-ttu-id="0dab0-120">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="0dab0-120">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="0dab0-121">True, wenn "Ende des Lebenszyklus" aussteht oder überschreitet.</span><span class="sxs-lookup"><span data-stu-id="0dab0-121">True if "End of Life" is pending or past.</span></span> <span data-ttu-id="0dab0-122">False gibt an, dass die Benutzeroberfläche und die Clients alle EOL-bezogenen Zustände löschen können.</span><span class="sxs-lookup"><span data-stu-id="0dab0-122">If false, UI and clients can clear any EOL related states.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0dab0-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0dab0-123">Requirements</span></span>



| <span data-ttu-id="0dab0-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0dab0-124">Requirement</span></span> | <span data-ttu-id="0dab0-125">Wert</span><span class="sxs-lookup"><span data-stu-id="0dab0-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0dab0-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0dab0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0dab0-127">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0dab0-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0dab0-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0dab0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0dab0-129">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0dab0-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0dab0-130">Header</span><span class="sxs-lookup"><span data-stu-id="0dab0-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0dab0-131"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="0dab0-131"><dt>MpClient.h</dt></span></span> </dl> |



 

 





