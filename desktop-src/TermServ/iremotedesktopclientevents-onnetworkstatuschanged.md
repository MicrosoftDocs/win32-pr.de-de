---
title: Iremotedesktopclientevents onnetworkstatuschangi-Methode
description: Wird aufgerufen, wenn sich der Netzwerkstatus geändert hat. | Iremotedesktopclientevents onnetworkstatuschangi-Methode
ms.assetid: B68D1AA0-6403-40CA-95C5-BBBF39CEFFD8
ms.tgt_platform: multiple
keywords:
- Onnetworkstatuschangi-Methode Remotedesktopdienste
- Onnetworkstatuschangi-Methode Remotedesktopdienste, iremotedesktopclientevents-Schnittstelle
- Iremotedesktopclientevents-Schnittstelle Remotedesktopdienste, onnetworkstatuschangi-Methode
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
ms.openlocfilehash: de64d8b16ea9acf9defc976d4baa91afd64f8fa7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530662"
---
# <a name="iremotedesktopclienteventsonnetworkstatuschanged-method"></a>Iremotedesktopclientevents:: onnetworkstatuschangi-Methode

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

*qualitylevel* \[ in\]
</dt> <dd>

Die neue Qualitätsstufe der Verbindung. Die Qualitätsstufe wird von den Werten für Bandbreite und Roundtrip-Zeit (RTT) bestimmt.

Einer der folgenden Werte.



| Wert                                                                        | Bedeutung                                                     |
|------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Die Qualitätsstufe konnte nicht bestimmt werden.<br/>       |
| <dl> <dt>1</dt> </dl> | Die Verbindungsqualität ist "schlecht" (ein Balken).<br/>        |
| <dl> <dt>2</dt> </dl> | Die Verbindungsqualität ist fair (zwei Balken).<br/>       |
| <dl> <dt>3</dt> </dl> | Die Verbindungsqualität ist gut (drei Balken).<br/>     |
| <dl> <dt>4</dt> </dl> | Die Verbindungsqualität ist hervorragend (vier Balken).<br/> |



 

</dd> <dt>

*Bandbreite* \[ in\]
</dt> <dd>

Gibt die neue Verbindungs Bandbreite in Kbit pro Sekunde (Kbit/s) an.

</dd> <dt>

*RTT* \[ in\]
</dt> <dd>

Gibt die neue Roundtripzeit der Verbindung (Latenzzeit) in Millisekunden an.

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
| IID<br/>                      | Diid \_ iremotedesktopclientevents ist als 079863b7-6d47-4105-8bfe-0cdcb360e67d definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iremotedesktopclientevents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





