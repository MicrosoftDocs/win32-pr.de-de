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
# <a name="span-idvspixengineiofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptrspaniofflineanalysisrequestrequestofflineanalysisasync-method"></a><span id="vspixengine.iofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptr"></span>Iofflineanalysisrequest:: requestofflineanalysisasync-Methode

Fordert an, eine Offline Analyse mit der angegebenen Quelle, dem angegebenen Manifest, den angegebenen Parametern und dem angegebenen Frame auszuführen.

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

*Analyse*   
Gibt an, wo die Analyse Quelle von zwischengespeicherten Berichten oder der Wiedergabe stammt.

*manifestXml*   
Eine com-Zeichenfolge, die den Pfadnamen der XML-Manifest-Datei enthält.

*parametersxml*   
Eine com-Zeichenfolge, die den Pfadnamen der XML-Parameterdatei enthält.

*KS*   
Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.

*capturefullfilename*   
Eine com-Zeichenfolge, die den absoluten Pfadnamen der Erfassungs Datei (. vsglog) enthält.

*Framezahl*   
Der angegebene Frame.

*outputfullfilename*   
Eine com-Zeichenfolge, die den absoluten Pfadnamen der Datei enthält, in die die Ausgabe geschrieben wird.

*requestCallback*   
Die Adresse eines Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Iofflineanalysisrequest**](/windows/desktop/direct3dtools/iofflineanalysisrequest)

 

 
