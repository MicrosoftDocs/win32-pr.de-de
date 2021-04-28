---
description: 'IMpeg2PsiParser::GetPatVersionNumber-Methode: Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.'
ms.assetid: 2f5ad9bf-3d70-491a-ab45-15cd922a02d4
title: IMpeg2PsiParser::GetPatVersionNumber-Methode
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
ms.openlocfilehash: 978da4c7076bcf8ffe91bc2b9a4b2077d9d3d48a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089148"
---
# <a name="impeg2psiparsergetpatversionnumber-method"></a><span data-ttu-id="50dd1-104">IMpeg2PsiParser::GetPatVersionNumber-Methode</span><span class="sxs-lookup"><span data-stu-id="50dd1-104">IMpeg2PsiParser::GetPatVersionNumber method</span></span>

<span data-ttu-id="50dd1-105">Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="50dd1-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="50dd1-106">Es handelt sich nicht um eine unterstützte DirectShow-API.</span><span class="sxs-lookup"><span data-stu-id="50dd1-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="50dd1-107">Die `GetPatVersionNumber` -Methode ruft das Feld mit \_ der Versionsnummer aus dem PAT ab.</span><span class="sxs-lookup"><span data-stu-id="50dd1-107">The `GetPatVersionNumber` method retrieves the version\_number field from the PAT.</span></span> <span data-ttu-id="50dd1-108">Ein Transportstream enthält mindestens ein PAT.</span><span class="sxs-lookup"><span data-stu-id="50dd1-108">A transport stream contains at most one PAT.</span></span> <span data-ttu-id="50dd1-109">Die Versionsnummer wird erhöht, wenn sich die Informationen in der Tabelle ändern.</span><span class="sxs-lookup"><span data-stu-id="50dd1-109">The version number is incremented whenever the information in the table changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="50dd1-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="50dd1-110">Syntax</span></span>


```C++
HRESULT GetPatVersionNumber(
  [out] BYTE *pPatVersion
);
```



## <a name="parameters"></a><span data-ttu-id="50dd1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="50dd1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50dd1-112">*pPatVersion* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="50dd1-112">*pPatVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50dd1-113">Zeiger auf eine Variable, die das Versionsnummerfeld \_ empfängt.</span><span class="sxs-lookup"><span data-stu-id="50dd1-113">Pointer to a variable that receives the version\_number field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50dd1-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50dd1-114">Return value</span></span>

<span data-ttu-id="50dd1-115">Die -Methode gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="50dd1-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="50dd1-116">Mögliche Werte sind, aber nicht beschränkt auf, die in der folgenden Tabelle gezeigten Werte.</span><span class="sxs-lookup"><span data-stu-id="50dd1-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="50dd1-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="50dd1-117">Return code</span></span>                                                                          | <span data-ttu-id="50dd1-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50dd1-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="50dd1-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="50dd1-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="50dd1-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="50dd1-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="50dd1-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="50dd1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50dd1-122">**IMpeg2PsiParser-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="50dd1-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="50dd1-123">BEISPIEL FÜR PSI-Parserfilter</span><span class="sxs-lookup"><span data-stu-id="50dd1-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




