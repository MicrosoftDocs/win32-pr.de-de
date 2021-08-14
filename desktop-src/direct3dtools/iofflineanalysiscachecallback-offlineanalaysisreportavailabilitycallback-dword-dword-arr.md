---
description: Eine Rückruffunktion, mit der der Host benachrichtigt wird, für welche Frames Offlineanalyseberichte verfügbar sind.
MS-HAID: vspixengine.IOfflineAnalysisCacheCallback\_OfflineAnalaysisReportAvailabilityCallback\_DWORD\_DWORD\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IOfflineAnalysisCacheCallback::OfflineAnalaysisReportAvailabilityCallback-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2061EB62-4CBD-4668-BFCD-6E43014BB406
api_name:
- IOfflineAnalysisCacheCallback.OfflineAnalaysisReportAvailabilityCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ec2d874f06bb850538579edc29f5caa289d6f163846eff0657d49a41becc8f6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721861"
---
# <a name="span-idvspixengineiofflineanalysiscachecallback_offlineanalaysisreportavailabilitycallback_dword_dword_arrspaniofflineanalysiscachecallbackofflineanalaysisreportavailabilitycallback-method"></a><span id="vspixengine.iofflineanalysiscachecallback_offlineanalaysisreportavailabilitycallback_dword_dword_arr"></span>IOfflineAnalysisCacheCallback::OfflineAnalaysisReportAvailabilityCallback-Methode

Eine Rückruffunktion, mit der der Host benachrichtigt wird, für welche Frames Offlineanalyseberichte verfügbar sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT OfflineAnalaysisReportAvailabilityCallback(
   DWORD    numFramesWithReports,
   DWORD [] count0_framesWithReports
);
```

## <a name="parameters"></a>Parameter

*numFramesWithReports*   
Die Anzahl der Frames in count0 \_ framesWithReports.

*count0 \_ framesWithReports*   
Ein Array, das die Framenummern der Frames enthält, für die Offlineanalyseberichte verfügbar sind.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IOfflineAnalysisCacheCallback**](/windows/desktop/direct3dtools/iofflineanalysiscachecallback)

 

 
