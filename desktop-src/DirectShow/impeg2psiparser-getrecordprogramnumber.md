---
description: Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.
ms.assetid: 3800a0b1-a581-40ed-81ab-3d5f77f442df
title: 'IMpeg2PsiParser:: getrecordprogramnumber-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetRecordProgramNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2bedc5922ce90fa2fda612f30571f884e75841d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346807"
---
# <a name="impeg2psiparsergetrecordprogramnumber-method"></a><span data-ttu-id="c5e0e-104">IMpeg2PsiParser:: getrecordprogramnumber-Methode</span><span class="sxs-lookup"><span data-stu-id="c5e0e-104">IMpeg2PsiParser::GetRecordProgramNumber method</span></span>

<span data-ttu-id="c5e0e-105">Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c5e0e-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="c5e0e-106">Es handelt sich nicht um eine unterstützte DirectShow-API.</span><span class="sxs-lookup"><span data-stu-id="c5e0e-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="c5e0e-107">Die- `GetRecordProgramNumber` Methode ruft die Programmnummer für ein angegebenes Programm ab.</span><span class="sxs-lookup"><span data-stu-id="c5e0e-107">The `GetRecordProgramNumber` method retrieves the program number for a specified program.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5e0e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5e0e-108">Syntax</span></span>


```C++
HRESULT GetRecordProgramNumber(
  [in]  DWORD dwIndex,
  [out] WORD  *pwVal
);
```



## <a name="parameters"></a><span data-ttu-id="c5e0e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5e0e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5e0e-110">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5e0e-110">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5e0e-111">Gibt den Eintrag in Pat an, der das Programm definiert, das von 0 (null) indiziert wird.</span><span class="sxs-lookup"><span data-stu-id="c5e0e-111">Specifies the entry in the PAT that defines the program, indexed from zero.</span></span>

</dd> <dt>

<span data-ttu-id="c5e0e-112">*pwval* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c5e0e-112">*pwVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5e0e-113">Ein Zeiger auf eine Variable, die das Programm \_ Nummern Feld von Pat empfängt.</span><span class="sxs-lookup"><span data-stu-id="c5e0e-113">Pointer to a variable that receives the program\_number field from the PAT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5e0e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5e0e-114">Return value</span></span>

<span data-ttu-id="c5e0e-115">Die-Methode gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c5e0e-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="c5e0e-116">Mögliche Werte sind u. a. die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="c5e0e-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="c5e0e-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c5e0e-117">Return code</span></span>                                                                          | <span data-ttu-id="c5e0e-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5e0e-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="c5e0e-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c5e0e-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c5e0e-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="c5e0e-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="c5e0e-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5e0e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5e0e-122">**IMpeg2PsiParser-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c5e0e-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="c5e0e-123">Beispiel für PSI-Parser-Filter</span><span class="sxs-lookup"><span data-stu-id="c5e0e-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




