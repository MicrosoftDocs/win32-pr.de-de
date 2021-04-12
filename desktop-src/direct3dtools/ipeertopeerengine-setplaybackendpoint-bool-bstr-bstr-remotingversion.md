---
description: Legt die Endpunkt Adresse fest, die zum Herstellen einer Verbindung mit einem Remote Modul verwendet wird.
MS-HAID: vspixengine.IPeerToPeerEngine\_SetPlaybackEndpoint\_BOOL\_BSTR\_BSTR\_RemotingVersion
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ietertopeerengine:: setplaybackendpoint-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D261D2EA-C930-406E-A5E1-CE5E98162399
api_name:
- IPeerToPeerEngine.SetPlaybackEndpoint
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bbec4826fb2659604a4b9f4388beed1829b42770
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482406"
---
# <a name="span-idvspixengineipeertopeerengine_setplaybackendpoint_bool_bstr_bstr_remotingversionspanipeertopeerenginesetplaybackendpoint-method"></a><span id="vspixengine.ipeertopeerengine_setplaybackendpoint_bool_bstr_bstr_remotingversion"></span>Ietertopeerengine:: setplaybackendpoint-Methode

Legt die Endpunkt Adresse fest, die zum Herstellen einer Verbindung mit einem Remote Modul verwendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPlaybackEndpoint(
   BOOL            bUseAuthentication,
   BSTR            endpoint,
   BSTR            sessionKey,
   RemotingVersion remoteVersion
);
```

## <a name="parameters"></a>Parameter

*busauthentifizierung*   
true, wenn Authentifizierung verwendet werden soll. andernfalls false.

*Dreher*   
Eine com-Zeichenfolge, die die Endpunkt Adresse enthält.

*SessionKey*   
Eine com-Zeichenfolge, die den für die Verschlüsselung verwendeten Sitzungsschlüssel enthält.

*Remoteversion*   
Gibt die Version der zu verwendenden Remote-Engine an.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IPeer-topeerengine**](/windows/desktop/direct3dtools/ipeertopeerengine)

 

 
