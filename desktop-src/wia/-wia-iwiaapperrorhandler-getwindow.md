---
description: Ruft ein Handle für das Dialogfeld ab, das Fehlermeldungen anzeigt und eine oder mehrere Schaltflächen zum Fortfahren, Abbrechen oder Abbrechen der Anwendung bereitstellt.
ms.assetid: 54deac2e-a395-45dc-b9f9-ecf8140fd9d7
title: 'Iwiaapperrorhandler:: GetWindow-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.GetWindow
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 89a3b2bf87d99c767ab3bea46a27c8a53fab7825
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349428"
---
# <a name="iwiaapperrorhandlergetwindow-method"></a>Iwiaapperrorhandler:: GetWindow-Methode

Ruft ein Handle für das Dialogfeld ab, das Fehlermeldungen anzeigt und eine oder mehrere Schaltflächen zum Fortfahren, Abbrechen oder Abbrechen der Anwendung bereitstellt.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetWindow(
  [out] HWND *phwnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*phwnd* \[ vorgenommen\]
</dt> <dd>

Geben Sie Folgendes ein: **HWND \** _

HWND, das vom Anwendungsfehler Handler, dem Treiber Fehlerhandler und dem Standardfehler Handler für Geräte Meldungs Dialogfelder (Fehler und Information) verwendet wird. Der Ausgabewert ist möglicherweise _ * NULL * *.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

*phwnd* zeigt auf das Fenster, das vom Windows-Abbild Erfassungs Proxy (WIA) 2,0 an [**Report Status**](-wia-iwiaerrorhandler-reportstatus.md) weitergeleitet wird. Dieses Fenster muss für die Dauer der Datenübertragung gültig bleiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 




