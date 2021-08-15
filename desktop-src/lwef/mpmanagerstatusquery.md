---
title: MpManagerStatusQuery-Funktion (MpClient.h)
description: Gibt Statusinformationen zu verschiedenen Komponenten des Schadsoftwareschutz-Managers zurück. | MpManagerStatusQuery-Funktion (MpClient.h)
ms.assetid: E993FD8B-A35D-41C1-9522-1B9F0BC10B3D
keywords:
- Funktionen der MpManagerStatusQuery-Legacy Windows umgebung
topic_type:
- apiref
api_name:
- MpManagerStatusQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d05751f30e1579ef8b12e31a4f858469b1c997cf9c29d7643c0600a133840fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883375"
---
# <a name="mpmanagerstatusquery-function"></a>MpManagerStatusQuery-Funktion

\[**MpManagerStatusQuery** wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen [**MpManagerStatusQueryEx.**](mpmanagerstatusqueryex.md)\]

Gibt Statusinformationen zu verschiedenen Komponenten des Schadsoftwareschutz-Managers zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI MpManagerStatusQuery(
  _In_  MPHANDLE       hMpHandle,
  _Out_ PMPSTATUS_INFO pStatusInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hMpHandle* \[ In\]
</dt> <dd>

Typ: **MPHANDLE**

Handle für die Benutzeroberfläche des Schadsoftwareschutz-Managers. Dieses Handle wird von der [**MpManagerOpen-Funktion**](mpmanageropen.md) zurückgegeben.

</dd> <dt>

*pStatusInfo* \[ out\]
</dt> <dd>

Typ: **PMPSTATUS \_ INFO**

Zeiger auf eine -Struktur, die Statusinformationen zu letzten Scans, aktiven Bedrohungen und verschiedenen Komponentenstatus zurückgibt. Weitere Informationen [**finden Sie unter MPSTATUS \_ INFO**](mpstatus-info.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert **S \_ OK.** Dieser Funktionsaufruf ist auch dann erfolgreich, wenn kein AntiMalware-Dienst ausgeführt wird.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT-Code.** Der Aufrufer kann die [**MpErrorMessageFormat-Funktion**](mperrormessageformat.md) verwenden, um eine generische Beschreibung der Fehlermeldung zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md)
</dt> <dt>

[**\_MPSTATUS-INFORMATIONEN**](mpstatus-info.md)
</dt> </dl>

 

 





