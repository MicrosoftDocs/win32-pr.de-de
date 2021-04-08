---
description: Die Drucker \_ Info \_ 8-Struktur gibt die globalen Standarddrucker Einstellungen an.
ms.assetid: 98f26a45-5302-4358-bed6-691d9bc37554
title: PRINTER_INFO_8 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_8
- _PRINTER_INFO_8A
- _PRINTER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: e17780dc2f39dc3041e690de1ef7b5728c8743e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868340"
---
# <a name="printer_info_8-structure"></a><span data-ttu-id="2aca1-103">Drucker \_ Info \_ 8-Struktur</span><span class="sxs-lookup"><span data-stu-id="2aca1-103">PRINTER\_INFO\_8 structure</span></span>

<span data-ttu-id="2aca1-104">Die **Drucker \_ Info \_ 8** -Struktur gibt die globalen Standarddrucker Einstellungen an.</span><span class="sxs-lookup"><span data-stu-id="2aca1-104">The **PRINTER\_INFO\_8** structure specifies the global default printer settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="2aca1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2aca1-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_8 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_8, *PPRINTER_INFO_8;
```



## <a name="members"></a><span data-ttu-id="2aca1-106">Member</span><span class="sxs-lookup"><span data-stu-id="2aca1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2aca1-107">**pdevmode**</span><span class="sxs-lookup"><span data-stu-id="2aca1-107">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="2aca1-108">Ein Zeiger auf eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die die globalen Standarddrucker Daten definiert, z. b. die Papier Ausrichtung und die Auflösung.</span><span class="sxs-lookup"><span data-stu-id="2aca1-108">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that defines the global default printer data such as the paper orientation and the resolution.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2aca1-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2aca1-109">Remarks</span></span>

<span data-ttu-id="2aca1-110">Die globalen Standardwerte werden vom Administrator eines Druckers festgelegt, der von jedem verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2aca1-110">The global defaults are set by the administrator of a printer that can be used by anyone.</span></span> <span data-ttu-id="2aca1-111">Im Gegensatz dazu wirken sich die benutzerspezifischen Standardeinstellungen auf einen bestimmten Benutzer oder andere Benutzer aus, die das Profil verwenden.</span><span class="sxs-lookup"><span data-stu-id="2aca1-111">In contrast, the per-user defaults will affect a particular user or anyone else who uses the profile.</span></span> <span data-ttu-id="2aca1-112">Verwenden Sie für benutzerspezifische Standardeinstellungen [**Drucker \_ Informationen \_ 9**](printer-info-9.md).</span><span class="sxs-lookup"><span data-stu-id="2aca1-112">For per-user defaults, use [**PRINTER\_INFO\_9**](printer-info-9.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2aca1-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2aca1-113">Requirements</span></span>



| <span data-ttu-id="2aca1-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2aca1-114">Requirement</span></span> | <span data-ttu-id="2aca1-115">Wert</span><span class="sxs-lookup"><span data-stu-id="2aca1-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2aca1-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2aca1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2aca1-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2aca1-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2aca1-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2aca1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2aca1-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2aca1-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2aca1-120">Header</span><span class="sxs-lookup"><span data-stu-id="2aca1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2aca1-121"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2aca1-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="2aca1-122">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="2aca1-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2aca1-123">**\_ Drucker \_ Info \_ 8W** (Unicode) und **\_ Drucker \_ Info \_ 8a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2aca1-123">**\_PRINTER\_INFO\_8W** (Unicode) and **\_PRINTER\_INFO\_8A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="2aca1-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2aca1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2aca1-125">Drucken</span><span class="sxs-lookup"><span data-stu-id="2aca1-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2aca1-126">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="2aca1-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="2aca1-127">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="2aca1-127">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="2aca1-128">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="2aca1-128">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="2aca1-129">**Drucker \_ Informationen \_ 9**</span><span class="sxs-lookup"><span data-stu-id="2aca1-129">**PRINTER\_INFO\_9**</span></span>](printer-info-9.md)
</dt> </dl>

 

 




