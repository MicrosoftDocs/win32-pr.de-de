---
description: Fordert an, eine Offline Analyse mit der angegebenen Quelle, dem angegebenen Manifest, den angegebenen Parametern und dem angegebenen Frame auszuführen.
MS-HAID: vspixengine.IOfflineAnalysisRequest\_RequestOfflineAnalysisAsync\_enumOFFLINEANALYSISSOURCE\_BSTR\_BSTR\_DWORD\_BSTR\_DWORD\_BSTR\_IOfflineAnalysisCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iofflineanalysisrequest:: requestofflineanalysisasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C836D9C1-D3E0-4661-9B89-048B61028F53
api_name:
- IOfflineAnalysisRequest.RequestOfflineAnalysisAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d027b9ec463c0bebfefca3ee7f9af4b50c514755
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392685"
---
# <a name="span-idvspixengineiofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptrspaniofflineanalysisrequestrequestofflineanalysisasync-method"></a><span data-ttu-id="b8320-103"><span id="vspixengine.iofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptr"></span>Iofflineanalysisrequest:: requestofflineanalysisasync-Methode</span><span class="sxs-lookup"><span data-stu-id="b8320-103"><span id="vspixengine.iofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptr"></span>IOfflineAnalysisRequest::RequestOfflineAnalysisAsync method</span></span>

<span data-ttu-id="b8320-104">Fordert an, eine Offline Analyse mit der angegebenen Quelle, dem angegebenen Manifest, den angegebenen Parametern und dem angegebenen Frame auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b8320-104">Requests to run offline analysis with the specified source, manifest, parameters and of the specified frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8320-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8320-105">Syntax</span></span>


```C++
HRESULT RequestOfflineAnalysisAsync(
   enum OFFLINEANALYSISSOURCE analysisSource,
   BSTR                       manifestXml,
   BSTR                       parametersXml,
   DWORD                      cookie,
   BSTR                       captureFullFileName,
   DWORD                      frameNumber,
   BSTR                       outputFullFileName,
   IOfflineAnalysisCallback * requestCallback
);
```

## <a name="parameters"></a><span data-ttu-id="b8320-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8320-106">Parameters</span></span>

<span data-ttu-id="b8320-107">*Analyse* </span><span class="sxs-lookup"><span data-stu-id="b8320-107">*analysisSource* </span></span>  
<span data-ttu-id="b8320-108">Gibt an, wo die Analyse Quelle von zwischengespeicherten Berichten oder der Wiedergabe stammt.</span><span class="sxs-lookup"><span data-stu-id="b8320-108">Specfies where the analysis source come from cached reports or from playback.</span></span>

<span data-ttu-id="b8320-109">*manifestXml* </span><span class="sxs-lookup"><span data-stu-id="b8320-109">*manifestXml* </span></span>  
<span data-ttu-id="b8320-110">Eine com-Zeichenfolge, die den Pfadnamen der XML-Manifest-Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="b8320-110">A COM string containing the pathname of the XML manifest file.</span></span>

<span data-ttu-id="b8320-111">*parametersxml* </span><span class="sxs-lookup"><span data-stu-id="b8320-111">*parametersXml* </span></span>  
<span data-ttu-id="b8320-112">Eine com-Zeichenfolge, die den Pfadnamen der XML-Parameterdatei enthält.</span><span class="sxs-lookup"><span data-stu-id="b8320-112">A COM string containing the pathname of the XML parameters file.</span></span>

<span data-ttu-id="b8320-113">*KS* </span><span class="sxs-lookup"><span data-stu-id="b8320-113">*cookie* </span></span>  
<span data-ttu-id="b8320-114">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8320-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="b8320-115">*capturefullfilename* </span><span class="sxs-lookup"><span data-stu-id="b8320-115">*captureFullFileName* </span></span>  
<span data-ttu-id="b8320-116">Eine com-Zeichenfolge, die den absoluten Pfadnamen der Erfassungs Datei (. vsglog) enthält.</span><span class="sxs-lookup"><span data-stu-id="b8320-116">A COM string containing the absolute pathname of the capture file (.vsglog).</span></span>

<span data-ttu-id="b8320-117">*Framezahl* </span><span class="sxs-lookup"><span data-stu-id="b8320-117">*frameNumber* </span></span>  
<span data-ttu-id="b8320-118">Der angegebene Frame.</span><span class="sxs-lookup"><span data-stu-id="b8320-118">The specified frame.</span></span>

<span data-ttu-id="b8320-119">*outputfullfilename* </span><span class="sxs-lookup"><span data-stu-id="b8320-119">*outputFullFileName* </span></span>  
<span data-ttu-id="b8320-120">Eine com-Zeichenfolge, die den absoluten Pfadnamen der Datei enthält, in die die Ausgabe geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="b8320-120">A COM string containing the absolute pathname of the file where output is written.</span></span>

<span data-ttu-id="b8320-121">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="b8320-121">*requestCallback* </span></span>  
<span data-ttu-id="b8320-122">Die Adresse eines Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b8320-122">The address of a callback used to notify the host of results.</span></span>

## <a name="return-value"></a><span data-ttu-id="b8320-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8320-123">Return value</span></span>

<span data-ttu-id="b8320-124">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="b8320-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b8320-125">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b8320-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8320-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8320-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b8320-127">Header</span><span class="sxs-lookup"><span data-stu-id="b8320-127">Header</span></span></p></td><td><span data-ttu-id="b8320-128">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b8320-128">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b8320-129"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8320-129"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b8320-130">**Iofflineanalysisrequest**</span><span class="sxs-lookup"><span data-stu-id="b8320-130">**IOfflineAnalysisRequest**</span></span>](/windows/desktop/direct3dtools/iofflineanalysisrequest)

 

 
