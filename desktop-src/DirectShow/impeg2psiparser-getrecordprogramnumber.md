---
description: 'IMpeg2PsiParser::GetRecordProgramNumber-Methode: Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.'
ms.assetid: 3800a0b1-a581-40ed-81ab-3d5f77f442df
title: IMpeg2PsiParser::GetRecordProgramNumber-Methode
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
ms.openlocfilehash: 0fd99178edaa23f2cdf32672a746f79c368b4265
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089138"
---
# <a name="impeg2psiparsergetrecordprogramnumber-method"></a><span data-ttu-id="36188-104">IMpeg2PsiParser::GetRecordProgramNumber-Methode</span><span class="sxs-lookup"><span data-stu-id="36188-104">IMpeg2PsiParser::GetRecordProgramNumber method</span></span>

<span data-ttu-id="36188-105">Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="36188-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="36188-106">Es handelt sich nicht um eine unterstützte DirectShow-API.</span><span class="sxs-lookup"><span data-stu-id="36188-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="36188-107">Die `GetRecordProgramNumber` -Methode ruft die Programmnummer für ein angegebenes Programm ab.</span><span class="sxs-lookup"><span data-stu-id="36188-107">The `GetRecordProgramNumber` method retrieves the program number for a specified program.</span></span>

## <a name="syntax"></a><span data-ttu-id="36188-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="36188-108">Syntax</span></span>


```C++
HRESULT GetRecordProgramNumber(
  [in]  DWORD dwIndex,
  [out] WORD  *pwVal
);
```



## <a name="parameters"></a><span data-ttu-id="36188-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="36188-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36188-110">*dwIndex* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="36188-110">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36188-111">Gibt den Eintrag im PAT an, der das Programm definiert, indiziert von 0 (null).</span><span class="sxs-lookup"><span data-stu-id="36188-111">Specifies the entry in the PAT that defines the program, indexed from zero.</span></span>

</dd> <dt>

<span data-ttu-id="36188-112">*pwVal* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="36188-112">*pwVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36188-113">Zeiger auf eine Variable, die das Programmnummerfeld \_ vom PAT empfängt.</span><span class="sxs-lookup"><span data-stu-id="36188-113">Pointer to a variable that receives the program\_number field from the PAT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36188-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="36188-114">Return value</span></span>

<span data-ttu-id="36188-115">Die -Methode gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="36188-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="36188-116">Mögliche Werte sind, aber nicht beschränkt auf, die in der folgenden Tabelle gezeigten Werte.</span><span class="sxs-lookup"><span data-stu-id="36188-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="36188-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="36188-117">Return code</span></span>                                                                          | <span data-ttu-id="36188-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36188-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="36188-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="36188-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="36188-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="36188-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="36188-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="36188-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36188-122">**IMpeg2PsiParser-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="36188-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="36188-123">BEISPIEL FÜR PSI-Parserfilter</span><span class="sxs-lookup"><span data-stu-id="36188-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




