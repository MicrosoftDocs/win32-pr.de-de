---
description: Fordern Sie ein Token für den Endpunkt des Diensts mit den angegebenen Anmelde Informationen an.
ms.assetid: 2CA0F826-9A05-4385-AF1A-A8C05B3DAFE2
title: 'Iupdateendpointauthprovider:: getendpointtoken-Methode (updateendpointauth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetEndpointToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 55efe38ce9782b691e1ad32f7a21f6124e1f0bf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752080"
---
# <a name="iupdateendpointauthprovidergetendpointtoken-method"></a>Iupdateendpointauthprovider:: getendpointtoken-Methode

Fordern Sie ein Token für den Endpunkt des Diensts mit den angegebenen Anmelde Informationen an.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetEndpointToken(
  [in]  GUID                        serviceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  UpdateEndpointAuthTokenType tokenType,
  [in]  BOOL                        fRefreshOnline,
  [out] IUnknown                    **ppEndpointToken
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*serviceid* \[ in\]
</dt> <dd>

Identifiziert den zu aktualisierenden Dienst.

</dd> <dt>

*EndpointType* \[ in\]
</dt> <dd>

Identifiziert den Typ des Endpunkts, der vom Dienst implementiert wird.

</dd> <dt>

*proxysettings* \[ in\]
</dt> <dd>

Die Einstellungen, die beim Herstellen einer Verbindung mit einem Proxy Server verwendet werden sollen. Weitere Informationen finden Sie in der [**updateendpointproxysettings**](updateendpointproxysettings.md) -Struktur.

</dd> <dt>

*husertoken* \[ in\]
</dt> <dd></dd> <dt>

 Verzeichnis \[ in\]
</dt> <dd>

Identifiziert den Authentifizierungstyp, der für die Authentifizierung verwendet wird.

</dd> <dt>

*frefreshonline* \[ in\]
</dt> <dd>

Gibt an, dass Wetter WUA ein neues Token anfordert. True gibt an, dass ein neues Token angefordert wird. False gibt an, dass ein neues oder zwischengespeichertes Token angefordert wird. Weitere Informationen finden Sie unter Hinweise.

</dd> <dt>

*ppendpointtoken* \[ vorgenommen\]
</dt> <dd>

Geben Sie das zu verwendende Endpunkt Token an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK zurück. Andernfalls wird ein com-oder Windows-Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

WUA legt den Parameter "frefreshonline" in der Regel auf "false" fest, wenn diese Methode erstmals aufgerufen wird. Wenn ein Verbindungsfehler auftritt, legt WUA diesen Parameter auf "true" fest, wenn die Methode erneut aufgerufen wird. Die Implementierung dieser Methode kann jedoch ein neues Token von einem Sicherheitstokendienst (Security Token Service, STS) anfordern oder jederzeit ein zwischengespeichertes Token bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]<br/>                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]<br/>                |
| Header<br/>                   | <dl> <dt>Updateendpointauth. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Updateendpointauth. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Updateendpointauth. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iupdateendpointauthprovider**](iupdateendpointauthprovider.md)
</dt> </dl>

 

 




