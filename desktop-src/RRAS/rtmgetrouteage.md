---
title: Rtmgetrouteage-Funktion (RTM. h)
description: Die Funktion rtmgetrouteage gibt das Alter einer Route zurück. Das Alter ist die Zeit (in Sekunden), seit der es erstellt oder zuletzt aktualisiert wurde.
ms.assetid: 93052412-227f-4c9e-978b-3ec4bde4a256
keywords:
- Rtmgetrouteage-Funktion (RAS)
topic_type:
- apiref
api_name:
- RtmGetRouteAge
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a484bb5684fde974ce5fa704c0d0cca38c320851
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742184"
---
# <a name="rtmgetrouteage-function"></a>Rtmgetrouteage-Funktion

\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar. Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]

Die Funktion **rtmgetrouteage** gibt das Alter einer Route zurück. Das Alter ist die Zeit (in Sekunden), seit der es erstellt oder zuletzt aktualisiert wurde.

## <a name="syntax"></a>Syntax


```C++
ULONG RtmGetRouteAge(
  _In_ PVOID Route
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Route* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Protokoll Familien spezifische Struktur, die Routendaten angibt, die vor kurzem vom Routing Tabellen-Manager abgerufen wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist einer der folgenden Werte.



| Wert                                                                                   | BESCHREIBUNG                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Routeage**</dt> </dl> | Die Zeit (in Sekunden), seit der eine Route erstellt oder zuletzt aktualisiert wurde.<br/>                                                                                    |
| <dl> <dt>**Lichem**</dt> </dl> | Der Inhalt der Routen Struktur ist ungültig. In diesem Fall gibt ein Aufrufen von " [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) " einen \_ ungültigen \_ Parameter zurück.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das Routing Alter wird aus dem RR- \_ timestamp-Member der Struktur berechnet, auf die durch den *Routen* Parameter verwiesen wird. Der Routing Tabellen-Manager legt den Wert dieses Members fest, wenn eine Route hinzugefügt oder aktualisiert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                     |
| Header<br/>                   | <dl> <dt>RTM. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>RTM. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Referenz für Routing Tabellen-Manager Version \_ 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funktionen der Routing-Tabellen-Manager-Version 1](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**RTM \_ -IP- \_ Route**](rtm-ip-route.md)
</dt> <dt>

[**RTM- \_ IPX- \_ Route**](rtm-ipx-route.md)
</dt> </dl>

 

