---
description: Stellt einen Bericht über die Bericht der öffentlichen Adressen dar
ms.assetid: 7c6e790f-0150-4ea8-9583-df633ebf035d
title: LocationDisp. dispcivicaddressreport-Objekt
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
ms.openlocfilehash: 2a2a96f3d0c2a1fe8e3ac78e5db67ded031a4aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348089"
---
# <a name="locationdispdispcivicaddressreport-object"></a>LocationDisp. dispcivicaddressreport-Objekt

\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen. Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]

Stellt einen Bericht über die Bericht der öffentlichen Adressen dar

## <a name="members"></a>Member

Das **LocationDisp. dispcivicaddressreport** -Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **LocationDisp. dispcivicaddressreport** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                              | Zugriffstyp          | BESCHREIBUNG                                                 |
|:--------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------|
| [**AddressLine1**](locationdisp-dispcivicaddressreport-addressline1.md)<br/>   | Schreibgeschützt<br/> | Die erste Zeile einer Straße.<br/>              |
| [**AddressLine2**](locationdisp-dispcivicaddressreport-addressline2.md)<br/>   | Schreibgeschützt<br/> | Die zweite Zeile einer Straße.<br/>             |
| [**Stadt**](locationdisp-dispcivicaddressreport-city.md)<br/>                   | Schreibgeschützt<br/> | Der Name der Stadt.<br/>                                   |
| [**CountryRegion**](locationdisp-civicaddressreport-countryregion.md)<br/>     | Schreibgeschützt<br/> | Der Name des Landes oder der Region.<br/>                      |
| [**Detail Level**](locationdisp-dispcivicaddressreport-detaillevel.md)<br/>     | Schreibgeschützt<br/> | Die Detailebene für den Bericht.<br/>                 |
| [**PostalCode**](locationdisp-dispcivicaddressreport-postalcode.md)<br/>       | Schreibgeschützt<br/> | Die Postleitzahl.<br/>                                 |
| [**StateProvince**](locationdisp-dispcivicaddressreport-stateprovince.md)<br/> | Schreibgeschützt<br/> | Der Name des Bundesstaats oder der Provinz.<br/>                      |
| [**Timestamp**](locationdisp-dispcivicaddressreport-timestamp.md)<br/>         | Schreibgeschützt<br/> | Das Datum und die Uhrzeit, zu der der Bericht generiert wurde.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Sie können dieses Objekt über die Eigenschaft [**civicaddressreport**](locationdisp-dispcivicaddressreport-civicaddressreport.md) eines [**civicaddressreportfactory**](locationdisp-civicaddressreportfactory.md) -Objekts abrufen. Sie können dieses Objekt über das [**newcivicaddressreport**](newcivicaddressreport.md) -Ereignis empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

