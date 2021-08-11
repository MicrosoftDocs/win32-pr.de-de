---
title: MpFreeMemory-Funktion (MpClient.h)
description: Gibt Arbeitsspeicher für den Schadsoftwareschutz-Manager frei.
ms.assetid: D0B43AE5-756F-4E86-B8A5-8268A41901BC
keywords:
- MpFreeMemory-Funktion – Legacy-Windows-Umgebungsfeatures
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
ms.openlocfilehash: 806795cee45fcfe95473c0961106da074c1157b65ac5c19f5d4813c84865616a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247425"
---
# <a name="mpfreememory-function"></a>MpFreeMemory-Funktion

Gibt Arbeitsspeicher für den Schadsoftwareschutz-Manager frei. Alle Puffer, die von Schadsoftwareschutzfunktionen zugeordnet und zurückgegeben werden, müssen vom Aufrufer mit dieser Funktion freigegeben werden.

## <a name="syntax"></a>Syntax


```C++
void WINAPI MpFreeMemory(
  _In_ PVOID pMemory
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMemory* \[ In\]
</dt> <dd>

Typ: **PVOID**

Ein Zeiger auf den von einer Schadsoftwareschutzfunktion belegten Arbeitsspeicher.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Um die Speicherverwaltung für Clients zu vereinfachen, definiert der Malwareschutz-Manager auch Makros, um Arbeitsspeicher freizugeben, der verschiedenen Strukturen zugeordnet ist, die von Funktionen zum Schutz vor Schadsoftware zurückgegeben werden. Die folgenden Makros sind in der Headerdatei mpmemfree.h definiert:



| Name                            | BESCHREIBUNG                                                                      |
|---------------------------------|----------------------------------------------------------------------------------|
| MPRESOURCE \_ INFO \_ FREE          | Gibt eine zugeordnete [**MPRESOURCE \_ INFO**](mpresource-info.md)frei.                  |
| MPTHREAT \_ INFO \_ FREE            | Gibt eine zugeordnete [**MPTHREAT \_ INFO**](mpthreat-info.md)frei.                      |
| LOKALISIERTE MPTHREAT-INFORMATIONEN \_ \_ \_ KOSTENLOS | Gibt eine zugeordnete [**LOKALISIERTE MPTHREAT-INFO \_ \_**](mpthreat-localized-info.md)frei. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**\_MPRESOURCE-INFORMATIONEN**](mpresource-info.md)
</dt> <dt>

[**\_MPTHREAT-INFORMATIONEN**](mpthreat-info.md)
</dt> <dt>

[**LOKALISIERTE \_ \_ MPTHREAT-INFORMATIONEN**](mpthreat-localized-info.md)
</dt> </dl>

 

 





