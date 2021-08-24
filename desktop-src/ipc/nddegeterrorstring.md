---
description: Konvertiert einen Fehlercode, der von einer Netzwerk-DDE-Funktion zurückgegeben wird, in eine Fehlerzeichenfolge, die den zurückgegebenen Fehlercode erläutert.
ms.assetid: 7077e3bc-df6e-401b-9ac7-15144b79af96
title: NDdeGetErrorString-Funktion (Nddeapi.h)
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
ms.openlocfilehash: 728ccd283f0f65caafd6f23781bd75f18e9c796ad2fb147f00ab6350c53bfd2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119557040"
---
# <a name="nddegeterrorstring-function"></a>NDdeGetErrorString-Funktion

\[Netzwerk-DDE wird nicht mehr unterstützt. Nddeapi.dll ist auf Windows Vista vorhanden, aber alle Funktionsaufrufe geben NDDE \_ NICHT \_ IMPLEMENTIERT zurück.\]

Konvertiert einen Fehlercode, der von einer Netzwerk-DDE-Funktion zurückgegeben wird, in eine Fehlerzeichenfolge, die den zurückgegebenen Fehlercode erläutert.

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

*uErrorCode* \[ In\]
</dt> <dd>

Der Fehlercode, der in eine Fehlerzeichenfolge konvertiert werden soll.

</dd> <dt>

*lpszErrorString* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die übersetzte Fehlerzeichenfolge empfängt. Dieser Parameter darf nicht **NULL sein.** Wenn der Puffer nicht groß genug ist, um die vollständige Fehlerzeichenfolge zu speichern, wird die Zeichenfolge abgeschnitten.

</dd> <dt>

*cBufSize* \[ In\]
</dt> <dd>

Die Größe des Puffers, der die Fehlerzeichenfolge empfangen soll, in **TCHARs**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert „0“.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null). Wenn der *lpszErrorString-Puffer* nicht groß genug ist, um die vollständige Fehlerzeichenfolge zu akzeptieren, und die Zeichenfolge abgeschnitten wird, gibt die Funktion den Wert NDDE \_ INTERNAL ERROR \_ zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **NDdeGetErrorStringW** (Unicode) und **NDdeGetErrorStringA** (ANSI)<br/>        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht dynamische Daten Exchange Netzwerksicherheit](network-dynamic-data-exchange.md)
</dt> <dt>

[DDE-Netzwerkfunktionen](network-dde-functions.md)
</dt> </dl>

 

 




