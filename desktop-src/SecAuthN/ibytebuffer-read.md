---
description: Die Read-Methode liest eine angegebene Anzahl von Bytes aus dem Puffer Objekt in den Arbeitsspeicher, beginnend beim aktuellen Such Zeiger.
ms.assetid: 98c4de75-9ecf-4c57-9075-9d0e3675079f
title: 'Ibytebuffer:: Read-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Read
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0574fb640d60fd8af824ff54abce5d109675ba87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217774"
---
# <a name="ibytebufferread-method"></a><span data-ttu-id="c20ce-103">Ibytebuffer:: Read-Methode</span><span class="sxs-lookup"><span data-stu-id="c20ce-103">IByteBuffer::Read method</span></span>

<span data-ttu-id="c20ce-104">\[Die **Read** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c20ce-104">\[The **Read** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c20ce-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c20ce-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c20ce-106">Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="c20ce-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="c20ce-107">Die **Read** -Methode liest eine angegebene Anzahl von Bytes aus dem Puffer Objekt in den Arbeitsspeicher, beginnend beim aktuellen Such Zeiger.</span><span class="sxs-lookup"><span data-stu-id="c20ce-107">The **Read** method reads a specified number of bytes from the buffer object into memory starting at the current seek pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c20ce-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c20ce-108">Syntax</span></span>


```C++
HRESULT Read(
  [out] BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbRead
);
```



## <a name="parameters"></a><span data-ttu-id="c20ce-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c20ce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c20ce-110">*PBYTE* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c20ce-110">*pByte* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c20ce-111">Zeigt auf den Puffer, in den die Streamdaten gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="c20ce-111">Points to the buffer into which the stream data is read.</span></span> <span data-ttu-id="c20ce-112">Wenn ein Fehler auftritt, ist dieser Wert **null**.</span><span class="sxs-lookup"><span data-stu-id="c20ce-112">If an error occurs, this value is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c20ce-113">*CB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c20ce-113">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c20ce-114">Anzahl der Daten bytes, die aus dem Datenstrom Objekt gelesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c20ce-114">Number of bytes of data to attempt to read from the stream object.</span></span>

</dd> <dt>

<span data-ttu-id="c20ce-115">*pcbread* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c20ce-115">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c20ce-116">Adresse einer **Long** -Variablen, die die tatsächliche Anzahl von Bytes empfängt, die aus dem Streamobjekt gelesen wurden.</span><span class="sxs-lookup"><span data-stu-id="c20ce-116">Address of a **LONG** variable that receives the actual number of bytes read from the stream object.</span></span> <span data-ttu-id="c20ce-117">Sie können diesen Zeiger auf **null** festlegen, um anzugeben, dass dieser Wert nicht von Interesse ist.</span><span class="sxs-lookup"><span data-stu-id="c20ce-117">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="c20ce-118">In diesem Fall stellt diese Methode nicht die tatsächliche Anzahl der gelesenen Bytes bereit.</span><span class="sxs-lookup"><span data-stu-id="c20ce-118">In this case, this method does not provide the actual number of bytes read.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c20ce-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c20ce-119">Return value</span></span>

<span data-ttu-id="c20ce-120">Der Rückgabewert ist ein **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c20ce-120">The return value is an **HRESULT**.</span></span> <span data-ttu-id="c20ce-121">Der Wert S OK gibt an, dass \_ der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="c20ce-121">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c20ce-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c20ce-122">Remarks</span></span>

<span data-ttu-id="c20ce-123">Diese Methode liest Bytes aus diesem Datenstrom Objekt in den Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="c20ce-123">This method reads bytes from this stream object into memory.</span></span> <span data-ttu-id="c20ce-124">Das Stream-Objekt muss im STGM- \_ Lesemodus geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="c20ce-124">The stream object must be opened in STGM\_READ mode.</span></span> <span data-ttu-id="c20ce-125">Mit dieser Methode wird der Such Zeiger mit der tatsächlichen Anzahl der gelesenen Bytes angepasst.</span><span class="sxs-lookup"><span data-stu-id="c20ce-125">This method adjusts the seek pointer by the actual number of bytes read.</span></span>

<span data-ttu-id="c20ce-126">Die Anzahl der tatsächlich gelesenen Bytes wird auch im *pcbread* -Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c20ce-126">The number of bytes actually read is also returned in the *pcbRead* parameter.</span></span>

<span data-ttu-id="c20ce-127">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="c20ce-127">Notes to Callers</span></span>

<span data-ttu-id="c20ce-128">Die tatsächliche Anzahl von gelesenen Bytes kann weniger als die Anzahl der angeforderten Bytes sein, wenn ein Fehler auftritt oder wenn das Ende des Streams während des Lesevorgangs erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="c20ce-128">The actual number of bytes read can be fewer than the number of bytes requested if an error occurs or if the end of the stream is reached during the read operation.</span></span>

<span data-ttu-id="c20ce-129">Einige Implementierungen geben möglicherweise einen Fehler zurück, wenn das Ende des Streams während des Lesevorgang erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="c20ce-129">Some implementations might return an error if the end of the stream is reached during the read.</span></span> <span data-ttu-id="c20ce-130">Sie müssen darauf vorbereitet sein, die Fehlerrückgabe-oder S \_ OK-Rückgabewerte am Ende der Datenstrom Lesevorgänge zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="c20ce-130">You must be prepared to deal with the error return or S\_OK return values on end of stream reads.</span></span>

## <a name="examples"></a><span data-ttu-id="c20ce-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c20ce-131">Examples</span></span>

<span data-ttu-id="c20ce-132">Das folgende Beispiel zeigt, wie Bytes aus dem Puffer gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="c20ce-132">The following example shows reading bytes from the buffer.</span></span>


```C++
BYTE     byAtr[32];
long     lBytesRead, i;
HRESULT  hr;

// pAtr is a pointer to a previously instantiated IByteBuffer.
// It was used in an earlier call by ISCard::get_Atr.
// Use IByteBuffer::Read to access the retrieved ATR bytes.
hr = pAtr->Read(byAtr, 32, &lBytesRead);
// Use the ATR value. (This example merely displays the bytes.)
for ( i = 0; i < lBytesRead; i++)
    printf("%c", *(byAtr + i));
printf("\n");
```



## <a name="requirements"></a><span data-ttu-id="c20ce-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c20ce-133">Requirements</span></span>



| <span data-ttu-id="c20ce-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c20ce-134">Requirement</span></span> | <span data-ttu-id="c20ce-135">Wert</span><span class="sxs-lookup"><span data-stu-id="c20ce-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c20ce-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c20ce-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c20ce-137">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c20ce-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c20ce-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c20ce-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c20ce-139">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c20ce-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c20ce-140">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c20ce-140">End of client support</span></span><br/>    | <span data-ttu-id="c20ce-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c20ce-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="c20ce-142">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="c20ce-142">End of server support</span></span><br/>    | <span data-ttu-id="c20ce-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c20ce-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="c20ce-144">Header</span><span class="sxs-lookup"><span data-stu-id="c20ce-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="c20ce-145"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="c20ce-145"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c20ce-146">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c20ce-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="c20ce-147"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c20ce-147"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c20ce-148">DLL</span><span class="sxs-lookup"><span data-stu-id="c20ce-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c20ce-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c20ce-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c20ce-150">IID</span><span class="sxs-lookup"><span data-stu-id="c20ce-150">IID</span></span><br/>                      | <span data-ttu-id="c20ce-151">IID \_ ibytebuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.</span><span class="sxs-lookup"><span data-stu-id="c20ce-151">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

