---
description: Ruft ein Handle für das Dialogfeld ab, das Fehlermeldungen anzeigt und eine oder mehrere Schaltflächen zum Fortsetzen, Abbrechen oder Abbrechen der Anwendung enthält.
ms.assetid: 54deac2e-a395-45dc-b9f9-ecf8140fd9d7
title: IWiaAppErrorHandler::GetWindow-Methode (Wia.h)
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
ms.openlocfilehash: 1bac7ba2f2f9d394218d851f9bbe7939168c2abbc7df5fb8c57a52f29fa6e2b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965759"
---
# <a name="iwiaapperrorhandlergetwindow-method"></a>IWiaAppErrorHandler::GetWindow-Methode

Ruft ein Handle für das Dialogfeld ab, das Fehlermeldungen anzeigt und eine oder mehrere Schaltflächen zum Fortsetzen, Abbrechen oder Abbrechen der Anwendung enthält.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetWindow(
  [out] HWND *phwnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*phwnd* \[ out\]
</dt> <dd>

Typ: **HWND\***

HWND, das vom Anwendungsfehlerhandler, vom Treiberfehlerhandler und vom Standardfehlerhandler für Gerätemeldungsdialogfelder verwendet wird (fehler- und informationell). Der Ausgabewert kann **NULL sein.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

*phwnd* zeigt auf das Fenster, das vom WIA 2.0-Proxy (Windows Image Acquisition) an [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md) übergeben wird. Dieses Fenster muss für die Dauer der Datenübertragung gültig bleiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 




