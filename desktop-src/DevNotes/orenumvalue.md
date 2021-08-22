---
description: Listet die Werte für den angegebenen offenen Registrierungsschlüssel in einer Offlineregistrierungsstruktur auf. Die Funktion ruft bei jedem Aufruf der Funktion Informationen für einen Wert unter dem angegebenen Schlüssel ab.
ms.assetid: 592a404f-a35d-4d89-ad1e-d572787bcb12
title: OREnumValue-Funktion (Offreg.h)
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
ms.openlocfilehash: 57a65e8fd862215bd6281e487520857580cf6026b94b2ca375079f84407e4cc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331800"
---
# <a name="orenumvalue-function"></a>OREnumValue-Funktion

Listet die Werte für den angegebenen offenen Registrierungsschlüssel in einer Offlineregistrierungsstruktur auf. Die Funktion ruft bei jedem Aufruf der Funktion Informationen für einen Wert unter dem angegebenen Schlüssel ab.

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

*Handle* \[ In\]
</dt> <dd>

Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offlineregistrierungsstruktur.

</dd> <dt>

*dwIndex* \[ In\]
</dt> <dd>

Der Index des abzurufenden Werts. Dieser Parameter sollte für den ersten Aufruf der Funktion 0 (null) sein und dann für nachfolgende Aufrufe erhöht werden.

Da Werte nicht sortiert sind, verfügt jeder neue Wert über einen beliebigen Index. Dies bedeutet, dass die Funktion Werte in beliebiger Reihenfolge zurückgeben kann.

</dd> <dt>

*lpValueName* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der den Namen des Werts als auf NULL endende Zeichenfolge empfängt. Dieser Puffer muss groß genug sein, um das abschließende NULL-Zeichen einzuschließt.

Weitere Informationen finden Sie unter [Größenbeschränkungen für Registrierungselemente.](../sysinfo/registry-element-size-limits.md)

</dd> <dt>

*lpcValueName* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe des Puffers angibt, auf den der *lpValueName-Parameter* in Zeichen zeigt. Wenn die Funktion zurückgegeben wird, empfängt die Variable die Anzahl der im Puffer gespeicherten Zeichen, ohne das abschließende NULL-Zeichen zu enthalten.

</dd> <dt>

*lpType* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Code empfängt, der den Typ der im angegebenen Wert gespeicherten Daten angibt. Eine Liste der möglichen Typcodes finden Sie unter [Registrierungswerttypen.](../sysinfo/registry-value-types.md) Der *lpType-Parameter* kann **NULL** sein, wenn der Typcode nicht erforderlich ist.

</dd> <dt>

*lpData* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die Daten für den Werteintrag empfängt. Dieser Parameter kann **NULL** sein, wenn die Daten nicht erforderlich sind.

Wenn *lpData* **NULL** und *lpcbData* ungleich **NULL** ist, speichert die Funktion die Größe der Daten in Bytes in der Variablen, auf die *lpcbData* zeigt. Dadurch kann eine Anwendung die beste Methode zum Zuordnen eines Puffers für die Daten bestimmen.

</dd> <dt>

*lpcbData* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe des Puffers angibt, auf den der *lpData-Parameter* zeigt, in Bytes. Wenn die Funktion zurückgegeben wird, empfängt die Variable die Anzahl der im Puffer gespeicherten Bytes.

Dieser Parameter kann nur **NULL** sein, wenn *lpData* **NULL** ist.

Wenn die Daten den \_ Reg SZ-, REG \_ MULTI \_ SZ- oder REG EXPAND \_ \_ SZ-Typ aufweisen, enthält diese Größe alle abschließenden NULL-Zeichen oder -Zeichen. Weitere Informationen finden Sie in den Hinweisen.

Wenn der von *lpData* angegebene Puffer nicht groß genug ist, um die Daten aufzunehmen, gibt die Funktion ERROR MORE DATA zurück \_ und speichert die erforderliche \_ Puffergröße in der Variablen, auf die *lpcbData* zeigt. In diesem Fall ist der Inhalt von *lpData* nicht definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in Winerror.h definiert ist. Sie können die [FormatMessage-Funktion](/windows/win32/api/winbase/nf-winbase-formatmessage) mit dem \_ FORMAT MESSAGE FROM \_ \_ SYSTEM-Flag verwenden, um eine generische Beschreibung des Fehlers abzurufen.

Wenn der *lpData-Puffer* zu klein ist, um den Wert zu empfangen, gibt die Funktion ERROR \_ MORE DATA \_ zurück.

## <a name="remarks"></a>Hinweise

Um Werte aufzuzählen, sollte eine Anwendung zunächst die **OREnumValue-Funktion** aufrufen, wobei der *dwIndex-Parameter* auf 0 (null) festgelegt ist. Die Anwendung sollte dann *dwIndex* erhöhen und die **OREnumValue-Funktion** aufrufen, bis keine weiteren Werte vorhanden sind (bis die Funktion ERROR NO MORE ITEMS zurückgibt). \_ \_ \_

Die Anwendung kann *dwIndex* auch auf den Index des letzten Werts beim ersten Aufruf der Funktion festlegen und den Index dekrementieren, bis der Wert mit Index 0 aufzählt wird. Um den Index des letzten Werts abzurufen, verwenden Sie die [**ORQueryInfoKey-Funktion.**](orqueryinfokey.md)

Bei Verwendung von **OREnumValue** sollte eine Anwendung keine Offlineregistrierungsfunktionen aufrufen, die den abgefragten Schlüssel ändern könnten.

Wenn die Daten den \_ Reg SZ-, REG \_ MULTI \_ SZ- oder REG EXPAND \_ \_ SZ-Typ aufweisen, wurde die Zeichenfolge möglicherweise nicht mit den richtigen Zeichen für den NULL-Abschluss gespeichert. Selbst wenn die Funktion ERROR \_ SUCCESS zurückgibt, sollte die Anwendung daher sicherstellen, dass die Zeichenfolge ordnungsgemäß beendet wird, bevor sie verwendet wird. Andernfalls kann sie einen Puffer überschreiben. (Beachten Sie, dass REG \_ MULTI \_ SZ-Zeichenfolgen sollten zwei Zeichen mit NULL-Terminierung aufweisen.)

Verwenden Sie die [**ORQueryInfoKey-Funktion,**](orqueryinfokey.md) um die maximale Größe des Namens und der Datenpuffer zu bestimmen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows Offline registry library version 1.0 or later (Offlineregistrierungsbibliothek, Version 1.0 oder höher)<br/>                      |
| Header<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**OREnumKey**](orenumkey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORQueryInfoKey**](orqueryinfokey.md)
</dt> </dl>

 

 
