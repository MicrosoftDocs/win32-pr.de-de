---
description: Anforderungen zum Ausführen der Offlineanalyse mit der angegebenen Quelle, dem angegebenen Manifest, den angegebenen Parametern und dem angegebenen Frame.
MS-HAID: vspixengine.IOfflineAnalysisRequest\_RequestOfflineAnalysisAsync\_enumOFFLINEANALYSISSOURCE\_BSTR\_BSTR\_DWORD\_BSTR\_DWORD\_BSTR\_IOfflineAnalysisCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IOfflineAnalysisRequest::RequestOfflineAnalysisAsync-Methode
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
ms.openlocfilehash: 2a8a36f65f2158d03650257cf13458d36330e7fd3184210d99c05200e1731231
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981140"
---
# <a name="span-idvspixengineiofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptrspaniofflineanalysisrequestrequestofflineanalysisasync-method"></a><span id="vspixengine.iofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptr"></span>IOfflineAnalysisRequest::RequestOfflineAnalysisAsync-Methode

Anforderungen zum Ausführen der Offlineanalyse mit der angegebenen Quelle, dem angegebenen Manifest, den angegebenen Parametern und dem angegebenen Frame.

## <a name="syntax"></a>Syntax


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

## <a name="parameters"></a>Parameter

*analysisSource*   
Gibt an, wo die Analysequelle aus zwischengespeicherten Berichten oder aus der Wiedergabe stammt.

*manifestXml*   
Eine COM-Zeichenfolge, die den Pfadnamen der XML-Manifestdatei enthält.

*parametersXml*   
Eine COM-Zeichenfolge, die den Pfadnamen der XML-Parameterdatei enthält.

*Cookie*   
Ein Cookie, das die Anforderung eindeutig identifiziert und verwendet werden kann, um zu signalisieren, dass sie abgebrochen wird.

*captureFullFileName*   
Eine COM-Zeichenfolge, die den absoluten Pfadnamen der Erfassungsdatei (.vsglog) enthält.

*frameNumber*   
Der angegebene Frame.

*outputFullFileName*   
Eine COM-Zeichenfolge, die den absoluten Pfadnamen der Datei enthält, in die die Ausgabe geschrieben wird.

*requestCallback*   
Die Adresse eines Rückrufs, der verwendet wird, um den Host über Ergebnisse zu benachrichtigen.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IOfflineAnalysisRequest**](/windows/desktop/direct3dtools/iofflineanalysisrequest)

 

 
