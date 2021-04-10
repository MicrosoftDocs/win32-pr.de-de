---
description: Übersetzt die angegebene Quell Zeichenfolge unter Verwendung der UTF-8-Codepage (8-Bit-Unicode Transformation Format) in eine Unicode-Zeichenfolge.
ms.assetid: 2871a81b-74f9-462e-9e5c-c59d06bb6841
title: RtlUTF8ToUnicodeN-Funktion (WDM. h)
ms.topic: reference
ms.date: 02/21/2019
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUTF8ToUnicodeN
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8b3de7192a9a26d367fc0b6ad231fbc046514ec6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214099"
---
# <a name="rtlutf8tounicoden-function"></a>RtlUTF8ToUnicodeN-Funktion

Übersetzt die angegebene Quell Zeichenfolge unter Verwendung der UTF-8-Codepage (8-Bit-Unicode Transformation Format) in eine Unicode-Zeichenfolge.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI RtlUTF8ToUnicodeN(
  _Out_     PWSTR  UnicodeStringDestination,
  _In_      ULONG  UnicodeStringMaxByteCount,
  _Out_opt_ PULONG UnicodeStringActualByteCount,
  _In_      PCCH   UTF8StringSource,
  _In_      ULONG  UTF8StringByteCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Unicodestringdestination* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen vom Aufrufer zugewiesenen Puffer, der die übersetzte Zeichenfolge empfängt.

</dd> <dt>

*Unicodestringmaxbytecount* \[ in\]
</dt> <dd>

Maximale Anzahl von Bytes, die bei *unicodestringdestination* geschrieben werden sollen. Wenn dieser Wert bewirkt, dass die übersetzte Zeichenfolge abgeschnitten wird, gibt **RtlUTF8ToUnicodeN** einen Fehlerstatus zurück.

</dd> <dt>

*Unicodestringactualbytecount* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine vom Aufrufer zugewiesene Variable, die die Länge der übersetzten Zeichenfolge in Bytes empfängt. Dieser Parameter ist optional und kann **null** sein. Wenn die Zeichenfolge abgeschnitten wird, zählt die zurückgegebene Zahl die tatsächliche Anzahl der abgeschnittene Zeichen folgen.

</dd> <dt>

*UTF8StringSource* \[ in\]
</dt> <dd>

Ein Zeiger auf die Zeichenfolge, die übersetzt werden soll.

</dd> <dt>

*UTF8StringByteCount* \[ in\]
</dt> <dd>

Größe (in Bytes) der Zeichenfolge in *UTF8StringSource*.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**RtlUTF8ToUnicodeN** gibt einen der folgenden NTSTATUS-Werte zurück:



| Rückgabecode                                                                                                  | Beschreibung                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Status \_ Erfolg**</dt> </dl>               | Die Zeichenfolge wurde in Unicode konvertiert.<br/>                                                                 |
| <dl> <dt>**Status \_ " \_ nicht \_ zugeordnet"**</dt> </dl>     | Es wurde ein ungültiges Eingabezeichen gefunden und ersetzt. Dieser Status wird als Erfolgsstatus betrachtet.<br/> |
| <dl> <dt>**\_ungültiger \_ Parameter.**</dt> </dl>    | Beide Zeiger auf *unicodestringdestination* und *unicodestringactualbytecount* waren **null**.<br/>       |
| <dl> <dt>**\_Ungültiger \_ Parameter \_ 4**</dt> </dl> | Der *UTF8StringSource* war **null**.<br/>                                                                 |
| <dl> <dt>**Status \_ Puffer \_ zu \_ klein**</dt> </dl>    | *Unicodestringdestination* wurde abgeschnitten.<br/>                                                            |



 

## <a name="remarks"></a>Bemerkungen

Obwohl *unicodestringactualbytecount* optional ist und **null** sein kann, sollten Aufrufer Speicher für die Anwendung bereitstellen, da die empfangene Länge verwendet werden kann, um zu bestimmen, ob die Konvertierung erfolgreich war.

Wenn die Ausgabe abgeschnitten wird und ein ungültiges Eingabezeichen gefunden wird, gibt die Funktion den Status \_ Puffer \_ zu \_ klein.

Wenn *unicodestringdestination* auf **null** festgelegt ist, gibt die Funktion die erforderliche Anzahl von Bytes zurück, um die übersetzte Zeichenfolge zu hosten, ohne dass in *unicodestringactualbytecount* abgeschnitten wird.

**RtlUTF8ToUnicodeN** ändert nicht die Quell Zeichenfolge, es sei denn, die *unicodestringdestination* -und *UTF8StringSource* -Zeiger sind gleichwertig. Die zurückgegebene Unicode-Zeichenfolge wird nicht mit Null beendet.

Aufrufer von **RtlUTF8ToUnicodeN** müssen auf der < Dispatch-Ebene von "iriql" ausgeführt werden \_

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>WDM. h</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RtlUnicodeToUTF8N**](rtlunicodetoutf8n.md)
</dt> </dl>

 

 




