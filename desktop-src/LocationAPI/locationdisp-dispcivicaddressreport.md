---
description: Stellt einen Stadtadressbericht dar.
ms.assetid: 7c6e790f-0150-4ea8-9583-df633ebf035d
title: LocationDisp.DispCivicAddressReport-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispCivicAddressReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: e5646bd6df1a2523faf481bc867acc67dbd0a647b4cdf3f033d7327a66174d8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129980"
---
# <a name="locationdispdispcivicaddressreport-object"></a>LocationDisp.DispCivicAddressReport-Objekt

\[Das Location API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-Geolocation-API,](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))um von einer Website aus auf den Standort zuzugreifen. Um von einer Desktopanwendung aus auf den Speicherort zuzugreifen, verwenden Sie die [**Windows. Devices.Geolocation-API.**](/uwp/api/Windows.Devices.Geolocation)\]

Stellt einen Stadtadressbericht dar.

## <a name="members"></a>Member

Das **LocationDisp.DispCivicAddressReport-Objekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **LocationDisp.DispCivicAddressReport-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                                              | Zugriffstyp          | Beschreibung                                                 |
|:--------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------|
| [**AddressLine1**](locationdisp-dispcivicaddressreport-addressline1.md)<br/>   | Schreibgeschützt<br/> | Die erste Zeile einer Straße.<br/>              |
| [**AddressLine2**](locationdisp-dispcivicaddressreport-addressline2.md)<br/>   | Schreibgeschützt<br/> | Die zweite Zeile einer Straße.<br/>             |
| [**Stadt**](locationdisp-dispcivicaddressreport-city.md)<br/>                   | Schreibgeschützt<br/> | Der Name der Stadt.<br/>                                   |
| [**Countryregion**](locationdisp-civicaddressreport-countryregion.md)<br/>     | Schreibgeschützt<br/> | Der Name des Landes oder der Region.<br/>                      |
| [**DetailLevel**](locationdisp-dispcivicaddressreport-detaillevel.md)<br/>     | Schreibgeschützt<br/> | Die Detailebene für den Bericht.<br/>                 |
| [**Postalcode**](locationdisp-dispcivicaddressreport-postalcode.md)<br/>       | Schreibgeschützt<br/> | Die Postleitzahl.<br/>                                 |
| [**Stateprovince**](locationdisp-dispcivicaddressreport-stateprovince.md)<br/> | Schreibgeschützt<br/> | Der Name des Bundesstaats oder kantons.<br/>                      |
| [**Timestamp**](locationdisp-dispcivicaddressreport-timestamp.md)<br/>         | Schreibgeschützt<br/> | Das Datum und die Uhrzeit, zu der der Bericht generiert wurde.<br/> |



 

## <a name="remarks"></a>Hinweise

Sie können dieses Objekt über die [**CivicAddressReport-Eigenschaft**](locationdisp-dispcivicaddressreport-civicaddressreport.md) eines [**CivicAddressReportFactory-Objekts**](locationdisp-civicaddressreportfactory.md) abrufen. Sie können dieses Objekt über das [**NewCivicAddressReport-Ereignis**](newcivicaddressreport.md) empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

