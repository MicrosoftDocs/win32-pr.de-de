---
description: Das Datum und die Uhrzeit, zu der der Bericht generiert wurde.
ms.assetid: 3b8036aa-499c-4baf-bcc4-5b6c3f54eb7b
title: LocationDisp. displatlongreport. Timestamp (Eigenschaft)
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
ms.openlocfilehash: 5ec179c5958b1be73a5fd5f74e48d0063edb6696
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369872"
---
# <a name="locationdispdisplatlongreporttimestamp-property"></a>LocationDisp. displatlongreport. Timestamp (Eigenschaft)

\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen. Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]

Das Datum und die Uhrzeit, zu der der Bericht generiert wurde.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
Timestamp = LocationDisp.DispLatLongReport.Timestamp
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft ist ein Schreib geschütztes **Datum**. Zeitstempel werden als koordinierte Weltzeit (UTC) bereitgestellt.

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass es für Skriptsprachen wie z. b. Microsoft JScript erforderlich ist, Konvertierungen in andere Zeitformate auszuführen, wenn Sie Zeitstempel als Zeichen folgen anzeigen.

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Eigenschaft finden Sie unter [Beispiel für einen einfachen latlong-Bericht](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

