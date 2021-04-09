---
description: Definiert die verschiedenen Fehlerzustände der Medienquellen Erweiterung.
ms.assetid: 8FD54833-F60B-49E8-A673-6130F3B06160
title: MF_MSE_ERROR-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_ERROR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 6b6aaea772376b0e57c006a56a5a1bb30bc497c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130717"
---
# <a name="mf_mse_error-enumeration"></a><span data-ttu-id="42c34-103">MF- \_ MSE- \_ Fehler Enumeration</span><span class="sxs-lookup"><span data-stu-id="42c34-103">MF\_MSE\_ERROR enumeration</span></span>

<span data-ttu-id="42c34-104">Definiert die verschiedenen Fehlerzustände der Medienquellen Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="42c34-104">Defines the different error states of the Media Source Extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="42c34-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="42c34-105">Syntax</span></span>


```C++
typedef enum _MF_MSE_ERROR { 
  MF_MSE_ERROR_NOERROR        =  0,
  MF_MSE_ERROR_NETWORK        = 1,
  MF_MSE_ERROR_DECODE         = 2,
  MF_MSE_ERROR_UNKNOWN_ERROR  =  3
} MF_MSE_ERROR;
```



## <a name="constants"></a><span data-ttu-id="42c34-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="42c34-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="42c34-107"><span id="MF_MSE_ERROR_NOERROR"></span><span id="mf_mse_error_noerror"></span>**MF- \_ MSE- \_ Fehler \_ noError**</span><span class="sxs-lookup"><span data-stu-id="42c34-107"><span id="MF_MSE_ERROR_NOERROR"></span><span id="mf_mse_error_noerror"></span>**MF\_MSE\_ERROR\_NOERROR**</span></span>
</dt> <dd>

<span data-ttu-id="42c34-108">Gibt keinen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="42c34-108">Specifies no error.</span></span>

</dd> <dt>

<span data-ttu-id="42c34-109"><span id="MF_MSE_ERROR_NETWORK"></span><span id="mf_mse_error_network"></span>**Netzwerk für MF- \_ MSE- \_ Fehler \_**</span><span class="sxs-lookup"><span data-stu-id="42c34-109"><span id="MF_MSE_ERROR_NETWORK"></span><span id="mf_mse_error_network"></span>**MF\_MSE\_ERROR\_NETWORK**</span></span>
</dt> <dd>

<span data-ttu-id="42c34-110">Gibt einen Fehler im Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="42c34-110">Specifies an error with the network.</span></span>

</dd> <dt>

<span data-ttu-id="42c34-111"><span id="MF_MSE_ERROR_DECODE"></span><span id="mf_mse_error_decode"></span>**\_ \_ Fehler beim \_ Decodieren von MF-MSE**</span><span class="sxs-lookup"><span data-stu-id="42c34-111"><span id="MF_MSE_ERROR_DECODE"></span><span id="mf_mse_error_decode"></span>**MF\_MSE\_ERROR\_DECODE**</span></span>
</dt> <dd>

<span data-ttu-id="42c34-112">Gibt einen Fehler beim Decodieren an.</span><span class="sxs-lookup"><span data-stu-id="42c34-112">Specifies an error with decoding.</span></span>

</dd> <dt>

<span data-ttu-id="42c34-113"><span id="MF_MSE_ERROR_UNKNOWN_ERROR"></span><span id="mf_mse_error_unknown_error"></span>**Unbekannter Fehler im MF-MSE-Fehler. \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="42c34-113"><span id="MF_MSE_ERROR_UNKNOWN_ERROR"></span><span id="mf_mse_error_unknown_error"></span>**MF\_MSE\_ERROR\_UNKNOWN\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="42c34-114">Gibt einen unbekannten Fehler an.</span><span class="sxs-lookup"><span data-stu-id="42c34-114">Specifies an unknown error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42c34-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42c34-115">Requirements</span></span>



| <span data-ttu-id="42c34-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42c34-116">Requirement</span></span> | <span data-ttu-id="42c34-117">Wert</span><span class="sxs-lookup"><span data-stu-id="42c34-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="42c34-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42c34-118">Minimum supported client</span></span><br/> | <span data-ttu-id="42c34-119">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="42c34-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="42c34-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42c34-120">Minimum supported server</span></span><br/> | <span data-ttu-id="42c34-121">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42c34-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="42c34-122">IDL</span><span class="sxs-lookup"><span data-stu-id="42c34-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="42c34-123"><dt>MF mediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="42c34-123"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42c34-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42c34-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42c34-125">Media Foundation Enumerationen</span><span class="sxs-lookup"><span data-stu-id="42c34-125">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




