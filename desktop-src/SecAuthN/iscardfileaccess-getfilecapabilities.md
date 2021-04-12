---
description: Die getfilefunktionalitäten-Methode ruft eine Liste der Dateifunktionen aus der aktuellen Datei ab.
ms.assetid: 0d24efd2-d411-4fb3-95c2-4742a58aeb5e
title: 'Iscardfileaccess:: getfilefunktionen-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.GetFileCapabilities
api_type:
- COM
api_location: ''
ms.openlocfilehash: ca22f02d327cdfbea527fba3a87f3f149774c091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216729"
---
# <a name="iscardfileaccessgetfilecapabilities-method"></a><span data-ttu-id="4170e-103">Iscardfileaccess:: getfilefunktionen-Methode</span><span class="sxs-lookup"><span data-stu-id="4170e-103">ISCardFileAccess::GetFileCapabilities method</span></span>

<span data-ttu-id="4170e-104">\[Die **getfilefunktionen** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="4170e-104">\[The **GetFileCapabilities** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4170e-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4170e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4170e-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="4170e-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="4170e-107">Die **getfilefunktionalitäten** -Methode ruft eine Liste der Dateifunktionen aus der aktuellen Datei ab.</span><span class="sxs-lookup"><span data-stu-id="4170e-107">The **GetFileCapabilities** method retrieves a list of file capabilities from the current file.</span></span>

## <a name="syntax"></a><span data-ttu-id="4170e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4170e-108">Syntax</span></span>


```C++
HRESULT GetFileCapabilities(
  [in, out] LPTLV_TABLE *ppProperties,
  [in, out] LONG        *plProperties,
  [in]      SCARD_FLAGS Flags
);
```



## <a name="parameters"></a><span data-ttu-id="4170e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4170e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4170e-110">*ppproperties* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4170e-110">*ppProperties* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4170e-111">Zeiger auf TLV-Strukturen (Tag, length, Wert).</span><span class="sxs-lookup"><span data-stu-id="4170e-111">Pointer to TLV (tag, length, value) structures.</span></span> <span data-ttu-id="4170e-112">Bei der Eingabe gibt dieser Parameter die Dateien an, für die Eigenschaften zu erhalten sind. bei der Ausgabe enthält dieser Parameter die Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4170e-112">On input, this parameter indicates the files for which to get properties; on output, this parameter contains the properties.</span></span> <span data-ttu-id="4170e-113">Das folgende Beispiel zeigt eine Definition der TLV-Struktur.</span><span class="sxs-lookup"><span data-stu-id="4170e-113">The following example is a definition of the TLV structure.</span></span>


```C++
#include <windows.h>

typedef struct
{
  DWORD  Tag;
  DWORD  Length;
  BYTE[]  Value;
  BOOL  Valid;
} TLV;
```



<span data-ttu-id="4170e-114">Weitere Informationen zu TLV-Strukturen finden Sie unter [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) .</span><span class="sxs-lookup"><span data-stu-id="4170e-114">For more information on TLV structures, see [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/).</span></span>

</dd> <dt>

<span data-ttu-id="4170e-115">*plproperties* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4170e-115">*plProperties* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4170e-116">Zeiger auf die Anzahl der TLV-Einträge in *ppproperties*.</span><span class="sxs-lookup"><span data-stu-id="4170e-116">Pointer to the number of TLV entries in *ppProperties*.</span></span>

</dd> <dt>

<span data-ttu-id="4170e-117">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="4170e-117">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4170e-118">Gibt an, ob sicheres Messaging verwendet werden muss und welche Daten vorab zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4170e-118">Specifies whether secure messaging has to be used and data preallocated.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="4170e-119">**SC \_ FL \_ Secure \_ Messaging**</span><span class="sxs-lookup"><span data-stu-id="4170e-119">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

<span data-ttu-id="4170e-120">**SC \_ FL, \_ vorab zugeordnet**</span><span class="sxs-lookup"><span data-stu-id="4170e-120">**SC\_FL\_PREALLOCATED**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4170e-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4170e-121">Return value</span></span>

<span data-ttu-id="4170e-122">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="4170e-122">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="4170e-123">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4170e-123">Return code</span></span>                                                                                   | <span data-ttu-id="4170e-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4170e-124">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="4170e-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4170e-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4170e-126">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="4170e-126">Operation was completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="4170e-127"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="4170e-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4170e-128">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="4170e-128">Invalid parameter.</span></span><br/>                    |
| <dl> <span data-ttu-id="4170e-129"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="4170e-129"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4170e-130">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="4170e-130">A bad pointer was passed in.</span></span><br/>          |
| <dl> <span data-ttu-id="4170e-131"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="4170e-131"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4170e-132">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="4170e-132">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="4170e-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4170e-133">Remarks</span></span>

<span data-ttu-id="4170e-134">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardfileaccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="4170e-134">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="4170e-135">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="4170e-135">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="4170e-136">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="4170e-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4170e-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4170e-137">Requirements</span></span>



| <span data-ttu-id="4170e-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4170e-138">Requirement</span></span> | <span data-ttu-id="4170e-139">Wert</span><span class="sxs-lookup"><span data-stu-id="4170e-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4170e-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4170e-140">Minimum supported client</span></span><br/> | <span data-ttu-id="4170e-141">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4170e-141">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="4170e-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4170e-142">Minimum supported server</span></span><br/> | <span data-ttu-id="4170e-143">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4170e-143">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4170e-144">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="4170e-144">End of client support</span></span><br/>    | <span data-ttu-id="4170e-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4170e-145">Windows XP</span></span><br/>                                |
| <span data-ttu-id="4170e-146">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="4170e-146">End of server support</span></span><br/>    | <span data-ttu-id="4170e-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4170e-147">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="4170e-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4170e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4170e-149">**Iscardfileaccess**</span><span class="sxs-lookup"><span data-stu-id="4170e-149">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
