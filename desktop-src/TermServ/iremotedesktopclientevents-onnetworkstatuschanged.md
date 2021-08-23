---
title: IRemoteDesktopClientEvents OnNetworkStatusChanged-Methode
description: Wird aufgerufen, wenn sich der Netzwerkstatus geändert hat. | IRemoteDesktopClientEvents OnNetworkStatusChanged-Methode
ms.assetid: B68D1AA0-6403-40CA-95C5-BBBF39CEFFD8
ms.tgt_platform: multiple
keywords:
- OnNetworkStatusChanged-Remotedesktopdienste
- OnNetworkStatusChanged-Remotedesktopdienste , IRemoteDesktopClientEvents-Schnittstelle
- IRemoteDesktopClientEvents-Schnittstelle Remotedesktopdienste , OnNetworkStatusChanged-Methode
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96d14519f5da78a0d42b5bd7e52abf790c21406bfe20848235d2639beed2e215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515110"
---
# <a name="iremotedesktopclienteventsonnetworkstatuschanged-method"></a>IRemoteDesktopClientEvents::OnNetworkStatusChanged-Methode

Wird aufgerufen, wenn sich der Netzwerkstatus geändert hat.

## <a name="syntax"></a>Syntax


```C++
void OnNetworkStatusChanged(
  [in] unsigned long qualityLevel,
  [in] long          bandwidth,
  [in] long          rtt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*qualityLevel* \[ In\]
</dt> <dd>

Die neue Qualitätsstufe der Verbindung. Der Qualitätsgrad wird anhand der Werte für Bandbreite und Roundtripzeit (rtt) bestimmt.

Einer der folgenden Werte.



| Wert                                                                        | Bedeutung                                                     |
|------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Der Qualitätsgrad konnte nicht bestimmt werden.<br/>       |
| <dl> <dt>1</dt> </dl> | Die Verbindungsqualität ist schlecht (ein Balken).<br/>        |
| <dl> <dt>2</dt> </dl> | Die Verbindungsqualität ist fair (zwei Balken).<br/>       |
| <dl> <dt>3</dt> </dl> | Die Verbindungsqualität ist gut (drei Balken).<br/>     |
| <dl> <dt>4</dt> </dl> | Die Verbindungsqualität ist hervorragend (vier Balken).<br/> |



 

</dd> <dt>

*Bandbreite* \[ In\]
</dt> <dd>

Gibt die neue Verbindungsbandbreite in Kilobits pro Sekunde (KBit/s) an.

</dd> <dt>

*rtt* \[ In\]
</dt> <dd>

Gibt die neue Verbindungsrundtripzeit (Latenz) in Millisekunden an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                 |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents ist als 079863B7-6D47-4105-8BFE-0CDCB360E67D definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





