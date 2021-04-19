---
description: Listet die Unterschlüssel des angegebenen geöffneten Registrierungsschlüssels in einer Offline Registrierungs Struktur auf. Die-Funktion Ruft bei jedem Aufruf Informationen zu einem Unterschlüssel ab.
ms.assetid: 46d13c37-473a-4772-992c-a565ad702fb9
title: Orenkey-Funktion (offreg. h)
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
ms.openlocfilehash: 24278bc59c75f32aed92c2ea5b5428f6ef6d9b45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366809"
---
# <a name="orenumkey-function"></a>Orenkey-Funktion

Listet die Unterschlüssel des angegebenen geöffneten Registrierungsschlüssels in einer Offline Registrierungs Struktur auf. Die-Funktion Ruft bei jedem Aufruf Informationen zu einem Unterschlüssel ab.

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

*Handle* \[ in\]
</dt> <dd>

Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur.

</dd> <dt>

*dwIndex* \[ in\]
</dt> <dd>

Der Index des abzurufenden unter Schlüssels. Dieser Parameter sollte für den ersten Aufruf der-Funktion 0 (null) sein und dann für nachfolgende Aufrufe inkrementiert werden.

Da Unterschlüssel nicht geordnet sind, verfügen alle neuen Unterschlüssel über einen beliebigen Index. Dies bedeutet, dass die Funktion Unterschlüssel in beliebiger Reihenfolge zurückgeben kann.

</dd> <dt>

*lpname* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der den Namen des unter Schlüssels einschließlich des abschließenden NULL-Zeichens empfängt. Die-Funktion kopiert nur den Namen des unter Schlüssels, nicht die vollständige Schlüssel Hierarchie, in den Puffer. Wenn die Funktion fehlschlägt, werden keine Informationen in diesen Puffer kopiert.

Weitere Informationen finden Sie unter [Größenbeschränkungen für das Registrierungs Element](../sysinfo/registry-element-size-limits.md).

</dd> <dt>

*lpcname* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe des Puffers angibt, der durch den *lpname* -Parameter in **WCHARs** angegeben wird. Diese Größe sollte das abschließende Null-Zeichen enthalten. Wenn die Funktion erfolgreich ausgeführt wird, enthält die Variable, auf die von *lpcname* verwiesen wird, die Anzahl von Zeichen, die im Puffer gespeichert sind, ohne das abschließende Null Zeichen.

</dd> <dt>

*lpclass* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die NULL-terminierte Klassen Zeichenfolge des enumerierten unter Schlüssels empfängt. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*lpcclass* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe des Puffers angibt, der durch den *lpclass* -Parameter in **WCHARs** angegeben wird. Die Größe sollte das abschließende Null-Zeichen enthalten. Wenn die Funktion erfolgreich ausgeführt wird, enthält *lpcclass* die Anzahl von Zeichen, die im Puffer gespeichert sind, ohne das abschließende Null Zeichen. Dieser Parameter kann nur **null** sein, wenn *lpclass* **null** ist.

</dd> <dt>

*lpftlastschreitezeit* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf die [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur, die die Uhrzeit empfängt, zu der der enumerierte Unterschlüssel zuletzt geschrieben wurde. Dieser Parameter kann **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist. Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten. Folgende Fehlercodes sind möglich:

-   Wenn der *lpname* -Puffer zu klein ist, um den Namen des Schlüssels zu erhalten, gibt die Funktion Fehler \_ Weitere \_ Daten zurück.
-   Wenn keine weiteren Unterschlüssel verfügbar sind, gibt die Funktion einen Fehler \_ ohne \_ Weitere \_ Elemente zurück.

## <a name="remarks"></a>Bemerkungen

Um Unterschlüssel aufzulisten, sollte eine Anwendung zunächst die Funktion " **orenkey** " aufrufen, wobei der *dwIndex* -Parameter auf 0 (null) festgelegt ist. Die Anwendung sollte dann den *dwIndex* -Parameter Inkrement erhöhen und " **gatumschlag Key** " aufrufen, bis keine Unterschlüssel mehr vorhanden sind (d. h., die Funktion gibt \_ einen Fehler ohne \_ Weitere \_ Elemente zurück)

Die Anwendung kann *dwIndex* auch auf den Index des letzten unter Schlüssels beim ersten Aufrufe der Funktion festlegen und den Index verringern, bis der Unterschlüssel mit dem Index 0 aufgezählt wird. Verwenden Sie die [**orqueryinfokey**](/windows/win32/api/winreg/nf-winreg-regqueryinfokeya) -Funktion, um den Index des letzten unter Schlüssels abzurufen.

Obwohl eine Anwendung die Funktion " **atenumkey** " verwendet, sollte Sie keine Offline Registrierungsfunktionen aufrufen, die möglicherweise den aufzuzählenden Schlüssel ändern.

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

[**Ordeletekey**](ordeletekey.md)
</dt> <dt>

[**Oropenkey**](oropenkey.md)
</dt> <dt>

[**Orqueryinfokey**](orqueryinfokey.md)
</dt> </dl>

 

 
