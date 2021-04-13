---
description: Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.
ms.assetid: 2f5ad9bf-3d70-491a-ab45-15cd922a02d4
title: 'IMpeg2PsiParser:: getpatversionnumber-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPatVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6117060cf0c8d3c56d03e5838376485244fde8d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392449"
---
# <a name="impeg2psiparsergetpatversionnumber-method"></a><span data-ttu-id="2778a-104">IMpeg2PsiParser:: getpatversionnumber-Methode</span><span class="sxs-lookup"><span data-stu-id="2778a-104">IMpeg2PsiParser::GetPatVersionNumber method</span></span>

<span data-ttu-id="2778a-105">Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="2778a-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="2778a-106">Es handelt sich nicht um eine unterstützte DirectShow-API.</span><span class="sxs-lookup"><span data-stu-id="2778a-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="2778a-107">Die- `GetPatVersionNumber` Methode ruft das Feld mit der Versions \_ Nummer von Pat ab.</span><span class="sxs-lookup"><span data-stu-id="2778a-107">The `GetPatVersionNumber` method retrieves the version\_number field from the PAT.</span></span> <span data-ttu-id="2778a-108">Ein Transportstream enthält höchstens einen Pat.</span><span class="sxs-lookup"><span data-stu-id="2778a-108">A transport stream contains at most one PAT.</span></span> <span data-ttu-id="2778a-109">Die Versionsnummer wird jedes Mal inkrementiert, wenn sich die Informationen in der Tabelle ändern.</span><span class="sxs-lookup"><span data-stu-id="2778a-109">The version number is incremented whenever the information in the table changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="2778a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="2778a-110">Syntax</span></span>


```C++
HRESULT GetPatVersionNumber(
  [out] BYTE *pPatVersion
);
```



## <a name="parameters"></a><span data-ttu-id="2778a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2778a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2778a-112">*ppatversion* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2778a-112">*pPatVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2778a-113">Ein Zeiger auf eine Variable, die das Feld mit der Versions \_ Nummer empfängt.</span><span class="sxs-lookup"><span data-stu-id="2778a-113">Pointer to a variable that receives the version\_number field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2778a-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2778a-114">Return value</span></span>

<span data-ttu-id="2778a-115">Die-Methode gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2778a-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="2778a-116">Mögliche Werte sind u. a. die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="2778a-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="2778a-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2778a-117">Return code</span></span>                                                                          | <span data-ttu-id="2778a-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2778a-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="2778a-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2778a-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2778a-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="2778a-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="2778a-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2778a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2778a-122">**IMpeg2PsiParser-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="2778a-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="2778a-123">Beispiel für PSI-Parser-Filter</span><span class="sxs-lookup"><span data-stu-id="2778a-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




