---
description: Die \_ Methode Get Leuchtdichte Ruft den Wert für die Leuchtkraft ab, nach dem der Schlüssel abgerufen werden soll. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp dxtkey- \_ Beleuchtung ist.
ms.assetid: 92113331-a7b7-4618-81b2-ea02e7bcc923
title: 'Idxtkey:: get_Luminance-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Luminance
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 85dcba3720e007d0f3de890c085b0b223e3df350
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352934"
---
# <a name="idxtkeyget_luminance-method"></a><span data-ttu-id="5f22e-104">Idxtkey:: get- \_ Methode "Luminance"</span><span class="sxs-lookup"><span data-stu-id="5f22e-104">IDxtKey::get\_Luminance method</span></span>

> [!Note]  
> <span data-ttu-id="5f22e-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="5f22e-105">\[Deprecated.</span></span> <span data-ttu-id="5f22e-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="5f22e-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5f22e-107">Die- `get_Luminance` Methode ruft den Wert der Leuchtkraft ab, nach dem der Schlüssel abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f22e-107">The `get_Luminance` method retrieves the luminance value on which to key.</span></span> <span data-ttu-id="5f22e-108">Diese Eigenschaft gilt nur, wenn der Schlüsseltyp dxtkey- \_ Beleuchtung ist.</span><span class="sxs-lookup"><span data-stu-id="5f22e-108">This property applies only when the key type is DXTKEY\_LUMINANCE.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f22e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f22e-109">Syntax</span></span>


```C++
HRESULT get_Luminance(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="5f22e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f22e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f22e-111">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5f22e-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5f22e-112">Empfängt den Wert für die Leuchtkraft, auf den die Taste geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="5f22e-112">Receives the luminance value on which to key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f22e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f22e-113">Return value</span></span>

<span data-ttu-id="5f22e-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="5f22e-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5f22e-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5f22e-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f22e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f22e-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5f22e-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="5f22e-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5f22e-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="5f22e-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5f22e-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5f22e-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5f22e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f22e-120">Requirements</span></span>



| <span data-ttu-id="5f22e-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f22e-121">Requirement</span></span> | <span data-ttu-id="5f22e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="5f22e-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f22e-123">Header</span><span class="sxs-lookup"><span data-stu-id="5f22e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5f22e-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="5f22e-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5f22e-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5f22e-125">Library</span></span><br/> | <dl> <span data-ttu-id="5f22e-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="5f22e-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f22e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f22e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f22e-128">**Idxtkey-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5f22e-128">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="5f22e-129">**Idxtkey:: get \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="5f22e-129">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 




