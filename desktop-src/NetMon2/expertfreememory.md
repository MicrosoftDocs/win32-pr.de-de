---
description: Die Funktion "expertfrememory" gibt Speicher frei, der durch Aufrufe der Funktionen "ExpertAllocMemory" und "expertrebelegcmemory" abgerufen wurde.
ms.assetid: 0e7cc791-98dd-4522-afab-76ac9e74c715
title: Funktion "expertfrememory" (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertFreeMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: cc26056a3ec3e8820c363d97f92c7eb382cd0622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345663"
---
# <a name="expertfreememory-function"></a>Funktion "expertfrememory"

Die Funktion " **expertfrememory** " gibt Speicher frei, der durch Aufrufe der Funktionen " [**ExpertAllocMemory**](expertallocmemory.md) " und " [**expertrebelegcmemory**](expertreallocmemory.md) " abgerufen wurde.

## <a name="syntax"></a>Syntax


```C++
SIZE_T WINAPI ExpertFreeMemory(
       HEXPERTKEY hExpertKey,
  _In_ LPVOID     pMemory
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hexpertkey* 
</dt> <dd>

Eindeutige expertenkennung. Netzwerkmonitor übergibt *hexpertkey* an den Experten, wenn die Funktion [Run](run.md) aufgerufen wird.

</dd> <dt>

*pmemory* \[ in\]
</dt> <dd>

Zeiger auf den Arbeitsspeicher, der von Netzwerkmonitor zugeordnet wird. Der *pmemory* -Zeiger kann von einem vorherigen-Befehl von " [**expertenlocmemory**](expertallocmemory.md) " oder " [**expertenspeicher**](expertreallocmemory.md)" zurückgegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

, Wenn die Funktion erfolgreich ausgeführt wurde. der Rückgabewert ist "nmerr \_ Success".

Wenn die Funktion nicht erfolgreich ist, gibt der Rückgabewert den Grund für den Fehler an. Wenn der Rückgabewert nmerr- \_ Experte \_ beendet ist, bereinigt der Experte sofort und gibt ihn zurück.

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



 

 




