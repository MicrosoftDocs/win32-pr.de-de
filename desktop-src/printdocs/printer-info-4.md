---
description: Die Drucker \_ Info \_ 4-Struktur gibt allgemeine Drucker Informationen an. Die-Struktur kann verwendet werden, um beim Aufrufen von enumdruckern minimale Drucker Informationen abzurufen.
ms.assetid: 81bd0eab-dc1e-4cf1-8f63-3686f1711c1f
title: PRINTER_INFO_4 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_4
- _PRINTER_INFO_4A
- _PRINTER_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 9a1501008f0235ea303dd1457fc8756c28abc21c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217390"
---
# <a name="printer_info_4-structure"></a><span data-ttu-id="232c3-103">Drucker \_ Info \_ 4-Struktur</span><span class="sxs-lookup"><span data-stu-id="232c3-103">PRINTER\_INFO\_4 structure</span></span>

<span data-ttu-id="232c3-104">Die **Drucker \_ Info \_ 4** -Struktur gibt allgemeine Drucker Informationen an.</span><span class="sxs-lookup"><span data-stu-id="232c3-104">The **PRINTER\_INFO\_4** structure specifies general printer information.</span></span>

<span data-ttu-id="232c3-105">Die-Struktur kann verwendet werden, um beim Aufrufen von [**enumdruckern**](enumprinters.md)minimale Drucker Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="232c3-105">The structure can be used to retrieve minimal printer information on a call to [**EnumPrinters**](enumprinters.md).</span></span> <span data-ttu-id="232c3-106">Ein solcher Rückruf ist eine schnelle und einfache Möglichkeit zum Abrufen der Namen und Attribute aller lokal installierten Drucker auf einem System und aller Remote Drucker Verbindungen, die ein Benutzer eingerichtet hat.</span><span class="sxs-lookup"><span data-stu-id="232c3-106">Such a call is a fast and easy way to retrieve the names and attributes of all locally installed printers on a system and all remote printer connections that a user has established.</span></span>

## <a name="syntax"></a><span data-ttu-id="232c3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="232c3-107">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_4 {
  LPTSTR pPrinterName;
  LPTSTR pServerName;
  DWORD  Attributes;
} PRINTER_INFO_4, *PPRINTER_INFO_4;
```



## <a name="members"></a><span data-ttu-id="232c3-108">Member</span><span class="sxs-lookup"><span data-stu-id="232c3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="232c3-109">**pprintername**</span><span class="sxs-lookup"><span data-stu-id="232c3-109">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="232c3-110">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Druckers angibt (lokal oder Remote).</span><span class="sxs-lookup"><span data-stu-id="232c3-110">Pointer to a null-terminated string that specifies the name of the printer (local or remote).</span></span>

</dd> <dt>

<span data-ttu-id="232c3-111">**pservername**</span><span class="sxs-lookup"><span data-stu-id="232c3-111">**pServerName**</span></span>
</dt> <dd>

<span data-ttu-id="232c3-112">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Servers ist.</span><span class="sxs-lookup"><span data-stu-id="232c3-112">Pointer to a null-terminated string that is the name of the server.</span></span>

</dd> <dt>

<span data-ttu-id="232c3-113">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="232c3-113">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="232c3-114">Gibt Informationen zu den zurückgegebenen Daten an.</span><span class="sxs-lookup"><span data-stu-id="232c3-114">Specifies information about the returned data.</span></span>



| <span data-ttu-id="232c3-115">Wert</span><span class="sxs-lookup"><span data-stu-id="232c3-115">Value</span></span>                       | <span data-ttu-id="232c3-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="232c3-116">Meaning</span></span>                          |
|-----------------------------|----------------------------------|
| <span data-ttu-id="232c3-117">Drucker \_ Attribut \_ lokal</span><span class="sxs-lookup"><span data-stu-id="232c3-117">PRINTER\_ATTRIBUTE\_LOCAL</span></span>   | <span data-ttu-id="232c3-118">Der Drucker ist ein lokaler Drucker.</span><span class="sxs-lookup"><span data-stu-id="232c3-118">The printer is a local printer.</span></span>  |
| <span data-ttu-id="232c3-119">Drucker \_ Attribut \_ Netzwerk</span><span class="sxs-lookup"><span data-stu-id="232c3-119">PRINTER\_ATTRIBUTE\_NETWORK</span></span> | <span data-ttu-id="232c3-120">Der Drucker ist ein Remote Drucker.</span><span class="sxs-lookup"><span data-stu-id="232c3-120">The printer is a remote printer.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="232c3-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="232c3-121">Remarks</span></span>

<span data-ttu-id="232c3-122">Die **Drucker \_ Info \_ 4** -Struktur bietet eine einfache und äußerst schnelle Möglichkeit, die Namen der Drucker, die auf einem lokalen Computer installiert sind, sowie die von einem Benutzer eingerichteten Remote Verbindungen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="232c3-122">The **PRINTER\_INFO\_4** structure provides an easy and extremely fast way to retrieve the names of the printers installed on a local machine, as well as the remote connections that a user has established.</span></span> <span data-ttu-id="232c3-123">Wenn [**enumprinter**](enumprinters.md) mit einer Datenstruktur vom Typ " **Printer \_ Info \_ 4** " aufgerufen wird, fragt diese Funktion die Registrierung nach den angegebenen Informationen ab und wird dann sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="232c3-123">When [**EnumPrinters**](enumprinters.md) is called with a **PRINTER\_INFO\_4** data structure, that function queries the registry for the specified information, then returns immediately.</span></span> <span data-ttu-id="232c3-124">Dies unterscheidet sich vom Verhalten von **enumdruckern** , wenn es mit anderen Ebenen von **Drucker \_ Informationen \_ xxx** -Datenstrukturen aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="232c3-124">This differs from the behavior of **EnumPrinters** when called with other levels of **PRINTER\_INFO\_xxx** data structures.</span></span> <span data-ttu-id="232c3-125">Insbesondere, wenn **enumprinter** mit einer Datenstruktur der Ebene 2 (**Printer \_ Info \_ 2** ) aufgerufen wird, führt Sie einen **OpenPrinter** -Aufruf für jede Remote Verbindung aus.</span><span class="sxs-lookup"><span data-stu-id="232c3-125">In particular, when **EnumPrinters** is called with a level 2 (**PRINTER\_INFO\_2** ) data structure, it performs an **OpenPrinter** call on each remote connection.</span></span> <span data-ttu-id="232c3-126">Wenn eine Remote Verbindung nicht mehr vorhanden ist, wenn der Remote Server nicht mehr vorhanden ist oder der Remote Drucker nicht mehr vorhanden ist, muss die Funktion auf das Timeout von RPC warten und somit den **OpenPrinter** -Aufruf fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="232c3-126">If a remote connection is down, if the remote server no longer exists, or if the remote printer no longer exists, the function must wait for RPC to time out and consequently fail the **OpenPrinter** call.</span></span> <span data-ttu-id="232c3-127">Dies kann eine Weile dauern.</span><span class="sxs-lookup"><span data-stu-id="232c3-127">This can take a while.</span></span> <span data-ttu-id="232c3-128">Durch die Übergabe einer **Drucker \_ Info \_ 4** -Struktur kann eine Anwendung ein Minimum an erforderlichen Informationen abrufen. wenn ausführlichere Informationen gewünscht werden, kann ein nachfolgende **aufrufergrad** 2 aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="232c3-128">Passing a **PRINTER\_INFO\_4** structure lets an application retrieve a bare minimum of required information; if more detailed information is desired, a subsequent **EnumPrinter** level 2 call can be made.</span></span>

<span data-ttu-id="232c3-129">**Attribute** können auch Werte enthalten, die im Feld **Attribute** von **Printer \_ Info \_ 2** definiert sind.</span><span class="sxs-lookup"><span data-stu-id="232c3-129">**Attributes** can also contain values that are defined in the **Attributes** field of **PRINTER\_INFO\_2**.</span></span>

<span data-ttu-id="232c3-130">Einige Drucker Konfigurationen, wie z. b. Drucker Verbindungen mit einigen nicht auf Windows basierenden Druckservern, geben möglicherweise sowohl das **\_ \_ lokale Drucker Attribut** als auch das **Drucker Attribut \_ \_ Netzwerk** zurück.</span><span class="sxs-lookup"><span data-stu-id="232c3-130">Some printer configurations, such as printer connections to some non-Windows-based print servers, might return both **PRINTER\_ATTRIBUTE\_LOCAL** and **PRINTER\_ATTRIBUTE\_NETWORK**.</span></span>

## <a name="requirements"></a><span data-ttu-id="232c3-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="232c3-131">Requirements</span></span>



| <span data-ttu-id="232c3-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="232c3-132">Requirement</span></span> | <span data-ttu-id="232c3-133">Wert</span><span class="sxs-lookup"><span data-stu-id="232c3-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="232c3-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="232c3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="232c3-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="232c3-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="232c3-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="232c3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="232c3-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="232c3-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="232c3-138">Header</span><span class="sxs-lookup"><span data-stu-id="232c3-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="232c3-139"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="232c3-139"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="232c3-140">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="232c3-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="232c3-141">**\_ Drucker \_ Info \_ 4W** (Unicode) und **\_ Drucker \_ Info \_ 4a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="232c3-141">**\_PRINTER\_INFO\_4W** (Unicode) and **\_PRINTER\_INFO\_4A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="232c3-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="232c3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="232c3-143">Drucken</span><span class="sxs-lookup"><span data-stu-id="232c3-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="232c3-144">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="232c3-144">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="232c3-145">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="232c3-145">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="232c3-146">**Enumdrucker**</span><span class="sxs-lookup"><span data-stu-id="232c3-146">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="232c3-147">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="232c3-147">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="232c3-148">**Drucker \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="232c3-148">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="232c3-149">**Drucker \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="232c3-149">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="232c3-150">**Drucker \_ Informationen \_ 3**</span><span class="sxs-lookup"><span data-stu-id="232c3-150">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> </dl>

 

 




