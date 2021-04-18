---
description: Ruft den Typ und die Daten für den angegebenen Registrierungs Wert in einer Offline Registrierungs Struktur ab.
ms.assetid: 83604743-cb59-42a1-9951-620ad5bd8de7
title: Orgetvalue-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 375dae37e2e6b6299a7bf1fd36f9b950d0433d89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368545"
---
# <a name="orgetvalue-function"></a>Orgetvalue-Funktion

Ruft den Typ und die Daten für den angegebenen Registrierungs Wert in einer Offline Registrierungs Struktur ab.

## <a name="syntax"></a>Syntax


```C++
DWORD ORGetValue(
  _In_        ORHKEY Handle,
  _In_opt_    PCWSTR lpSubKey,
  _In_opt_    PCWSTR lpValue,
  _Out_opt_   PDWORD pdwType,
  _Out_opt_   PVOID  pvData,
  _Inout_opt_ PDWORD pcbData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handle* \[ in\]
</dt> <dd>

Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur.

</dd> <dt>

*lpsubkey* \[ in, optional\]
</dt> <dd>

Der Name des Registrierungsschlüssels. Dieser Schlüssel muss ein Unterschlüssel des Schlüssels sein, der durch den *handle* -Parameter angegeben wird. Dieser Parameter kann **NULL** sein.

Bei Schlüsselnamen wird Groß-/Kleinschreibung nicht beachtet.

</dd> <dt>

*lpValue* \[ in, optional\]
</dt> <dd>

Der Name des Registrierungs Werts. Wenn dieser Parameter **null** oder eine leere Zeichenfolge ("") ist, ruft die Funktion den Typ und die Daten für den unbenannten oder Standardwert des Schlüssels ab, sofern vorhanden. Weitere Informationen finden Sie unter [Größenbeschränkungen für das Registrierungs Element](../sysinfo/registry-element-size-limits.md).

Schlüssel haben nicht automatisch einen unbenannten oder Standardwert. Unbenannte Werte können von einem beliebigen Typ sein.

Bei Werten Namen wird die Groß-/Kleinschreibung nicht beachtet

</dd> <dt>

*pdwtype* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Code empfängt, der den Typ der im angegebenen Wert gespeicherten Daten angibt. Eine Liste der möglichen Typcodes finden Sie unter [Registrierungs Werttypen](../sysinfo/registry-value-types.md). Dieser Parameter kann **null** sein, wenn der Typ nicht erforderlich ist.

</dd> <dt>

*pvData* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die Daten des Werts empfängt. Dieser Parameter kann **null** sein, wenn die Daten nicht erforderlich sind.

Wenn es sich bei den Daten um eine Zeichenfolge handelt, prüft die Funktion auf ein abschließendes NULL-Zeichen. Wenn eine solche nicht gefunden wird, wird die Zeichenfolge mit einem NULL-Terminator gespeichert, wenn der Puffer groß genug ist, um das zusätzliche Zeichen aufnehmen zu können. Andernfalls schlägt die Funktion fehl und gibt Fehlermeldungen zurück \_ \_ .

</dd> <dt>

*pcbData* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe des Puffers angibt, auf den der *pvData* -Parameter zeigt (in Bytes). Wenn die Funktion zurückgegeben wird, enthält diese Variable die Größe der Daten, die in *pvData* kopiert werden.

Der *pcbData* -Parameter kann nur **null** sein, wenn *pvData* **null** ist.

Wenn die Daten über das reg \_ SZ-Format, den reg \_ \_ MultiSZ-oder den reg-Typ "SZ" aufweisen \_ \_ , enthält diese Größe alle abschließenden NULL-Zeichen oder Zeichen. Weitere Informationen finden Sie in den Hinweisen.

Wenn der durch den *pvData* -Parameter angegebene Puffer nicht groß genug ist, um die Daten zu speichern, gibt die Funktion Fehler \_ Weitere \_ Daten zurück und speichert die erforderliche Puffergröße in der Variablen, auf die von *pcbData* verwiesen wird. In diesem Fall ist der Inhalt des *pvData* -Puffers nicht definiert.

Wenn *pvData* den Wert **null** hat und *pcbData* ungleich **null** ist, gibt die Funktion den Fehler Erfolg zurück \_ und speichert die Größe der Daten in Bytes in der Variablen, auf die von *pcbData* verwiesen wird. Dies ermöglicht es einer Anwendung, die beste Methode zum Zuordnen eines Puffers für die Daten des Werts zu bestimmen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist. Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung ruft in der Regel die Funktion " [**orenvalue**](orenumvalue.md) " auf, um die Wertnamen zu bestimmen, und ruft dann die **orgetvalue** -Funktion auf, um die Daten für die Namen abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher<br/>                      |
| Header<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Orkreatekey**](orcreatekey.md)
</dt> <dt>

[**Orenkey**](orenumkey.md)
</dt> <dt>

[**Orenvalue**](orenumvalue.md)
</dt> <dt>

[**Oropenkey**](oropenkey.md)
</dt> <dt>

[**Orqueryinfokey**](orqueryinfokey.md)
</dt> </dl>

 

 
