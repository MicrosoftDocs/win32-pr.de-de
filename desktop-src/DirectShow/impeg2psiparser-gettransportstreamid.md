---
description: 'IMpeg2PsiParser::GetTransportStreamId-Methode: Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.'
ms.assetid: 0c35abc0-984f-42df-a2a2-30cd400d4599
title: IMpeg2PsiParser::GetTransportStreamId-Methode
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
ms.openlocfilehash: a24253b021abacf398a3a169b63bbb2f01ec2354
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084568"
---
# <a name="impeg2psiparsergettransportstreamid-method"></a><span data-ttu-id="57f1e-104">IMpeg2PsiParser::GetTransportStreamId-Methode</span><span class="sxs-lookup"><span data-stu-id="57f1e-104">IMpeg2PsiParser::GetTransportStreamId method</span></span>

<span data-ttu-id="57f1e-105">Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="57f1e-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="57f1e-106">Es handelt sich nicht um eine unterstützte DirectShow-API.</span><span class="sxs-lookup"><span data-stu-id="57f1e-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="57f1e-107">Die `GetTransportStreamId` -Methode ruft das Feld für die \_ \_ Transportstream-ID aus dem PAT ab.</span><span class="sxs-lookup"><span data-stu-id="57f1e-107">The `GetTransportStreamId` method retrieves the transport\_stream\_id field from the PAT.</span></span> <span data-ttu-id="57f1e-108">Dieser Wert wird vom Benutzer definiert und kann verwendet werden, um einen bestimmten Transportstream von anderen Datenströmen im gleichen Netzwerk zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="57f1e-108">This value is defined by the user, and can be used to distinguish a particular transport stream from other streams on the same network.</span></span> <span data-ttu-id="57f1e-109">Ein Transportstream enthält mindestens ein PAT.</span><span class="sxs-lookup"><span data-stu-id="57f1e-109">A transport stream contains at most one PAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="57f1e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="57f1e-110">Syntax</span></span>


```C++
HRESULT GetTransportStreamId(
  [out] WORD *pStreamId
);
```



## <a name="parameters"></a><span data-ttu-id="57f1e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="57f1e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57f1e-112">*pStreamId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="57f1e-112">*pStreamId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57f1e-113">Zeiger auf eine Variable, die das Feld für die \_ \_ Transportstream-ID empfängt.</span><span class="sxs-lookup"><span data-stu-id="57f1e-113">Pointer to a variable that receives the transport\_stream\_id field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57f1e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57f1e-114">Return value</span></span>

<span data-ttu-id="57f1e-115">Die -Methode gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="57f1e-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="57f1e-116">Mögliche Werte sind, aber nicht beschränkt auf, die in der folgenden Tabelle gezeigten Werte.</span><span class="sxs-lookup"><span data-stu-id="57f1e-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="57f1e-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="57f1e-117">Return code</span></span>                                                                          | <span data-ttu-id="57f1e-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57f1e-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="57f1e-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="57f1e-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="57f1e-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="57f1e-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="57f1e-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="57f1e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57f1e-122">**IMpeg2PsiParser-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="57f1e-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="57f1e-123">BEISPIEL FÜR PSI-Parserfilter</span><span class="sxs-lookup"><span data-stu-id="57f1e-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




