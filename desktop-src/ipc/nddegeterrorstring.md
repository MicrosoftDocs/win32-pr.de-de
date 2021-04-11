---
description: Konvertiert einen Fehlercode, der von einer Network DDE-Funktion zurückgegeben wird, in eine Fehler Zeichenfolge, die den zurückgegebenen Fehlercode
ms.assetid: 7077e3bc-df6e-401b-9ac7-15144b79af96
title: Nddebug. String-Funktion (nddecoapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetErrorString
- NDdeGetErrorStringA
- NDdeGetErrorStringW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 8e043c8281d3ad049346ac7ce68991eb6bd08af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041591"
---
# <a name="nddegeterrorstring-function"></a>Nddebug-terrorstring-Funktion

\[Network DDE wird nicht mehr unterstützt. Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]

Konvertiert einen Fehlercode, der von einer Network DDE-Funktion zurückgegeben wird, in eine Fehler Zeichenfolge, die den zurückgegebenen Fehlercode

## <a name="syntax"></a>Syntax


```C++
UINT NDdeGetErrorString(
  _In_  UINT   uErrorCode,
  _Out_ LPTSTR lpszErrorString,
  _In_  DWORD  cBufSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*uerrorcode* \[ in\]
</dt> <dd>

Der Fehlercode, der in eine Fehler Zeichenfolge konvertiert werden soll.

</dd> <dt>

*lpszerrorstring* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die übersetzte Fehler Zeichenfolge empfängt. Dieser Parameter darf nicht **null** sein. Wenn der Puffer nicht groß genug ist, um die gesamte Fehler Zeichenfolge zu speichern, wird die Zeichenfolge abgeschnitten.

</dd> <dt>

*cbubsize* \[ in\]
</dt> <dd>

Die Größe des Puffers, der die Fehler Zeichenfolge empfängt, in **tchars**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert „0“.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null). Wenn der *lpszerrorstring* -Puffer nicht groß genug ist, um die gesamte Fehler Zeichenfolge zu akzeptieren, und die Zeichenfolge abgeschnitten wird, gibt die Funktion den Wert "ndde \_ internal error" zurück \_ .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Ndde API. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ndde API. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Ndbegeterrorstringw** (Unicode) und **nddebug** (ANSI)<br/>        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über das Netzwerk dynamischer Datenaustausch](network-dynamic-data-exchange.md)
</dt> <dt>

[Network DDE-Funktionen](network-dde-functions.md)
</dt> </dl>

 

 




