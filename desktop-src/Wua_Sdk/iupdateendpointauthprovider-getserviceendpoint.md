---
description: Fordert einen Endpunkt an, der zum Herstellen einer Verbindung mit einem Dienst verwendet wird.
ms.assetid: 4C02EA78-AD77-42CD-B94F-C8C3ED26CB4C
title: 'Iupdateendpointprovider:: getserviceendpoint-Methode (updateendpointauth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider.GetServiceEndpoint
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: bddb77237d6d5edabab41eefe1931514fd6aed42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347792"
---
# <a name="iupdateendpointprovidergetserviceendpoint-method"></a>Iupdateendpointprovider:: getserviceendpoint-Methode

Fordert einen Endpunkt an, der zum Herstellen einer Verbindung mit einem Dienst verwendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetServiceEndpoint(
  [in]  GUID                        ServiceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  BOOL                        fRefreshOnline,
  [out] BSTR                        *pbstrEndpointLoc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Serviceid* \[ in\]
</dt> <dd>

Identifiziert den zu aktualisierenden Dienst.

</dd> <dt>

*EndpointType* \[ in\]
</dt> <dd>

Identifiziert den Typ des Endpunkts, der vom Dienst implementiert wird.

Die [**updateendpointtype**](updateendpointtype.md) -Enumeration definiert die folgenden Konstanten.

<dt>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetclientserver**


</dt> <dd>

Ein Client/Server-Endpunkt, der zum Herstellen der Verbindung mit dem Aktualisierungs Dienst verwendet wird.

</dd> <dt>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetreporting**


</dt> <dd>

Ein Berichterstattungs Endpunkt, der verwendet wird, wenn der Client die Ergebnisse von Scans, Downloads und Installationen zurück an den Aktualisierungs Dienst meldet

</dd> <dt>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetwuaselfupdate**


</dt> <dd>

Ein Self-Update Endpunkt, der verwendet wird, wenn der Client Computer einen Update Dienst kontaktiert, um festzustellen, ob eine neue Version der Windows Update Agent-Client Software vorhanden ist.

</dd> <dt>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetregulations**


</dt> <dd>

Ein-Regel Endpunkt, der verwendet wird, wenn der Client Computer eine Verbindung mit dem-Verwaltungs Endpunkt hergestellt hat, um ein bestimmtes Update zu ergreifen, das auf den Zielcomputer anwendbar ist.

</dd> <dt>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetsimpletargeting**


</dt> <dd>

Ein Simple-Targeting endoint, das nur mit privaten Diensten (WSUS-Server in Unternehmensumgebungen) verwendet wird.

</dd> </dl> </dd> <dt>

*proxysettings* \[ in\]
</dt> <dd>

Gibt die Einstellungen an, die beim Herstellen einer Verbindung mit einem Proxy Server verwendet werden.

</dd> <dt>

*husertoken* \[ in\]
</dt> <dd>

Enthält ein Tokenhandle-Objekt, das den Benutzer darstellt. Der Endpunkt Anbieter verwendet dieses Token, um zu bestimmen, welche Proxy Einstellungen und Anmelde Informationen verwendet werden sollen.

</dd> <dt>

*frefreshonline* \[ in\]
</dt> <dd>

Gibt an, dass Wetter WUA ein neues Token anfordert. True gibt an, dass ein neues Token angefordert wird. False gibt an, dass ein neues oder zwischengespeichertes Token angefordert wird. Weitere Informationen finden Sie unter Hinweise.

</dd> <dt>

*pbstrauendpointloc* \[ vorgenommen\]
</dt> <dd>

Geben Sie die URL an, die zur Kommunikation mit dem Dienst verwendet wird. Für einen Cleint-Server-Endpunkt wäre dies z. b. die URL zum Client Server Dienst. Weitere Informationen finden Sie unter Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg **S \_ OK** zurück. Andernfalls wird ein com-oder Windows-Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

WUA legt den Parameter " *frefreshonline* " in der Regel auf "false" fest, wenn diese Methode erstmals aufgerufen wird. Wenn ein Verbindungsfehler auftritt, legt WUA diesen Parameter auf "true" fest, wenn die Methode erneut aufgerufen wird. Die Implementierung dieser Methode kann jedoch ein neues Token von einem Sicherheitstokendienst (Security Token Service, STS) anfordern oder jederzeit ein zwischengespeichertes Token bereitstellen.

Wenn für den Endpunkt keine Authentifizierung erforderlich ist, kann der Aufrufer nur mit der URL, die vom *pbstrauendpointloc* -Parameter angegeben wird, eine Verbindung mit dem Dienst herstellen.

Wenn für den Endpunkt eine Authentifizierung erforderlich ist, kann der Aufrufer die vom *pbstrinendpointloc* -Parameter angegebene URL und die von den anderen Parametern bereitgestellten Daten verwenden.

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

[**Iupdateendpointprovider**](iupdateendpointprovider.md)
</dt> </dl>

 

 




