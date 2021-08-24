---
description: Übersetzt die angegebene Unicode-Zeichenfolge mithilfe der Codepage 8-Bit Unicode Transformation Format (UTF-8) in eine neue Zeichenfolge.
ms.assetid: ecd63eee-bf86-42b5-93d8-3c7871aa6324
title: RtlUnicodeToUTF8N-Funktion (Wdm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUnicodeToUTF8N
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3580eb86deba77bcc214cf69fbd21f65fee2735ef3a5ff73319b415d2c814d88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538030"
---
# <a name="rtlunicodetoutf8n-function"></a>RtlUnicodeToUTF8N-Funktion

Übersetzt die angegebene Unicode-Zeichenfolge mithilfe der Codepage 8-Bit Unicode Transformation Format (UTF-8) in eine neue Zeichenfolge.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI RtlUnicodeToUTF8N(
  _Out_     PCHAR  UTF8StringDestination,
  _In_      ULONG  UTF8StringMaxByteCount,
  _Out_opt_ PULONG UTF8StringActualByteCount,
  _In_      PCWSTR UnicodeStringSource,
  _In_      ULONG  UnicodeStringByteCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*UTF8StringDestination* \[ out\]
</dt> <dd>

Ein Zeiger auf einen vom Aufrufer zugeordneten Puffer, um die übersetzte Zeichenfolge zu empfangen.

</dd> <dt>

*UTF8StringMaxByteCount* \[ In\]
</dt> <dd>

Maximale Anzahl von Bytes, die in *UTF8StringDestination* geschrieben werden sollen. Wenn dieser Wert bewirkt, dass die übersetzte Zeichenfolge abgeschnitten wird, gibt **RtlUnicodeToUTF8N** einen Fehlerstatus zurück.

</dd> <dt>

*UTF8StringActualByteCount* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf eine vom Aufrufer zugeordnete Variable, die die Länge der übersetzten Zeichenfolge in Bytes empfängt. Dieser Parameter ist optional und kann **NULL** sein. Wenn die Zeichenfolge abgeschnitten wird, zählt die zurückgegebene Zahl die tatsächliche abgeschnittene Zeichenfolgenanzahl.

</dd> <dt>

*UnicodeStringSource* \[ In\]
</dt> <dd>

Ein Zeiger auf die zu übersetzende Unicode-Quellzeichenfolge.

</dd> <dt>

*UnicodeStringByteCount * \[ in\]
</dt> <dd>

Gibt die Anzahl der Bytes in der Unicode-Quellzeichenfolge an, auf die der *UnicodeStringSource-Parameter* zeigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**RtlUnicodeToUTF8N** gibt einen der folgenden NTSTATUS-Werte zurück:



| Rückgabecode                                                                                                  | Beschreibung                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**STATUS \_ ERFOLGREICH**</dt> </dl>               | Die Unicode-Zeichenfolge wurde in UTF-8 konvertiert.<br/>                                                           |
| <dl> <dt>**STATUS \_ EINIGE \_ NICHT \_ ZUGEORDNET**</dt> </dl>     | Ein ungültiges Eingabezeichen wurde gefunden und ersetzt. Dieser Status wird als Erfolgsstatus betrachtet.<br/> |
| <dl> <dt>**STATUS \_ UNGÜLTIGER \_ PARAMETER**</dt> </dl>    | Beide Zeiger auf *UTF8StringDestination* und *UTF8StringActualByteCount* waren **NULL.**<br/>              |
| <dl> <dt>**STATUS \_ UNGÜLTIGER \_ PARAMETER \_ 4**</dt> </dl> | *UnicodeStringSource* war **NULL.**<br/>                                                              |
| <dl> <dt>**STATUSPUFFER \_ \_ ZU \_ KLEIN**</dt> </dl>    | *UTF8StringDestination* wurde abgeschnitten.<br/>                                                               |



 

## <a name="remarks"></a>Hinweise

Obwohl *UTF8StringActualByteCount* optional ist und **NULL** sein kann, sollten Aufrufer Speicher dafür bereitstellen, da die empfangene Länge verwendet werden kann, um zu bestimmen, ob die Konvertierung erfolgreich war. Diese Routine ändert die Quellzeichenfolge nicht. Sie gibt eine auf NULL endende UTF-8-Zeichenfolge zurück, wenn die angegebene *UnicodeStringSource* ein NULL-Abschlusszeichen enthielt und die angegebene *UTF8StringMaxByteCount* keine Kürzung verursacht hat.

Wenn die Ausgabe abgeschnitten wird und ein ungültiges Eingabezeichen gefunden wird, gibt die Funktion den Fehler STATUS \_ BUFFER \_ TOO SMALL \_ zurück.

Wenn die *UTF8StringDestination* auf **NULL** festgelegt ist, gibt die Funktion die erforderliche Anzahl von Bytes zurück, um die übersetzte Zeichenfolge ohne Kürzung in *UTF8StringActualByteCount* zu hosten.

Aufrufer von **RtlUnicodeToUTF8N** müssen auf IRQL < DISPATCH LEVEL ausgeführt \_ werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Wdm.h</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RtlUTF8ToUnicodeN**](rtlutf8tounicoden.md)
</dt> </dl>

 

 




