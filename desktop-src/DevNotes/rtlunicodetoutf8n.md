---
description: Übersetzt die angegebene Unicode-Zeichenfolge mithilfe der UTF-8-Codepage (8-Bit-Unicode Transformation Format) in eine neue Zeichenfolge.
ms.assetid: ecd63eee-bf86-42b5-93d8-3c7871aa6324
title: RtlUnicodeToUTF8N-Funktion (WDM. h)
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
ms.openlocfilehash: 46153dd152ed5a45a65de50ca214fbb24a6dc2ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126398"
---
# <a name="rtlunicodetoutf8n-function"></a>RtlUnicodeToUTF8N-Funktion

Übersetzt die angegebene Unicode-Zeichenfolge mithilfe der UTF-8-Codepage (8-Bit-Unicode Transformation Format) in eine neue Zeichenfolge.

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

*UTF8StringDestination* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen vom Aufrufer zugewiesenen Puffer, der die übersetzte Zeichenfolge empfängt.

</dd> <dt>

*UTF8StringMaxByteCount* \[ in\]
</dt> <dd>

Maximale Anzahl von Bytes, die in *UTF8StringDestination* geschrieben werden sollen. Wenn dieser Wert bewirkt, dass die übersetzte Zeichenfolge abgeschnitten wird, gibt **RtlUnicodeToUTF8N** einen Fehlerstatus zurück.

</dd> <dt>

*UTF8StringActualByteCount* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine vom Aufrufer zugewiesene Variable, die die Länge der übersetzten Zeichenfolge in Bytes empfängt. Dieser Parameter ist optional und kann **null** sein. Wenn die Zeichenfolge abgeschnitten wird, zählt die zurückgegebene Zahl die tatsächliche Anzahl der abgeschnittene Zeichen folgen.

</dd> <dt>

*Unicodestringsource* \[ in\]
</dt> <dd>

Ein Zeiger auf die Unicode-Quell Zeichenfolge, die übersetzt werden soll.

</dd> <dt>

* Unicodestringbytecount * \[ in\]
</dt> <dd>

Gibt die Anzahl der Bytes in der Unicode-Quell Zeichenfolge an, auf die der *unicodestringsource* -Parameter verweist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**RtlUnicodeToUTF8N** gibt einen der folgenden NTSTATUS-Werte zurück:



| Rückgabecode                                                                                                  | Beschreibung                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Status \_ Erfolg**</dt> </dl>               | Die Unicode-Zeichenfolge wurde in UTF-8 konvertiert.<br/>                                                           |
| <dl> <dt>**Status \_ " \_ nicht \_ zugeordnet"**</dt> </dl>     | Es wurde ein ungültiges Eingabezeichen gefunden und ersetzt. Dieser Status wird als Erfolgsstatus betrachtet.<br/> |
| <dl> <dt>**\_ungültiger \_ Parameter.**</dt> </dl>    | Beide Zeiger auf *UTF8StringDestination* und *UTF8StringActualByteCount* waren **null**.<br/>              |
| <dl> <dt>**\_Ungültiger \_ Parameter \_ 4**</dt> </dl> | *Unicodestringsource* war **null**.<br/>                                                              |
| <dl> <dt>**Status \_ Puffer \_ zu \_ klein**</dt> </dl>    | *UTF8StringDestination* wurde abgeschnitten.<br/>                                                               |



 

## <a name="remarks"></a>Bemerkungen

Obwohl *UTF8StringActualByteCount* optional ist und **null** sein kann, sollten Aufrufer Speicher für die Anwendung bereitstellen, da die empfangene Länge verwendet werden kann, um zu bestimmen, ob die Konvertierung erfolgreich war. Die Quell Zeichenfolge wird von dieser Routine nicht geändert. Sie gibt eine auf NULL abschließende UTF-8-Zeichenfolge zurück, wenn die angegebene *unicodestringsource* ein NULL-Terminator enthielt und wenn die angegebene *UTF8StringMaxByteCount* keine abkürzen verursacht hat.

Wenn die Ausgabe abgeschnitten wird und ein ungültiges Eingabezeichen gefunden wird, gibt die Funktion den Status \_ Puffer \_ zu \_ klein.

Wenn *UTF8StringDestination* auf **null** festgelegt ist, gibt die Funktion die erforderliche Anzahl von Bytes zurück, um die übersetzte Zeichenfolge ohne Abschneiden in *UTF8StringActualByteCount* zu hosten.

Aufrufer von **RtlUnicodeToUTF8N** müssen auf der < Dispatch-Ebene von "iriql" ausgeführt werden \_

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>WDM. h</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RtlUTF8ToUnicodeN**](rtlutf8tounicoden.md)
</dt> </dl>

 

 




