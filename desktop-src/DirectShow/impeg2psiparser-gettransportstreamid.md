---
description: Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.
ms.assetid: 0c35abc0-984f-42df-a2a2-30cd400d4599
title: 'IMpeg2PsiParser:: gettransportstreamid-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetTransportStreamId
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9615c50d8d16aa6d78e3e1b83a3ec0e356c6cb50
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344922"
---
# <a name="impeg2psiparsergettransportstreamid-method"></a><span data-ttu-id="eef6c-104">IMpeg2PsiParser:: gettransportstreamid-Methode</span><span class="sxs-lookup"><span data-stu-id="eef6c-104">IMpeg2PsiParser::GetTransportStreamId method</span></span>

<span data-ttu-id="eef6c-105">Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="eef6c-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="eef6c-106">Es handelt sich nicht um eine unterstützte DirectShow-API.</span><span class="sxs-lookup"><span data-stu-id="eef6c-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="eef6c-107">Die- `GetTransportStreamId` Methode ruft das Transportdaten \_ Strom-ID- \_ Feld aus der PAT-Datei ab.</span><span class="sxs-lookup"><span data-stu-id="eef6c-107">The `GetTransportStreamId` method retrieves the transport\_stream\_id field from the PAT.</span></span> <span data-ttu-id="eef6c-108">Dieser Wert wird vom Benutzer definiert und kann verwendet werden, um einen bestimmten Transportstream von anderen Datenströmen im gleichen Netzwerk zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="eef6c-108">This value is defined by the user, and can be used to distinguish a particular transport stream from other streams on the same network.</span></span> <span data-ttu-id="eef6c-109">Ein Transportstream enthält höchstens einen Pat.</span><span class="sxs-lookup"><span data-stu-id="eef6c-109">A transport stream contains at most one PAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="eef6c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="eef6c-110">Syntax</span></span>


```C++
HRESULT GetTransportStreamId(
  [out] WORD *pStreamId
);
```



## <a name="parameters"></a><span data-ttu-id="eef6c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="eef6c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eef6c-112">*pstreamid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="eef6c-112">*pStreamId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eef6c-113">Ein Zeiger auf eine Variable, die das \_ Transportstream- \_ ID-Feld empfängt.</span><span class="sxs-lookup"><span data-stu-id="eef6c-113">Pointer to a variable that receives the transport\_stream\_id field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eef6c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eef6c-114">Return value</span></span>

<span data-ttu-id="eef6c-115">Die-Methode gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="eef6c-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="eef6c-116">Mögliche Werte sind u. a. die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="eef6c-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="eef6c-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="eef6c-117">Return code</span></span>                                                                          | <span data-ttu-id="eef6c-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eef6c-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="eef6c-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="eef6c-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="eef6c-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="eef6c-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="eef6c-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eef6c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eef6c-122">**IMpeg2PsiParser-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="eef6c-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="eef6c-123">Beispiel für PSI-Parser-Filter</span><span class="sxs-lookup"><span data-stu-id="eef6c-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




