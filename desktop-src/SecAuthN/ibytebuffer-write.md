---
description: Die Write-Methode schreibt eine angegebene Anzahl von Bytes in das Streamobjekt, beginnend beim aktuellen Such Zeiger.
ms.assetid: 0019cd10-8f8a-4190-bae4-e134e7b76882
title: 'Ibytebuffer:: Write-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Write
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b5f9b60a296041a18fbd850f1405088f5b0da2ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867868"
---
# <a name="ibytebufferwrite-method"></a><span data-ttu-id="a89f5-103">Ibytebuffer:: Write-Methode</span><span class="sxs-lookup"><span data-stu-id="a89f5-103">IByteBuffer::Write method</span></span>

<span data-ttu-id="a89f5-104">\[Die **Write** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="a89f5-104">\[The **Write** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a89f5-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a89f5-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a89f5-106">Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="a89f5-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="a89f5-107">Die **Write** -Methode schreibt eine angegebene Anzahl von Bytes in das Streamobjekt, beginnend beim aktuellen Such Zeiger.</span><span class="sxs-lookup"><span data-stu-id="a89f5-107">The **Write** method writes a specified number from bytes into the stream object starting at the current seek pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a89f5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a89f5-108">Syntax</span></span>


```C++
HRESULT Write(
  [in]  BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbWritten
);
```



## <a name="parameters"></a><span data-ttu-id="a89f5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a89f5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a89f5-110">*PBYTE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a89f5-110">*pByte* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a89f5-111">Adresse des Puffers, der die Daten enthält, die in den Stream geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a89f5-111">Address of the buffer containing the data that is to be written to the stream.</span></span> <span data-ttu-id="a89f5-112">Für diesen Parameter muss ein gültiger Zeiger angegeben werden, auch wenn *CB* NULL ist.</span><span class="sxs-lookup"><span data-stu-id="a89f5-112">A valid pointer must be provided for this parameter even when *cb* is zero.</span></span>

</dd> <dt>

<span data-ttu-id="a89f5-113">*CB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a89f5-113">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a89f5-114">Anzahl der Daten bytes, die in den Stream geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a89f5-114">Number of bytes of data to attempt to write into the stream.</span></span> <span data-ttu-id="a89f5-115">Dieser Parameter kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="a89f5-115">This parameter can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a89f5-116">*pcbwritten* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a89f5-116">*pcbWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a89f5-117">Adresse einer **langen** Variablen, bei der diese Methode die tatsächliche Anzahl von Bytes schreibt, die in das Datenstrom Objekt geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="a89f5-117">Address of a **LONG** variable where this method writes the actual number of bytes written to the stream object.</span></span> <span data-ttu-id="a89f5-118">Der Aufrufer kann diesen Zeiger auf **null** festlegen. in diesem Fall stellt diese Methode nicht die tatsächliche Anzahl der geschriebenen Bytes bereit.</span><span class="sxs-lookup"><span data-stu-id="a89f5-118">The caller can set this pointer to **NULL**, in which case, this method does not provide the actual number of bytes written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a89f5-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a89f5-119">Return value</span></span>

<span data-ttu-id="a89f5-120">Der Rückgabewert ist ein **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a89f5-120">The return value is an **HRESULT**.</span></span> <span data-ttu-id="a89f5-121">Der Wert S OK gibt an, dass \_ der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="a89f5-121">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a89f5-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a89f5-122">Remarks</span></span>

<span data-ttu-id="a89f5-123">Die **ibytebuffer:: Write** -Methode schreibt die angegebenen Daten in ein Datenstrom Objekt.</span><span class="sxs-lookup"><span data-stu-id="a89f5-123">The **IByteBuffer::Write** method writes the specified data to a stream object.</span></span> <span data-ttu-id="a89f5-124">Der Seek-Zeiger wird für die Anzahl der tatsächlich geschriebenen Bytes angepasst.</span><span class="sxs-lookup"><span data-stu-id="a89f5-124">The seek pointer is adjusted for the number of bytes actually written.</span></span> <span data-ttu-id="a89f5-125">Die Anzahl der tatsächlich geschriebenen Bytes wird im *pcbwritten* -Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a89f5-125">The number of bytes actually written is returned in the *pcbWritten* parameter.</span></span> <span data-ttu-id="a89f5-126">Wenn die Byte Anzahl 0 Bytes beträgt, hat der Schreibvorgang keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="a89f5-126">If the byte count is zero bytes, the write operation has no effect.</span></span>

<span data-ttu-id="a89f5-127">Wenn sich der Suchzeiger momentan hinter dem Ende des Streams befindet und die Byte Anzahl ungleich NULL ist, erhöht diese Methode die Größe des Streams auf den Such Zeiger und schreibt die angegebenen Bytes beginnend beim Such Zeiger.</span><span class="sxs-lookup"><span data-stu-id="a89f5-127">If the seek pointer is currently past the end of the stream and the byte count is nonzero, this method increases the size of the stream to the seek pointer and writes the specified bytes starting at the seek pointer.</span></span> <span data-ttu-id="a89f5-128">Die in den Stream geschriebenen Füll Bytes werden nicht mit einem bestimmten Wert initialisiert.</span><span class="sxs-lookup"><span data-stu-id="a89f5-128">The fill bytes written to the stream are not initialized to any particular value.</span></span> <span data-ttu-id="a89f5-129">Dies entspricht dem dateiendeverhalten im DOS-FAT-Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="a89f5-129">This is the same as the end-of-file behavior in the MS-DOS FAT file system.</span></span>

<span data-ttu-id="a89f5-130">Mit einer Byte Anzahl von 0 (null) und einem Such Zeiger hinter das Ende des Streams erstellt diese Methode nicht die Füll bytes, um den Stream auf den Such Zeiger zu vergrößern.</span><span class="sxs-lookup"><span data-stu-id="a89f5-130">With a zero byte count and a seek pointer past the end of the stream, this method does not create the fill bytes to increase the stream to the seek pointer.</span></span> <span data-ttu-id="a89f5-131">In diesem Fall müssen Sie die [**ibytebuffer:: SetSize**](ibytebuffer-setsize.md) -Methode aufrufen, um die Größe des Streams zu vergrößern und die Füll Bytes zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="a89f5-131">In this case, you must call the [**IByteBuffer::SetSize**](ibytebuffer-setsize.md) method to increase the size of the stream and write the fill bytes.</span></span>

<span data-ttu-id="a89f5-132">Der *pcbwritten* -Parameter kann auch dann einen Wert aufweisen, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="a89f5-132">The *pcbWritten* parameter can have a value even if an error occurs.</span></span>

<span data-ttu-id="a89f5-133">In der von com bereitgestellten Implementierung sind Streamobjekte nicht sparsam.</span><span class="sxs-lookup"><span data-stu-id="a89f5-133">In the COM-provided implementation, stream objects are not sparse.</span></span> <span data-ttu-id="a89f5-134">Alle Füll Bytes werden schließlich auf dem Datenträger zugeordnet und dem Stream zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a89f5-134">Any fill bytes are eventually allocated on the disk and assigned to the stream.</span></span>

## <a name="examples"></a><span data-ttu-id="a89f5-135">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a89f5-135">Examples</span></span>

<span data-ttu-id="a89f5-136">Das folgende Beispiel zeigt das Schreiben von Bytes in das Stream-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a89f5-136">The following example shows writing bytes into the stream object.</span></span>


```C++
LONG     lWrite;
HRESULT  hr;

// Write to the buffer.
// byData is an array of 64 bytes.
hr = pIByteBuff->Write(byData,
                       64,
                       &lWrite);
if (FAILED(hr))
  printf("Failed IByteBuffer::Write\n");
```



## <a name="requirements"></a><span data-ttu-id="a89f5-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a89f5-137">Requirements</span></span>



| <span data-ttu-id="a89f5-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a89f5-138">Requirement</span></span> | <span data-ttu-id="a89f5-139">Wert</span><span class="sxs-lookup"><span data-stu-id="a89f5-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a89f5-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a89f5-140">Minimum supported client</span></span><br/> | <span data-ttu-id="a89f5-141">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a89f5-141">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a89f5-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a89f5-142">Minimum supported server</span></span><br/> | <span data-ttu-id="a89f5-143">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a89f5-143">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a89f5-144">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a89f5-144">End of client support</span></span><br/>    | <span data-ttu-id="a89f5-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a89f5-145">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a89f5-146">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="a89f5-146">End of server support</span></span><br/>    | <span data-ttu-id="a89f5-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a89f5-147">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a89f5-148">Header</span><span class="sxs-lookup"><span data-stu-id="a89f5-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="a89f5-149"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="a89f5-149"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a89f5-150">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a89f5-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="a89f5-151"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a89f5-151"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a89f5-152">DLL</span><span class="sxs-lookup"><span data-stu-id="a89f5-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a89f5-153"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a89f5-153"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a89f5-154">IID</span><span class="sxs-lookup"><span data-stu-id="a89f5-154">IID</span></span><br/>                      | <span data-ttu-id="a89f5-155">IID \_ ibytebuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.</span><span class="sxs-lookup"><span data-stu-id="a89f5-155">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

