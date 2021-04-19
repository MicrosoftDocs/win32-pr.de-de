---
description: Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.
ms.assetid: 19ef96a8-3d5b-4da1-8cff-d6a271ad4915
title: 'IMpeg2PsiParser:: getzähltofelementarystreams-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfElementaryStreams
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6593b699592c913940b14c2c26aea42057acfa40
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343126"
---
# <a name="impeg2psiparsergetcountofelementarystreams-method"></a><span data-ttu-id="277a2-104">IMpeg2PsiParser:: getzähltofelementarystreams-Methode</span><span class="sxs-lookup"><span data-stu-id="277a2-104">IMpeg2PsiParser::GetCountOfElementaryStreams method</span></span>

<span data-ttu-id="277a2-105">Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="277a2-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="277a2-106">Es handelt sich nicht um eine unterstützte DirectShow-API.</span><span class="sxs-lookup"><span data-stu-id="277a2-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="277a2-107">Die- `GetCountOfElementaryStreams` Methode ruft die Anzahl der elementaren Datenströme in einem angegebenen Programm ab.</span><span class="sxs-lookup"><span data-stu-id="277a2-107">The `GetCountOfElementaryStreams` method retrieves the number of elementary streams in a specified program.</span></span>

## <a name="syntax"></a><span data-ttu-id="277a2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="277a2-108">Syntax</span></span>


```C++
HRESULT GetCountOfElementaryStreams(
  [in]  WORD wProgramNumber,
  [out] WORD *pwVal
);
```



## <a name="parameters"></a><span data-ttu-id="277a2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="277a2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="277a2-110">*wprogramnumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="277a2-110">*wProgramNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="277a2-111">Gibt das \_ Feld für die Programmnummer des Programms an, wie in Pat angegeben.</span><span class="sxs-lookup"><span data-stu-id="277a2-111">Specifies the program\_number field for the program, as given in the PAT.</span></span>

</dd> <dt>

<span data-ttu-id="277a2-112">*pwval* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="277a2-112">*pwVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="277a2-113">Ein Zeiger auf eine Variable, die die Anzahl der elementaren Datenströme im Programm empfängt.</span><span class="sxs-lookup"><span data-stu-id="277a2-113">Pointer to a variable that receives the number of elementary streams in the program.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="277a2-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="277a2-114">Return value</span></span>

<span data-ttu-id="277a2-115">Die-Methode gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="277a2-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="277a2-116">Mögliche Werte sind u. a. die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="277a2-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="277a2-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="277a2-117">Return code</span></span>                                                                          | <span data-ttu-id="277a2-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="277a2-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="277a2-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="277a2-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="277a2-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="277a2-120">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="277a2-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="277a2-121">Remarks</span></span>

<span data-ttu-id="277a2-122">Verwenden Sie die **getrecordprogramnumber** -Methode, um die Programmnummer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="277a2-122">Use the **GetRecordProgramNumber** method to obtain the program number.</span></span>

## <a name="see-also"></a><span data-ttu-id="277a2-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="277a2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="277a2-124">**IMpeg2PsiParser-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="277a2-124">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="277a2-125">**IMpeg2PsiParser:: getrecordprogramnumber**</span><span class="sxs-lookup"><span data-stu-id="277a2-125">**IMpeg2PsiParser::GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[<span data-ttu-id="277a2-126">Beispiel für PSI-Parser-Filter</span><span class="sxs-lookup"><span data-stu-id="277a2-126">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




