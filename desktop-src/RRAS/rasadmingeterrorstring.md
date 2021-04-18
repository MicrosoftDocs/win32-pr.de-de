---
title: Rasadmingeterrorstring-Funktion (rassapi. h)
description: Die rasadmingeterrorstring-Funktion Ruft eine Meldungs Zeichenfolge ab, die einem RAS-Fehlercode entspricht, der von einer der RAS-Server Verwaltungsfunktionen (rasadmin) zurückgegeben wurde.
ms.assetid: b51bc1f9-fed7-43b6-9a07-f19ea4c0cd01
keywords:
- Rasadmingeterrorstring-Funktion (RAS)
topic_type:
- apiref
api_name:
- RasAdminGetErrorString
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc239c5f26061b5234631079ba21ce0d24ad570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372037"
---
# <a name="rasadmingeterrorstring-function"></a>Rasadmingeterrorstring-Funktion

\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4,0 bereitgestellt. Es wird ein Fehler zurückgegeben, \_ \_ \_ der auf Windows Server 2003 nicht implementiert ist. Anwendungen sollten die [**mpradmingeterrorstring**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) -Funktion verwenden.\]

Die **rasadmingeterrorstring** -Funktion Ruft eine Meldungs Zeichenfolge ab, die einem RAS-Fehlercode entspricht, der von einer der RAS-Server Verwaltungsfunktionen (rasadmin) zurückgegeben wurde. Diese Nachrichten Zeichenfolgen werden aus dem Rasmsg.dll abgerufen, der als Teil von RAS installiert wird.

## <a name="syntax"></a>Syntax


```C++
DWORD RasAdminGetErrorString(
  _In_  UINT  ResourceId,
  _Out_ WCHAR *lpszString,
  _In_  DWORD InBufSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ResourceId* \[ in\]
</dt> <dd>

Gibt einen Fehlercode an, der von einer der rasadmin-Funktionen zurückgegeben wurde. Dieser Wert muss im Bereich der Fehlercodes von "rasbase" zu "rasbaseend" liegen. Diese werden in "raserror. h" definiert.

</dd> <dt>

*lpszstring* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die Fehlermeldung empfängt, die dem angegebenen Fehlercode entspricht.

</dd> <dt>

*Inbubsize* \[ in\]
</dt> <dd>

Gibt die Größe des *lpszstring* -Puffers in Zeichen an. Fehlermeldungen sind in der Regel 80 Zeichen oder weniger. eine Puffergröße von 512 Zeichen ist immer ausreichend.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode. Dieser Wert kann ein letzter Fehlerwert sein, der von den Funktionen [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [**globalzuordc**](/windows/win32/api/winbase/nf-winbase-globalalloc)oder [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) festgelegt wird. oder Sie können einen der folgenden Fehlercodes aufweisen:



| Wert                                                                                                      | Bedeutung                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**Fehler bei \_ ungültigem \_ Parameter**</dt> </dl>   | Die Parameter " *ResourceId* " oder " *lpszstring* " sind ungültig.<br/>      |
| <dl> <dt>**Fehler \_ beim \_ Puffer.**</dt> </dl> | Die vom *inbubsize* -Parameter angegebene Größe ist zu klein.<br/> |



 

Es sind keine erweiterten Fehlerinformationen für diese Funktion vorhanden. " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)" nicht aufrufen.

## <a name="remarks"></a>Bemerkungen

Die rasadmin-Funktionen können Fehlercodes zurückgeben, die nicht im von der **rasadmingeterrorstring** -Funktion unterstützten Bereich liegen. Die rasadmin-Funktionen können z. b. Fehlercodes zurückgeben, die in "lmerr. h" und "Winerror. h" definiert sind. Vergewissern Sie sich vor dem Aufrufen von **rasadmingeterrorstring**, dass sich der Fehlercode im Bereich "rasbase" zu "rasbaseend" befindet, wie in "raserror. h" definiert.

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

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc)
</dt> <dt>

[**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> </dl>

 

