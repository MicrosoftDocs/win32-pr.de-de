---
description: Ruft einen Wert ab, der angibt, ob der angegebene MIME-Typ von der Medienquelle unterstützt wird.
ms.assetid: 894ef7d2-d008-42e1-8a61-26f35a8877be
title: 'Imfmediasourceextension:: istypesupportiert-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 4c2784dc4e97f96ae28ba56544a7f425de8ce742
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106366553"
---
# <a name="imfmediasourceextensionistypesupported-method"></a><span data-ttu-id="492dc-103">Imfmediasourceextension:: istypesupportiert-Methode</span><span class="sxs-lookup"><span data-stu-id="492dc-103">IMFMediaSourceExtension::IsTypeSupported method</span></span>

<span data-ttu-id="492dc-104">Ruft einen Wert ab, der angibt, ob der angegebene MIME-Typ von der Medienquelle unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="492dc-104">Gets a value that indicates if the specified MIME type is supported by the media source.</span></span>

## <a name="syntax"></a><span data-ttu-id="492dc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="492dc-105">Syntax</span></span>


```C++
BOOL IsTypeSupported(
  [in] BSTR type
);
```



## <a name="parameters"></a><span data-ttu-id="492dc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="492dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="492dc-107">*Typ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="492dc-107">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="492dc-108">Der Medientyp, für den Unterstützung überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="492dc-108">The media type to check support for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="492dc-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="492dc-109">Return value</span></span>

<span data-ttu-id="492dc-110">**true** , wenn der Medientyp unterstützt wird. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="492dc-110">**true** if the media type is supported; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="492dc-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="492dc-111">Requirements</span></span>



| <span data-ttu-id="492dc-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="492dc-112">Requirement</span></span> | <span data-ttu-id="492dc-113">Wert</span><span class="sxs-lookup"><span data-stu-id="492dc-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="492dc-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="492dc-114">Minimum supported client</span></span><br/> | <span data-ttu-id="492dc-115">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="492dc-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="492dc-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="492dc-116">Minimum supported server</span></span><br/> | <span data-ttu-id="492dc-117">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="492dc-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="492dc-118">IDL</span><span class="sxs-lookup"><span data-stu-id="492dc-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="492dc-119"><dt>MF mediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="492dc-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="492dc-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="492dc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="492dc-121">**Imfmediasourceextension**</span><span class="sxs-lookup"><span data-stu-id="492dc-121">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




