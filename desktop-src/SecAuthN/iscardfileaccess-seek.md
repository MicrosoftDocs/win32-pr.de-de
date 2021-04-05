---
description: Die Seek-Methode wählt das Objekt aus, von dem aus der Zugriff (Lese-/Schreibzugriff) erfolgen soll.
ms.assetid: 9e06df70-6415-46dd-b34f-59614d1cbee7
title: 'Iscardfileaccess:: Seek-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Seek
api_type:
- COM
api_location: ''
ms.openlocfilehash: c0d23925ba1c38a05e15bea5e6ee63b3a1c87125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756882"
---
# <a name="iscardfileaccessseek-method"></a><span data-ttu-id="b1bdb-103">Iscardfileaccess:: Seek-Methode</span><span class="sxs-lookup"><span data-stu-id="b1bdb-103">ISCardFileAccess::Seek method</span></span>

<span data-ttu-id="b1bdb-104">\[Die **Seek** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="b1bdb-104">\[The **Seek** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b1bdb-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b1bdb-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b1bdb-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="b1bdb-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b1bdb-107">Die **Seek** -Methode wählt das Objekt aus, von dem aus der Zugriff (Lese-/Schreibzugriff) erfolgen soll.</span><span class="sxs-lookup"><span data-stu-id="b1bdb-107">The **Seek** method selects the object from which (read/write) access will be done.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1bdb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1bdb-108">Syntax</span></span>


```C++
HRESULT Seek(
  [in] HSCARD_FILE hFile,
  [in] SEEKTYPE    *Seek,
  [in] LONG        lOffset 
);
```



## <a name="parameters"></a><span data-ttu-id="b1bdb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1bdb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1bdb-110">*hFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1bdb-110">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1bdb-111">Handle der geöffneten Datei.</span><span class="sxs-lookup"><span data-stu-id="b1bdb-111">Handle of the open file.</span></span>

</dd> <dt>

<span data-ttu-id="b1bdb-112">*Suchen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1bdb-112">*Seek* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1bdb-113">Der Speicherort, an dem der Suchvorgang beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="b1bdb-113">Location where the seek should begin.</span></span>



| <span data-ttu-id="b1bdb-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b1bdb-114">Value</span></span>                                                                                                | <span data-ttu-id="b1bdb-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b1bdb-115">Meaning</span></span>                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="b1bdb-116"><dt>SC- \_ Suche \_ von \_ Anfang an</dt></span><span class="sxs-lookup"><span data-stu-id="b1bdb-116"><dt>SC\_SEEK\_FROM\_BEGINNING</dt></span></span> </dl> | <span data-ttu-id="b1bdb-117">Beginnen Sie mit der Suche am Anfang.</span><span class="sxs-lookup"><span data-stu-id="b1bdb-117">Begin search at the beginning.</span></span><br/>          |
| <dl> <span data-ttu-id="b1bdb-118"><dt>SC- \_ Suche \_ von \_ Ende </dt></span><span class="sxs-lookup"><span data-stu-id="b1bdb-118"><dt>SC\_SEEK\_FROM\_END </dt></span></span> </dl>      | <span data-ttu-id="b1bdb-119">Starten Sie die Suche vom Ende.</span><span class="sxs-lookup"><span data-stu-id="b1bdb-119">Begin search from the end.</span></span><br/>              |
| <dl> <span data-ttu-id="b1bdb-120"><dt>SC- \_ Suche \_ relativ</dt></span><span class="sxs-lookup"><span data-stu-id="b1bdb-120"><dt>SC\_SEEK\_RELATIVE</dt></span></span> </dl>        | <span data-ttu-id="b1bdb-121">Startet die Suche von der aktuellen Position aus.</span><span class="sxs-lookup"><span data-stu-id="b1bdb-121">Begin search from the current position.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b1bdb-122">*loffset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1bdb-122">*lOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1bdb-123">Anzahl der Datenobjekte aus dem Verweis Objekt.</span><span class="sxs-lookup"><span data-stu-id="b1bdb-123">Number of data objects from the reference object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1bdb-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b1bdb-124">Return value</span></span>

<span data-ttu-id="b1bdb-125">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="b1bdb-125">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="b1bdb-126">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b1bdb-126">Return code</span></span>                                                                                   | <span data-ttu-id="b1bdb-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1bdb-127">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b1bdb-128"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b1bdb-128"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b1bdb-129">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b1bdb-129">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="b1bdb-130"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="b1bdb-130"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b1bdb-131">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="b1bdb-131">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="b1bdb-132"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="b1bdb-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b1bdb-133">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="b1bdb-133">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="b1bdb-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1bdb-134">Remarks</span></span>

<span data-ttu-id="b1bdb-135">Um in eine Datei zu lesen oder in diese zu schreiben, geben [**Sie Read**](iscardfileaccess-read.md) bzw. [**Write**](iscardfileaccess-write.md) an.</span><span class="sxs-lookup"><span data-stu-id="b1bdb-135">To read to or write from a file, call [**Read**](iscardfileaccess-read.md) or [**Write**](iscardfileaccess-write.md) respectively.</span></span>

<span data-ttu-id="b1bdb-136">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardfileaccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="b1bdb-136">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="b1bdb-137">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="b1bdb-137">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="b1bdb-138">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="b1bdb-138">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1bdb-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1bdb-139">Requirements</span></span>



| <span data-ttu-id="b1bdb-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1bdb-140">Requirement</span></span> | <span data-ttu-id="b1bdb-141">Wert</span><span class="sxs-lookup"><span data-stu-id="b1bdb-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b1bdb-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1bdb-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b1bdb-143">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1bdb-143">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b1bdb-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1bdb-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b1bdb-145">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1bdb-145">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b1bdb-146">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b1bdb-146">End of client support</span></span><br/>    | <span data-ttu-id="b1bdb-147">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1bdb-147">Windows XP</span></span><br/>                                |
| <span data-ttu-id="b1bdb-148">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="b1bdb-148">End of server support</span></span><br/>    | <span data-ttu-id="b1bdb-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b1bdb-149">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="b1bdb-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1bdb-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1bdb-151">**Iscardfileaccess**</span><span class="sxs-lookup"><span data-stu-id="b1bdb-151">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="b1bdb-152">**Lesen**</span><span class="sxs-lookup"><span data-stu-id="b1bdb-152">**Read**</span></span>](iscardfileaccess-read.md)
</dt> <dt>

[<span data-ttu-id="b1bdb-153">**Schreiben**</span><span class="sxs-lookup"><span data-stu-id="b1bdb-153">**Write**</span></span>](iscardfileaccess-write.md)
</dt> </dl>

 

 
