---
description: 'LocationDisp.DispLatLongReport.Timestamp-Eigenschaft: Datum und Uhrzeit der Berichtgenerierung.'
ms.assetid: 3b8036aa-499c-4baf-bcc4-5b6c3f54eb7b
title: LocationDisp.DispLatLongReport.Timestamp-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Timestamp
api_type:
- COM
api_location: ''
ms.openlocfilehash: 02b1d2bc344ec954f8c309e2370755464857fd754b16f6664760f9df4e0e5f54
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129910"
---
# <a name="locationdispdisplatlongreporttimestamp-property"></a>LocationDisp.DispLatLongReport.Timestamp-Eigenschaft

\[Das Location API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-Geolocation-API,](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))um von einer Website aus auf den Standort zuzugreifen. Um von einer Desktopanwendung aus auf den Speicherort zuzugreifen, verwenden Sie die [**Windows. Devices.Geolocation-API.**](/uwp/api/Windows.Devices.Geolocation)\]

Das Datum und die Uhrzeit, zu der der Bericht generiert wurde.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
Timestamp = LocationDisp.DispLatLongReport.Timestamp
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft ist ein schreibgeschütztes **Datum.** Zeitstempel werden als koordinierte Weltzeit (UTC) bereitgestellt.

## <a name="remarks"></a>Hinweise

Beachten Sie, dass Skriptsprachen wie Microsoft JScript möglicherweise Konvertierungen in andere Zeitformate erfordern, wenn Sie Zeitstempel als Zeichenfolgen anzeigen.

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Eigenschaft finden Sie unter [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

