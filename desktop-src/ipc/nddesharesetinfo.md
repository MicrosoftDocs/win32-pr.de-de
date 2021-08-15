---
description: Legt DDE-Freigabeinformationen fest. Dies erfolgt in der Regel nach der Bearbeitung.
ms.assetid: 002c73ce-7b35-4e8e-bb7e-0e1393b97ccc
title: NDdeShareSetInfo-Funktion (Nddeapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareSetInfo
- NDdeShareSetInfoA
- NDdeShareSetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: ccfa8cc80f60477e8512ac43f0e93825642dd0603ee398e232bbb67d6979a4c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481700"
---
# <a name="nddesharesetinfo-function"></a>NDdeShareSetInfo-Funktion

\[Netzwerk-DDE wird nicht mehr unterstützt. Nddeapi.dll ist auf Windows Vista vorhanden, aber alle Funktionsaufrufe geben NDDE \_ NOT \_ IMPLEMENTED zurück.\]

Legt DDE-Freigabeinformationen fest. Dies erfolgt in der Regel nach der Bearbeitung.

## <a name="syntax"></a>Syntax


```C++
UINT NDdeShareSetInfo(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   nLevel,
  _In_ LPBYTE lpBuffer,
  _In_ DWORD  cBufSize,
  _In_ WORD   sParmNum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszServer* \[ In\]
</dt> <dd>

Der Name des Servers, dessen DSDM geändert werden soll.

</dd> <dt>

*lpszShareName* \[ In\]
</dt> <dd>

Der Name des Freigabenamens, dessen Informationen geändert werden sollen. Dieser Parameter darf nicht **NULL** sein.

</dd> <dt>

*nLevel* \[ In\]
</dt> <dd>

Die Informationsebene. Dieser Parameter muss 2 sein.

</dd> <dt>

*lpBuffer* \[in\]
</dt> <dd>

Ein Zeiger auf die [**NDDESHAREINFO-Struktur,**](nddeshareinfo-str.md) der die DDE-Freigabeinformationen angibt, die im DSDM gespeichert werden sollen. Derzeit werden die DDE-Freigabeinformationen als Ganzes geändert, d. h., es werden keine Teilbearbeitungen vorgenommen. Dieser Parameter darf nicht **NULL** sein.

</dd> <dt>

*cBufSize* \[ In\]
</dt> <dd>

Die Größe des *lpBuffer-Puffers* in Bytes.

</dd> <dt>

*sParmNum* \[ In\]
</dt> <dd>

Der zu ändernde Parameterindex. Die aktuelle Implementierung unterstützt keine Teiländerungen. daher muss dieser Parameter 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert NDDE \_ NO \_ ERROR.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch Aufrufen von [**NDdeGetErrorString**](nddegeterrorstring.md)in eine Textfehlermeldung übersetzt werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **NDdeShareSetInfoW** (Unicode) und **NDdeShareSetInfoA** (ANSI)<br/>            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Network dynamische Daten Exchange Overview (Übersicht über Netzwerk-dynamische Daten Exchange)](network-dynamic-data-exchange.md)
</dt> <dt>

[Netzwerk-DDE-Funktionen](network-dde-functions.md)
</dt> <dt>

[**NDDESHAREINFO**](nddeshareinfo-str.md)
</dt> <dt>

[**NDdeShareGetInfo**](nddesharegetinfo.md)
</dt> </dl>

 

 




