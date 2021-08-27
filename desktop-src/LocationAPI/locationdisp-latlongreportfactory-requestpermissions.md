---
description: 'LocationDisp.LatLongReportFactory.RequestPermissions-Methode: Öffnet ein Systemdialogfeld zum Anfordern der Benutzerberechtigung für standortfähige Geräte.'
ms.assetid: 25b4368d-ff9d-4806-a22e-4ae0760d6f0f
title: LocationDisp.LatLongReportFactory.RequestPermissions-Methode
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
ms.openlocfilehash: ffbae03d22cee89b5974b32b224c779210e82feb23292628a5a705bc203dbc5e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129830"
---
# <a name="locationdisplatlongreportfactoryrequestpermissions-method"></a>LocationDisp.LatLongReportFactory.RequestPermissions-Methode

\[Das Location-API-Objektmodell steht für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen zur Verfügung. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-Geolocation-API,](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))um von einer Website aus auf den Standort zuzugreifen. Um über eine Desktopanwendung auf den Speicherort zu zugreifen, verwenden Sie [**die Windows. Devices.Geolocation-API.**](/uwp/api/Windows.Devices.Geolocation)\]

Öffnet ein Systemdialogfeld, in dem Benutzerberechtigungen für standortfähige Geräte anfordern werden.

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

## <a name="remarks"></a>Hinweise

Der Aufruf ist synchron, und der Aufrufer wartet darauf, dass das Dialogfeld geschlossen wird.

> [!Note]  
> Wenn eine Anwendung, die im geschützten Modus ausgeführt wird, z. B. ein Browser-Hilfsobjekt (Browser  Helper Object, BHO) für Internet Explorer, **RequestPermissions** aufruft und der Benutzer die Option Diesen Standortsensor nicht aktivieren im Dialogfeld auswählt, wird der Standortanbieter nicht aktiviert, aber Windows zeigt das Dialogfeld erneut an, wenn **RequestPermissions** erneut vom gleichen Benutzer aufgerufen wird. Anwendungen, die im geschützten Modus ausgeführt werden, können **requestPermissions** beim Start nicht aufrufen, damit dem Benutzer nicht bei jedem Start der Anwendung ein möglicherweise unerwünschtes Dialogfeld angezeigt wird.

 

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Methode finden Sie unter [Lauschen auf LatLong-Berichtsereignisse.](/uwp/api/Windows.Devices.Geolocation)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

