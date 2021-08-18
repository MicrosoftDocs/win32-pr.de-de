---
title: RasAdminPortClearStatistics-Funktion (Rassapi.h)
description: Die RasAdminPortClearStatistics-Funktion setzt die Leistungsindikatoren zurück, die die verschiedenen Statistiken darstellen, die von der RasAdminPortGetInfo-Funktion in der RAS \_ PORT \_ STATISTICS-Struktur gemeldet werden. Die Leistungsindikatoren werden auf null zurückgesetzt und beginnen mit der Akkumulierung.
ms.assetid: d2ce4652-1034-4ded-aa26-2678c719d5b9
keywords:
- RasAdminPortClearStatistics-Funktion RAS
topic_type:
- apiref
api_name:
- RasAdminPortClearStatistics
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3da7d17516e7dd7708821a7c60c2d93db913f25c38471524367ae96494e41f38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788987"
---
# <a name="rasadminportclearstatistics-function"></a>RasAdminPortClearStatistics-Funktion

\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4.0 bereitgestellt. Es wird ERROR \_ CALL NOT IMPLEMENTED auf Windows Server \_ \_ 2003 zurückgegeben. Anwendungen sollten die [**MprAdminPortClearStats-Funktion**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) verwenden.\]

Die **RasAdminPortClearStatistics-Funktion** setzt die Leistungsindikatoren zurück, die die verschiedenen Statistiken darstellen, die von der [**RasAdminPortGetInfo-Funktion**](rasadminportgetinfo.md) in der [**RAS PORT \_ \_ STATISTICS-Struktur gemeldet**](ras-port-statistics-str.md) werden. Die Leistungsindikatoren werden auf null zurückgesetzt und beginnen mit der Akkumulierung.

## <a name="syntax"></a>Syntax


```C++
DWORD RasAdminPortClearStatistics(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszServer* \[ In\]
</dt> <dd>

Zeiger auf eine auf NULL beendete Unicode-Zeichenfolge, die den Namen des RAS-Servers angibt. Geben Sie den Namen mit den \\ \\ führenden Zeichen " " im folgenden Formular an: \\ \\ *Servername*.

</dd> <dt>

*lpszPort* \[ In\]
</dt> <dd>

Zeiger auf eine auf NULL beendete Unicode-Zeichenfolge, die den Namen des Ports auf dem Server angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, kann der Rückgabewert der folgende Fehlercode sein.



| Wert                                                                                                 | Bedeutung                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**FEHLER \_ DEV \_ NICHT \_ VORHANDEN**</dt> </dl> | Der angegebene Port ist ungültig.<br/> |



 

Es gibt keine erweiterten Fehlerinformationen für diese Funktion. Rufen Sie [**getLastError nicht auf.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Hinweise

Mit **der RasAdminPortClearStatistics-Funktion** werden die Statistiken auf dem Server und nicht lokal innerhalb der Anwendung, die den Aufruf vor sich hat, entiert. Dies bedeutet, dass die Statistiken auch für jede andere Anwendung zurückgesetzt werden, die den angegebenen Port überwacht.

Wenn der *lpszPort-Port* Teil einer Multilinkverbindung ist, setzt **RasAdminPortClearStatistics** die Statistiken für den angegebenen Port zurück. Die Funktion setzt auch die kumulativen Statistiken für die Multilinkverbindung zurück. Die Funktion wirkt sich jedoch nicht auf die einzelnen Statistiken für andere Ports aus, die Teil der Multilinkverbindung sind.

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

[**\_ \_ RAS-PORTSTATISTIK**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

