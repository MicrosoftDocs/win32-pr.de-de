---
description: Erstellt einen Enumerator für die Übertragungs Formate, die vom Windows-Abbild Erfassungsgerät (WIA) 2,0 unterstützt werden.
ms.assetid: 70fffc7b-b500-4404-9d94-76d1828ddc8c
title: 'Iwiatransfer:: EnumWIA_FORMAT_INFO-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.EnumWIA_FORMAT_INFO
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 66f3c91d6023655daf85b2a0d726d98a685b001b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354497"
---
# <a name="iwiatransferenumwia_format_info-method"></a><span data-ttu-id="fc8dd-103">Iwiatransfer:: enumwia- \_ Format \_ Info-Methode</span><span class="sxs-lookup"><span data-stu-id="fc8dd-103">IWiaTransfer::EnumWIA\_FORMAT\_INFO method</span></span>

<span data-ttu-id="fc8dd-104">Erstellt einen Enumerator für die Übertragungs Formate, die vom Windows-Abbild Erfassungsgerät (WIA) 2,0 unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="fc8dd-104">Creates an enumerator for the transfer formats that the Windows Image Acquisition (WIA) 2.0 device supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc8dd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc8dd-105">Syntax</span></span>


```C++
HRESULT EnumWIA_FORMAT_INFO(
  [out] IEnumWIA_FORMAT_INFO **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="fc8dd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc8dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc8dd-107">*ppiumum* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fc8dd-107">*ppIEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc8dd-108">Typ: **[ **ienumwia- \_ Format \_ Informationen**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info)\*\***</span><span class="sxs-lookup"><span data-stu-id="fc8dd-108">Type: **[**IEnumWIA\_FORMAT\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info)\*\***</span></span>

<span data-ttu-id="fc8dd-109">Die Adresse des Zeigers auf die [**ienumwia- \_ Format \_ Info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) -Schnittstelle für den Enumerator.</span><span class="sxs-lookup"><span data-stu-id="fc8dd-109">The address of the pointer to the [**IEnumWIA\_FORMAT\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) interface for the enumerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc8dd-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fc8dd-110">Return value</span></span>

<span data-ttu-id="fc8dd-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fc8dd-111">Type: **HRESULT**</span></span>

<span data-ttu-id="fc8dd-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="fc8dd-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fc8dd-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fc8dd-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc8dd-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc8dd-114">Remarks</span></span>

<span data-ttu-id="fc8dd-115">Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für den Schnittstellen Zeiger aufrufen, der über den *ppienum* -Parameter empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="fc8dd-115">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointer received through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc8dd-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc8dd-116">Requirements</span></span>



| <span data-ttu-id="fc8dd-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc8dd-117">Requirement</span></span> | <span data-ttu-id="fc8dd-118">Wert</span><span class="sxs-lookup"><span data-stu-id="fc8dd-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc8dd-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fc8dd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fc8dd-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc8dd-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fc8dd-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fc8dd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fc8dd-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc8dd-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fc8dd-123">Header</span><span class="sxs-lookup"><span data-stu-id="fc8dd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc8dd-124"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc8dd-124"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="fc8dd-125">IDL</span><span class="sxs-lookup"><span data-stu-id="fc8dd-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fc8dd-126"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fc8dd-126"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="fc8dd-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fc8dd-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="fc8dd-128"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc8dd-128"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
