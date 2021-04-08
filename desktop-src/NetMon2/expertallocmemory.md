---
description: Die Funktion "ExpertAllocMemory" ordnet dem Experten Arbeitsspeicher zu.
ms.assetid: 9ada5d3f-5f1d-4d3a-b79a-d51e021240f6
title: Funktion "ExpertAllocMemory" (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertAllocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b30aba5e2b448df141d0c82e6ec5a2b0d9b3303f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750105"
---
# <a name="expertallocmemory-function"></a>Funktion "ExpertAllocMemory"

Die Funktion " **ExpertAllocMemory** " ordnet dem Experten Arbeitsspeicher zu.

## <a name="syntax"></a>Syntax


```C++
LPVOID WINAPI ExpertAllocMemory(
        HEXPERTKEY hExpertKey,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hexpertkey* 
</dt> <dd>

Eindeutige expertenkennung. Netzwerkmonitor übergibt *hexpertkey* an den Experten, wenn die Funktion [Run](run.md) aufgerufen wird.

</dd> <dt>

*nbytes* \[ in\]
</dt> <dd>

Zugewiesener Arbeitsspeicher (gemessen in Bytes).

</dd> <dt>

*perror* \[ vorgenommen\]
</dt> <dd>

Fehler Indikator. Wenn die Funktion fehlschlägt, enthält der *nbytes* -Parameter den Fehlercode. Wenn der Fehlercode nmerr \_ -Experte \_ beendet ist, muss der Experte eine Bereinigung durchsetzen und sofort zurückkehren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den zugeordneten Arbeitsspeicher.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**, und *perror* bietet einen Fehlercode, der den Grund für den Fehler angibt.

## <a name="remarks"></a>Bemerkungen

Es ist wichtig zu beachten, dass ein Experte die Netzwerkmonitor Speicher Belegungs Funktionen (einschließlich " [expertenspeicher](expertreallocmemory.md)") für die Speicherverwaltung verwenden sollte. Wenn Ihr Experte während der Laufzeit einen Fehler verursacht, ermöglicht die Verwendung dieser Funktionen Netzwerkmonitor, den zugeordneten Arbeitsspeicher freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




