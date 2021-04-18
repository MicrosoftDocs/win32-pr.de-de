---
description: Die Drucker \_ Info \_ 9-Struktur gibt die Standarddrucker Einstellungen pro Benutzer an.
ms.assetid: 8bafb995-f31c-46e3-a950-45e240c678aa
title: PRINTER_INFO_9 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_9
- _PRINTER_INFO_9A
- _PRINTER_INFO_9W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c0ae3c099da17d7fc437a67035d8da2cd00136bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350905"
---
# <a name="printer_info_9-structure"></a><span data-ttu-id="81047-103">Drucker \_ Info \_ 9-Struktur</span><span class="sxs-lookup"><span data-stu-id="81047-103">PRINTER\_INFO\_9 structure</span></span>

<span data-ttu-id="81047-104">Die **Drucker \_ Info \_ 9** -Struktur gibt die Standarddrucker Einstellungen pro Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="81047-104">The **PRINTER\_INFO\_9** structure specifies the per-user default printer settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="81047-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="81047-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_9 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_9, *PPRINTER_INFO_9;
```



## <a name="members"></a><span data-ttu-id="81047-106">Member</span><span class="sxs-lookup"><span data-stu-id="81047-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="81047-107">**pdevmode**</span><span class="sxs-lookup"><span data-stu-id="81047-107">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="81047-108">Ein Zeiger auf eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die die Standarddrucker Daten des Benutzers definiert, z. b. die Papier Ausrichtung und die Auflösung.</span><span class="sxs-lookup"><span data-stu-id="81047-108">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that defines the per-user default printer data such as the paper orientation and the resolution.</span></span> <span data-ttu-id="81047-109">**DEVMODE** wird in der Registrierung des Benutzers gespeichert.</span><span class="sxs-lookup"><span data-stu-id="81047-109">The **DEVMODE** is stored in the user's registry.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81047-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81047-110">Remarks</span></span>

<span data-ttu-id="81047-111">Die benutzerspezifischen Standardeinstellungen wirken sich nur auf einen bestimmten Benutzer oder auf alle Benutzer aus, die das Profil verwenden.</span><span class="sxs-lookup"><span data-stu-id="81047-111">The per-user defaults will affect only a particular user or anyone who uses the profile.</span></span> <span data-ttu-id="81047-112">Im Gegensatz dazu werden die globalen Standardwerte vom Administrator eines Druckers festgelegt, der von jedem verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="81047-112">In contrast, the global defaults are set by the administrator of a printer that can be used by anyone.</span></span> <span data-ttu-id="81047-113">Verwenden Sie bei globalen Standardeinstellungen [**Drucker \_ Informationen \_ 8**](printer-info-8.md).</span><span class="sxs-lookup"><span data-stu-id="81047-113">For global defaults, use [**PRINTER\_INFO\_8**](printer-info-8.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="81047-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81047-114">Requirements</span></span>



| <span data-ttu-id="81047-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81047-115">Requirement</span></span> | <span data-ttu-id="81047-116">Wert</span><span class="sxs-lookup"><span data-stu-id="81047-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81047-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81047-117">Minimum supported client</span></span><br/> | <span data-ttu-id="81047-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81047-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="81047-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81047-119">Minimum supported server</span></span><br/> | <span data-ttu-id="81047-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81047-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="81047-121">Header</span><span class="sxs-lookup"><span data-stu-id="81047-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="81047-122"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81047-122"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="81047-123">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="81047-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="81047-124">**\_ Drucker \_ Informationen \_ 9W** (Unicode) und **\_ Drucker \_ Info \_ 9a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="81047-124">**\_PRINTER\_INFO\_9W** (Unicode) and **\_PRINTER\_INFO\_9A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="81047-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81047-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81047-126">Drucken</span><span class="sxs-lookup"><span data-stu-id="81047-126">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="81047-127">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="81047-127">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="81047-128">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="81047-128">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="81047-129">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="81047-129">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="81047-130">**Drucker \_ Informationen \_ 8**</span><span class="sxs-lookup"><span data-stu-id="81047-130">**PRINTER\_INFO\_8**</span></span>](printer-info-8.md)
</dt> </dl>

 

 




