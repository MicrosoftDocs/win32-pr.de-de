---
title: Mpfrememory-Funktion (mpclient. h)
description: Gibt Arbeitsspeicher für den Malware Schutz-Manager frei.
ms.assetid: D0B43AE5-756F-4E86-B8A5-8268A41901BC
keywords:
- Mpfrememory-Funktion Legacy Funktionen der Windows-Umgebung
topic_type:
- apiref
api_name:
- MpFreeMemory
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a15a2845b034a3aa739b1ba2f33a023b742b4b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741009"
---
# <a name="mpfreememory-function"></a>Mpfrememory-Funktion

Gibt Arbeitsspeicher für den Malware Schutz-Manager frei. Alle Puffer, die von Malware Schutzfunktionen zugeordnet und zurückgegeben werden, müssen vom Aufrufer mithilfe dieser Funktion freigegeben werden.

## <a name="syntax"></a>Syntax


```C++
void WINAPI MpFreeMemory(
  _In_ PVOID pMemory
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmemory* \[ in\]
</dt> <dd>

Typ: **pVoid**

Ein Zeiger auf den Arbeitsspeicher, der von einer Malware Schutzfunktion zugewiesen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Um die Speicherverwaltung für Clients zu vereinfachen, definiert der Malware Schutz-Manager auch Makros, um Speicher freizugeben, der mit verschiedenen von Malware Schutzfunktionen zurückgegebenen Strukturen verknüpft ist. Die folgenden Makros sind in der Header Datei mpmemfree. h definiert:



| Name                            | BESCHREIBUNG                                                                      |
|---------------------------------|----------------------------------------------------------------------------------|
| mpresource- \_ Informationen \_ frei          | Gibt zugeordnete [**mpresource- \_ Informationen**](mpresource-info.md)frei.                  |
| mpthreat- \_ Informationen \_ frei            | Gibt zugeordnete [**mpthreat- \_ Informationen**](mpthreat-info.md)frei.                      |
| lokalisierte mpthreat- \_ \_ Informationen \_ kostenlos | Gibt eine zugeordnete, [**mpthreat \_ lokalisierte \_ Information**](mpthreat-localized-info.md)frei. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mperrormessageformat**](mperrormessageformat.md)
</dt> <dt>

[**mpresource- \_ Informationen**](mpresource-info.md)
</dt> <dt>

[**mpthreat- \_ Informationen**](mpthreat-info.md)
</dt> <dt>

[**lokalisierte mpthreat- \_ \_ Informationen**](mpthreat-localized-info.md)
</dt> </dl>

 

 





