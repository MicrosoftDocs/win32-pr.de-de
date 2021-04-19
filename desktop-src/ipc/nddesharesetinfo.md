---
description: Legt DDE-Freigabe Informationen fest. Dies erfolgt in der Regel nach der Bearbeitung.
ms.assetid: 002c73ce-7b35-4e8e-bb7e-0e1393b97ccc
title: Nddesharesetinfo-Funktion (nddeapi. h)
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
ms.openlocfilehash: cee7660a58e8f2747a800650b79db20f95504f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339736"
---
# <a name="nddesharesetinfo-function"></a>Nddesharesetinfo-Funktion

\[Network DDE wird nicht mehr unterstützt. Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]

Legt DDE-Freigabe Informationen fest. Dies erfolgt in der Regel nach der Bearbeitung.

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

*lpszserver* \[ in\]
</dt> <dd>

Der Name des Servers, dessen DSDM geändert werden soll.

</dd> <dt>

*lpszsharename* \[ in\]
</dt> <dd>

Der Name des Freigabe namens, dessen Informationen geändert werden sollen. Dieser Parameter darf nicht **null** sein.

</dd> <dt>

*Nlevel* \[ in\]
</dt> <dd>

Die Informationsebene. Dieser Parameter muss 2 sein.

</dd> <dt>

*lpBuffer* \[in\]
</dt> <dd>

Ein Zeiger auf die [**nddeshareinfo**](nddeshareinfo-str.md) -Struktur, die die DDE-Freigabe Informationen angibt, die in der DSDM gespeichert werden sollen. Derzeit werden die DDE-Freigabe Informationen als Ganzes geändert, d. h., es werden keine partiellen Änderungen vorgenommen. Dieser Parameter darf nicht **null** sein.

</dd> <dt>

*cbubsize* \[ in\]
</dt> <dd>

Die Größe des *lpBuffer* -Puffers in Bytes.

</dd> <dt>

*sparmnum* \[ in\]
</dt> <dd>

Der Parameter Index, der geändert werden soll. Die aktuelle Implementierung unterstützt keine partielle Änderung. Daher muss dieser Parameter NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert "ndde \_ No \_ Error".

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch den Aufruf von [**nddegeterrorstring**](nddegeterrorstring.md)in eine Text Fehlermeldung übersetzt werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Ndde API. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ndde API. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Ndde sharesetinfow** (Unicode) und **nddebug** (ANSI)<br/>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über das Netzwerk dynamischer Datenaustausch](network-dynamic-data-exchange.md)
</dt> <dt>

[Network DDE-Funktionen](network-dde-functions.md)
</dt> <dt>

[**Nddebug-Info**](nddeshareinfo-str.md)
</dt> <dt>

[**Ndde sharegetinfo**](nddesharegetinfo.md)
</dt> </dl>

 

 




