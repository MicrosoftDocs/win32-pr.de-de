---
description: Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.
ms.assetid: 282dd779-9aca-46e3-a791-cb9ea86f637d
title: 'IMpeg2PsiParser:: getzählto-Programme-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfPrograms
api_type:
- COM
api_location: ''
ms.openlocfilehash: e4f01b2a360465b9670b52547cff1ff4c312a705
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860358"
---
# <a name="impeg2psiparsergetcountofprograms-method"></a><span data-ttu-id="1d315-104">IMpeg2PsiParser:: getzählto-Programme-Methode</span><span class="sxs-lookup"><span data-stu-id="1d315-104">IMpeg2PsiParser::GetCountOfPrograms method</span></span>

<span data-ttu-id="1d315-105">Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="1d315-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="1d315-106">Es handelt sich nicht um eine unterstützte DirectShow-API.</span><span class="sxs-lookup"><span data-stu-id="1d315-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="1d315-107">Die- `GetCountOfPrograms` Methode ruft die Anzahl der Programme im Transportstream ab.</span><span class="sxs-lookup"><span data-stu-id="1d315-107">The `GetCountOfPrograms` method retrieves the number of programs in the transport stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d315-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d315-108">Syntax</span></span>


```C++
HRESULT GetCountOfPrograms(
  [out] int *pNumOfPrograms
);
```



## <a name="parameters"></a><span data-ttu-id="1d315-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d315-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d315-110">*pnumuf-Programme* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1d315-110">*pNumOfPrograms* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d315-111">Ein Zeiger auf eine Variable, die die Anzahl der Programme empfängt.</span><span class="sxs-lookup"><span data-stu-id="1d315-111">Pointer to a variable that receives the number of programs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d315-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d315-112">Return value</span></span>

<span data-ttu-id="1d315-113">Die-Methode gibt einen HRESULT-Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1d315-113">The method returns an HRESULT value.</span></span> <span data-ttu-id="1d315-114">Mögliche Werte sind u. a. die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="1d315-114">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="1d315-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1d315-115">Return code</span></span>                                                                          | <span data-ttu-id="1d315-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1d315-116">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="1d315-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1d315-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1d315-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="1d315-118">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="1d315-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d315-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d315-120">**IMpeg2PsiParser-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="1d315-120">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="1d315-121">Beispiel für PSI-Parser-Filter</span><span class="sxs-lookup"><span data-stu-id="1d315-121">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




