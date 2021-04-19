---
description: Die addprintprovidor-Funktion installiert einen lokalen Druckanbieter und verknüpft die Konfigurations-, Daten-und Anbieter Dateien.
ms.assetid: f34549c3-0474-48ba-9307-5b36f02dbe1c
title: Addprintprovidor-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProvidor
- AddPrintProvidorA
- AddPrintProvidorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: adf5f914046eb82e070e3e9915325989ff868d1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362451"
---
# <a name="addprintprovidor-function"></a><span data-ttu-id="3793b-103">Addprintprovidor-Funktion</span><span class="sxs-lookup"><span data-stu-id="3793b-103">AddPrintProvidor function</span></span>

<span data-ttu-id="3793b-104">Die **addprintprovidor** -Funktion installiert einen lokalen Druckanbieter und verknüpft die Konfigurations-, Daten-und Anbieter Dateien.</span><span class="sxs-lookup"><span data-stu-id="3793b-104">The **AddPrintProvidor** function installs a local print provider and links the configuration, data, and provider files.</span></span>

## <a name="syntax"></a><span data-ttu-id="3793b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3793b-105">Syntax</span></span>


```C++
BOOL AddPrintProvidor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pProviderInfo
);
```



## <a name="parameters"></a><span data-ttu-id="3793b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3793b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3793b-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3793b-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3793b-108">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt, auf dem der Anbieter installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3793b-108">A pointer to a null-terminated string that specifies the name of the server on which the provider should be installed.</span></span> <span data-ttu-id="3793b-109">Für Systeme, die nur die lokale Installation von Anbietern unterstützen, sollte dieser Parameter **null** sein.</span><span class="sxs-lookup"><span data-stu-id="3793b-109">For systems that only support local installation of providers, this parameter should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3793b-110">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3793b-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3793b-111">Die Ebene der-Struktur, auf die *pproviderinfo* verweist.</span><span class="sxs-lookup"><span data-stu-id="3793b-111">The level of the structure to which *pProviderInfo* points.</span></span> <span data-ttu-id="3793b-112">Dies kann einer der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="3793b-112">It can be one of the following.</span></span>



| <span data-ttu-id="3793b-113">Wert</span><span class="sxs-lookup"><span data-stu-id="3793b-113">Value</span></span>                                                                                                | <span data-ttu-id="3793b-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3793b-114">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="3793b-115"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="3793b-115"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="3793b-116">Die Funktion verwendet eine [**providor \_ Info \_ 1**](providor-info-1.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="3793b-116">Function uses a [**PROVIDOR\_INFO\_1**](providor-info-1.md) structure.</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="3793b-117"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="3793b-117"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="3793b-118">Die Funktion verwendet eine [**providor \_ Info \_ 2**](providor-info-2.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="3793b-118">Function uses a [**PROVIDOR\_INFO\_2**](providor-info-2.md) structure.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3793b-119">*pproviderinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3793b-119">*pProviderInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3793b-120">Ein Zeiger auf eine Druckanbieter Struktur, wie nach *Ebene* angegeben.</span><span class="sxs-lookup"><span data-stu-id="3793b-120">A pointer to a print provider structure, as indicated by *Level*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3793b-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3793b-121">Return value</span></span>

<span data-ttu-id="3793b-122">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="3793b-122">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="3793b-123">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="3793b-123">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3793b-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3793b-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3793b-125">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3793b-125">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="3793b-126">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="3793b-126">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="3793b-127">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="3793b-127">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="3793b-128">Bevor eine Anwendung die **addprintprovidor** -Funktion aufruft, müssen alle vom Anbieter benötigten Dateien in das Verzeichnis "System32" kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="3793b-128">Before an application calls the **AddPrintProvidor** function, all files required by the provider must be copied to the SYSTEM32 directory.</span></span>

<span data-ttu-id="3793b-129">Ein von **addprintprovidor** hinzugefügter Anbieter kann entfernt werden, indem [**deleteprintprovidor**](deleteprintprovidor.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3793b-129">A provider added by **AddPrintProvidor** may be removed by calling [**DeletePrintProvidor**](deleteprintprovidor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3793b-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3793b-130">Requirements</span></span>



| <span data-ttu-id="3793b-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3793b-131">Requirement</span></span> | <span data-ttu-id="3793b-132">Wert</span><span class="sxs-lookup"><span data-stu-id="3793b-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3793b-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3793b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3793b-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3793b-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3793b-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3793b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3793b-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3793b-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3793b-137">Header</span><span class="sxs-lookup"><span data-stu-id="3793b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="3793b-138"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3793b-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3793b-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3793b-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="3793b-140"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3793b-140"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="3793b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="3793b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3793b-142"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="3793b-142"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="3793b-143">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="3793b-143">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3793b-144">**Addprintprovidorw** (Unicode) und **addprintprovidora** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3793b-144">**AddPrintProvidorW** (Unicode) and **AddPrintProvidorA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="3793b-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3793b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3793b-146">Drucken</span><span class="sxs-lookup"><span data-stu-id="3793b-146">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3793b-147">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="3793b-147">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="3793b-148">**Deleteprintprovidor**</span><span class="sxs-lookup"><span data-stu-id="3793b-148">**DeletePrintProvidor**</span></span>](deleteprintprovidor.md)
</dt> <dt>

[<span data-ttu-id="3793b-149">**Providor- \_ Info \_ 1**</span><span class="sxs-lookup"><span data-stu-id="3793b-149">**PROVIDOR\_INFO\_1**</span></span>](providor-info-1.md)
</dt> <dt>

[<span data-ttu-id="3793b-150">**Providor- \_ Info \_ 2**</span><span class="sxs-lookup"><span data-stu-id="3793b-150">**PROVIDOR\_INFO\_2**</span></span>](providor-info-2.md)
</dt> </dl>

 

 




