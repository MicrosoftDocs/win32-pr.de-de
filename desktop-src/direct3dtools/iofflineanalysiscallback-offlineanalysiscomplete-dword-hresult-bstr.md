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
# <a name="span-idvspixengineiofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstrspaniofflineanalysiscallbackofflineanalysiscomplete-method"></a><span id="vspixengine.iofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstr"></span>Iofflineanalysiscallback:: offlineanalysiscomplete-Methode

Eine Rückruffunktion, mit der der Host benachrichtigt wird, dass die Offline Analyse abgeschlossen wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT OfflineAnalysisComplete(
   DWORD   cookie,
   HRESULT result,
   BSTR    outputFullFileName
);
```

## <a name="parameters"></a>Parameter

*KS*   
Ein Cookie, das die Anforderung eindeutig identifiziert, die die Offline Analyse initiiert hat.

*result*   
Gibt an, ob die Offline Analyse erfolgreich war oder nicht. Wenn erfolgreich, wurden die Ergebnisse in eine Datei geschrieben.

*outputfullfilename*   
Eine com-Zeichenfolge, die den Namen der Datei zusammenführt, in der die Ergebnisse der Offline Analyse geschrieben wurden.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Iofflineanalysiscallback**](/windows/desktop/direct3dtools/iofflineanalysiscallback)

 

 
