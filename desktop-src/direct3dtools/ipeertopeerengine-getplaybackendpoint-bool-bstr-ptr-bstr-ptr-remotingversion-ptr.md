---
description: Ruft die Endpunktadresse einer Remote-Engine ab.
MS-HAID: vspixengine.IPeerToPeerEngine\_GetPlaybackEndpoint\_BOOL\_BSTR\_ptr\_BSTR\_ptr\_RemotingVersion\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPeerToPeerEngine::GetPlaybackEndpoint-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3B391048-E7F7-4DA7-96A3-05875B170DCA
api_name:
- IPeerToPeerEngine.GetPlaybackEndpoint
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 06fea01d134aa58f9dc3839a48fa2f1bd910fc0b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629749"
---
# <a name="span-idvspixengineipeertopeerengine_getplaybackendpoint_bool_bstr_ptr_bstr_ptr_remotingversion_ptrspanipeertopeerenginegetplaybackendpoint-method"></a><span id="vspixengine.ipeertopeerengine_getplaybackendpoint_bool_bstr_ptr_bstr_ptr_remotingversion_ptr"></span>IPeerToPeerEngine::GetPlaybackEndpoint-Methode

Ruft die Endpunktadresse einer Remote-Engine ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPlaybackEndpoint(
   BOOL              bUseAuthentication,
   BSTR *            pEndpoint,
   BSTR *            sessionKey,
   RemotingVersion * pRemoteVersion
);
```

## <a name="parameters"></a>Parameter

*bUseAuthentication*   
TRUE, wenn die Remote-Engine die Authentifizierung verwendet; andernfalls FALSE.

*pEndpoint*   
Bei der Rückgabe eine COM-Zeichenfolge, die die Endpunktadresse des Remotewiedergabecomputers enthält.

*sessionKey*   
Bei der Rückgabe eine COM-Zeichenfolge, die den für die Verschlüsselung verwendeten Sitzungsschlüssel enthält.

*pRemoteVersion*   
Bei rückgabe die Version der Remote-Engine.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IPeerToPeerEngine**](/windows/desktop/direct3dtools/ipeertopeerengine)

 

 
