---
description: Listet die Werte für den angegebenen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur auf. Die-Funktion Ruft bei jedem Aufruf der-Funktion Informationen für einen Wert unter dem angegebenen Schlüssel ab.
ms.assetid: 592a404f-a35d-4d89-ad1e-d572787bcb12
title: Orenvalue-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b8049a5d16a88dc87bf4c0f6f5e8ef18b30beadc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372069"
---
# <a name="orenumvalue-function"></a>Orenvalue-Funktion

Listet die Werte für den angegebenen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur auf. Die-Funktion Ruft bei jedem Aufruf der-Funktion Informationen für einen Wert unter dem angegebenen Schlüssel ab.

## <a name="syntax"></a>Syntax


```C++
DWORD OREnumValue(
  _In_        ORHKEY Handle,
  _In_        DWORD  dwIndex,
  _Out_       PWSTR  lpValueName,
  _Inout_     PDWORD lpcValueName,
  _Out_opt_   PDWORD lpType,
  _Out_opt_   PBYTE  lpData,
  _Inout_opt_ PDWORD lpcbData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handle* \[ in\]
</dt> <dd>

Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur.

</dd> <dt>

*dwIndex* \[ in\]
</dt> <dd>

Der Index des abzurufenden Werts. Dieser Parameter sollte für den ersten Aufruf der Funktion 0 (null) sein und dann für nachfolgende Aufrufe inkrementiert werden.

Da die Werte nicht geordnet sind, haben alle neuen Werte einen beliebigen Index. Dies bedeutet, dass die Funktion Werte in beliebiger Reihenfolge zurückgeben kann.

</dd> <dt>

*lpvaluename* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der den Namen des Werts als NULL-terminierte Zeichenfolge empfängt. Dieser Puffer muss groß genug sein, um das abschließende Null-Zeichen einzuschließen.

Weitere Informationen finden Sie unter [Größenbeschränkungen für das Registrierungs Element](../sysinfo/registry-element-size-limits.md).

</dd> <dt>

*lpcvaluename* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe des Puffers angibt, auf den der *lpvaluename* -Parameter zeigt (in Zeichen). Wenn die Funktion zurückgibt, empfängt die-Variable die Anzahl der im Puffer gespeicherten Zeichen, ohne das abschließende Null Zeichen.

</dd> <dt>

*lptype* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Code empfängt, der den Typ der im angegebenen Wert gespeicherten Daten angibt. Eine Liste der möglichen Typcodes finden Sie unter [Registrierungs Werttypen](../sysinfo/registry-value-types.md). Der *lptype* -Parameter kann **null** sein, wenn der Typcode nicht erforderlich ist.

</dd> <dt>

*lpdata* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die Daten für den Wert Eintrag empfängt. Dieser Parameter kann **null** sein, wenn die Daten nicht erforderlich sind.

Wenn *lpdata* den Wert **null** hat und *lpcbdata* ungleich **null** ist, speichert die Funktion die Größe der Daten in Bytes in der Variablen, auf die von *lpcbdata* verwiesen wird. Dadurch kann eine Anwendung die beste Methode zum Zuordnen eines Puffers für die Daten bestimmen.

</dd> <dt>

*lpcbdata* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe des Puffers angibt, auf den der *lpdata* -Parameter zeigt (in Bytes). Wenn die Funktion zurückgegeben wird, empfängt die-Variable die Anzahl von Bytes, die im Puffer gespeichert werden.

Dieser Parameter kann nur **null** sein, wenn *lpdata* **null** ist.

Wenn die Daten über das reg \_ SZ-Format, den reg \_ \_ MultiSZ-oder den reg-Typ "SZ" aufweisen \_ \_ , enthält diese Größe alle abschließenden NULL-Zeichen oder Zeichen. Weitere Informationen finden Sie in den Hinweisen.

Wenn der von *lpdata* angegebene Puffer nicht groß genug ist, um die Daten zu speichern, gibt die Funktion Fehler \_ Weitere \_ Daten zurück und speichert die erforderliche Puffergröße in der Variablen, auf die von *lpcbdata* verwiesen wird. In diesem Fall ist der Inhalt von *lpdata* nicht definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist. Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.

Wenn der *lpdata* -Puffer zu klein ist, um den Wert zu erhalten, gibt die Funktion Fehler \_ Weitere \_ Daten zurück.

## <a name="remarks"></a>Bemerkungen

Um Werte aufzuzählen, sollte eine Anwendung zunächst die Funktion " **orenvalue** " aufrufen, wobei der *dwIndex* -Parameter auf NULL festgelegt ist. Die Anwendung sollte dann *dwIndex* Inkrement erhöhen und die Funktion " **orenvalue** " so lange aufzurufen, bis keine weiteren Werte vorhanden sind (bis die Funktion "Error \_ No More Items" zurückgibt \_ \_ ).

Die Anwendung kann *dwIndex* auch auf den Index des letzten Werts beim ersten Aufrufe der Funktion festlegen und den Index verringern, bis der Wert mit Index 0 aufgezählt wird. Um den Index des letzten Werts abzurufen, verwenden Sie die [**orqueryinfokey**](orqueryinfokey.md) -Funktion.

Bei der Verwendung von " **orenvalue**" sollte eine Anwendung keine Offline Registrierungsfunktionen aufzurufen, die möglicherweise den abgefragten Schlüssel ändern.

Wenn die Daten den "reg \_ SZ"-, "reg \_ MultiSZ"-oder "reg expand"- \_ \_ \_ Dokumenttyp aufweisen, wurde die Zeichenfolge möglicherweise nicht mit den ordnungsgemäßen NULL-abschließenden Zeichen gespeichert. Daher sollte die Anwendung auch dann, wenn die Funktion Fehler erfolgreich zurückgibt \_ , sicherstellen, dass die Zeichenfolge ordnungsgemäß beendet wird, bevor Sie verwendet wird. andernfalls kann Sie einen Puffer überschreiben. (Beachten Sie, dass reg \_ \_MultiSZ-Zeichen folgen sollten zwei NULL-abschließende Zeichen aufweisen.)

Verwenden Sie die [**orqueryinfokey**](orqueryinfokey.md) -Funktion, um die maximale Größe des Namens und der Datenpuffer zu ermitteln.

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

[**Oropenkey**](oropenkey.md)
</dt> <dt>

[**Orqueryinfokey**](orqueryinfokey.md)
</dt> </dl>

 

 
