---
title: RasAdminPortGetInfo-Funktion (Rassapi.h)
description: Die RasAdminPortGetInfo-Funktion ruft Informationen zu einem angegebenen Port auf einem angegebenen Server ab.
ms.assetid: 22837685-62a4-4e55-b88f-11019d5d4154
keywords:
- RasAdminPortGetInfo-Funktion RAS
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
ms.openlocfilehash: e633b663e9c4b35810585a2ac738c79ae2d39be06d7b91be0df75fd0455a5213
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028510"
---
# <a name="rasadminportgetinfo-function"></a>RasAdminPortGetInfo-Funktion

\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4.0 bereitgestellt. Auf \_ Windows \_ Server 2003 wird ERROR CALL NOT \_ IMPLEMENTED zurückgegeben. Anwendungen sollten die [**MprAdminPortGetInfo-Funktion**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) verwenden.\]

Die **RasAdminPortGetInfo-Funktion** ruft Informationen zu einem angegebenen Port auf einem angegebenen Server ab.

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

*lpszServer* \[ In\]
</dt> <dd>

Zeiger auf eine auf NULL endende Unicode-Zeichenfolge, die den Namen des RAS-Servers angibt. Geben Sie den Namen mit führenden Zeichen vom Typ \\ \\ " " im Format \\ \\ *Servername an.*

</dd> <dt>

*lpszPort* \[ In\]
</dt> <dd>

Zeiger auf eine auf NULL endende Unicode-Zeichenfolge, die den Namen des Ports auf dem Server angibt.

</dd> <dt>

*pRasPort1* \[ out\]
</dt> <dd>

Zeiger auf die [**RAS \_ PORT \_ 1-Struktur,**](ras-port-1-str.md) die die Funktion mit Informationen zum Zustand des Ports ausfüllt.

</dd> <dt>

*pRasStats* \[ out\]
</dt> <dd>

Zeiger auf die [**RAS \_ PORT \_ STATISTICS-Struktur,**](ras-port-statistics-str.md) die die Funktion mit Statistiken zum Port auffüllt.

</dd> <dt>

*ppRasParams* \[ out\]
</dt> <dd>

Zeiger auf eine Zeigervariable, die die Adresse eines Arrays von [**RAS \_ PARAMETERS-Strukturen**](ras-parameters-str.md) empfängt. Jede Struktur enthält den Namen eines medienspezifischen Schlüssels, z. B. MAXCONNECTBPS, und den zugehörigen Wert. Wenn die Anwendung mit diesem Arbeitsspeicher fertig ist, können Sie sie freigeben, indem Sie die [**RasAdminFreeBuffer-Funktion**](rasadminfreebuffer.md) aufrufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Fehlercodes sein.



| Wert                                                                                                     | Bedeutung                                                                          |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**FEHLER \_ BEI \_ NICHT \_ VORHANDENER ENTWICKLUNG**</dt> </dl>     | Der angegebene Port ist ungültig.<br/>                                        |
| <dl> <dt>**FEHLER \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**</dt> </dl> | Nicht genügend Arbeitsspeicher zum Zuordnen eines Puffers für das *ppRasParams-Array.*<br/> |



 

Für diese Funktion sind keine erweiterten Fehlerinformationen vorhanden. Rufen [**Sie getLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)nicht auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows 2000 Professional<br/>                                                   |
| Ende des Supports (Server)<br/> | Windows 2000 Server<br/>                                                         |
| Header<br/>                | <dl> <dt>Rassapi.h</dt> </dl>   |
| Bibliothek<br/>               | <dl> <dt>Rassapi.lib</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remotezugriffsdienst (RAS) – Übersicht](about-remote-access-service.md)
</dt> <dt>

[RAS-Serververwaltungsfunktionen](ras-server-administration-functions.md)
</dt> <dt>

[**\_RAS-PARAMETER**](ras-parameters-str.md)
</dt> <dt>

[**\_RAS-PORT \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**\_ \_ RAS-PORTSTATISTIKEN**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminFreeBuffer**](rasadminfreebuffer.md)
</dt> </dl>

 

