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
ms.openlocfilehash: 1b2d21a032a2e4c08c6f80e4f0ae79349a49ce21
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088928"
---
# <a name="locationdisplatlongreportfactoryrequestpermissions-method"></a>LocationDisp.LatLongReportFactory.RequestPermissions-Methode

\[Das Location-API-Objektmodell steht für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen zur Verfügung. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [W3C-Geolocation-API,](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))um von einer Website aus auf den Standort zuzugreifen. Verwenden Sie die [**Windows.Devices.Geolocation-API,**](/uwp/api/Windows.Devices.Geolocation) um über eine Desktopanwendung auf den Standort zuzugreifen.\]

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

## <a name="remarks"></a>Bemerkungen

Der Aufruf ist synchron, und der Aufrufer wartet darauf, dass das Dialogfeld geschlossen wird.

> [!Note]  
> Wenn eine Anwendung, die im geschützten Modus ausgeführt wird, z. B. ein Browser-Hilfsobjekt (Browser  Helper Object, BHO) für Internet Explorer, **RequestPermissions** aufruft und der Benutzer die Option Diesen Standortsensor nicht aktivieren im Dialogfeld auswählt, wird der Standortanbieter nicht aktiviert, aber Windows zeigt das Dialogfeld erneut an, wenn **RequestPermissions** erneut vom gleichen Benutzer aufgerufen wird. Anwendungen, die im geschützten Modus ausgeführt werden, können **requestPermissions** beim Start nicht aufrufen, damit dem Benutzer nicht bei jedem Start der Anwendung ein möglicherweise unerwünschtes Dialogfeld angezeigt wird.

 

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Methode finden Sie unter [Lauschen auf LatLong-Berichtsereignisse.](/uwp/api/Windows.Devices.Geolocation)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|--------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ 7-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                  |



 

