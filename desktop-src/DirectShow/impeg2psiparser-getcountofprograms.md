---
description: 'IMpeg2PsiParser::GetCountOfPrograms-Methode: Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.'
ms.assetid: 282dd779-9aca-46e3-a791-cb9ea86f637d
title: IMpeg2PsiParser::GetCountOfPrograms-Methode
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
ms.openlocfilehash: d6bfe698a45ea1cfe0a4bac6e65b839292bc1996
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119428"
---
# <a name="impeg2psiparsergetcountofprograms-method"></a><span data-ttu-id="32bf8-104">IMpeg2PsiParser::GetCountOfPrograms-Methode</span><span class="sxs-lookup"><span data-stu-id="32bf8-104">IMpeg2PsiParser::GetCountOfPrograms method</span></span>

<span data-ttu-id="32bf8-105">Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="32bf8-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="32bf8-106">Es handelt sich nicht um eine unterstützte DirectShow-API.</span><span class="sxs-lookup"><span data-stu-id="32bf8-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="32bf8-107">Die `GetCountOfPrograms` -Methode ruft die Anzahl der Programme im Transportstream ab.</span><span class="sxs-lookup"><span data-stu-id="32bf8-107">The `GetCountOfPrograms` method retrieves the number of programs in the transport stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="32bf8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="32bf8-108">Syntax</span></span>


```C++
HRESULT GetCountOfPrograms(
  [out] int *pNumOfPrograms
);
```



## <a name="parameters"></a><span data-ttu-id="32bf8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="32bf8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32bf8-110">*pNumOfPrograms* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="32bf8-110">*pNumOfPrograms* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32bf8-111">Zeiger auf eine Variable, die die Anzahl der Programme empfängt.</span><span class="sxs-lookup"><span data-stu-id="32bf8-111">Pointer to a variable that receives the number of programs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32bf8-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="32bf8-112">Return value</span></span>

<span data-ttu-id="32bf8-113">Die -Methode gibt einen HRESULT-Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="32bf8-113">The method returns an HRESULT value.</span></span> <span data-ttu-id="32bf8-114">Mögliche Werte sind, aber nicht beschränkt auf, die in der folgenden Tabelle gezeigten Werte.</span><span class="sxs-lookup"><span data-stu-id="32bf8-114">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="32bf8-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="32bf8-115">Return code</span></span>                                                                          | <span data-ttu-id="32bf8-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="32bf8-116">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="32bf8-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="32bf8-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="32bf8-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="32bf8-118">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="32bf8-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="32bf8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32bf8-120">**IMpeg2PsiParser-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="32bf8-120">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="32bf8-121">BEISPIEL FÜR PSI-Parserfilter</span><span class="sxs-lookup"><span data-stu-id="32bf8-121">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




