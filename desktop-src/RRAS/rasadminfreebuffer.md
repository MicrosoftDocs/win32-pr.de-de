---
title: RasAdminFreeBuffer-Funktion (Rassapi.h)
description: Die RasAdminFreeBuffer-Funktion gibt Arbeitsspeicher frei, der vom RAS im Auftrag des Aufrufers zugeordnet wurde.
ms.assetid: 6dfbba22-3af1-4771-8c22-506996f30c6b
keywords:
- RasAdminFreeBuffer-Funktion RAS
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
ms.openlocfilehash: 9550c072840fabf5d862e32f3bbdc6c26d3b32faf9cf6bf6dcfeae1be400e0a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789095"
---
# <a name="rasadminfreebuffer-function"></a>RasAdminFreeBuffer-Funktion

\[Diese Funktion wird nur aus Gründen der Abwärtskompatibilität mit Windows NT Server 4.0 bereitgestellt. Es wird ERROR \_ CALL NOT IMPLEMENTED auf Windows Server \_ \_ 2003 zurückgegeben. Anwendungen sollten die [**MprAdminBufferFree-Funktion**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) verwenden.\]

Die **RasAdminFreeBuffer-Funktion** gibt Arbeitsspeicher frei, der vom RAS im Auftrag des Aufrufers zugeordnet wurde.

## <a name="syntax"></a>Syntax


```C++
DWORD RasAdminFreeBuffer(
  _In_ PVOID Pointer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zeiger* \[ In\]
</dt> <dd>

Zeiger auf den frei zu werdenden Puffer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, kann der Rückgabewert der folgende Fehlercode sein.



| Wert                                                                                                    | Bedeutung                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**FEHLER \_ UNGÜLTIGER \_ PARAMETER**</dt> </dl> | Der *Zeigerparameter* ist ungültig.<br/> |



 

Es gibt keine erweiterten Fehlerinformationen für diese Funktion. Rufen Sie [**getLastError nicht auf.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Hinweise

Verwenden Sie **die Funktion RasAdminFreeBuffer,** um die Puffer frei zu geben, die von den [**Funktionen RasAdminPortEnum**](rasadminportenum.md) und [**RasAdminPortGetInfo zugeordnet**](rasadminportgetinfo.md) werden.

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

[**RasAdminPortEnum**](rasadminportenum.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

