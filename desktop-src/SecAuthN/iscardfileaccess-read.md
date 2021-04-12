---
description: Die Read-Methode liest die angegebenen Daten aus einer angegebenen Datei und gibt Sie zurück.
ms.assetid: 697b8dfa-754b-46cf-ab5c-1ac1d8ae47f2
title: 'Iscardfileaccess:: Read-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Read
api_type:
- COM
api_location: ''
ms.openlocfilehash: b3d66b5c6e314a4ef7a00a76fabc8660f3bf65eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216213"
---
# <a name="iscardfileaccessread-method"></a><span data-ttu-id="c1439-103">Iscardfileaccess:: Read-Methode</span><span class="sxs-lookup"><span data-stu-id="c1439-103">ISCardFileAccess::Read method</span></span>

<span data-ttu-id="c1439-104">\[Die **Read** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c1439-104">\[The **Read** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c1439-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c1439-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c1439-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="c1439-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="c1439-107">Die **Read** -Methode liest die angegebenen Daten aus einer angegebenen Datei und gibt Sie zurück.</span><span class="sxs-lookup"><span data-stu-id="c1439-107">The **Read** method reads and returns the specified data from a given file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1439-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1439-108">Syntax</span></span>


```C++
HRESULT Read(
  [in]  HSCARD_FILE  hFile,
  [in]  LONG         *lBytesToRead,
  [in]  SCARD_FLAGS  flags,
  [out] LPBYTEBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="c1439-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1439-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1439-110">*hFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1439-110">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1439-111">Handle der geöffneten Datei, auf die zugegriffen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c1439-111">Handle of the open file to access.</span></span>

</dd> <dt>

<span data-ttu-id="c1439-112">*lbytestoread* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1439-112">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1439-113">Die Länge der zu lesenden Daten (in) oder die Anzahl der gelesenen Bytes (aus).</span><span class="sxs-lookup"><span data-stu-id="c1439-113">Length of data to be read (in) or number of bytes read (out).</span></span> <span data-ttu-id="c1439-114">Gibt eine Liste der Dateien als ein Array von bstrins zurück.</span><span class="sxs-lookup"><span data-stu-id="c1439-114">Returns list of files as an array of BSTRs.</span></span>

</dd> <dt>

<span data-ttu-id="c1439-115">*Flags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1439-115">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1439-116">Gibt an, ob sicheres Messaging verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c1439-116">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="c1439-117">**SC \_ FL \_ Secure \_ Messaging**</span><span class="sxs-lookup"><span data-stu-id="c1439-117">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="c1439-118">*ppbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c1439-118">*ppBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1439-119">Ein [**ibytebuffer**](ibytebuffer.md) -Objekt, das die gelesenen Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="c1439-119">An [**IByteBuffer**](ibytebuffer.md) object containing the read data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1439-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1439-120">Return value</span></span>

<span data-ttu-id="c1439-121">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="c1439-121">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="c1439-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c1439-122">Return code</span></span>                                                                                   | <span data-ttu-id="c1439-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1439-123">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c1439-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c1439-124"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c1439-125">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c1439-125">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="c1439-126"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="c1439-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c1439-127">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="c1439-127">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="c1439-128"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="c1439-128"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c1439-129">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="c1439-129">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="c1439-130"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="c1439-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c1439-131">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="c1439-131">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="c1439-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1439-132">Remarks</span></span>

<span data-ttu-id="c1439-133">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardfileaccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="c1439-133">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="c1439-134">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c1439-134">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="c1439-135">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="c1439-135">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1439-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1439-136">Requirements</span></span>



| <span data-ttu-id="c1439-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1439-137">Requirement</span></span> | <span data-ttu-id="c1439-138">Wert</span><span class="sxs-lookup"><span data-stu-id="c1439-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c1439-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1439-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c1439-140">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1439-140">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="c1439-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1439-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c1439-142">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1439-142">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c1439-143">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c1439-143">End of client support</span></span><br/>    | <span data-ttu-id="c1439-144">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c1439-144">Windows XP</span></span><br/>                                |
| <span data-ttu-id="c1439-145">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="c1439-145">End of server support</span></span><br/>    | <span data-ttu-id="c1439-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c1439-146">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="c1439-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1439-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1439-148">**Iscardfileaccess**</span><span class="sxs-lookup"><span data-stu-id="c1439-148">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
