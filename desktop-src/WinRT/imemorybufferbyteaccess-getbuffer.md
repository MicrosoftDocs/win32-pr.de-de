---
description: Ruft ein imemorybuffer-Element als Bytearray ab.
ms.assetid: E9C2AF2D-ADBE-4D76-A549-2DBCB9818B09
title: 'Imemorybufferbyteaccess:: GetBuffer-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMemoryBufferByteAccess.GetBuffer
api_type:
- COM
api_location: ''
ms.openlocfilehash: f31d1506822f21977e2d60492248c2d70a51829c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353074"
---
# <a name="imemorybufferbyteaccessgetbuffer-method"></a><span data-ttu-id="bd5f6-103">Imemorybufferbyteaccess:: GetBuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="bd5f6-103">IMemoryBufferByteAccess::GetBuffer method</span></span>

<span data-ttu-id="bd5f6-104">Ruft ein [**imemorybuffer**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) -Element als Bytearray ab.</span><span class="sxs-lookup"><span data-stu-id="bd5f6-104">Gets an [**IMemoryBuffer**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) as an array of bytes.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd5f6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd5f6-105">Syntax</span></span>


```C++
HRESULT GetBuffer(
  [out] BYTE   **value,
  [out] UINT32 *capacity
);
```



## <a name="parameters"></a><span data-ttu-id="bd5f6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd5f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd5f6-107">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bd5f6-107">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd5f6-108">Ein Zeiger auf ein Bytearray, das die Puffer Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="bd5f6-108">A pointer to a byte array containing the buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="bd5f6-109">*Kapazität* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bd5f6-109">*capacity* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd5f6-110">Die Anzahl der Bytes im zurückgegebenen Array.</span><span class="sxs-lookup"><span data-stu-id="bd5f6-110">The number of bytes in the returned array</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd5f6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd5f6-111">Return value</span></span>

<span data-ttu-id="bd5f6-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="bd5f6-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bd5f6-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bd5f6-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd5f6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd5f6-114">Remarks</span></span>

<span data-ttu-id="bd5f6-115">Wenn [**memorybuffer:: Close**](/uwp/api/Windows.Foundation.MemoryBuffer?view=winrt-19041) aufgerufen wird, sollte der Code, der diesen Puffer verwendet, den *Wert* Zeiger auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="bd5f6-115">When [**MemoryBuffer::Close**](/uwp/api/Windows.Foundation.MemoryBuffer?view=winrt-19041) is called, the code using this buffer should set the *value* pointer to null.</span></span>

## <a name="see-also"></a><span data-ttu-id="bd5f6-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd5f6-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="bd5f6-117">[**Imemorybufferbyteaccess**](/previous-versions//mt297505(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bd5f6-117">[**IMemoryBufferByteAccess**](/previous-versions//mt297505(v=vs.85))</span></span>
</dt> </dl>

 

 
