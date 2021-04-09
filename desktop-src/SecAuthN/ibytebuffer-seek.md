---
description: Die Seek-Methode ändert den Such Zeiger an eine neue Position relativ zum Anfang des Puffers, bis zum Ende des Puffers oder zum aktuellen Such Zeiger.
ms.assetid: 3541f3dd-7b92-4f72-89b7-4e04e007aaa3
title: 'Ibytebuffer:: Seek-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Seek
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: eacfedc3ed23a7a4cf1f60e6c6ac21936c3c94f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867871"
---
# <a name="ibytebufferseek-method"></a><span data-ttu-id="4ccdf-103">Ibytebuffer:: Seek-Methode</span><span class="sxs-lookup"><span data-stu-id="4ccdf-103">IByteBuffer::Seek method</span></span>

<span data-ttu-id="4ccdf-104">\[Die **Seek** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-104">\[The **Seek** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4ccdf-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4ccdf-106">Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="4ccdf-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="4ccdf-107">Die **Seek** -Methode ändert den Such Zeiger an eine neue Position relativ zum Anfang des Puffers, bis zum Ende des Puffers oder zum aktuellen Such Zeiger.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-107">The **Seek** method changes the seek pointer to a new location relative to the beginning of the buffer, to the end of the buffer, or to the current seek pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ccdf-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ccdf-108">Syntax</span></span>


```C++
HRESULT Seek(
  [in]  LONG dlibMove,
  [in]  LONG dwOrigin,
  [out] LONG *plibNewPosition
);
```



## <a name="parameters"></a><span data-ttu-id="4ccdf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ccdf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ccdf-110">*dlibmove* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ccdf-110">*dlibMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ccdf-111">Die Verschiebung, die dem durch *dwOrigin* festgelegten Speicherort hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-111">Displacement to be added to the location indicated by *dwOrigin*.</span></span> <span data-ttu-id="4ccdf-112">Wenn *dwOrigin* für Stream \_ Seek \_ festgelegt ist, wird dies als unsignierter Wert und nicht als signiert interpretiert.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-112">If *dwOrigin* is STREAM\_SEEK\_SET, this is interpreted as an unsigned value rather than signed.</span></span>

</dd> <dt>

<span data-ttu-id="4ccdf-113">*dwOrigin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ccdf-113">*dwOrigin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ccdf-114">Gibt den Ursprung der in *dlibmove* angegebenen Verschiebung an.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-114">Specifies the origin for the displacement specified in *dlibMove*.</span></span> <span data-ttu-id="4ccdf-115">Der Ursprung kann einer der Werte in der folgenden Tabelle sein.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-115">The origin can be one of the values in the following table.</span></span>



| <span data-ttu-id="4ccdf-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4ccdf-116">Value</span></span>                                                                                                                                                                | <span data-ttu-id="4ccdf-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4ccdf-117">Meaning</span></span>                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STREAM_SEEK_SET"></span><span id="stream_seek_set"></span><dl> <span data-ttu-id="4ccdf-118"><dt>**Stream \_ - \_ Suchsatz**</dt></span><span class="sxs-lookup"><span data-stu-id="4ccdf-118"><dt>**STREAM\_SEEK\_SET**</dt></span></span> </dl> | <span data-ttu-id="4ccdf-119">Der neue Seek-Zeiger ist ein Offset relativ zum Anfang des Streams.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-119">The new seek pointer is an offset relative to the beginning of the stream.</span></span> <span data-ttu-id="4ccdf-120">In diesem Fall ist der *dlibmove* -Parameter die neue Suchposition relativ zum Anfang des Streams.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-120">In this case, the *dlibMove* parameter is the new seek position relative to the beginning of the stream.</span></span><br/> |
| <span id="STREAM_SEEK_CUR"></span><span id="stream_seek_cur"></span><dl> <span data-ttu-id="4ccdf-121"><dt>**Stream \_ Seek \_ cur**</dt></span><span class="sxs-lookup"><span data-stu-id="4ccdf-121"><dt>**STREAM\_SEEK\_CUR**</dt></span></span> </dl> | <span data-ttu-id="4ccdf-122">Der neue Seek-Zeiger ist ein Offset relativ zum aktuellen suchzeigerort.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-122">The new seek pointer is an offset relative to the current seek pointer location.</span></span> <span data-ttu-id="4ccdf-123">In diesem Fall ist der *dlibmove* -Parameter die signierte Verschiebung von der aktuellen Suchposition.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-123">In this case, the *dlibMove* parameter is the signed displacement from the current seek position.</span></span><br/>  |
| <span id="STREAM_SEEK_END"></span><span id="stream_seek_end"></span><dl> <span data-ttu-id="4ccdf-124"><dt>**\_ \_ streamsuchende**</dt></span><span class="sxs-lookup"><span data-stu-id="4ccdf-124"><dt>**STREAM\_SEEK\_END**</dt></span></span> </dl> | <span data-ttu-id="4ccdf-125">Der neue Seek-Zeiger ist ein Offset relativ zum Ende des Streams.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-125">The new seek pointer is an offset relative to the end of the stream.</span></span> <span data-ttu-id="4ccdf-126">In diesem Fall ist der *dlibmove* -Parameter die neue Suchposition relativ zum Ende des Streams.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-126">In this case, the *dlibMove* parameter is the new seek position relative to the end of the stream.</span></span><br/>             |



 

</dd> <dt>

<span data-ttu-id="4ccdf-127">*plibnewposition* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4ccdf-127">*plibNewPosition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ccdf-128">Ein Zeiger auf den Speicherort, an dem diese Methode den Wert des neuen Such Zeigers vom Anfang des Streams schreibt.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-128">Pointer to the location where this method writes the value of the new seek pointer from the beginning of the stream.</span></span> <span data-ttu-id="4ccdf-129">Sie können diesen Zeiger auf **null** festlegen, um anzugeben, dass dieser Wert nicht von Interesse ist.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-129">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="4ccdf-130">In diesem Fall bietet diese Methode nicht den neuen Such Zeiger.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-130">In this case, this method does not provide the new seek pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ccdf-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4ccdf-131">Return value</span></span>

<span data-ttu-id="4ccdf-132">Der Rückgabewert ist ein **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-132">The return value is an **HRESULT**.</span></span> <span data-ttu-id="4ccdf-133">Der Wert S OK gibt an, dass \_ der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-133">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ccdf-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ccdf-134">Remarks</span></span>

<span data-ttu-id="4ccdf-135">Die **Seek** -Methode ändert den Seek-Zeiger, sodass nachfolgende Lese-und Schreibvorgänge an einem anderen Speicherort im Stream-Objekt stattfinden können.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-135">The **Seek** method changes the seek pointer so subsequent read and write operations can take place at a different location in the stream object.</span></span> <span data-ttu-id="4ccdf-136">Es ist ein Fehler, vor dem Anfang des Streams zu suchen.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-136">It is an error to seek before the beginning of the stream.</span></span> <span data-ttu-id="4ccdf-137">Es handelt sich jedoch nicht um einen Fehler, der über das Ende des Streams hinaus sucht.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-137">It is not, however, an error to seek past the end of the stream.</span></span> <span data-ttu-id="4ccdf-138">Die Suche über das Ende des Streams ist für nachfolgende Schreibvorgänge nützlich, da der Stream zu diesem Zeitpunkt direkt vor dem Schreibvorgang auf die Suchposition erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-138">Seeking past the end of the stream is useful for subsequent write operations, as the stream will at that time be extended to the seek position immediately before the write operation is done.</span></span>

<span data-ttu-id="4ccdf-139">Sie können diese Methode auch verwenden, um den aktuellen Wert des Such Zeigers abzurufen, indem Sie diese Methode aufrufen, wobei der *dwOrigin* -Parameter auf Stream \_ Seek \_ cur festgelegt und der *dlibmove* -Parameter auf 0 (null) festgelegt ist, sodass der Such Zeiger nicht geändert wird.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-139">You can also use this method to obtain the current value of the seek pointer by calling this method with the *dwOrigin* parameter set to STREAM\_SEEK\_CUR and the *dlibMove* parameter set to zero so the seek pointer is not changed.</span></span> <span data-ttu-id="4ccdf-140">Der aktuelle Seek-Zeiger wird im Parameter " *plibnewposition* " zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-140">The current seek pointer is returned in the *plibNewPosition* parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="4ccdf-141">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ccdf-141">Examples</span></span>

<span data-ttu-id="4ccdf-142">Im folgenden Beispiel wird gezeigt, wie der Such Zeiger auf eine neue Position positioniert wird.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-142">The following example shows positioning the seek pointer to a new location.</span></span>


```C++
LONG     lNewPos;
HRESULT  hr;

// Change the seek pointer.
hr = pIByteBuff->Seek(5, STREAM_SEEK_SET, &lNewPos);
if (FAILED(hr))
  printf("Failed IByteBuffer::Seek\n");
else
  printf("New position is %x\n", lNewPos);
```



## <a name="requirements"></a><span data-ttu-id="4ccdf-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ccdf-143">Requirements</span></span>



| <span data-ttu-id="4ccdf-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ccdf-144">Requirement</span></span> | <span data-ttu-id="4ccdf-145">Wert</span><span class="sxs-lookup"><span data-stu-id="4ccdf-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ccdf-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4ccdf-146">Minimum supported client</span></span><br/> | <span data-ttu-id="4ccdf-147">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4ccdf-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4ccdf-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4ccdf-148">Minimum supported server</span></span><br/> | <span data-ttu-id="4ccdf-149">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4ccdf-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4ccdf-150">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="4ccdf-150">End of client support</span></span><br/>    | <span data-ttu-id="4ccdf-151">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4ccdf-151">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4ccdf-152">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="4ccdf-152">End of server support</span></span><br/>    | <span data-ttu-id="4ccdf-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4ccdf-153">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4ccdf-154">Header</span><span class="sxs-lookup"><span data-stu-id="4ccdf-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ccdf-155"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="4ccdf-155"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4ccdf-156">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="4ccdf-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="4ccdf-157"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4ccdf-157"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4ccdf-158">DLL</span><span class="sxs-lookup"><span data-stu-id="4ccdf-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ccdf-159"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ccdf-159"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4ccdf-160">IID</span><span class="sxs-lookup"><span data-stu-id="4ccdf-160">IID</span></span><br/>                      | <span data-ttu-id="4ccdf-161">IID \_ ibytebuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-161">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

