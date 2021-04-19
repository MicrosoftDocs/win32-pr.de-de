---
description: Ruft das Medien Schlüsselobjekt ab, das der Medien-Engine zugeordnet ist, oder NULL, wenn kein Medien Schlüsselobjekt vorhanden ist.
ms.assetid: e6556a02-445d-4436-80de-e4156d6a3d63
title: 'IMF mediaengineeme:: get_Keys-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineEME.get_Keys
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: dcb06352065b28739a616a9f2216c20eedebb913
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106355726"
---
# <a name="imfmediaengineemeget_keys-method"></a><span data-ttu-id="2be9e-103">IMF mediaengineeme:: get \_ Keys-Methode</span><span class="sxs-lookup"><span data-stu-id="2be9e-103">IMFMediaEngineEME::get\_Keys method</span></span>

<span data-ttu-id="2be9e-104">Ruft das Medien Schlüsselobjekt ab, das der Medien-Engine zugeordnet ist, oder **null** , wenn kein Medien Schlüsselobjekt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2be9e-104">Gets the media keys object associated with the media engine or **null** if there is not a media keys object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2be9e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2be9e-105">Syntax</span></span>


```C++
HRESULT get_Keys(
   IMFMediaKeys **keys
);
```



## <a name="parameters"></a><span data-ttu-id="2be9e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2be9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2be9e-107">*or*</span><span class="sxs-lookup"><span data-stu-id="2be9e-107">*keys*</span></span> 
</dt> <dd>

<span data-ttu-id="2be9e-108">Das Media Keys-Objekt, das der Medien-Engine zugeordnet ist, oder **null** , wenn kein Medien Schlüsselobjekt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2be9e-108">The media keys object associated with the media engine or **null** if there is not a media keys object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2be9e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2be9e-109">Return value</span></span>

<span data-ttu-id="2be9e-110">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="2be9e-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2be9e-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2be9e-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2be9e-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2be9e-112">Requirements</span></span>



| <span data-ttu-id="2be9e-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2be9e-113">Requirement</span></span> | <span data-ttu-id="2be9e-114">Wert</span><span class="sxs-lookup"><span data-stu-id="2be9e-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2be9e-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2be9e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2be9e-116">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="2be9e-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2be9e-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2be9e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2be9e-118">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2be9e-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2be9e-119">IDL</span><span class="sxs-lookup"><span data-stu-id="2be9e-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2be9e-120"><dt>MF mediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2be9e-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2be9e-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2be9e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2be9e-122">**IMF mediaengineeme**</span><span class="sxs-lookup"><span data-stu-id="2be9e-122">**IMFMediaEngineEME**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineeme)
</dt> </dl>

 

 




