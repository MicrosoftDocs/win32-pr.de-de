---
description: Fordert Ereignisse zum Melden von Bürgeradressen an.
ms.assetid: cb02f611-7cda-405f-aeee-833b7385a4be
title: LocationDisp.CivicAddressReportFactory.ListenForReports-Methode (Locationapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.ListenForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 218684dcdb1c79b3b1a37517a4369ad492031cae1badfb9f0b16bbb6933289d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979770"
---
# <a name="locationdispcivicaddressreportfactorylistenforreports-method"></a>LocationDisp.CivicAddressReportFactory.ListenForReports-Methode

\[Das Location-API-Objektmodell steht für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen zur Verfügung. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-Geolocation-API,](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))um von einer Website aus auf den Standort zuzugreifen. Um über eine Desktopanwendung auf den Speicherort zu zugreifen, verwenden Sie [**die Windows. Devices.Geolocation-API.**](/uwp/api/Windows.Devices.Geolocation)\]

Fordert Ereignisse zum Melden von Bürgeradressen an.

## <a name="syntax"></a>Syntax


```JScript
LocationDisp.CivicAddressReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*requestedReportInterval* 
</dt> <dd> Zahl (**Doppeltes Wort**), die die angeforderte Zeit zwischen Denkberichtsereignissen in Millisekunden darstellt. Siehe Hinweise.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Standortanbieter muss nicht die von Ihnen geforderte Genauigkeit bereitstellen. Lesen Sie den Wert der [**ReportInterval-Eigenschaft,**](locationdisp-civicaddressreportfactory-reportinterval.md) um die Einstellung true report interval zu finden.

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Methode finden Sie unter [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                |
| Header<br/>                   | <dl> <dt>Locationapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**NewCivicAddressReport-Ereignis**](newcivicaddressreport.md)
</dt> </dl>

 

