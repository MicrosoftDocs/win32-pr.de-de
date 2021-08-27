---
description: Listet die Unterschlüssel des angegebenen geöffneten Registrierungsschlüssels in einer Offlineregistrierungsstruktur auf. Die Funktion ruft bei jedem Aufruf Informationen zu einem Unterschlüssel ab.
ms.assetid: 46d13c37-473a-4772-992c-a565ad702fb9
title: OREnumKey-Funktion (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ab72c9b0df79d464f802a1c574b749d04a8a16e89645f25959681e7f03eea5ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058710"
---
# <a name="orenumkey-function"></a>OREnumKey-Funktion

Listet die Unterschlüssel des angegebenen geöffneten Registrierungsschlüssels in einer Offlineregistrierungsstruktur auf. Die Funktion ruft bei jedem Aufruf Informationen zu einem Unterschlüssel ab.

## <a name="syntax"></a>Syntax


```C++
DWORD OREnumKey(
  _In_        ORHKEY    Handle,
  _In_        DWORD     dwIndex,
  _Out_       PWSTR     lpName,
  _Inout_     PDWORD    lpcName,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PFILETIME lpftLastWriteTime
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

Der Index des abzurufende Unterschlüssels. Dieser Parameter sollte 0 (null) für den ersten Aufruf der Funktion sein und dann für nachfolgende Aufrufe erhöht werden.

Da Unterschlüssel nicht sortiert sind, verfügt jeder neue Unterschlüssel über einen beliebigen Index. Dies bedeutet, dass die Funktion Unterschlüssel in beliebiger Reihenfolge zurückgeben kann.

</dd> <dt>

*lpName* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der den Namen des Unterschlüssels einschließlich des abschließenden NULL-Zeichens empfängt. Die Funktion kopiert nur den Namen des Unterschlüssels, nicht die vollständige Schlüsselhierarchie, in den Puffer. Wenn die Funktion fehlschlägt, werden keine Informationen in diesen Puffer kopiert.

Weitere Informationen finden Sie unter [Größenbeschränkungen für Registrierungselemente.](../sysinfo/registry-element-size-limits.md)

</dd> <dt>

*lpcName* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe des puffers angibt, der durch den *lpName-Parameter* in **WCHARs** angegeben wird. Diese Größe sollte das abschließende NULL-Zeichen enthalten. Wenn die Funktion erfolgreich ausgeführt wird, enthält die Variable, auf die *von lpcName* verwiesen wird, die Anzahl der im Puffer gespeicherten Zeichen, ohne das abschließende NULL-Zeichen.

</dd> <dt>

*lpClass* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die NULL-terminierte Klassenzeichenfolge des aufzählten Unterschlüssels empfängt. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*lpcClass* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe des vom *lpClass-Parameter* angegebenen Puffers in **WCHARs** angibt. Die Größe sollte das abschließende NULL-Zeichen enthalten. Wenn die Funktion erfolgreich ausgeführt wird, enthält *lpcClass* die Anzahl der im Puffer gespeicherten Zeichen, ohne das abschließende NULL-Zeichen. Dieser Parameter kann nur **NULL** sein, wenn *lpClass* **NULL** ist.

</dd> <dt>

*lpftLastWriteTime* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf die [FILETIME-Struktur,](/windows/win32/api/minwinbase/ns-minwinbase-filetime) der den Zeitpunkt empfängt, zu dem der aufzählte Unterschlüssel zuletzt geschrieben wurde. Dieser Parameter kann **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in Winerror.h definiert ist. Sie können die [FormatMessage-Funktion](/windows/win32/api/winbase/nf-winbase-formatmessage) mit dem \_ FORMAT MESSAGE FROM \_ \_ SYSTEM-Flag verwenden, um eine generische Beschreibung des Fehlers abzurufen. Mögliche Fehlercodes sind:

-   Wenn der *lpName-Puffer* zu klein ist, um den Namen des Schlüssels zu erhalten, gibt die Funktion ERROR \_ MORE DATA \_ zurück.
-   Wenn keine Unterschlüssel mehr verfügbar sind, gibt die Funktion ERROR \_ NO \_ MORE ITEMS \_ zurück.

## <a name="remarks"></a>Hinweise

Um Unterschlüssel aufzuzählen, sollte eine Anwendung zunächst die **OREnumKey-Funktion** aufrufen, wobei der *dwIndex-Parameter* auf 0 (null) festgelegt ist. Die Anwendung sollte dann den *dwIndex-Parameter* erhöhen und **OREnumKey** aufrufen, bis keine Unterschlüssel mehr vorhanden sind (was bedeutet, dass die Funktion ERROR NO MORE ITEMS zurückgibt). \_ \_ \_

Die Anwendung kann *dwIndex* auch auf den Index des letzten Unterschlüssels beim ersten Aufruf der Funktion festlegen und den Index dekrementieren, bis der Unterschlüssel mit dem Index 0 aufzählt wird. Verwenden Sie die [**ORQueryInfoKey-Funktion,**](/windows/win32/api/winreg/nf-winreg-regqueryinfokeya) um den Index des letzten Unterschlüssels abzurufen.

Während eine Anwendung die **OREnumKey-Funktion** verwendet, sollte sie keine Offlineregistrierungsfunktionen aufrufen, die den aufzuzähligen Schlüssel ändern könnten.

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

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORQueryInfoKey**](orqueryinfokey.md)
</dt> </dl>

 

 
