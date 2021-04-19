---
title: Rasadminfrebuffer-Funktion (rassapi. h)
description: Die rasadminfrebuffer-Funktion gibt Arbeitsspeicher frei, der von RAS im Auftrag des Aufrufers zugeordnet wurde.
ms.assetid: 6dfbba22-3af1-4771-8c22-506996f30c6b
keywords:
- Rasadminfrebuffer-Funktion (RAS)
topic_type:
- apiref
api_name:
- RasAdminFreeBuffer
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf86a3005a2b865b2096eddc5ffa9c0c33f848a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370956"
---
# <a name="rasadminfreebuffer-function"></a>Rasadminfrebuffer-Funktion

\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4,0 bereitgestellt. Es wird ein Fehler zurückgegeben, \_ \_ \_ der auf Windows Server 2003 nicht implementiert ist. Anwendungen sollten die [**mpradminbufferfree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) -Funktion verwenden.\]

Die **rasadminfrebuffer** -Funktion gibt Arbeitsspeicher frei, der von RAS im Auftrag des Aufrufers zugeordnet wurde.

## <a name="syntax"></a>Syntax


```C++
DWORD RasAdminFreeBuffer(
  _In_ PVOID Pointer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zeiger* \[ in\]
</dt> <dd>

Zeiger auf den Puffer, der freigegeben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, kann der folgende Fehlercode als Rückgabewert zurückgegeben werden.



| Wert                                                                                                    | Bedeutung                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**Fehler bei \_ ungültigem \_ Parameter**</dt> </dl> | Der *Zeiger* Parameter ist ungültig.<br/> |



 

Es sind keine erweiterten Fehlerinformationen für diese Funktion vorhanden. " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)" nicht aufrufen.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **rasadminfreebuffer** -Funktion, um die Puffer freizugeben, die von den Funktionen [**rasadminportenum**](rasadminportenum.md) und [**rasadminportgetinfo**](rasadminportgetinfo.md) belegt werden.

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

[**Rasadminportenum**](rasadminportenum.md)
</dt> <dt>

[**Rasadminportgetinfo**](rasadminportgetinfo.md)
</dt> </dl>

 

