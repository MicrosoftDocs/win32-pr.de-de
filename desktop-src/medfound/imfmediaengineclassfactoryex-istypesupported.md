---
description: Ruft einen Wert ab, der angibt, ob das angegebene Schlüsselsystem den angegebenen Medientyp unterstützt.
ms.assetid: 6f4f50db-e491-46c2-a8b2-1b8e51033b5b
title: 'IMF mediaengineclassfactoryex:: istypesupportiert-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineClassFactoryEx.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 92bf3d64d36c043e9e33b897294ff74a3fda0445
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354900"
---
# <a name="imfmediaengineclassfactoryexistypesupported-method"></a><span data-ttu-id="b5a0b-103">IMF mediaengineclassfactoryex:: istypesupportiert-Methode</span><span class="sxs-lookup"><span data-stu-id="b5a0b-103">IMFMediaEngineClassFactoryEx::IsTypeSupported method</span></span>

<span data-ttu-id="b5a0b-104">Ruft einen Wert ab, der angibt, ob das angegebene Schlüsselsystem den angegebenen Medientyp unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b5a0b-104">Gets a value that indicates if the specified key system supports the specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5a0b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5a0b-105">Syntax</span></span>


```C++
HRESULT IsTypeSupported(
   BSTR type,
   BSTR keySystem,
   BOOL *isSupported
);
```



## <a name="parameters"></a><span data-ttu-id="b5a0b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5a0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5a0b-107">*type*</span><span class="sxs-lookup"><span data-stu-id="b5a0b-107">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="b5a0b-108">Der MIME-Typ, für den Unterstützung überprüft werden soll</span><span class="sxs-lookup"><span data-stu-id="b5a0b-108">The MIME type to check support for.</span></span>

</dd> <dt>

<span data-ttu-id="b5a0b-109">*Keysystem*</span><span class="sxs-lookup"><span data-stu-id="b5a0b-109">*keySystem*</span></span> 
</dt> <dd>

<span data-ttu-id="b5a0b-110">Das Schlüsselsystem, für das die Unterstützung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="b5a0b-110">The key system to check support for.</span></span>

</dd> <dt>

<span data-ttu-id="b5a0b-111">*isSupported*</span><span class="sxs-lookup"><span data-stu-id="b5a0b-111">*isSupported*</span></span> 
</dt> <dd>

<span data-ttu-id="b5a0b-112">**true** , wenn der Typ von *Keysystem* unterstützt wird. andernfalls **false.**</span><span class="sxs-lookup"><span data-stu-id="b5a0b-112">**true** if type is supported by *keySystem*; otherwise, **false.**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5a0b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5a0b-113">Return value</span></span>

<span data-ttu-id="b5a0b-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="b5a0b-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b5a0b-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b5a0b-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5a0b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5a0b-116">Requirements</span></span>



| <span data-ttu-id="b5a0b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5a0b-117">Requirement</span></span> | <span data-ttu-id="b5a0b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b5a0b-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5a0b-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b5a0b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b5a0b-120">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="b5a0b-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b5a0b-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b5a0b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b5a0b-122">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5a0b-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b5a0b-123">IDL</span><span class="sxs-lookup"><span data-stu-id="b5a0b-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b5a0b-124"><dt>MF mediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b5a0b-124"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5a0b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5a0b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5a0b-126">**IMF mediaengineclassfacrenyex**</span><span class="sxs-lookup"><span data-stu-id="b5a0b-126">**IMFMediaEngineClassFactoryEx**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactoryex)
</dt> </dl>

 

 




