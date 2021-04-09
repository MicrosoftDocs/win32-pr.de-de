---
description: Die enumprinter-Funktion Listet verfügbare Drucker, Druckserver, Domänen oder Druckanbieter auf.
ms.assetid: 0d0cc726-c515-4146-9273-cdf1db3c76b7
title: Enumprinter-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinters
- EnumPrintersA
- EnumPrintersW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 6d82e8e6ff4f56a3c67fa29c48e982ebe0fd4599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864971"
---
# <a name="enumprinters-function"></a><span data-ttu-id="9f24d-103">Enumprinter-Funktion</span><span class="sxs-lookup"><span data-stu-id="9f24d-103">EnumPrinters function</span></span>

<span data-ttu-id="9f24d-104">Die **enumprinter** -Funktion Listet verfügbare Drucker, Druckserver, Domänen oder Druckanbieter auf.</span><span class="sxs-lookup"><span data-stu-id="9f24d-104">The **EnumPrinters** function enumerates available printers, print servers, domains, or print providers.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f24d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f24d-105">Syntax</span></span>


```C++
BOOL EnumPrinters(
  _In_  DWORD   Flags,
  _In_  LPTSTR  Name,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinterEnum,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="9f24d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f24d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f24d-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="9f24d-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f24d-108">Die Typen von Druck Objekten, die von der Funktion aufgelistet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9f24d-108">The types of print objects that the function should enumerate.</span></span> <span data-ttu-id="9f24d-109">Dieser Wert kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9f24d-109">This value can be one or more of the following values.</span></span>



| <span data-ttu-id="9f24d-110">Wert</span><span class="sxs-lookup"><span data-stu-id="9f24d-110">Value</span></span>                                                                                                                                                                                               | <span data-ttu-id="9f24d-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9f24d-111">Meaning</span></span>                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_ENUM_LOCAL"></span><span id="printer_enum_local"></span><dl> <span data-ttu-id="9f24d-112"><dt>**Drucker-Aufzählung \_ \_ lokal**</dt></span><span class="sxs-lookup"><span data-stu-id="9f24d-112"><dt>**PRINTER\_ENUM\_LOCAL**</dt></span></span> </dl>                       | <span data-ttu-id="9f24d-113">Wenn das \_ \_ druckerenumerationsnamensflag nicht ebenfalls übergeben wird, ignoriert die Funktion den *Name* -Parameter und listet die lokal installierten Drucker auf.</span><span class="sxs-lookup"><span data-stu-id="9f24d-113">If the PRINTER\_ENUM\_NAME flag is not also passed, the function ignores the *Name* parameter, and enumerates the locally installed printers.</span></span> <span data-ttu-id="9f24d-114">Wenn \_ \_ der druckerenumerationsname ebenfalls überschritten wird, listet die Funktion die lokalen Drucker unter *Name* auf.</span><span class="sxs-lookup"><span data-stu-id="9f24d-114">If PRINTER\_ENUM\_NAME is also passed, the function enumerates the local printers on *Name*.</span></span> <br/> |
| <span id="PRINTER_ENUM_NAME"></span><span id="printer_enum_name"></span><dl> <span data-ttu-id="9f24d-115"><dt>**\_Name der druckerenum \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9f24d-115"><dt>**PRINTER\_ENUM\_NAME**</dt></span></span> </dl>                          | <span data-ttu-id="9f24d-116">Die-Funktion Listet den durch den *Namen* identifizierten Drucker auf.</span><span class="sxs-lookup"><span data-stu-id="9f24d-116">The function enumerates the printer identified by *Name*.</span></span> <span data-ttu-id="9f24d-117">Dabei kann es sich um einen Server, eine Domäne oder einen Druckanbieter handeln.</span><span class="sxs-lookup"><span data-stu-id="9f24d-117">This can be a server, a domain, or a print provider.</span></span> <span data-ttu-id="9f24d-118">Wenn *Name* den Wert **null** hat, listet die Funktion verfügbare Druckanbieter auf.</span><span class="sxs-lookup"><span data-stu-id="9f24d-118">If *Name* is **NULL**, the function enumerates available print providers.</span></span><br/>                                                    |
| <span id="PRINTER_ENUM_SHARED"></span><span id="printer_enum_shared"></span><dl> <span data-ttu-id="9f24d-119"><dt>**Drucker-Aufzählung frei \_ \_ gegeben**</dt></span><span class="sxs-lookup"><span data-stu-id="9f24d-119"><dt>**PRINTER\_ENUM\_SHARED**</dt></span></span> </dl>                    | <span data-ttu-id="9f24d-120">Die-Funktion Listet Drucker auf, die über das Shared-Attribut verfügen.</span><span class="sxs-lookup"><span data-stu-id="9f24d-120">The function enumerates printers that have the shared attribute.</span></span> <span data-ttu-id="9f24d-121">Kann nicht isoliert verwendet werden; Verwenden Sie eine OR-Operation, um einen anderen druckeraufgabentyp zu verwenden \_ .</span><span class="sxs-lookup"><span data-stu-id="9f24d-121">Cannot be used in isolation; use an OR operation to combine with another PRINTER\_ENUM type.</span></span><br/>                                                                               |
| <span id="PRINTER_ENUM_CONNECTIONS"></span><span id="printer_enum_connections"></span><dl> <span data-ttu-id="9f24d-122"><dt>**Drucker-Aufzählungs \_ \_ Verbindungen**</dt></span><span class="sxs-lookup"><span data-stu-id="9f24d-122"><dt>**PRINTER\_ENUM\_CONNECTIONS**</dt></span></span> </dl>     | <span data-ttu-id="9f24d-123">Mit der-Funktion wird die Liste der Drucker aufgelistet, auf die der Benutzer vorherige Verbindungen hergestellt hat.</span><span class="sxs-lookup"><span data-stu-id="9f24d-123">The function enumerates the list of printers to which the user has made previous connections.</span></span><br/>                                                                                                                                               |
| <span id="PRINTER_ENUM_NETWORK"></span><span id="printer_enum_network"></span><dl> <span data-ttu-id="9f24d-124"><dt>**Drucker-Aufzählungs \_ \_ Netzwerk**</dt></span><span class="sxs-lookup"><span data-stu-id="9f24d-124"><dt>**PRINTER\_ENUM\_NETWORK**</dt></span></span> </dl>                 | <span data-ttu-id="9f24d-125">Die-Funktion Listet Netzwerkdrucker in der Domäne des Computers auf.</span><span class="sxs-lookup"><span data-stu-id="9f24d-125">The function enumerates network printers in the computer's domain.</span></span> <span data-ttu-id="9f24d-126">Dieser Wert ist nur gültig, wenn *Level* 1 ist.</span><span class="sxs-lookup"><span data-stu-id="9f24d-126">This value is valid only if *Level* is 1.</span></span><br/>                                                                                                                                |
| <span id="PRINTER_ENUM_REMOTE"></span><span id="printer_enum_remote"></span><dl> <span data-ttu-id="9f24d-127"><dt>**druckeraufzählungs \_ \_ Remote**</dt></span><span class="sxs-lookup"><span data-stu-id="9f24d-127"><dt>**PRINTER\_ENUM\_REMOTE**</dt></span></span> </dl>                    | <span data-ttu-id="9f24d-128">Die-Funktion Listet Netzwerkdrucker und Drucker Server in der Domäne des Computers auf.</span><span class="sxs-lookup"><span data-stu-id="9f24d-128">The function enumerates network printers and print servers in the computer's domain.</span></span> <span data-ttu-id="9f24d-129">Dieser Wert ist nur gültig, wenn *Level* 1 ist.</span><span class="sxs-lookup"><span data-stu-id="9f24d-129">This value is valid only if *Level* is 1.</span></span><br/>                                                                                                              |
| <span id="PRINTER_ENUM_CATEGORY_3D"></span><span id="printer_enum_category_3d"></span><dl> <span data-ttu-id="9f24d-130"><dt>**\_Druckerenum \_ \_ -Kategorie 3D**</dt></span><span class="sxs-lookup"><span data-stu-id="9f24d-130"><dt>**PRINTER\_ENUM\_CATEGORY\_3D**</dt></span></span> </dl>    | <span data-ttu-id="9f24d-131">Die-Funktion Listet nur 3D-Drucker auf.</span><span class="sxs-lookup"><span data-stu-id="9f24d-131">The function enumerates only 3D printers.</span></span><br/>                                                                                                                                                                                                   |
| <span id="PRINTER_ENUM_CATEGORY_ALL"></span><span id="printer_enum_category_all"></span><dl> <span data-ttu-id="9f24d-132"><dt>**\_druckerenum- \_ Kategorie \_ alle**</dt></span><span class="sxs-lookup"><span data-stu-id="9f24d-132"><dt>**PRINTER\_ENUM\_CATEGORY\_ALL**</dt></span></span> </dl> | <span data-ttu-id="9f24d-133">Die-Funktion Listet alle Druckgeräte auf, einschließlich 3D-Druckern.</span><span class="sxs-lookup"><span data-stu-id="9f24d-133">The function enumerates all print devices, including 3D printers.</span></span><br/>                                                                                                                                                                           |



 

<span data-ttu-id="9f24d-134">Wenn *Level den Wert* 4 hat, können Sie nur die Drucker-enumerationsverbindungen \_ und die lokalen Drucker Enumerationskonstanten verwenden \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9f24d-134">If *Level* is 4, you can only use the PRINTER\_ENUM\_CONNECTIONS and PRINTER\_ENUM\_LOCAL constants.</span></span>

> [!Note]  
> <span data-ttu-id="9f24d-135">3D-Druckgeräte werden standardmäßig nicht aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9f24d-135">3D print devices are not enumerated by default.</span></span> <span data-ttu-id="9f24d-136">Sie müssen die beiden **\_ druckerenum \_ \_ -Kategorie 3D** und die Drucker Enumeration **\_ \_ local** einschließen, um nur 3D-Drucker aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="9f24d-136">You must include both **PRINTER\_ENUM\_CATEGORY\_3D** and **PRINTER\_ENUM\_LOCAL** to enumerate only 3D printers.</span></span> <span data-ttu-id="9f24d-137">Wenn Sie 3D-Drucker zusammen mit allen anderen lokalen Druckern einschließen möchten, verwenden Sie die **\_ druckerenum- \_ Kategorie \_ all** und **Printer \_ Enum \_ local**.</span><span class="sxs-lookup"><span data-stu-id="9f24d-137">To include 3D printers, along with all other local printers, use **PRINTER\_ENUM\_CATEGORY\_ALL** and **PRINTER\_ENUM\_LOCAL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="9f24d-138">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f24d-138">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f24d-139">Wenn *die Ebene* 1 ist *, Flags* \_ \_ den druckerenumerationsnamen und der *Name* ungleich **null** sind, ist *Name* ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des aufzuzählenden Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="9f24d-139">If *Level* is 1, *Flags* contains PRINTER\_ENUM\_NAME, and *Name* is non-**NULL**, then *Name* is a pointer to a null-terminated string that specifies the name of the object to enumerate.</span></span> <span data-ttu-id="9f24d-140">Diese Zeichenfolge kann der Name eines Servers, einer Domäne oder eines Druck Anbieters sein.</span><span class="sxs-lookup"><span data-stu-id="9f24d-140">This string can be the name of a server, a domain, or a print provider.</span></span>

<span data-ttu-id="9f24d-141">Wenn *Level* 1 ist, enthält *Flags* \_ den druckerenumerationsnamen \_ , und der *Name* ist **null**. die Funktion Listet die verfügbaren Druckanbieter auf.</span><span class="sxs-lookup"><span data-stu-id="9f24d-141">If *Level* is 1, *Flags* contains PRINTER\_ENUM\_NAME, and *Name* is **NULL**, then the function enumerates the available print providers.</span></span>

<span data-ttu-id="9f24d-142">Wenn die *Ebene* 1 ist, enthält *Flags* die Drucker \_ \_ -enumerationsremote, und der *Name* ist **null**. anschließend listet die Funktion die Drucker in der Domäne des Benutzers auf.</span><span class="sxs-lookup"><span data-stu-id="9f24d-142">If *Level* is 1, *Flags* contains PRINTER\_ENUM\_REMOTE, and *Name* is **NULL**, then the function enumerates the printers in the user's domain.</span></span>

<span data-ttu-id="9f24d-143">Wenn *Level* 2 oder 5 ist, ist *Name* ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen eines Servers angibt, dessen Drucker aufgelistet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9f24d-143">If *Level* is 2 or 5,*Name* is a pointer to a null-terminated string that specifies the name of a server whose printers are to be enumerated.</span></span> <span data-ttu-id="9f24d-144">Wenn diese Zeichenfolge **null** ist, listet die Funktion die auf dem lokalen Computer installierten Drucker auf.</span><span class="sxs-lookup"><span data-stu-id="9f24d-144">If this string is **NULL**, then the function enumerates the printers installed on the local computer.</span></span>

<span data-ttu-id="9f24d-145">Wenn die *Ebene* 4 ist, muss der *Name* **null** sein.</span><span class="sxs-lookup"><span data-stu-id="9f24d-145">If *Level* is 4, *Name* should be **NULL**.</span></span> <span data-ttu-id="9f24d-146">Die Funktion fragt immer auf dem lokalen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="9f24d-146">The function always queries on the local computer.</span></span>

<span data-ttu-id="9f24d-147">Wenn *Name* den Wert **null** hat, werden die  \_ \_ \| \_ \_ auf dem lokalen Computer installierten Drucker durch Festlegen von Flags für die Drucker Enumeration lokale Drucker enumerationsverbindungen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9f24d-147">When *Name* is **NULL**, setting *Flags* to PRINTER\_ENUM\_LOCAL \| PRINTER\_ENUM\_CONNECTIONS enumerates printers that are installed on the local machine.</span></span> <span data-ttu-id="9f24d-148">Zu diesen Druckern gehören diejenigen, die physisch mit dem lokalen Computer verbunden sind, sowie Remote Drucker, an die Sie über eine Netzwerkverbindung verfügen.</span><span class="sxs-lookup"><span data-stu-id="9f24d-148">These printers include those that are physically attached to the local machine as well as remote printers to which it has a network connection.</span></span>

<span data-ttu-id="9f24d-149">Wenn *Name* nicht **null** ist, werden  \_ \_ \| \_ \_ die lokalen Drucker, die auf dem Server *Namen* installiert sind, durch Festlegen von Flags auf den Drucker enumerationsenum-Namen des lokalen Druckers aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9f24d-149">When *Name* is not **NULL**, setting *Flags* to PRINTER\_ENUM\_LOCAL \| PRINTER\_ENUM\_NAME enumerates the local printers that are installed on the server *Name*.</span></span>

</dd> <dt>

<span data-ttu-id="9f24d-150">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f24d-150">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f24d-151">Der Typ der Datenstrukturen, auf die von *pprinterenum* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="9f24d-151">The type of data structures pointed to by *pPrinterEnum*.</span></span> <span data-ttu-id="9f24d-152">Gültige Werte sind 1, 2, 4 und 5. diese entsprechen den Datenstrukturen " [**Printer Info \_ \_ 1**](printer-info-1.md)", "Printer Info [**\_ \_ 2**](printer-info-2.md) ", "Printer Info [**\_ \_ 4**](printer-info-4.md)" und " [**Printer \_ Info \_ 5**](printer-info-5.md) ".</span><span class="sxs-lookup"><span data-stu-id="9f24d-152">Valid values are 1, 2, 4, and 5, which correspond to the [**PRINTER\_INFO\_1**](printer-info-1.md), [**PRINTER\_INFO\_2**](printer-info-2.md) , [**PRINTER\_INFO\_4**](printer-info-4.md), and [**PRINTER\_INFO\_5**](printer-info-5.md) data structures.</span></span>

<span data-ttu-id="9f24d-153">Dieser Wert kann 1, 2, 4 oder 5 sein.</span><span class="sxs-lookup"><span data-stu-id="9f24d-153">This value can be 1, 2, 4, or 5.</span></span>

</dd> <dt>

<span data-ttu-id="9f24d-154">*pprinteraufumum* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9f24d-154">*pPrinterEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f24d-155">Ein Zeiger auf einen Puffer, der ein Array von [**Druckern \_ Info \_ 1**](printer-info-1.md), [**Printer \_ Info \_ 2**](printer-info-2.md), [**Printer \_ Info \_ 4**](printer-info-4.md)oder [**Printer \_ Info \_ 5**](printer-info-5.md) -Strukturen empfängt.</span><span class="sxs-lookup"><span data-stu-id="9f24d-155">A pointer to a buffer that receives an array of [**PRINTER\_INFO\_1**](printer-info-1.md), [**PRINTER\_INFO\_2**](printer-info-2.md), [**PRINTER\_INFO\_4**](printer-info-4.md), or [**PRINTER\_INFO\_5**](printer-info-5.md) structures.</span></span> <span data-ttu-id="9f24d-156">Jede Struktur enthält Daten, die ein verfügbares Druckobjekt beschreiben.</span><span class="sxs-lookup"><span data-stu-id="9f24d-156">Each structure contains data that describes an available print object.</span></span>

<span data-ttu-id="9f24d-157">Wenn *Level* 1 ist, enthält das Array [**Drucker \_ Informationen \_ 1**](printer-info-1.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="9f24d-157">If *Level* is 1, the array contains [**PRINTER\_INFO\_1**](printer-info-1.md) structures.</span></span> <span data-ttu-id="9f24d-158">Wenn *Level* 2 ist, enthält das Array [**Drucker \_ Informationen \_ 2**](printer-info-2.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="9f24d-158">If *Level* is 2, the array contains [**PRINTER\_INFO\_2**](printer-info-2.md) structures.</span></span> <span data-ttu-id="9f24d-159">Wenn *Level* 4 ist, enthält das Array [**Drucker \_ Info \_ 4**](printer-info-4.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="9f24d-159">If *Level* is 4, the array contains [**PRINTER\_INFO\_4**](printer-info-4.md) structures.</span></span> <span data-ttu-id="9f24d-160">Wenn *Level* 5 ist, enthält das Array [**Drucker \_ Informationen \_ 5**](printer-info-5.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="9f24d-160">If *Level* is 5, the array contains [**PRINTER\_INFO\_5**](printer-info-5.md) structures.</span></span>

<span data-ttu-id="9f24d-161">Der Puffer muss groß genug sein, um das Array von Datenstrukturen und Zeichen folgen oder andere Daten zu empfangen, auf die die Strukturmember zeigen.</span><span class="sxs-lookup"><span data-stu-id="9f24d-161">The buffer must be large enough to receive the array of data structures and any strings or other data to which the structure members point.</span></span> <span data-ttu-id="9f24d-162">Wenn der Puffer zu klein ist, gibt der Parameter *pcbrequired* die erforderliche Puffergröße zurück.</span><span class="sxs-lookup"><span data-stu-id="9f24d-162">If the buffer is too small, the *pcbNeeded* parameter returns the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="9f24d-163">*cbbuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f24d-163">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f24d-164">Die Größe (in Bytes) des Puffers, auf den *pprinterenum* zeigt.</span><span class="sxs-lookup"><span data-stu-id="9f24d-164">The size, in bytes, of the buffer pointed to by *pPrinterEnum*.</span></span>

</dd> <dt>

<span data-ttu-id="9f24d-165">*pcbbenötigte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9f24d-165">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f24d-166">Ein Zeiger auf einen Wert, der die Anzahl der kopierten Bytes empfängt, wenn die Funktion erfolgreich ausgeführt wird, oder die Anzahl der Bytes, die erforderlich sind, wenn *cbbuf* zu klein ist.</span><span class="sxs-lookup"><span data-stu-id="9f24d-166">A pointer to a value that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> <dt>

<span data-ttu-id="9f24d-167">*pkreturned* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9f24d-167">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f24d-168">Ein Zeiger auf einen Wert, der die Anzahl der [**Drucker \_ Info \_ 1**](printer-info-1.md), [**Printer \_ Info \_ 2**](printer-info-2.md) , [**Printer \_ Info \_ 4**](printer-info-4.md)oder [**Printer \_ Info \_ 5**](printer-info-5.md) -Strukturen empfängt, die die Funktion in dem Array zurückgibt, auf das *pprinterenum* zeigt.</span><span class="sxs-lookup"><span data-stu-id="9f24d-168">A pointer to a value that receives the number of [**PRINTER\_INFO\_1**](printer-info-1.md), [**PRINTER\_INFO\_2**](printer-info-2.md) , [**PRINTER\_INFO\_4**](printer-info-4.md), or [**PRINTER\_INFO\_5**](printer-info-5.md) structures that the function returns in the array to which *pPrinterEnum* points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f24d-169">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f24d-169">Return value</span></span>

<span data-ttu-id="9f24d-170">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="9f24d-170">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="9f24d-171">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="9f24d-171">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f24d-172">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f24d-172">Remarks</span></span>

<span data-ttu-id="9f24d-173">Diese Methode darf nicht in [**DllMain**](/windows/desktop/Dlls/dllmain)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="9f24d-173">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="9f24d-174">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9f24d-174">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="9f24d-175">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="9f24d-175">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="9f24d-176">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="9f24d-176">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="9f24d-177">Wenn **enumprinter** eine [**Drucker \_ Info \_ 1**](printer-info-1.md) -Struktur zurückgibt, in der der druckerenumerationscontainer \_ \_ angegeben ist, weist dies darauf hin, dass eine Hierarchie von Drucker Objekten vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9f24d-177">If **EnumPrinters** returns a [**PRINTER\_INFO\_1**](printer-info-1.md) structure in which PRINTER\_ENUM\_CONTAINER is specified, this indicates that there is a hierarchy of printer objects.</span></span> <span data-ttu-id="9f24d-178">Eine Anwendung kann die Hierarchie durch Aufrufen von **enumdruckern** auflisten, wobei *Name* auf den Wert des **PName** -Members der **Drucker \_ Info \_ 1** -Struktur festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="9f24d-178">An application can enumerate the hierarchy by calling **EnumPrinters** again, setting *Name* to the value of the **PRINTER\_INFO\_1** structure's **pName** member.</span></span>

<span data-ttu-id="9f24d-179">Die **enumprinter** -Funktion ruft keine Sicherheitsinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="9f24d-179">The **EnumPrinters** function does not retrieve security information.</span></span> <span data-ttu-id="9f24d-180">Wenn [**Drucker \_ Informationen \_ 2**](printer-info-2.md) -Strukturen im Array zurückgegeben werden, auf das von *pprinterenum* verwiesen wird, werden die *psecuritydescriptor* -Member auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9f24d-180">If [**PRINTER\_INFO\_2**](printer-info-2.md) structures are returned in the array pointed to by *pPrinterEnum*, their *pSecurityDescriptor* members will be set to **NULL**.</span></span>

<span data-ttu-id="9f24d-181">Um Informationen zum Standarddrucker abzurufen, nennen Sie [**GetDefaultPrinter**](getdefaultprinter.md).</span><span class="sxs-lookup"><span data-stu-id="9f24d-181">To get information about the default printer, call [**GetDefaultPrinter**](getdefaultprinter.md).</span></span>

<span data-ttu-id="9f24d-182">Die [**Drucker \_ Info \_ 4**](printer-info-4.md) -Struktur bietet eine einfache und äußerst schnelle Möglichkeit, die Namen der Drucker, die auf einem lokalen Computer installiert sind, sowie die von einem Benutzer eingerichteten Remote Verbindungen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9f24d-182">The [**PRINTER\_INFO\_4**](printer-info-4.md) structure provides an easy and extremely fast way to retrieve the names of the printers installed on a local machine, as well as the remote connections that a user has established.</span></span> <span data-ttu-id="9f24d-183">Wenn **enumprinter** mit einer Datenstruktur vom Typ " **Printer \_ Info \_ 4** " aufgerufen wird, fragt diese Funktion die Registrierung nach den angegebenen Informationen ab und wird dann sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9f24d-183">When **EnumPrinters** is called with a **PRINTER\_INFO\_4** data structure, that function queries the registry for the specified information, then returns immediately.</span></span> <span data-ttu-id="9f24d-184">Dies unterscheidet sich vom Verhalten von **enumdruckern** , wenn es mit anderen Ebenen von **Printer \_ Info \_ \* *_-Datenstrukturen aufgerufen wird. Insbesondere, wenn _* enumprinter** mit einer Datenstruktur der Ebene 2 ([**Printer \_ Info \_ 2**](printer-info-2.md)) aufgerufen wird, führt Sie einen [**OpenPrinter**](openprinter.md) -Aufruf für jede Remote Verbindung aus.</span><span class="sxs-lookup"><span data-stu-id="9f24d-184">This differs from the behavior of **EnumPrinters** when called with other levels of **PRINTER\_INFO\_\**_ data structures. In particular, when _\* EnumPrinters*\* is called with a level 2 ([**PRINTER\_INFO\_2**](printer-info-2.md)) data structure, it performs an [**OpenPrinter**](openprinter.md) call on each remote connection.</span></span> <span data-ttu-id="9f24d-185">Wenn eine Remote Verbindung nicht mehr vorhanden ist oder der Remote Server nicht mehr vorhanden ist oder der Remote Drucker nicht mehr vorhanden ist, muss die Funktion auf das Timeout von RPC warten und somit den **OpenPrinter** -Aufruf nicht mehr ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f24d-185">If a remote connection is down, or the remote server no longer exists, or the remote printer no longer exists, the function must wait for RPC to time out and consequently fail the **OpenPrinter** call.</span></span> <span data-ttu-id="9f24d-186">Dies kann eine Weile dauern.</span><span class="sxs-lookup"><span data-stu-id="9f24d-186">This can take a while.</span></span> <span data-ttu-id="9f24d-187">Durch die Übergabe einer **Drucker \_ Info \_ 4** -Struktur kann eine Anwendung ein Minimum an erforderlichen Informationen abrufen. wenn ausführlichere Informationen gewünscht werden, kann ein nachfolgende **aufrufergrad** 2 aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="9f24d-187">Passing a **PRINTER\_INFO\_4** structure lets an application retrieve a bare minimum of required information; if more detailed information is desired, a subsequent **EnumPrinters** level 2 call can be made.</span></span>

<span data-ttu-id="9f24d-188">**Windows Vista:** Die von **enumdruckern** zurückgegebenen Druckerdaten werden aus einem lokalen Cache abgerufen, wenn der Wert der *Ebene* 4 ist.</span><span class="sxs-lookup"><span data-stu-id="9f24d-188">**Windows Vista:** The printer data returned by **EnumPrinters** is retrieved from a local cache when the value of *Level* is 4.</span></span>

<span data-ttu-id="9f24d-189">In der folgenden Tabelle wird die **enumprinter** -Ausgabe für verschiedene *Flags* -Werte angezeigt, wenn der *Level* -Parameter auf 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9f24d-189">The following table shows the **EnumPrinters** output for various *Flags* values when the *Level* parameter is set to 1.</span></span>

<span data-ttu-id="9f24d-190">In der Spalte *namens* Parameter der Tabelle sollten Sie einen entsprechenden Namen für Druckanbieter, Domäne und Computer ersetzen.</span><span class="sxs-lookup"><span data-stu-id="9f24d-190">In the *Name* parameter column of the table, you should substitute an appropriate name for Print Provider, Domain, and Machine.</span></span> <span data-ttu-id="9f24d-191">Beispielsweise können Sie für "Druckanbieter" den Namen des Netzwerkdruck Anbieters oder den Namen des lokalen Druck Anbieters verwenden.</span><span class="sxs-lookup"><span data-stu-id="9f24d-191">For example, for "Print Provider," you could use the name of the network print provider or the name of the local print provider.</span></span> <span data-ttu-id="9f24d-192">Rufen Sie zum Abrufen der Namen von Druckanbietern **enumprinter** auf, deren *Name* auf **null** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9f24d-192">To retrieve print provider names, call **EnumPrinters** with *Name* set to **NULL**.</span></span>



| <span data-ttu-id="9f24d-193">*Flags* -Parameter</span><span class="sxs-lookup"><span data-stu-id="9f24d-193">*Flags* parameter</span></span>                                  | <span data-ttu-id="9f24d-194">*Name* -Parameter</span><span class="sxs-lookup"><span data-stu-id="9f24d-194">*Name* parameter</span></span>                            | <span data-ttu-id="9f24d-195">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="9f24d-195">Result</span></span>                                                                                            |
|----------------------------------------------------|---------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f24d-196">Drucker Aufzählung \_ \_ lokal (und nicht Drucker Aufzählungs \_ \_ Name)</span><span class="sxs-lookup"><span data-stu-id="9f24d-196">PRINTER\_ENUM\_LOCAL (and not PRINTER\_ENUM\_NAME)</span></span> | <span data-ttu-id="9f24d-197">Der *Name* -Parameter wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9f24d-197">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="9f24d-198">Alle lokalen Drucker.</span><span class="sxs-lookup"><span data-stu-id="9f24d-198">All local printers.</span></span><br/>                                                                    |
| <span data-ttu-id="9f24d-199">\_Name der druckerenum \_</span><span class="sxs-lookup"><span data-stu-id="9f24d-199">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="9f24d-200">"Druckanbieter"</span><span class="sxs-lookup"><span data-stu-id="9f24d-200">"Print Provider"</span></span><br/>                 | <span data-ttu-id="9f24d-201">Alle Domänen Namen</span><span class="sxs-lookup"><span data-stu-id="9f24d-201">All domain names</span></span><br/>                                                                       |
| <span data-ttu-id="9f24d-202">\_Name der druckerenum \_</span><span class="sxs-lookup"><span data-stu-id="9f24d-202">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="9f24d-203">"Druckanbieter! -</span><span class="sxs-lookup"><span data-stu-id="9f24d-203">"Print Provider!Domain"</span></span><br/>          | <span data-ttu-id="9f24d-204">Alle Drucker und Druckserver in der Domäne des Computers</span><span class="sxs-lookup"><span data-stu-id="9f24d-204">All printers and print servers in the computer's domain</span></span><br/>                                |
| <span data-ttu-id="9f24d-205">\_Name der druckerenum \_</span><span class="sxs-lookup"><span data-stu-id="9f24d-205">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="9f24d-206">"Druckanbieter!! \\ \\ Computer</span><span class="sxs-lookup"><span data-stu-id="9f24d-206">"Print Provider!!\\\\Machine"</span></span><br/>    | <span data-ttu-id="9f24d-207">Alle auf dem Computer freigegebenen Drucker \\ \\</span><span class="sxs-lookup"><span data-stu-id="9f24d-207">All printers shared at \\\\Machine</span></span><br/>                                                     |
| <span data-ttu-id="9f24d-208">\_Name der druckerenum \_</span><span class="sxs-lookup"><span data-stu-id="9f24d-208">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="9f24d-209">Eine leere Zeichenfolge: ""</span><span class="sxs-lookup"><span data-stu-id="9f24d-209">An empty string, ""</span></span><br/>              | <span data-ttu-id="9f24d-210">Alle lokalen Drucker.</span><span class="sxs-lookup"><span data-stu-id="9f24d-210">All local printers.</span></span><br/>                                                                    |
| <span data-ttu-id="9f24d-211">\_Name der druckerenum \_</span><span class="sxs-lookup"><span data-stu-id="9f24d-211">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="9f24d-212">**NULL**</span><span class="sxs-lookup"><span data-stu-id="9f24d-212">**NULL**</span></span><br/>                         | <span data-ttu-id="9f24d-213">Alle Druckanbieter in der Domäne des Computers</span><span class="sxs-lookup"><span data-stu-id="9f24d-213">All print providers in the computer's domain</span></span><br/>                                           |
| <span data-ttu-id="9f24d-214">Drucker-Aufzählungs \_ \_ Verbindungen</span><span class="sxs-lookup"><span data-stu-id="9f24d-214">PRINTER\_ENUM\_CONNECTIONS</span></span>                         | <span data-ttu-id="9f24d-215">Der *Name* -Parameter wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9f24d-215">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="9f24d-216">Alle verbundenen Remote Drucker</span><span class="sxs-lookup"><span data-stu-id="9f24d-216">All connected remote printers</span></span><br/>                                                          |
| <span data-ttu-id="9f24d-217">Drucker-Aufzählungs \_ \_ Netzwerk</span><span class="sxs-lookup"><span data-stu-id="9f24d-217">PRINTER\_ENUM\_NETWORK</span></span>                             | <span data-ttu-id="9f24d-218">Der *Name* -Parameter wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9f24d-218">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="9f24d-219">Alle Drucker in der Domäne des Computers</span><span class="sxs-lookup"><span data-stu-id="9f24d-219">All printers in the computer's domain</span></span><br/>                                                  |
| <span data-ttu-id="9f24d-220">druckeraufzählungs \_ \_ Remote</span><span class="sxs-lookup"><span data-stu-id="9f24d-220">PRINTER\_ENUM\_REMOTE</span></span>                              | <span data-ttu-id="9f24d-221">Eine leere Zeichenfolge: ""</span><span class="sxs-lookup"><span data-stu-id="9f24d-221">An empty string, ""</span></span><br/>              | <span data-ttu-id="9f24d-222">Alle Drucker und Druckserver in der Domäne des Computers</span><span class="sxs-lookup"><span data-stu-id="9f24d-222">All printers and print servers in the computer's domain</span></span><br/>                                |
| <span data-ttu-id="9f24d-223">druckeraufzählungs \_ \_ Remote</span><span class="sxs-lookup"><span data-stu-id="9f24d-223">PRINTER\_ENUM\_REMOTE</span></span>                              | <span data-ttu-id="9f24d-224">"Druckanbieter"</span><span class="sxs-lookup"><span data-stu-id="9f24d-224">"Print Provider"</span></span><br/>                 | <span data-ttu-id="9f24d-225">Identisch mit dem \_ druckerenum- \_ Namen</span><span class="sxs-lookup"><span data-stu-id="9f24d-225">Same as PRINTER\_ENUM\_NAME</span></span><br/>                                                            |
| <span data-ttu-id="9f24d-226">druckeraufzählungs \_ \_ Remote</span><span class="sxs-lookup"><span data-stu-id="9f24d-226">PRINTER\_ENUM\_REMOTE</span></span>                              | <span data-ttu-id="9f24d-227">"Druckanbieter! -</span><span class="sxs-lookup"><span data-stu-id="9f24d-227">"Print Provider!Domain"</span></span><br/>          | <span data-ttu-id="9f24d-228">Alle Drucker und Druckserver in der Domäne des Computers, unabhängig von der angegebenen *Domäne* .</span><span class="sxs-lookup"><span data-stu-id="9f24d-228">All printers and print servers in computer's domain, regardless of *Domain* specified.</span></span><br/> |
| <span data-ttu-id="9f24d-229">\_Druckerenum \_ \_ -Kategorie 3D</span><span class="sxs-lookup"><span data-stu-id="9f24d-229">PRINTER\_ENUM\_CATEGORY\_3D</span></span>                        | <span data-ttu-id="9f24d-230">Der *Name* -Parameter wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9f24d-230">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="9f24d-231">Nur 3D-Drucker werden aufgezählt.</span><span class="sxs-lookup"><span data-stu-id="9f24d-231">Only 3D printers are enumerated.</span></span><br/>                                                       |
| <span data-ttu-id="9f24d-232">\_druckerenum- \_ Kategorie \_ alle</span><span class="sxs-lookup"><span data-stu-id="9f24d-232">PRINTER\_ENUM\_CATEGORY\_ALL</span></span>                       | <span data-ttu-id="9f24d-233">Der *Name* -Parameter wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9f24d-233">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="9f24d-234">3D-Drucker werden zusammen mit allen anderen Druckern aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9f24d-234">3D printers are enumerated, along with all other printers.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="9f24d-235">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f24d-235">Requirements</span></span>



| <span data-ttu-id="9f24d-236">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f24d-236">Requirement</span></span> | <span data-ttu-id="9f24d-237">Wert</span><span class="sxs-lookup"><span data-stu-id="9f24d-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f24d-238">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f24d-238">Minimum supported client</span></span><br/> | <span data-ttu-id="9f24d-239">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f24d-239">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9f24d-240">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f24d-240">Minimum supported server</span></span><br/> | <span data-ttu-id="9f24d-241">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f24d-241">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9f24d-242">Header</span><span class="sxs-lookup"><span data-stu-id="9f24d-242">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f24d-243"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f24d-243"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9f24d-244">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9f24d-244">Library</span></span><br/>                  | <dl> <span data-ttu-id="9f24d-245"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f24d-245"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="9f24d-246">DLL</span><span class="sxs-lookup"><span data-stu-id="9f24d-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f24d-247"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="9f24d-247"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="9f24d-248">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="9f24d-248">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9f24d-249">**Enumprintersw** (Unicode) und **enumprintersa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9f24d-249">**EnumPrintersW** (Unicode) and **EnumPrintersA** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="9f24d-250">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f24d-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f24d-251">Drucken</span><span class="sxs-lookup"><span data-stu-id="9f24d-251">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9f24d-252">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="9f24d-252">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="9f24d-253">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="9f24d-253">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="9f24d-254">**Deleteprinter**</span><span class="sxs-lookup"><span data-stu-id="9f24d-254">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="9f24d-255">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="9f24d-255">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="9f24d-256">**Drucker \_ Informationen \_ 1**</span><span class="sxs-lookup"><span data-stu-id="9f24d-256">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="9f24d-257">**Drucker \_ Informationen \_ 2**</span><span class="sxs-lookup"><span data-stu-id="9f24d-257">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="9f24d-258">**Drucker \_ Info \_ 4**</span><span class="sxs-lookup"><span data-stu-id="9f24d-258">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="9f24d-259">**Drucker \_ Informationen \_ 5**</span><span class="sxs-lookup"><span data-stu-id="9f24d-259">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> <dt>

[<span data-ttu-id="9f24d-260">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="9f24d-260">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

