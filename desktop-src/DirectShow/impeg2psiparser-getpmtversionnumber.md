---
description: 'IMpeg2PsiParser::GetPmtVersionNumber-Methode: Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.'
ms.assetid: 50113d6b-4e10-4dc9-aaef-f67c6918a2de
title: IMpeg2PsiParser::GetPmtVersionNumber-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPmtVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6f4fd8d0eba88ba1df54a1cc058bc0a2951b9a19
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084558"
---
# <a name="impeg2psiparsergetpmtversionnumber-method"></a><span data-ttu-id="4df3f-104">IMpeg2PsiParser::GetPmtVersionNumber-Methode</span><span class="sxs-lookup"><span data-stu-id="4df3f-104">IMpeg2PsiParser::GetPmtVersionNumber method</span></span>

<span data-ttu-id="4df3f-105">Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="4df3f-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="4df3f-106">Es handelt sich nicht um eine unterstützte DirectShow-API.</span><span class="sxs-lookup"><span data-stu-id="4df3f-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="4df3f-107">Die `GetPmtVersionNumber` -Methode ruft das Versionsnummerfeld \_ aus einem angegebenen PMT ab.</span><span class="sxs-lookup"><span data-stu-id="4df3f-107">The `GetPmtVersionNumber` method retrieves the version\_number field from a specified PMT.</span></span> <span data-ttu-id="4df3f-108">Die Versionsnummer wird erhöht, wenn sich die Definition des Programms ändert.</span><span class="sxs-lookup"><span data-stu-id="4df3f-108">The version number is incremented whenever the definition of the program changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="4df3f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4df3f-109">Syntax</span></span>


```C++
HRESULT GetPmtVersionNumber(
  [in]  WORD wProgramNumber,
  [out] BYTE *pPmtVersion
);
```



## <a name="parameters"></a><span data-ttu-id="4df3f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4df3f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4df3f-111">*wProgramNumber* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="4df3f-111">*wProgramNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4df3f-112">Gibt das \_ Programmnummerfeld des Programms an, wie im PAT angegeben.</span><span class="sxs-lookup"><span data-stu-id="4df3f-112">Specifies the program\_number field of the program, as given in the PAT.</span></span>

</dd> <dt>

<span data-ttu-id="4df3f-113">*pPmtVersion* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4df3f-113">*pPmtVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4df3f-114">Zeiger auf eine Variable, die das Versionsnummerfeld \_ empfängt.</span><span class="sxs-lookup"><span data-stu-id="4df3f-114">Pointer to a variable that receives the version\_number field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4df3f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4df3f-115">Return value</span></span>

<span data-ttu-id="4df3f-116">Die -Methode gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="4df3f-116">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="4df3f-117">Mögliche Werte sind, aber nicht beschränkt auf, die in der folgenden Tabelle gezeigten Werte.</span><span class="sxs-lookup"><span data-stu-id="4df3f-117">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="4df3f-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4df3f-118">Return code</span></span>                                                                          | <span data-ttu-id="4df3f-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4df3f-119">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="4df3f-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4df3f-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4df3f-121">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="4df3f-121">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4df3f-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4df3f-122">Remarks</span></span>

<span data-ttu-id="4df3f-123">Verwenden Sie **die GetRecordProgramNumber-Methode,** um die Programmnummer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4df3f-123">Use the **GetRecordProgramNumber** method to obtain the program number.</span></span>

## <a name="see-also"></a><span data-ttu-id="4df3f-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4df3f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4df3f-125">**IMpeg2PsiParser-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="4df3f-125">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="4df3f-126">**IMpeg2PsiParser::GetRecordProgramNumber**</span><span class="sxs-lookup"><span data-stu-id="4df3f-126">**IMpeg2PsiParser::GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[<span data-ttu-id="4df3f-127">BEISPIEL FÜR PSI-Parserfilter</span><span class="sxs-lookup"><span data-stu-id="4df3f-127">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




