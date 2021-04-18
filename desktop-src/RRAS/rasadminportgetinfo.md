---
title: Rasadminportgetinfo-Funktion (rassapi. h)
description: Die rasadminportgetinfo-Funktion Ruft Informationen zu einem angegebenen Port auf einem angegebenen Server ab.
ms.assetid: 22837685-62a4-4e55-b88f-11019d5d4154
keywords:
- Rasadminportgetinfo-Funktion (RAS)
topic_type:
- apiref
api_name:
- RasAdminPortGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d80c55b3182ec930732344cb7857f99c0dc411
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360952"
---
# <a name="rasadminportgetinfo-function"></a>Rasadminportgetinfo-Funktion

\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4,0 bereitgestellt. Es wird ein Fehler zurückgegeben, \_ \_ \_ der auf Windows Server 2003 nicht implementiert ist. Anwendungen sollten die [**mpradminportgetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) -Funktion verwenden.\]

Die **rasadminportgetinfo** -Funktion Ruft Informationen zu einem angegebenen Port auf einem angegebenen Server ab.

## <a name="syntax"></a>Syntax


```C++
DWORD RasAdminPortGetInfo(
  _In_  const WCHAR               *lpszServer,
  _In_  const WCHAR               *lpszPort,
  _Out_       RAS_PORT_1          *pRasPort1,
  _Out_       RAS_PORT_STATISTICS *pRasStats,
  _Out_       RAS_PARAMETERS      **ppRasParams
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

</dd> <dt>

*pRasPort1* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die [**RAS- \_ Port- \_ 1**](ras-port-1-str.md) -Struktur, die die Funktion mit Informationen über den Status des Ports füllt.

</dd> <dt>

" *prasstats* \[ " vorgenommen\]
</dt> <dd>

Ein Zeiger auf die Struktur der [**RAS- \_ Port \_ Statistik**](ras-port-statistics-str.md) , die die Funktion mit Statistiken zum Port füllt.

</dd> <dt>

*pprasparams* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine Zeiger Variable, die die Adresse eines Arrays von [**RAS- \_ Parameter**](ras-parameters-str.md) Strukturen empfängt. Jede Struktur enthält den Namen eines medienspezifischen Schlüssels (z. b. maxconnectbit/s) und den zugehörigen Wert. Wenn die Anwendung mit diesem Arbeitsspeicher fertig ist, können Sie Sie freigeben, indem Sie die [**rasadminfreebuffer**](rasadminfreebuffer.md) -Funktion aufrufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Fehlercodes sein.



| Wert                                                                                                     | Bedeutung                                                                          |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**Fehler \_ dev ist \_ nicht \_ vorhanden.**</dt> </dl>     | Der angegebene Port ist ungültig.<br/>                                        |
| <dl> <dt>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</dt> </dl> | Nicht genügend Arbeitsspeicher, um einen Puffer für das *pprasparams* -Array zuzuordnen.<br/> |



 

Es sind keine erweiterten Fehlerinformationen für diese Funktion vorhanden. " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)" nicht aufrufen.

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

[**RAS- \_ Parameter**](ras-parameters-str.md)
</dt> <dt>

[**RAS- \_ Port \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**RAS- \_ Port \_ Statistik**](ras-port-statistics-str.md)
</dt> <dt>

[**Rasadminfrebuffer**](rasadminfreebuffer.md)
</dt> </dl>

 

