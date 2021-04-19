---
description: Enthält das Erstellungstag eines Akkus.
ms.assetid: 0cda66fc-bf4a-4a38-b43c-6eecde46c414
title: BATTERY_MANUFACTURE_DATE-Struktur (poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_MANUFACTURE_DATE
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: cdd3f067bc3ed2e3339710e0a5bd48c8f42e6525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362223"
---
# <a name="battery_manufacture_date-structure"></a><span data-ttu-id="f3267-103">\_ \_ Datums Struktur der Akku Fertigung</span><span class="sxs-lookup"><span data-stu-id="f3267-103">BATTERY\_MANUFACTURE\_DATE structure</span></span>

<span data-ttu-id="f3267-104">Enthält das Erstellungstag eines Akkus.</span><span class="sxs-lookup"><span data-stu-id="f3267-104">Contains the date of manufacture of a battery.</span></span> <span data-ttu-id="f3267-105">Diese Struktur wird von der Struktur der [**Akku \_ Abfrage \_ Informationen**](battery-query-information-str.md) verwendet, wenn die Informationen auf der Ebene "batterymanufacturedate" angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="f3267-105">This structure is used by the [**BATTERY\_QUERY\_INFORMATION**](battery-query-information-str.md) structure when the BatteryManufactureDate information level is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3267-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3267-106">Syntax</span></span>


```C++
typedef struct _BATTERY_MANUFACTURE_DATE {
  UCHAR  Day;
  UCHAR  Month;
  USHORT Year;
} BATTERY_MANUFACTURE_DATE, *PBATTERY_MANUFACTURE_DATE;
```



## <a name="members"></a><span data-ttu-id="f3267-107">Member</span><span class="sxs-lookup"><span data-stu-id="f3267-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f3267-108">**Day**</span><span class="sxs-lookup"><span data-stu-id="f3267-108">**Day**</span></span>
</dt> <dd>

<span data-ttu-id="f3267-109">Der Tag des Herstellungs Monats im Bereich von 1 bis 31.</span><span class="sxs-lookup"><span data-stu-id="f3267-109">The day of the month of manufacture, in the range 1 to 31.</span></span> <span data-ttu-id="f3267-110">Trotz des-Datentyps ist dies kein ASCII-codierter Wert.</span><span class="sxs-lookup"><span data-stu-id="f3267-110">In spite of the data type, this is not an ASCII encoded value.</span></span> <span data-ttu-id="f3267-111">Dabei handelt es sich um ein Byte ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="f3267-111">It is an unsigned byte.</span></span>

</dd> <dt>

<span data-ttu-id="f3267-112">**Ges**</span><span class="sxs-lookup"><span data-stu-id="f3267-112">**Month**</span></span>
</dt> <dd>

<span data-ttu-id="f3267-113">Der Monat der Fertigung im Bereich von 1 (Januar) bis 12 (Dezember).</span><span class="sxs-lookup"><span data-stu-id="f3267-113">The month of manufacture, in the range 1 (January) to 12 (December).</span></span> <span data-ttu-id="f3267-114">Trotz des-Datentyps ist dies kein ASCII-codierter Wert.</span><span class="sxs-lookup"><span data-stu-id="f3267-114">In spite of the data type, this is not an ASCII encoded value.</span></span> <span data-ttu-id="f3267-115">Dabei handelt es sich um ein Byte ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="f3267-115">It is an unsigned byte.</span></span>

</dd> <dt>

<span data-ttu-id="f3267-116">**Jährigen**</span><span class="sxs-lookup"><span data-stu-id="f3267-116">**Year**</span></span>
</dt> <dd>

<span data-ttu-id="f3267-117">Das Jahr der Fertigung.</span><span class="sxs-lookup"><span data-stu-id="f3267-117">The year of manufacture.</span></span> <span data-ttu-id="f3267-118">Dies liegt in der Regel im Bereich von 1900-2100.</span><span class="sxs-lookup"><span data-stu-id="f3267-118">This will typically be in the range 1900-2100.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3267-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3267-119">Remarks</span></span>

<span data-ttu-id="f3267-120">Das Datum wird im gregorianischen oder westlichen Kalender Format codiert.</span><span class="sxs-lookup"><span data-stu-id="f3267-120">The date is encoded in the Gregorian or western calendar format.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3267-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3267-121">Requirements</span></span>



| <span data-ttu-id="f3267-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3267-122">Requirement</span></span> | <span data-ttu-id="f3267-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f3267-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3267-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f3267-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f3267-125">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3267-125">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="f3267-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f3267-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f3267-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3267-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="f3267-128">Header</span><span class="sxs-lookup"><span data-stu-id="f3267-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3267-129"><dt>Poclass. h; </dt> <dt>Batclass. h unter Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="f3267-129"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3267-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3267-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3267-131">**Akku \_ Abfrage \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="f3267-131">**BATTERY\_QUERY\_INFORMATION**</span></span>](battery-query-information-str.md)
</dt> <dt>

[<span data-ttu-id="f3267-132">**IOCTL- \_ Akku \_ Abfrage \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="f3267-132">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> </dl>

 

 




