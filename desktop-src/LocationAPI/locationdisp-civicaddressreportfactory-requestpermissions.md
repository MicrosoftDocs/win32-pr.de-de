---
description: 'LocationDisp.CivicAddressReportFactory.RequestPermissions-Methode: Öffnet ein Systemdialogfeld, in dem Benutzerberechtigungen für standortfähige Geräte angefordert werden.'
ms.assetid: b213591a-2830-4979-b532-e71cdef1b994
title: LocationDisp.CivicAddressReportFactory.RequestPermissions-Methode
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
ms.openlocfilehash: cab163585fa23839eb894f7ad83f29ed7975e589
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110908"
---
# <a name="locationdispcivicaddressreportfactoryrequestpermissions-method"></a>LocationDisp.CivicAddressReportFactory.RequestPermissions-Methode

\[Das Standort-API-Objektmodell ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-Geolocation-API,](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))um von einer Website aus auf den Standort zuzugreifen. Verwenden Sie die [**Windows.Devices.Geolocation-API,**](/uwp/api/Windows.Devices.Geolocation) um von einer Desktopanwendung aus auf den Standort zuzugreifen.\]

Öffnet ein Systemdialogfeld, in dem Benutzerberechtigungen für standortfähige Geräte angefordert werden.

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

Der Aufruf ist synchron, und der Aufrufer wartet, bis das Dialogfeld geschlossen wird.

> [!Note]  
> Wenn eine Anwendung, die im geschützten Modus ausgeführt wird, z. B. ein Browserhilfsobjekt (Browser Helper Object, BHO) für Internet Explorer, **RequestPermissions** aufruft und der Benutzer die Option **Diesen Standortsensor nicht aktivieren** im Dialogfeld aus wählt, wird der Standortanbieter nicht aktiviert, aber Windows zeigt das Dialogfeld erneut an, wenn **RequestPermissions** erneut vom gleichen Benutzer aufgerufen wird. Anwendungen, die im geschützten Modus ausgeführt werden, können [**requestPermissions**](/windows/win32/api/locationapi/nf-locationapi-ilocation-requestpermissions) beim Start nicht aufrufen, sodass dem Benutzer bei jedem Start der Anwendung kein möglicherweise unerwünschtes Dialogfeld angezeigt wird.

 

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Methode finden Sie unter [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ 7-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

