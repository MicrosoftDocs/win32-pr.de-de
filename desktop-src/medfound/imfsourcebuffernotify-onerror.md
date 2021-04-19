---
description: Wird verwendet, um anzugeben, dass ein Fehler im Quell Puffer aufgetreten ist.
ms.assetid: a7187b7a-0090-4380-82bb-a7f72d54232e
title: 'IMF sourcebuffernotify:: OnError-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBufferNotify.OnError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 8b5f48c3517eb62b0a70acb9cbb28a5ecf7c90cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348832"
---
# <a name="imfsourcebuffernotifyonerror-method"></a><span data-ttu-id="1a825-103">IMF sourcebuffernotify:: OnError-Methode</span><span class="sxs-lookup"><span data-stu-id="1a825-103">IMFSourceBufferNotify::OnError method</span></span>

<span data-ttu-id="1a825-104">Wird verwendet, um anzugeben, dass ein Fehler im Quell Puffer aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="1a825-104">Used to indicate that an error has occurred with the source buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a825-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a825-105">Syntax</span></span>


```C++
void OnError(
  [in] HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="1a825-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a825-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a825-107">*Personalabteilung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a825-107">*hr* \[in\]</span></span>
<span data-ttu-id="1a825-108"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1a825-108"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="1a825-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a825-109">Return value</span></span>

<span data-ttu-id="1a825-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1a825-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a825-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a825-111">Requirements</span></span>



| <span data-ttu-id="1a825-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a825-112">Requirement</span></span> | <span data-ttu-id="1a825-113">Wert</span><span class="sxs-lookup"><span data-stu-id="1a825-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a825-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1a825-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1a825-115">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="1a825-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1a825-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1a825-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1a825-117">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1a825-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1a825-118">IDL</span><span class="sxs-lookup"><span data-stu-id="1a825-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1a825-119"><dt>MF mediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1a825-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a825-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a825-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a825-121">**IMF sourcebuffernotify**</span><span class="sxs-lookup"><span data-stu-id="1a825-121">**IMFSourceBufferNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffernotify)
</dt> </dl>

 

 




