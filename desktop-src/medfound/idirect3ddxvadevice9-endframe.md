---
description: Beendet die Verarbeitung zum Erstellen eines decodierten Bilds.
ms.assetid: 4b47cd53-6ce0-47b0-83ed-84926e92430f
title: 'IDirect3DDXVADevice9:: Endframe-Methode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.EndFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: a6a737fe6c4c3020b7ebfe7fee98281e6c83f168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130344"
---
# <a name="idirect3ddxvadevice9endframe-method"></a><span data-ttu-id="44459-103">IDirect3DDXVADevice9:: Endframe-Methode</span><span class="sxs-lookup"><span data-stu-id="44459-103">IDirect3DDXVADevice9::EndFrame method</span></span>

<span data-ttu-id="44459-104">Beendet die Verarbeitung zum Erstellen eines decodierten Bilds.</span><span class="sxs-lookup"><span data-stu-id="44459-104">Ends the processing to create a decoded picture.</span></span>

## <a name="syntax"></a><span data-ttu-id="44459-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="44459-105">Syntax</span></span>


```C++
HRESULT EndFrame(
   DWORD SizeMiscData,
   VOID  *pMiscData
);
```



## <a name="parameters"></a><span data-ttu-id="44459-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="44459-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44459-107">*Sizefehldata*</span><span class="sxs-lookup"><span data-stu-id="44459-107">*SizeMiscData*</span></span> 
</dt> <dd>

<span data-ttu-id="44459-108">Die Größe des von *pfehldata* angegebenen Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="44459-108">The size of the buffer specified by *pMiscData*, in bytes.</span></span> <span data-ttu-id="44459-109">Der Wert muss 2 sein.</span><span class="sxs-lookup"><span data-stu-id="44459-109">The value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="44459-110">*pfehldaten*</span><span class="sxs-lookup"><span data-stu-id="44459-110">*pMiscData*</span></span> 
</dt> <dd>

<span data-ttu-id="44459-111">Zeiger auf einen Puffer, der Daten für die Video Zugriffstaste enthält.</span><span class="sxs-lookup"><span data-stu-id="44459-111">Pointer to a buffer that contains data for the video accelerator.</span></span> <span data-ttu-id="44459-112">Dieser Puffer muss den gleichen Frame Index enthalten, der der [**IDirect3DDXVADevice9:: beginFrame**](idirect3ddxvadevice9-beginframe.md) -Methode im *pinputdata* -Parameter übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="44459-112">This buffer must contain the same frame index that was passed to the [**IDirect3DDXVADevice9::BeginFrame**](idirect3ddxvadevice9-beginframe.md) method in the *pInputData* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44459-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44459-113">Return value</span></span>

<span data-ttu-id="44459-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="44459-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="44459-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="44459-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="44459-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44459-116">Requirements</span></span>



| <span data-ttu-id="44459-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44459-117">Requirement</span></span> | <span data-ttu-id="44459-118">Wert</span><span class="sxs-lookup"><span data-stu-id="44459-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="44459-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44459-119">Minimum supported client</span></span><br/> | <span data-ttu-id="44459-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44459-120">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="44459-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44459-121">Minimum supported server</span></span><br/> | <span data-ttu-id="44459-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44459-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="44459-123">Header</span><span class="sxs-lookup"><span data-stu-id="44459-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="44459-124"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="44459-124"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44459-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44459-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44459-126">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="44459-126">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




