---
description: Die Struktur der Drucker Standards \_ gibt den Standard Datentyp, die Umgebung, die Initialisierungs Daten und die Zugriffsrechte für einen Drucker an.
ms.assetid: df29c3a6-b1d1-4d40-887d-5ffc032a5871
title: PRINTER_DEFAULTS Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_DEFAULTS
- _PRINTER_DEFAULTSA
- _PRINTER_DEFAULTSW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ad3f9b2a6647c620b2d947bca5ef5201076e23ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363553"
---
# <a name="printer_defaults-structure"></a><span data-ttu-id="e502a-103">Struktur der Drucker Standards \_</span><span class="sxs-lookup"><span data-stu-id="e502a-103">PRINTER\_DEFAULTS structure</span></span>

<span data-ttu-id="e502a-104">Die **Struktur \_ der Drucker** Standards gibt den Standard Datentyp, die Umgebung, die Initialisierungs Daten und die Zugriffsrechte für einen Drucker an.</span><span class="sxs-lookup"><span data-stu-id="e502a-104">The **PRINTER\_DEFAULTS** structure specifies the default data type, environment, initialization data, and access rights for a printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e502a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e502a-105">Syntax</span></span>


```C++
typedef struct _PRINTER_DEFAULTS {
  LPTSTR      pDatatype;
  LPDEVMODE   pDevMode;
  ACCESS_MASK DesiredAccess;
} PRINTER_DEFAULTS, *PPRINTER_DEFAULTS;
```



## <a name="members"></a><span data-ttu-id="e502a-106">Member</span><span class="sxs-lookup"><span data-stu-id="e502a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e502a-107">**pdatatype**</span><span class="sxs-lookup"><span data-stu-id="e502a-107">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="e502a-108">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Standard Datentyp für einen Drucker angibt.</span><span class="sxs-lookup"><span data-stu-id="e502a-108">Pointer to a null-terminated string that specifies the default data type for a printer.</span></span>

</dd> <dt>

<span data-ttu-id="e502a-109">**pdevmode**</span><span class="sxs-lookup"><span data-stu-id="e502a-109">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="e502a-110">Zeiger auf eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die die Standardumgebung und die Initialisierungs Daten für einen Drucker identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e502a-110">Pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that identifies the default environment and initialization data for a printer.</span></span>

</dd> <dt>

<span data-ttu-id="e502a-111">**DesiredAccess**</span><span class="sxs-lookup"><span data-stu-id="e502a-111">**DesiredAccess**</span></span>
</dt> <dd>

<span data-ttu-id="e502a-112">Gibt die gewünschten Zugriffsrechte für einen Drucker an.</span><span class="sxs-lookup"><span data-stu-id="e502a-112">Specifies desired access rights for a printer.</span></span> <span data-ttu-id="e502a-113">Die [**OpenPrinter**](openprinter.md) -Funktion verwendet dieses Element, um die Zugriffsrechte für den Drucker festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e502a-113">The [**OpenPrinter**](openprinter.md) function uses this member to set access rights to the printer.</span></span> <span data-ttu-id="e502a-114">Diese Rechte können sich auf den Betrieb der Funktionen [**SetPrinter**](setprinter.md) und [**deleteprinter**](deleteprinter.md) auswirken.</span><span class="sxs-lookup"><span data-stu-id="e502a-114">These rights can affect the operation of the [**SetPrinter**](setprinter.md) and [**DeletePrinter**](deleteprinter.md) functions.</span></span> <span data-ttu-id="e502a-115">Die Zugriffsrechte können eines der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="e502a-115">The access rights can be one of the following.</span></span>



| <span data-ttu-id="e502a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e502a-116">Value</span></span>                                       | <span data-ttu-id="e502a-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e502a-117">Meaning</span></span>                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e502a-118">Drucker \_ Zugriffs \_ Verwaltung</span><span class="sxs-lookup"><span data-stu-id="e502a-118">PRINTER\_ACCESS\_ADMINISTER</span></span>                 | <span data-ttu-id="e502a-119">Zum Ausführen administrativer Aufgaben, wie z. b. die von [**SetPrinter**](setprinter.md)bereitgestellten.</span><span class="sxs-lookup"><span data-stu-id="e502a-119">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md).</span></span>                                                                                                 |
| <span data-ttu-id="e502a-120">Drucker \_ Zugriffs \_ Verwendung</span><span class="sxs-lookup"><span data-stu-id="e502a-120">PRINTER\_ACCESS\_USE</span></span>                        | <span data-ttu-id="e502a-121">Zum Ausführen grundlegender Druckvorgänge.</span><span class="sxs-lookup"><span data-stu-id="e502a-121">To perform basic printing operations.</span></span>                                                                                                                                                        |
| <span data-ttu-id="e502a-122">Drucker \_ Zugriff \_ mit \_ eingeschränkter Verwaltung</span><span class="sxs-lookup"><span data-stu-id="e502a-122">PRINTER\_ACCESS\_MANAGE\_LIMITED</span></span>            | <span data-ttu-id="e502a-123">Zum Ausführen administrativer Aufgaben, wie z. b. die von [**SetPrinter**](setprinter.md) und [**setprinterdata**](setprinterdata.md)bereitgestellten.</span><span class="sxs-lookup"><span data-stu-id="e502a-123">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md) and [**SetPrinterData**](setprinterdata.md).</span></span> <span data-ttu-id="e502a-124">Dieser Wert ist ab Windows 8.1 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e502a-124">This value is available starting from Windows 8.1.</span></span> |
| <span data-ttu-id="e502a-125">Drucker \_ \_ Zugriff</span><span class="sxs-lookup"><span data-stu-id="e502a-125">PRINTER\_ALL\_ACCESS</span></span>                        | <span data-ttu-id="e502a-126">Zum Ausführen aller Verwaltungsaufgaben und grundlegenden Druckvorgänge mit Ausnahme von Synchronisierung (siehe [Standard Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights) ).</span><span class="sxs-lookup"><span data-stu-id="e502a-126">To perform all administrative tasks and basic printing operations except for SYNCHRONIZE (see [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights) ).</span></span>                                   |
| <span data-ttu-id="e502a-127">generische Sicherheitswerte, z. b. \_ DAC schreiben</span><span class="sxs-lookup"><span data-stu-id="e502a-127">generic security values, such as WRITE\_DAC</span></span> | <span data-ttu-id="e502a-128">, Um bestimmte Zugriffsrechte für das Steuerelement zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="e502a-128">To allow specific control access rights.</span></span> <span data-ttu-id="e502a-129">Siehe [Standard Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="e502a-129">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                                                                      |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e502a-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e502a-130">Requirements</span></span>



| <span data-ttu-id="e502a-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e502a-131">Requirement</span></span> | <span data-ttu-id="e502a-132">Wert</span><span class="sxs-lookup"><span data-stu-id="e502a-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e502a-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e502a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e502a-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e502a-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e502a-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e502a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e502a-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e502a-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e502a-137">Header</span><span class="sxs-lookup"><span data-stu-id="e502a-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="e502a-138"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e502a-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e502a-139">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="e502a-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e502a-140">**\_ Drucker \_ defaultsw** (Unicode) und **\_ Drucker \_ defaultsa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e502a-140">**\_PRINTER\_DEFAULTSW** (Unicode) and **\_PRINTER\_DEFAULTSA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="e502a-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e502a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e502a-142">Drucken</span><span class="sxs-lookup"><span data-stu-id="e502a-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e502a-143">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="e502a-143">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="e502a-144">**Deleteprinter**</span><span class="sxs-lookup"><span data-stu-id="e502a-144">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="e502a-145">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="e502a-145">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="e502a-146">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="e502a-146">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="e502a-147">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="e502a-147">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

