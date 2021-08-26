---
title: RasAdminGetErrorString-Funktion (Rassapi.h)
description: Die RasAdminGetErrorString-Funktion ruft eine Meldungszeichenfolge ab, die einem RAS-Fehlercode entspricht, der von einer der RAS-Serververwaltungsfunktionen (RasAdmin) zurückgegeben wird.
ms.assetid: b51bc1f9-fed7-43b6-9a07-f19ea4c0cd01
keywords:
- RasAdminGetErrorString-Funktion RAS
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
ms.openlocfilehash: a45c768daef7c889351744c5e046c83f4de7e220f59752c1db271067efb68366
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028601"
---
# <a name="rasadmingeterrorstring-function"></a>RasAdminGetErrorString-Funktion

\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4.0 bereitgestellt. Es wird ERROR \_ CALL NOT IMPLEMENTED auf Windows Server \_ \_ 2003 zurückgegeben. Anwendungen sollten die [**MprAdminGetErrorString-Funktion**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) verwenden.\]

Die **RasAdminGetErrorString-Funktion** ruft eine Meldungszeichenfolge ab, die einem RAS-Fehlercode entspricht, der von einer der RAS-Serververwaltungsfunktionen (RasAdmin) zurückgegeben wird. Diese Meldungszeichenfolgen werden aus dem Rasmsg.dll abgerufen, der als Teil von RAS installiert ist.

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

*ResourceId* \[ In\]
</dt> <dd>

Gibt einen Fehlercode an, der von einer der RasAdmin-Funktionen zurückgegeben wird. Dieser Wert muss im Bereich der Fehlercodes von RASBASE bis RASBASEEND liegen. Diese werden in Raserror.h definiert.

</dd> <dt>

*lpszString* \[ out\]
</dt> <dd>

Zeiger auf einen Puffer, der die Fehlermeldung empfängt, die dem angegebenen Fehlercode entspricht.

</dd> <dt>

*InBufSize* \[ In\]
</dt> <dd>

Gibt die Größe des *lpszString-Puffers* in Zeichen an. Fehlermeldungen sind in der Regel 80 Zeichen oder weniger. Eine Puffergröße von 512 Zeichen ist immer ausreichend.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode. Dieser Wert kann ein letzter Fehlerwert sein, der von den [**LoadLibrary-,**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**GlobalAlloc-**](/windows/win32/api/winbase/nf-winbase-globalalloc)oder [**LoadString-Funktionen festgelegt**](/windows/win32/api/winuser/nf-winuser-loadstringa) wurde. Oder es kann einer der folgenden Fehlercodes sein.



| Wert                                                                                                      | Bedeutung                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**FEHLER \_ UNGÜLTIGER \_ PARAMETER**</dt> </dl>   | Die *Parameter ResourceId* oder *lpszString* sind ungültig.<br/>      |
| <dl> <dt>**FEHLER: \_ NICHT GENÜGEND \_ PUFFER**</dt> </dl> | Die vom *InBufSize-Parameter angegebene Größe* ist zu klein.<br/> |



 

Es gibt keine erweiterten Fehlerinformationen für diese Funktion. Rufen Sie [**getLastError nicht auf.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Hinweise

Die RasAdmin-Funktionen können Fehlercodes zurückgeben, die nicht im bereich liegen, der von der **RasAdminGetErrorString-Funktion unterstützt** wird. Beispielsweise können die RasAdmin-Funktionen Fehlercodes zurückgeben, die in Lmerr.h und Winerror.h definiert sind. Stellen Sie vor dem Aufrufen **von RasAdminGetErrorString** sicher, dass sich der Fehlercode im Bereich RASBASE bis RASBASEEND befindet, wie in Raserror.h definiert.

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

[Ras-Dienst (RAS): Übersicht](about-remote-access-service.md)
</dt> <dt>

[RAS-Serververwaltungsfunktionen](ras-server-administration-functions.md)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**Globalalloc**](/windows/win32/api/winbase/nf-winbase-globalalloc)
</dt> <dt>

[**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> </dl>

 

