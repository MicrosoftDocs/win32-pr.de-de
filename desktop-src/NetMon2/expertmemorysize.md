---
description: Die Funktion "expertmemorysize" gibt die Menge an Arbeitsspeicher zurück, die von der Funktion "expertenlocmemory" zugeordnet wird.
ms.assetid: 60d3f33d-dc03-4c39-98fa-ec093398b51b
title: Expertmemorysize-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertMemorySize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 57c83bc3e9535550086c9732b33a71a357e4da42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862019"
---
# <a name="expertmemorysize-function"></a>Expertmemorysize-Funktion

Die Funktion " **expertmemorysize** " gibt die Menge an Arbeitsspeicher zurück, die von der Funktion " [expertenlocmemory](expertallocmemory.md) " zugeordnet wird.

## <a name="syntax"></a>Syntax


```C++
SIZE_T WINAPI ExpertMemorySize(
  _In_ HEXPERTKEY hExpertKey,
  _In_ LPVOID     pOriginalMemory
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hexpertkey* \[ in\]
</dt> <dd>

Eindeutige expertenkennung. Netzwerkmonitor übergibt *hexpertkey* an den Experten, wenn die Funktion [Run](run.md) aufgerufen wird.

</dd> <dt>

*poriginalmemory* \[ in\]
</dt> <dd>

Ein Zeiger auf die Speicheradresse des von " [sachtallocmemory](expertallocmemory.md)" zugewiesenen Experten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt die Menge an zugeordnetem Arbeitsspeicher in Bytes zurück.

## <a name="remarks"></a>Bemerkungen

Informationen über den Datentyp " **size \_ T** ", der von " **expertenmemorysize** " zurückgegeben wird, finden Sie unter Datentypen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




