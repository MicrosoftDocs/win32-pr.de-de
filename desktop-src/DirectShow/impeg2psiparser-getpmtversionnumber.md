---
description: Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.
ms.assetid: 50113d6b-4e10-4dc9-aaef-f67c6918a2de
title: 'IMpeg2PsiParser:: getpmtversionnumber-Methode'
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
ms.openlocfilehash: 3af4b20067af52216181848f4cc63ac5a7784ba9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106338855"
---
# <a name="impeg2psiparsergetpmtversionnumber-method"></a><span data-ttu-id="732a6-104">IMpeg2PsiParser:: getpmtversionnumber-Methode</span><span class="sxs-lookup"><span data-stu-id="732a6-104">IMpeg2PsiParser::GetPmtVersionNumber method</span></span>

<span data-ttu-id="732a6-105">Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="732a6-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="732a6-106">Es handelt sich nicht um eine unterstützte DirectShow-API.</span><span class="sxs-lookup"><span data-stu-id="732a6-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="732a6-107">Die- `GetPmtVersionNumber` Methode ruft das Feld mit der Versions \_ Nummer von einem angegebenen PMT ab.</span><span class="sxs-lookup"><span data-stu-id="732a6-107">The `GetPmtVersionNumber` method retrieves the version\_number field from a specified PMT.</span></span> <span data-ttu-id="732a6-108">Die Versionsnummer wird jedes Mal inkrementiert, wenn sich die Programmdefinition ändert.</span><span class="sxs-lookup"><span data-stu-id="732a6-108">The version number is incremented whenever the definition of the program changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="732a6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="732a6-109">Syntax</span></span>


```C++
HRESULT GetPmtVersionNumber(
  [in]  WORD wProgramNumber,
  [out] BYTE *pPmtVersion
);
```



## <a name="parameters"></a><span data-ttu-id="732a6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="732a6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="732a6-111">*wprogramnumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="732a6-111">*wProgramNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="732a6-112">Gibt das Programm \_ Nummern Feld des Programms an, wie in Pat angegeben.</span><span class="sxs-lookup"><span data-stu-id="732a6-112">Specifies the program\_number field of the program, as given in the PAT.</span></span>

</dd> <dt>

<span data-ttu-id="732a6-113">*ppmtversion* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="732a6-113">*pPmtVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="732a6-114">Ein Zeiger auf eine Variable, die das Feld mit der Versions \_ Nummer empfängt.</span><span class="sxs-lookup"><span data-stu-id="732a6-114">Pointer to a variable that receives the version\_number field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="732a6-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="732a6-115">Return value</span></span>

<span data-ttu-id="732a6-116">Die-Methode gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="732a6-116">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="732a6-117">Mögliche Werte sind u. a. die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="732a6-117">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="732a6-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="732a6-118">Return code</span></span>                                                                          | <span data-ttu-id="732a6-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="732a6-119">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="732a6-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="732a6-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="732a6-121">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="732a6-121">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="732a6-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="732a6-122">Remarks</span></span>

<span data-ttu-id="732a6-123">Verwenden Sie die **getrecordprogramnumber** -Methode, um die Programmnummer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="732a6-123">Use the **GetRecordProgramNumber** method to obtain the program number.</span></span>

## <a name="see-also"></a><span data-ttu-id="732a6-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="732a6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="732a6-125">**IMpeg2PsiParser-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="732a6-125">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="732a6-126">**IMpeg2PsiParser:: getrecordprogramnumber**</span><span class="sxs-lookup"><span data-stu-id="732a6-126">**IMpeg2PsiParser::GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[<span data-ttu-id="732a6-127">Beispiel für PSI-Parser-Filter</span><span class="sxs-lookup"><span data-stu-id="732a6-127">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




