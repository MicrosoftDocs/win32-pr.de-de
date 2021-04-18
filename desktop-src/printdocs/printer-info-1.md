---
description: Die Struktur der Drucker \_ Info \_ 1 gibt allgemeine Drucker Informationen an.
ms.assetid: 0b0e2d0e-2625-4cab-a8f9-536185479443
title: PRINTER_INFO_1 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_1
- _PRINTER_INFO_1A
- _PRINTER_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: cbeff42a9125331c45ffd8bbbee5758fd864648c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351752"
---
# <a name="printer_info_1-structure"></a><span data-ttu-id="551a8-103">Drucker \_ Info \_ 1-Struktur</span><span class="sxs-lookup"><span data-stu-id="551a8-103">PRINTER\_INFO\_1 structure</span></span>

<span data-ttu-id="551a8-104">Die Struktur der **Drucker \_ Info \_ 1** gibt allgemeine Drucker Informationen an.</span><span class="sxs-lookup"><span data-stu-id="551a8-104">The **PRINTER\_INFO\_1** structure specifies general printer information.</span></span>

## <a name="syntax"></a><span data-ttu-id="551a8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="551a8-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_1 {
  DWORD  Flags;
  LPTSTR pDescription;
  LPTSTR pName;
  LPTSTR pComment;
} PRINTER_INFO_1, *PPRINTER_INFO_1;
```



## <a name="members"></a><span data-ttu-id="551a8-106">Member</span><span class="sxs-lookup"><span data-stu-id="551a8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="551a8-107">**Flags**</span><span class="sxs-lookup"><span data-stu-id="551a8-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="551a8-108">Gibt Informationen zu den zurückgegebenen Daten an.</span><span class="sxs-lookup"><span data-stu-id="551a8-108">Specifies information about the returned data.</span></span> <span data-ttu-id="551a8-109">Im folgenden finden Sie die Werte für diesen Member.</span><span class="sxs-lookup"><span data-stu-id="551a8-109">Following are the values for this member.</span></span>



| <span data-ttu-id="551a8-110">Wert</span><span class="sxs-lookup"><span data-stu-id="551a8-110">Value</span></span>                    | <span data-ttu-id="551a8-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="551a8-111">Meaning</span></span>                                                                                                                                                                                                                                                   |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="551a8-112">Druckeraufzählung \_ \_ erweitern</span><span class="sxs-lookup"><span data-stu-id="551a8-112">PRINTER\_ENUM\_EXPAND</span></span>    | <span data-ttu-id="551a8-113">Ein Druckanbieter kann dieses Flag als Hinweis auf eine aufrufende Anwendung festlegen, um dieses Objekt weiter aufzuzählen, wenn die Standard Erweiterung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="551a8-113">A print provider can set this flag as a hint to a calling application to enumerate this object further if default expansion is enabled.</span></span> <span data-ttu-id="551a8-114">Wenn z. b. Domänen aufgelistet werden, kann ein Druckanbieter die Domäne des Benutzers angeben, indem dieses Flag festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="551a8-114">For example, when domains are enumerated, a print provider might indicate the user's domain by setting this flag.</span></span> |
| <span data-ttu-id="551a8-115">druckeraufzählungs \_ \_ Container</span><span class="sxs-lookup"><span data-stu-id="551a8-115">PRINTER\_ENUM\_CONTAINER</span></span> | <span data-ttu-id="551a8-116">Wenn dieses Flag festgelegt ist, kann das Drucker Objekt Aufzähl Bare-Objekte enthalten.</span><span class="sxs-lookup"><span data-stu-id="551a8-116">If this flag is set, the printer object may contain enumerable objects.</span></span> <span data-ttu-id="551a8-117">Beispielsweise kann das Objekt ein Druckserver sein, der Drucker enthält.</span><span class="sxs-lookup"><span data-stu-id="551a8-117">For example, the object may be a print server that contains printers.</span></span>                                                                                                             |
| <span data-ttu-id="551a8-118">Druckeraufzählung \_ \_ ICON1</span><span class="sxs-lookup"><span data-stu-id="551a8-118">PRINTER\_ENUM\_ICON1</span></span>     | <span data-ttu-id="551a8-119">Gibt an, dass eine Anwendung ggf. ein Symbol anzeigt, das das Objekt als Netzwerknamen der obersten Ebene (z. b. Microsoft Windows-Netzwerk) identifiziert.</span><span class="sxs-lookup"><span data-stu-id="551a8-119">Indicates that, where appropriate, an application should display an icon identifying the object as a top-level network name, such as Microsoft Windows Network.</span></span>                                                                                           |
| <span data-ttu-id="551a8-120">Druckeraufzählung \_ \_ icon2</span><span class="sxs-lookup"><span data-stu-id="551a8-120">PRINTER\_ENUM\_ICON2</span></span>     | <span data-ttu-id="551a8-121">Gibt an, dass eine Anwendung ggf. ein Symbol anzeigt, das das Objekt als Netzwerk Domäne identifiziert.</span><span class="sxs-lookup"><span data-stu-id="551a8-121">Indicates that, where appropriate, an application should display an icon that identifies the object as a network domain.</span></span>                                                                                                                                  |
| <span data-ttu-id="551a8-122">Druckeraufzählung \_ \_ ICON3</span><span class="sxs-lookup"><span data-stu-id="551a8-122">PRINTER\_ENUM\_ICON3</span></span>     | <span data-ttu-id="551a8-123">Gibt an, dass eine Anwendung ggf. ein Symbol anzeigt, das das Objekt als Druckserver identifiziert.</span><span class="sxs-lookup"><span data-stu-id="551a8-123">Indicates that, where appropriate, an application should display an icon that identifies the object as a print server.</span></span>                                                                                                                                    |
| <span data-ttu-id="551a8-124">Druckeraufzählung \_ \_ ICON4</span><span class="sxs-lookup"><span data-stu-id="551a8-124">PRINTER\_ENUM\_ICON4</span></span>     | <span data-ttu-id="551a8-125">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="551a8-125">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="551a8-126">Druckeraufzählung \_ \_ ICON5</span><span class="sxs-lookup"><span data-stu-id="551a8-126">PRINTER\_ENUM\_ICON5</span></span>     | <span data-ttu-id="551a8-127">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="551a8-127">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="551a8-128">Druckeraufzählung \_ \_ ICON6</span><span class="sxs-lookup"><span data-stu-id="551a8-128">PRINTER\_ENUM\_ICON6</span></span>     | <span data-ttu-id="551a8-129">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="551a8-129">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="551a8-130">Druckeraufzählung \_ \_ ICON7</span><span class="sxs-lookup"><span data-stu-id="551a8-130">PRINTER\_ENUM\_ICON7</span></span>     | <span data-ttu-id="551a8-131">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="551a8-131">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="551a8-132">Druckeraufzählung \_ \_ ICON8</span><span class="sxs-lookup"><span data-stu-id="551a8-132">PRINTER\_ENUM\_ICON8</span></span>     | <span data-ttu-id="551a8-133">Gibt an, dass eine Anwendung ggf. ein Symbol anzeigt, das das Objekt als Drucker bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="551a8-133">Indicates that, where appropriate, an application should display an icon that identifies the object as a printer.</span></span>                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="551a8-134">**pdescription**</span><span class="sxs-lookup"><span data-stu-id="551a8-134">**pDescription**</span></span>
</dt> <dd>

<span data-ttu-id="551a8-135">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Inhalt der-Struktur beschreibt.</span><span class="sxs-lookup"><span data-stu-id="551a8-135">Pointer to a null-terminated string that describes the contents of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="551a8-136">**pName**</span><span class="sxs-lookup"><span data-stu-id="551a8-136">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="551a8-137">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Inhalt der-Struktur benennt.</span><span class="sxs-lookup"><span data-stu-id="551a8-137">Pointer to a null-terminated string that names the contents of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="551a8-138">**pcomment**</span><span class="sxs-lookup"><span data-stu-id="551a8-138">**pComment**</span></span>
</dt> <dd>

<span data-ttu-id="551a8-139">Zeiger auf eine mit NULL endenden Zeichenfolge, die zusätzliche Daten enthält, die die Struktur beschreiben.</span><span class="sxs-lookup"><span data-stu-id="551a8-139">Pointer to a null-terminated string that contains additional data describing the structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="551a8-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="551a8-140">Requirements</span></span>



| <span data-ttu-id="551a8-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="551a8-141">Requirement</span></span> | <span data-ttu-id="551a8-142">Wert</span><span class="sxs-lookup"><span data-stu-id="551a8-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="551a8-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="551a8-143">Minimum supported client</span></span><br/> | <span data-ttu-id="551a8-144">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="551a8-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="551a8-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="551a8-145">Minimum supported server</span></span><br/> | <span data-ttu-id="551a8-146">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="551a8-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="551a8-147">Header</span><span class="sxs-lookup"><span data-stu-id="551a8-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="551a8-148"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="551a8-148"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="551a8-149">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="551a8-149">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="551a8-150">**\_ Drucker \_ Info \_ 1W** (Unicode) und **\_ Drucker \_ Info \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="551a8-150">**\_PRINTER\_INFO\_1W** (Unicode) and **\_PRINTER\_INFO\_1A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="551a8-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="551a8-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="551a8-152">Drucken</span><span class="sxs-lookup"><span data-stu-id="551a8-152">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="551a8-153">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="551a8-153">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="551a8-154">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="551a8-154">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="551a8-155">**Enumdrucker**</span><span class="sxs-lookup"><span data-stu-id="551a8-155">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="551a8-156">**Drucker \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="551a8-156">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="551a8-157">**Drucker \_ Informationen \_ 3**</span><span class="sxs-lookup"><span data-stu-id="551a8-157">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="551a8-158">**Drucker \_ Info \_ 4**</span><span class="sxs-lookup"><span data-stu-id="551a8-158">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> </dl>

 

 




