---
description: Öffnet ein System Dialogfeld zum Anfordern von Benutzerberechtigungen für Geräte, die für den Standort aktiviert sind.
ms.assetid: b213591a-2830-4979-b532-e71cdef1b994
title: LocationDisp. civicaddressreportfactory. requestberechtigungs Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.RequestPermissions
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6d027687302c544974d13b1ba50194e8d6003a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349778"
---
# <a name="locationdispcivicaddressreportfactoryrequestpermissions-method"></a>LocationDisp. civicaddressreportfactory. requestberechtigungs Methode

\[Das Location-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Standort von einer Website zuzugreifen. Verwenden Sie die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API, um auf den Speicherort einer Desktop Anwendung zuzugreifen.\]

Öffnet ein System Dialogfeld zum Anfordern von Benutzerberechtigungen für Geräte, die für den Standort aktiviert sind.

## <a name="syntax"></a>Syntax


```JScript
LocationDisp.CivicAddressReportFactory.RequestPermissions(
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
> Wenn eine Anwendung, die im geschützten Modus ausgeführt wird, z. b. ein Browserhilfsobjekt (BHO) für Internet Explorer, **requestberechtigungen** aufruft und der Benutzer die Option **diesen Speicherort nicht aktivieren** im Dialogfeld aktiviert, wird der Speicherort Anbieter nicht aktiviert, aber Windows zeigt das Dialogfeld erneut an, wenn **requestberechtigungs Berechtigungen** vom gleichen Benutzer erneut aufgerufen werden. Anwendungen, die im geschützten Modus ausgeführt werden, können [**anfordererberechtigungen**](/windows/win32/api/locationapi/nf-locationapi-ilocation-requestpermissions) beim Start nicht aufrufen, damit dem Benutzer bei jedem Start der Anwendung kein möglicherweise unerwünschtes Dialogfeld angezeigt wird.

 

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Methode finden Sie unter Überwachen von [Ereignissen zu öffentlichen Adress Berichten](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

