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
ms.openlocfilehash: 85243b1c07db1f2c30a4e29b221582fd507360f1
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624336"
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

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IOfflineAnalysisRequest**](/windows/desktop/direct3dtools/iofflineanalysisrequest)

 

 
