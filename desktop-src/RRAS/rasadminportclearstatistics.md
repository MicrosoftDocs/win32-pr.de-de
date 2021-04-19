---
title: Rasadminportclearstatistics-Funktion (rassapi. h)
description: Die rasadminportclearstatistics-Funktion setzt die Zähler zurück, die die verschiedenen Statistiken darstellen, die von der rasadminportgetinfo-Funktion in der Struktur der RAS- \_ Port Statistik gemeldet werden \_ . Die Zähler werden auf 0 (null) zurückgesetzt und beginnen mit der Anhäufung
ms.assetid: d2ce4652-1034-4ded-aa26-2678c719d5b9
keywords:
- Rasadminportclearstatistics-Funktion (RAS)
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
ms.openlocfilehash: 57943fbefcba1625c7badff25827c62eaca8a8c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370082"
---
# <a name="rasadminportclearstatistics-function"></a>Rasadminportclearstatistics-Funktion

\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4,0 bereitgestellt. Es wird ein Fehler zurückgegeben, \_ \_ \_ der auf Windows Server 2003 nicht implementiert ist. Anwendungen sollten die [**mpradminportclearstats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) -Funktion verwenden.\]

Die **rasadminportclearstatistics** -Funktion setzt die Zähler zurück, die die verschiedenen Statistiken darstellen, die von der [**rasadminportgetinfo**](rasadminportgetinfo.md) -Funktion in der Struktur der [**RAS- \_ Port \_ Statistik**](ras-port-statistics-str.md) gemeldet werden. Die Zähler werden auf 0 (null) zurückgesetzt und beginnen mit der Anhäufung

## <a name="syntax"></a>Syntax


```C++
DWORD RasAdminPortClearStatistics(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszserver* \[ in\]
</dt> <dd>

Zeiger auf eine mit NULL endenden Unicode-Zeichenfolge, die den Namen des RAS-Servers angibt. Geben Sie den Namen mit führenden " \\ \\ " Zeichen im folgenden Format an: \\ \\ *Servername*.

</dd> <dt>

*lpszport* \[ in\]
</dt> <dd>

Zeiger auf eine mit NULL endenden Unicode-Zeichenfolge, die den Namen des Ports auf dem Server angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, kann der folgende Fehlercode als Rückgabewert zurückgegeben werden.



| Wert                                                                                                 | Bedeutung                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**Fehler \_ dev ist \_ nicht \_ vorhanden.**</dt> </dl> | Der angegebene Port ist ungültig.<br/> |



 

Es sind keine erweiterten Fehlerinformationen für diese Funktion vorhanden. " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)" nicht aufrufen.

## <a name="remarks"></a>Bemerkungen

Die **rasadminportclearstatistics** -Funktion löscht die Statistiken auf dem Server, nicht lokal innerhalb der Anwendung, die den-Befehl ausführt. Dies bedeutet, dass die Statistiken auch für alle anderen Anwendungen zurückgesetzt werden, die den angegebenen Port überwachen.

Wenn der *lpszport* -Port Teil einer Multilinkverbindung ist, setzt **rasadminportclearstatistics** die Statistiken für den angegebenen Port zurück, die-Funktion setzt auch die kumulativen Statistiken für die mehrfach-Verbindung zurück. Die Funktion wirkt sich jedoch nicht auf die einzelnen Statistiken für andere Ports aus, die Teil der mehrfach-Verbindung sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows 2000 Professional<br/>                                                   |
| Ende des Supports (Server)<br/> | Windows 2000 Server<br/>                                                         |
| Header<br/>                | <dl> <dt>Rassapi. h</dt> </dl>   |
| Bibliothek<br/>               | <dl> <dt>Rassapi. lib</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remote Zugriffs Dienst (RAS) (Übersicht)](about-remote-access-service.md)
</dt> <dt>

[RAS-Server-Verwaltungsfunktionen](ras-server-administration-functions.md)
</dt> <dt>

[**RAS- \_ Port \_ Statistik**](ras-port-statistics-str.md)
</dt> <dt>

[**Rasadminportgetinfo**](rasadminportgetinfo.md)
</dt> </dl>

 

