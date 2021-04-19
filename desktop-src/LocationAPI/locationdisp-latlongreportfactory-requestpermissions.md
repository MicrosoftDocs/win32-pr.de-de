---
description: Öffnet ein System Dialogfeld zum Anfordern von Benutzerberechtigungen für Geräte, die für den Standort aktiviert sind.
ms.assetid: 25b4368d-ff9d-4806-a22e-4ae0760d6f0f
title: LocationDisp. latlongreportfactory. requestberechtigungs Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.RequestPermissions
api_type:
- COM
api_location: ''
ms.openlocfilehash: ed789aca4b6c9d0db50a3e7b6cae33d55d22920c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358542"
---
# <a name="locationdisplatlongreportfactoryrequestpermissions-method"></a>LocationDisp. latlongreportfactory. requestberechtigungs Methode

\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen. Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]

Öffnet ein System Dialogfeld zum Anfordern von Benutzerberechtigungen für Geräte, die für den Standort aktiviert sind.

## <a name="syntax"></a>Syntax


```JScript
LocationDisp.LatLongReportFactory.RequestPermissions(
  hWnd
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hWnd* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und sollte auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Aufruf erfolgt synchron, und der Aufrufer wartet darauf, dass das Dialogfeld geschlossen wird.

> [!Note]  
> Wenn eine Anwendung, die im geschützten Modus ausgeführt wird, z. b. ein Browserhilfsobjekt (BHO) für Internet Explorer, **requestberechtigungen** aufruft und der Benutzer die Option **diesen Speicherort nicht aktivieren** im Dialogfeld aktiviert, wird der Speicherort Anbieter nicht aktiviert, aber Windows zeigt das Dialogfeld erneut an, wenn **requestberechtigungs Berechtigungen** vom gleichen Benutzer erneut aufgerufen werden. Anwendungen, die im geschützten Modus ausgeführt werden, können **anfordererberechtigungen** beim Start nicht aufrufen, damit dem Benutzer bei jedem Start der Anwendung kein möglicherweise unerwünschtes Dialogfeld angezeigt wird.

 

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Methode finden Sie unter [lauschen auf latlong-Bericht Ereignisse](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

