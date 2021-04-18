---
title: Rasadminportenum-Funktion (rassapi. h)
description: Die rasadminportenum-Funktion Listet alle Ports auf dem angegebenen RAS-Server auf. Für jeden Port auf dem Server gibt die-Funktion die RAS- \_ Port \_ 0-Struktur zurück, die Informationen über den Port enthält.
ms.assetid: ad23727c-8f54-4b10-9bc7-1425ac22bc88
keywords:
- Rasadminportenum-Funktion (RAS)
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
ms.openlocfilehash: a5e4841627ce5df3feee3f885b399a070388ed55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352982"
---
# <a name="rasadminportenum-function"></a>Rasadminportenum-Funktion

\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4,0 bereitgestellt. Es wird ein Fehler zurückgegeben, \_ \_ \_ der auf Windows Server 2003 nicht implementiert ist. Anwendungen sollten die [**mpradminportenum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) -Funktion verwenden.\]

Die **rasadminportenum** -Funktion Listet alle Ports auf dem angegebenen RAS-Server auf. Für jeden Port auf dem Server gibt die-Funktion die [**RAS- \_ Port \_ 0**](ras-port-0-str.md) -Struktur zurück, die Informationen über den Port enthält.

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

*lpszserver* \[ in\]
</dt> <dd>

Zeiger auf eine mit NULL endenden Unicode-Zeichenfolge, die den Namen des RAS-Servers angibt. Geben Sie den Namen mit führenden " \\ \\ " Zeichen im folgenden Format an: \\ \\ *Servername*.

</dd> <dt>

*ppRasPort0* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Zeiger auf einen Puffer empfängt, der ein Array von [**RAS- \_ Port \_ 0**](ras-port-0-str.md) -Strukturen enthält. Wenn die Anwendung mit dem Arbeitsspeicher fertig ist, können Sie Sie freigeben, indem Sie die [**rasadminfreebuffer**](rasadminfreebuffer.md) -Funktion aufrufen.

</dd> <dt>

*pcentriesread* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine 16-Bit-Variable, die die Gesamtzahl der [**RAS- \_ Port \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) -Strukturen empfängt, die im *ppRasPort0* -Array zurückgegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, kann der folgende Fehlercode als Rückgabewert zurückgegeben werden.



| Wert                                                                                             | Bedeutung                                                                                                                                     |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NERR \_ ItemNotFound**</dt> </dl> | Es konnten keine Ports aufgelistet werden. Dies liegt möglicherweise daran, dass alle konfigurierten Ports auf dem Server zurzeit für die Abwahl verwendet werden.<br/> |



 

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

[**RAS- \_ Port \_ 0**](ras-port-0-str.md)
</dt> <dt>

[**Rasadminfrebuffer**](rasadminfreebuffer.md)
</dt> </dl>

 

