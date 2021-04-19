---
description: Die Funktion "expertrebelegcmemory" erhöht oder verringert die Menge an Arbeitsspeicher, die von Netzwerkmonitor zugeordnet wird.
ms.assetid: 78b99a66-692a-4e83-8b0d-d68caf156bb6
title: Funktion "expertrebelegcmemory" (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertReallocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8f562443f9ca66def7e053f5958b17e70af50140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342821"
---
# <a name="expertreallocmemory-function"></a>Funktion "expertrebelegcmemory"

Die Funktion " **expertrebelegcmemory** " erhöht oder verringert die Menge an Arbeitsspeicher, die von Netzwerkmonitor zugeordnet wird.

## <a name="syntax"></a>Syntax


```C++
LPVOID WINAPI ExpertReallocMemory(
  _In_  HEXPERTKEY hExpertKey,
  _In_  LPVOID     pOriginalMemory,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hexpertkey* \[ in\]
</dt> <dd>

Eindeutiger Bezeichner, der beim [**Ausführen**](run.md) oder [**Konfigurieren**](configure.md)an den Experten übermittelt wird

</dd> <dt>

*poriginalmemory* \[ in\]
</dt> <dd>

Zeiger auf den durch Netzwerkmonitor zugeordneten Arbeitsspeicher. Der *poriginalmemory* -Zeiger kann von einem vorherigen-Befehl von " [**expertenlocmemory**](expertallocmemory.md) " oder " **expertenspeicher**" zurückgegeben werden.

</dd> <dt>

*nbytes* \[ in\]
</dt> <dd>

Größe des neu zugewiesenen Speichers.

</dd> <dt>

*perror* \[ vorgenommen\]
</dt> <dd>

Bei der Rückgabe ein Fehlercode, wenn die Funktion fehlschlägt. Wenn der Fehlercode nmerr- \_ Experte \_ beendet ist, muss der Experte einen Cleanup durchsetzen und sofort zurückkehren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den zugeordneten Arbeitsspeicher.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**, und *perror* (wenn es sich um einen nicht-**null** -Wert handelt) gibt den Grund für den Fehler an.

## <a name="remarks"></a>Bemerkungen

Es ist wichtig zu beachten, dass ein Experte die Netzwerkmonitor Speicher Belegungs Funktionen für die Speicherverwaltung verwenden sollte. Wenn Ihr Experte während der Laufzeit einen Fehler verursacht, ermöglicht die Verwendung dieser Funktionen Netzwerkmonitor, den zugeordneten Arbeitsspeicher freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




