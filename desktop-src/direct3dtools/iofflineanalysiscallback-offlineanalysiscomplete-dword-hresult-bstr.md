---
description: Eine Rückruffunktion, mit der der Host benachrichtigt wird, dass die Offline Analyse abgeschlossen wurde.
MS-HAID: vspixengine.IOfflineAnalysisCallback\_OfflineAnalysisComplete\_DWORD\_HRESULT\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iofflineanalysiscallback:: offlineanalysiscomplete-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36E10709-51DC-4657-B184-F1F807ABBBB4
api_name:
- IOfflineAnalysisCallback.OfflineAnalysisComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a1ece7106bee1c49f97238bf06348b049d3f7167
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522736"
---
# <a name="span-idvspixengineiofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstrspaniofflineanalysiscallbackofflineanalysiscomplete-method"></a><span data-ttu-id="65e9e-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstr"></span>Iofflineanalysiscallback:: offlineanalysiscomplete-Methode</span><span class="sxs-lookup"><span data-stu-id="65e9e-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstr"></span>IOfflineAnalysisCallback::OfflineAnalysisComplete method</span></span>

<span data-ttu-id="65e9e-104">Eine Rückruffunktion, mit der der Host benachrichtigt wird, dass die Offline Analyse abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="65e9e-104">A callback function used to notify the host that offline analysis has completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="65e9e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="65e9e-105">Syntax</span></span>


```C++
HRESULT OfflineAnalysisComplete(
   DWORD   cookie,
   HRESULT result,
   BSTR    outputFullFileName
);
```

## <a name="parameters"></a><span data-ttu-id="65e9e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="65e9e-106">Parameters</span></span>

<span data-ttu-id="65e9e-107">*KS* </span><span class="sxs-lookup"><span data-stu-id="65e9e-107">*cookie* </span></span>  
<span data-ttu-id="65e9e-108">Ein Cookie, das die Anforderung eindeutig identifiziert, die die Offline Analyse initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="65e9e-108">A cookie that uniquely identifies the request which initiated offline analysis.</span></span>

<span data-ttu-id="65e9e-109">*result* </span><span class="sxs-lookup"><span data-stu-id="65e9e-109">*result* </span></span>  
<span data-ttu-id="65e9e-110">Gibt an, ob die Offline Analyse erfolgreich war oder nicht.</span><span class="sxs-lookup"><span data-stu-id="65e9e-110">Indicates whether offline analysis succeeded or failed.</span></span> <span data-ttu-id="65e9e-111">Wenn erfolgreich, wurden die Ergebnisse in eine Datei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="65e9e-111">If it succeeded, results were written to a file.</span></span>

<span data-ttu-id="65e9e-112">*outputfullfilename* </span><span class="sxs-lookup"><span data-stu-id="65e9e-112">*outputFullFileName* </span></span>  
<span data-ttu-id="65e9e-113">Eine com-Zeichenfolge, die den Namen der Datei zusammenführt, in der die Ergebnisse der Offline Analyse geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="65e9e-113">A COM string contianing the name of the file where offline analysis results were written.</span></span>

## <a name="return-value"></a><span data-ttu-id="65e9e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65e9e-114">Return value</span></span>

<span data-ttu-id="65e9e-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="65e9e-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="65e9e-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="65e9e-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="65e9e-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65e9e-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="65e9e-118">Header</span><span class="sxs-lookup"><span data-stu-id="65e9e-118">Header</span></span></p></td><td><span data-ttu-id="65e9e-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="65e9e-119">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="65e9e-120"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65e9e-120"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="65e9e-121">**Iofflineanalysiscallback**</span><span class="sxs-lookup"><span data-stu-id="65e9e-121">**IOfflineAnalysisCallback**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscallback)

 

 
