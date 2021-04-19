---
description: Ruft den Fehlerstatus ab, der der Medien schlüsselsitzung zugeordnet ist.
ms.assetid: 4693b7d5-59ee-472f-83fc-1ecbcc165dac
title: 'IMF mediakeysession:: GetError-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.GetError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 4f0a42601698a9cd62dc6cb23ca9e69ac2cc8a49
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106363037"
---
# <a name="imfmediakeysessiongeterror-method"></a><span data-ttu-id="4d341-103">IMF mediakeysession:: GetError-Methode</span><span class="sxs-lookup"><span data-stu-id="4d341-103">IMFMediaKeySession::GetError method</span></span>

<span data-ttu-id="4d341-104">Ruft den Fehlerstatus ab, der der Medien schlüsselsitzung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4d341-104">Gets the error state associated with the media key session.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d341-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d341-105">Syntax</span></span>


```C++
HRESULT GetError(
   USHORT *code,
   DWORD  *systemCode
);
```



## <a name="parameters"></a><span data-ttu-id="4d341-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d341-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d341-107">*code*</span><span class="sxs-lookup"><span data-stu-id="4d341-107">*code*</span></span> 
</dt> <dd>

<span data-ttu-id="4d341-108">Der Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="4d341-108">The error code.</span></span>

</dd> <dt>

<span data-ttu-id="4d341-109">*Systemcode*</span><span class="sxs-lookup"><span data-stu-id="4d341-109">*systemCode*</span></span> 
</dt> <dd>

<span data-ttu-id="4d341-110">Plattformspezifische Fehlerinformationen.</span><span class="sxs-lookup"><span data-stu-id="4d341-110">Platform specific error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d341-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d341-111">Return value</span></span>

<span data-ttu-id="4d341-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="4d341-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4d341-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4d341-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d341-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d341-114">Requirements</span></span>



| <span data-ttu-id="4d341-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d341-115">Requirement</span></span> | <span data-ttu-id="4d341-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4d341-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d341-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4d341-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4d341-118">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="4d341-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4d341-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4d341-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4d341-120">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4d341-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4d341-121">IDL</span><span class="sxs-lookup"><span data-stu-id="4d341-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4d341-122"><dt>MF mediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4d341-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d341-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d341-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d341-124">**IMF mediakeysession**</span><span class="sxs-lookup"><span data-stu-id="4d341-124">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




