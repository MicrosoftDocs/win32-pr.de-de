---
description: Liest eine Zeile aus der Datei "Setup. inf" und extrahiert das angegebene Feld aus der Zeichenfolge.
ms.assetid: 621e85f8-af30-4f1f-bab1-b7f824daa363
title: Parametefield-Funktion (util. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParseField
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 45c7d5bc692f969ba821b5d3243b312d0883658e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216607"
---
# <a name="parsefield-function"></a>Parametefield-Funktion

\[In der nächsten Version des Microsoft Windows-Betriebssystems ist es derzeit wahrscheinlich, dass die Funktion " **Parser Field** " für die Verwendung in der nächsten Version verfügbar ist. Sie wird möglicherweise in nachfolgenden Versionen geändert oder ist nicht verfügbar.\]

Liest eine Zeile aus der Datei "Setup. inf" und extrahiert das angegebene Feld aus der Zeichenfolge.

## <a name="syntax"></a>Syntax


```C++
bool ParseField(
  _In_ LPCTSTR *szData,
  _In_ int     n,
  _In_ LPTSTR  *szBuf,
  _In_ int     iBufLen
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szdata* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **LPCTSTR \** _

Ein Zeiger auf die Zeile aus der Datei "Setup. inf".

</dd> <dt>

_N * \[ in\]
</dt> <dd>

Typ: **int**

**Int** , der angibt, welches Feld extrahiert werden soll.

<dt>



  (0)


</dt> <dd>

Gibt das Feld vor einem Gleichheitszeichen (=) an.

</dd> <dt>



 (1)


</dt> <dd>

Gibt das erste Feld an.

</dd> </dl> </dd> <dt>

*szbuf* \[ in\]
</dt> <dd>

Typ: **LPTSTR \** _

Ein Zeiger auf den Puffer, der das extrahierte Feld empfängt.

</dd> <dt>

_iBufLen * \[ in\]
</dt> <dd>

Typ: **int**

**Int** , der die Größe des Puffers empfängt, der das extrahierte Feld empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **bool**

Gibt **true** zurück, wenn die Funktion erfolgreich ist, und **false** , wenn Sie fehlschlägt.

## <a name="remarks"></a>Bemerkungen

Die Felder in der Zeichenfolge müssen durch Kommas getrennt werden.

Führende und nachfolgende Leerzeichen werden entfernt.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Util. h</dt> </dl>                             |
| Bibliothek<br/>                  | <dl> <dt>Shell32. lib</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



 

 




