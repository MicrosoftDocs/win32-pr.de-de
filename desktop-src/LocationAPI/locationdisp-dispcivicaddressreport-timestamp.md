---
description: 'LocationDisp.DispCivicAddressReport.Timestamp-Eigenschaft: Datum und Uhrzeit der Berichtgenerieren.'
ms.assetid: b9435384-72e0-42c4-a948-df52621a5ec2
title: LocationDisp.DispCivicAddressReport.Timestamp (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispCivicAddressReport.Timestamp
api_type:
- COM
api_location: ''
ms.openlocfilehash: d2ed39956bb542aa4e150bf9afa3e59a472a4d91
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110878"
---
# <a name="locationdispdispcivicaddressreporttimestamp-property"></a>LocationDisp.DispCivicAddressReport.Timestamp (Eigenschaft)

\[Das Location-API-Objektmodell steht für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen zur Verfügung. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-Geolocation-API,](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))um von einer Website aus auf den Standort zuzugreifen. Verwenden Sie die [**Windows.Devices.Geolocation-API,**](/uwp/api/Windows.Devices.Geolocation) um über eine Desktopanwendung auf den Standort zuzugreifen.\]

Das Datum und die Uhrzeit, zu der der Bericht generiert wurde.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
Timestamp = LocationDisp.DispCivicAddressReport.Timestamp
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft ist ein schreibgeschütztes **Datum.** Zeitstempel werden als koordinierte Weltzeit (UTC) bereitgestellt.

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass Skriptsprachen wie Microsoft JScript möglicherweise Konvertierungen in andere Zeitformate erfordern, wenn Sie Zeitstempel als Zeichenfolgen anzeigen.

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Eigenschaft finden Sie unter [A Simple Civic Address Report Example](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ 7-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

