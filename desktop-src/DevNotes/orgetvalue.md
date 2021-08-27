---
description: Ruft den Typ und die Daten für den angegebenen Registrierungswert in einer Offlineregistrierungsstruktur ab.
ms.assetid: 83604743-cb59-42a1-9951-620ad5bd8de7
title: ORGetValue-Funktion (Offreg.h)
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
ms.openlocfilehash: fc364e208e9c243754edf8731f077ec48e9133d4a95ba86b5a1f99971192b51e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058650"
---
# <a name="orgetvalue-function"></a>ORGetValue-Funktion

Ruft den Typ und die Daten für den angegebenen Registrierungswert in einer Offlineregistrierungsstruktur ab.

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

*Handle* \[ In\]
</dt> <dd>

Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offlineregistrierungsstruktur.

</dd> <dt>

*lpSubKey* \[ in, optional\]
</dt> <dd>

Der Name des Registrierungsschlüssels. Dieser Schlüssel muss ein Unterschlüssel des Schlüssels sein, der vom *Handle-Parameter* angegeben wird. Dieser Parameter kann **NULL** sein.

Bei Schlüsselnamen wird die Groß-/Kleinschreibung nicht beachtet.

</dd> <dt>

*lpValue* \[ in, optional\]
</dt> <dd>

Der Name des Registrierungswerts. Wenn dieser Parameter **NULL** oder eine leere Zeichenfolge ("") ist, ruft die Funktion den Typ und die Daten für den unbenannten oder ggf. standardwert des Schlüssels ab. Weitere Informationen finden Sie unter [Größenbeschränkungen für Registrierungselemente.](../sysinfo/registry-element-size-limits.md)

Schlüssel weisen nicht automatisch einen unbenannten oder Standardwert auf. Unbenannte Werte können einen beliebigen Typ aufweisen.

Bei Wertnamen wird die Groß-/Kleinschreibung nicht beachtet.

</dd> <dt>

*pdwType* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Code empfängt, der den Typ der im angegebenen Wert gespeicherten Daten angibt. Eine Liste der möglichen Typcodes finden Sie unter [Registrierungswerttypen.](../sysinfo/registry-value-types.md) Dieser Parameter kann **NULL** sein, wenn der Typ nicht erforderlich ist.

</dd> <dt>

*pvData* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die Daten des Werts empfängt. Dieser Parameter kann **NULL** sein, wenn die Daten nicht erforderlich sind.

Wenn es sich bei den Daten um eine Zeichenfolge handelt, sucht die Funktion nach einem abschließenden NULL-Zeichen. Wenn keines gefunden wird, wird die Zeichenfolge mit einem NULL-Abschlusszeichen gespeichert, wenn der Puffer groß genug ist, um das zusätzliche Zeichen aufzunehmen. Andernfalls schlägt die Funktion fehl und gibt ERROR \_ MORE \_ DATA zurück.

</dd> <dt>

*data* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe des Puffers angibt, auf den der *pvData-Parameter* zeigt, in Bytes. Wenn die Funktion zurückgegeben wird, enthält diese Variable die Größe der in *pvData* kopierten Daten.

Der *parameterdata* kann nur **NULL** sein, wenn *pvData* **NULL** ist.

Wenn die Daten den \_ Reg SZ-, REG \_ MULTI \_ SZ- oder REG EXPAND \_ \_ SZ-Typ aufweisen, enthält diese Größe alle abschließenden NULL-Zeichen oder -Zeichen. Weitere Informationen finden Sie in den Hinweisen.

Wenn der durch den *pvData-Parameter* angegebene Puffer nicht groß genug ist, um die Daten zu speichern, gibt die Funktion ERROR MORE DATA zurück \_ und speichert die erforderliche \_ Puffergröße in der Variablen, auf die *von "data"* verwiesen wird. In diesem Fall ist der Inhalt des *pvData-Puffers* nicht definiert.

Wenn *pvData* **NULL** ist und *"data"* ungleich **NULL** ist, gibt die Funktion ERROR SUCCESS zurück \_ und speichert die Größe der Daten in Bytes in der Variablen, auf die *von "data"* verwiesen wird. Dadurch kann eine Anwendung die beste Methode zum Zuordnen eines Puffers für die Daten des Werts bestimmen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in Winerror.h definiert ist. Sie können die [FormatMessage-Funktion](/windows/win32/api/winbase/nf-winbase-formatmessage) mit dem \_ FORMAT MESSAGE FROM \_ \_ SYSTEM-Flag verwenden, um eine generische Beschreibung des Fehlers abzurufen.

## <a name="remarks"></a>Hinweise

Eine Anwendung ruft in der Regel die [**OREnumValue-Funktion**](orenumvalue.md) auf, um die Wertnamen zu bestimmen, und ruft dann die **ORGetValue-Funktion** auf, um die Daten für die Namen abzurufen.

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

[**OREnumValue**](orenumvalue.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORQueryInfoKey**](orqueryinfokey.md)
</dt> </dl>

 

 
