---
title: RasAdminPortEnum-Funktion (Rassapi.h)
description: Die RasAdminPortEnum-Funktion aufzählt alle Ports auf dem angegebenen RAS-Server. Für jeden Port auf dem Server gibt die Funktion die RAS PORT 0-Struktur zurück, \_ die Informationen zum Port \_ enthält.
ms.assetid: ad23727c-8f54-4b10-9bc7-1425ac22bc88
keywords:
- RasAdminPortEnum-Funktion RAS
topic_type:
- apiref
api_name:
- RasAdminPortEnum
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 989b86cbf78a47a62c8d98799ac18adf987cbe623dc92e703537c54b54bf892a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788872"
---
# <a name="rasadminportenum-function"></a>RasAdminPortEnum-Funktion

\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4.0 bereitgestellt. Es wird ERROR \_ CALL NOT IMPLEMENTED auf Windows Server \_ \_ 2003 zurückgegeben. Anwendungen sollten die [**MprAdminPortEnum-Funktion**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) verwenden.\]

Die **RasAdminPortEnum-Funktion** aufzählt alle Ports auf dem angegebenen RAS-Server. Für jeden Port auf dem Server gibt die Funktion die [**RAS \_ PORT \_ 0-Struktur**](ras-port-0-str.md) zurück, die Informationen zum Port enthält.

## <a name="syntax"></a>Syntax


```C++
DWORD RasAdminPortEnum(
  _In_  const WCHAR       *lpszServer,
  _Out_       PRAS_PORT_0 *ppRasPort0,
  _Out_       WORD        *pcEntriesRead
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszServer* \[ In\]
</dt> <dd>

Zeiger auf eine auf NULL beendete Unicode-Zeichenfolge, die den Namen des RAS-Servers angibt. Geben Sie den Namen mit den \\ \\ führenden Zeichen " " im folgenden Formular an: \\ \\ *Servername*.

</dd> <dt>

*ppRasPort0* \[ out\]
</dt> <dd>

Zeiger auf eine Variable, die einen Zeiger auf einen Puffer empfängt, der ein Array von [**\_ RAS-PORT \_ 0-Strukturen**](ras-port-0-str.md) enthält. Wenn die Anwendung mit dem Arbeitsspeicher fertig ist, geben Sie sie frei, indem Sie die [**RasAdminFreeBuffer-Funktion**](rasadminfreebuffer.md) aufrufen.

</dd> <dt>

*pcEntriesRead* \[ out\]
</dt> <dd>

Zeiger auf eine 16-Bit-Variable, die die Gesamtzahl der [**RAS \_ PORT \_ 0-Strukturen**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) empfängt, die im *ppRasPort0-Array zurückgegeben* werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, kann der Rückgabewert der folgende Fehlercode sein.



| Wert                                                                                             | Bedeutung                                                                                                                                     |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NERR \_ ItemNotFound**</dt> </dl> | Es konnten keine Ports aufzählt werden. Dies kann daran liegen, dass derzeit alle konfigurierten Ports auf dem Server zum Auswählen verwendet werden.<br/> |



 

Es gibt keine erweiterten Fehlerinformationen für diese Funktion. Rufen Sie [**getLastError nicht auf.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows 2000 Professional<br/>                                                   |
| Ende des Supports (Server)<br/> | Windows 2000 Server<br/>                                                         |
| Header<br/>                | <dl> <dt>Rassapi.h</dt> </dl>   |
| Bibliothek<br/>               | <dl> <dt>Rassapi.lib</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Ras-Dienst (RAS): Übersicht](about-remote-access-service.md)
</dt> <dt>

[RAS-Serververwaltungsfunktionen](ras-server-administration-functions.md)
</dt> <dt>

[**\_RAS-PORT \_ 0**](ras-port-0-str.md)
</dt> <dt>

[**RasAdminFreeBuffer**](rasadminfreebuffer.md)
</dt> </dl>

 

