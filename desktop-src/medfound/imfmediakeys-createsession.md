---
description: Erstellt mithilfe der angegebenen Initialisierungs Daten und benutzerdefinierten Daten ein Medien Schlüssel-Sitzungs Objekt. .
ms.assetid: 9f11433c-7cff-4a59-9d4a-7f4b56ba62cf
title: 'IMF Media Keys:: foratesession-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeys.CreateSession
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 89d3abce0c1c15d472f7008fa0ef2c5f27bba6ad
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106366372"
---
# <a name="imfmediakeyscreatesession-method"></a><span data-ttu-id="5c7d9-104">IMF Media Keys:: foratesession-Methode</span><span class="sxs-lookup"><span data-stu-id="5c7d9-104">IMFMediaKeys::CreateSession method</span></span>

<span data-ttu-id="5c7d9-105">Erstellt mithilfe der angegebenen Initialisierungs Daten und benutzerdefinierten Daten ein Medien Schlüssel-Sitzungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="5c7d9-105">Creates a media key session object using the specified initialization data and custom data.</span></span> <span data-ttu-id="5c7d9-106">.</span><span class="sxs-lookup"><span data-stu-id="5c7d9-106">.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c7d9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c7d9-107">Syntax</span></span>


```C++
HRESULT CreateSession(
         BSTR                     mimeType,
   const BYTE                     *initData,
         DWORD                    cb,
   const BYTE                     *customData,
         DWORD                    cbCustomData,
         IMFMediaKeySessionNotify *notify,
         IMFMediaKeySession       **ppSession
);
```



## <a name="parameters"></a><span data-ttu-id="5c7d9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c7d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c7d9-109">*mimeType*</span><span class="sxs-lookup"><span data-stu-id="5c7d9-109">*mimeType*</span></span> 
</dt> <dd>

<span data-ttu-id="5c7d9-110">Der MIME-Typ des Medien Containers, der für den Inhalt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5c7d9-110">The MIME type of the media container used for the content.</span></span>

</dd> <dt>

<span data-ttu-id="5c7d9-111">*initData*</span><span class="sxs-lookup"><span data-stu-id="5c7d9-111">*initData*</span></span> 
</dt> <dd>

<span data-ttu-id="5c7d9-112">Die Initialisierungs Daten für das Schlüsselsystem.</span><span class="sxs-lookup"><span data-stu-id="5c7d9-112">The initialization data for the key system.</span></span>

</dd> <dt>

<span data-ttu-id="5c7d9-113">*betrieben*</span><span class="sxs-lookup"><span data-stu-id="5c7d9-113">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="5c7d9-114">Die Anzahl in Bytes von *initdata*.</span><span class="sxs-lookup"><span data-stu-id="5c7d9-114">The count in bytes of *initData*.</span></span>

</dd> <dt>

<span data-ttu-id="5c7d9-115">*CustomData*</span><span class="sxs-lookup"><span data-stu-id="5c7d9-115">*customData*</span></span> 
</dt> <dd>

<span data-ttu-id="5c7d9-116">Benutzerdefinierte Daten, die an das Schlüsselsystem gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="5c7d9-116">Custom data sent to the key system.</span></span>

</dd> <dt>

<span data-ttu-id="5c7d9-117">*cbcustomdata*</span><span class="sxs-lookup"><span data-stu-id="5c7d9-117">*cbCustomData*</span></span> 
</dt> <dd>

<span data-ttu-id="5c7d9-118">Die Anzahl in Bytes von *cbcustomdata*.</span><span class="sxs-lookup"><span data-stu-id="5c7d9-118">The count in bytes of *cbCustomData*.</span></span>

</dd> <dt>

<span data-ttu-id="5c7d9-119">*informiert*</span><span class="sxs-lookup"><span data-stu-id="5c7d9-119">*notify*</span></span> 
</dt> <dd>

<span data-ttu-id="5c7d9-120">informiert</span><span class="sxs-lookup"><span data-stu-id="5c7d9-120">notify</span></span>

</dd> <dt>

<span data-ttu-id="5c7d9-121">*ppSession*</span><span class="sxs-lookup"><span data-stu-id="5c7d9-121">*ppSession*</span></span> 
</dt> <dd>

<span data-ttu-id="5c7d9-122">Die Medien schlüsselsitzung.</span><span class="sxs-lookup"><span data-stu-id="5c7d9-122">The media key session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c7d9-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c7d9-123">Return value</span></span>

<span data-ttu-id="5c7d9-124">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="5c7d9-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5c7d9-125">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5c7d9-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c7d9-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c7d9-126">Requirements</span></span>



| <span data-ttu-id="5c7d9-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c7d9-127">Requirement</span></span> | <span data-ttu-id="5c7d9-128">Wert</span><span class="sxs-lookup"><span data-stu-id="5c7d9-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c7d9-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c7d9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5c7d9-130">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="5c7d9-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5c7d9-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c7d9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5c7d9-132">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c7d9-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5c7d9-133">IDL</span><span class="sxs-lookup"><span data-stu-id="5c7d9-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5c7d9-134"><dt>MF mediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5c7d9-134"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c7d9-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c7d9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c7d9-136">**IMF Media Keys**</span><span class="sxs-lookup"><span data-stu-id="5c7d9-136">**IMFMediaKeys**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




