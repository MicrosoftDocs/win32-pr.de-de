---
description: 'LocationDisp.DispCivicAddressReport.Timestamp-Eigenschaft: Datum und Uhrzeit der Berichtgenerierung.'
ms.assetid: b9435384-72e0-42c4-a948-df52621a5ec2
title: LocationDisp.DispCivicAddressReport.Timestamp-Eigenschaft
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
ms.openlocfilehash: 12388706c0b8e9205f398ec259314ab05ff5fe1c062f4b8920d610b7d74b36f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129990"
---
# <a name="locationdispdispcivicaddressreporttimestamp-property"></a>LocationDisp.DispCivicAddressReport.Timestamp-Eigenschaft

\[Das Location API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-Geolocation-API,](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))um von einer Website aus auf den Standort zuzugreifen. Um von einer Desktopanwendung aus auf den Speicherort zuzugreifen, verwenden Sie die [**Windows. Devices.Geolocation-API.**](/uwp/api/Windows.Devices.Geolocation)\]

Das Datum und die Uhrzeit, zu der der Bericht generiert wurde.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
Timestamp = LocationDisp.DispCivicAddressReport.Timestamp
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft ist ein schreibgeschütztes **Datum.** Zeitstempel werden als koordinierte Weltzeit (UTC) bereitgestellt.

## <a name="remarks"></a>Hinweise

Beachten Sie, dass Skriptsprachen wie Microsoft JScript möglicherweise Konvertierungen in andere Zeitformate erfordern, wenn Sie Zeitstempel als Zeichenfolgen anzeigen.

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Eigenschaft finden Sie unter [A Simple Civic Address Report Example](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

