---
description: Die Stat-Methode ruft statistische Informationen aus dem Streamobjekt ab.
ms.assetid: 7dfb59e9-143a-402e-990a-a2b35e6443dd
title: 'Ibytebuffer:: Stat-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Stat
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bbbf033fc9ad5a25b3bcf5c22028ac1237f46c14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349632"
---
# <a name="ibytebufferstat-method"></a><span data-ttu-id="4f1f8-103">Ibytebuffer:: Stat-Methode</span><span class="sxs-lookup"><span data-stu-id="4f1f8-103">IByteBuffer::Stat method</span></span>

<span data-ttu-id="4f1f8-104">\[Die **stat** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="4f1f8-104">\[The **Stat** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4f1f8-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4f1f8-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4f1f8-106">Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="4f1f8-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="4f1f8-107">Die **stat** -Methode ruft statistische Informationen aus dem Streamobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="4f1f8-107">The **Stat** method retrieves statistical information from the stream object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f1f8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f1f8-108">Syntax</span></span>


```C++
HRESULT Stat(
  [out] LPSTATSTRUCT pstatstg,
  [in]  LONG         grfStatFlag
);
```



## <a name="parameters"></a><span data-ttu-id="4f1f8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f1f8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f1f8-110">*pstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4f1f8-110">*pstatstg* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f1f8-111">Verweist auf eine **Status** Struktur, in der diese Methode Informationen zu diesem Streamobjekt platziert.</span><span class="sxs-lookup"><span data-stu-id="4f1f8-111">Points to a **STATSTRUCT** structure where this method places information about this stream object.</span></span> <span data-ttu-id="4f1f8-112">Dieser Zeiger ist **null** , wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="4f1f8-112">This pointer is **NULL** if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="4f1f8-113">*grsstatflag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f1f8-113">*grfStatFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f1f8-114">Gibt an, dass diese Methode einige der Felder in der Struktur der **Status** Struktur nicht zurückgibt, wodurch ein Speicher Belegungs Vorgang gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="4f1f8-114">Specifies that this method does not return some of the fields in the **STATSTRUCT** structure, thus saving a memory allocation operation.</span></span> <span data-ttu-id="4f1f8-115">Werte werden aus der [**StatFlag**](/windows/win32/api/wtypes/ne-wtypes-statflag) -Enumeration entnommen.</span><span class="sxs-lookup"><span data-stu-id="4f1f8-115">Values are taken from the [**STATFLAG**](/windows/win32/api/wtypes/ne-wtypes-statflag) enumeration</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f1f8-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f1f8-116">Return value</span></span>

<span data-ttu-id="4f1f8-117">Der Rückgabewert ist ein **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4f1f8-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="4f1f8-118">Der Wert S OK gibt an, dass \_ der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="4f1f8-118">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f1f8-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f1f8-119">Remarks</span></span>

<span data-ttu-id="4f1f8-120">Die **ibytebuffer:: stat** -Methode ruft einen Zeiger auf die **statstruct** -Struktur ab, die Informationen zu diesem geöffneten Stream enthält.</span><span class="sxs-lookup"><span data-stu-id="4f1f8-120">The **IByteBuffer::Stat** method retrieves a pointer to the **STATSTRUCT** structure that contains information about this open stream.</span></span>

## <a name="examples"></a><span data-ttu-id="4f1f8-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f1f8-121">Examples</span></span>

<span data-ttu-id="4f1f8-122">Das folgende Beispiel zeigt, wie statistische Informationen aus dem Stream abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4f1f8-122">The following example shows retrieving statistical information from the stream.</span></span>


```C++
STATSTRUCT  statstr;
HRESULT     hr;

// Retrieve the statistical information.
hr = pIByteBuff->Stat(&statstr,
                      STATFLAG_DEFAULT);
if (FAILED(hr))
  printf("Failed IByteBuffer::Stat\n");
else
  // Use statstr as needed.
```



## <a name="requirements"></a><span data-ttu-id="4f1f8-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f1f8-123">Requirements</span></span>



| <span data-ttu-id="4f1f8-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f1f8-124">Requirement</span></span> | <span data-ttu-id="4f1f8-125">Wert</span><span class="sxs-lookup"><span data-stu-id="4f1f8-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f1f8-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4f1f8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4f1f8-127">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f1f8-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4f1f8-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4f1f8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4f1f8-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f1f8-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4f1f8-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="4f1f8-130">End of client support</span></span><br/>    | <span data-ttu-id="4f1f8-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4f1f8-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4f1f8-132">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="4f1f8-132">End of server support</span></span><br/>    | <span data-ttu-id="4f1f8-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4f1f8-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4f1f8-134">Header</span><span class="sxs-lookup"><span data-stu-id="4f1f8-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f1f8-135"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="4f1f8-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4f1f8-136">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="4f1f8-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="4f1f8-137"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4f1f8-137"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4f1f8-138">DLL</span><span class="sxs-lookup"><span data-stu-id="4f1f8-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f1f8-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f1f8-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4f1f8-140">IID</span><span class="sxs-lookup"><span data-stu-id="4f1f8-140">IID</span></span><br/>                      | <span data-ttu-id="4f1f8-141">IID \_ ibytebuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.</span><span class="sxs-lookup"><span data-stu-id="4f1f8-141">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

