---
description: Die ExpertMemorySize-Funktion gibt die Menge an Arbeitsspeicher zurück, die von der ExpertAllocMemory-Funktion belegt wird.
ms.assetid: 60d3f33d-dc03-4c39-98fa-ec093398b51b
title: ExpertMemorySize-Funktion (Netmon.h)
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
ms.openlocfilehash: 69dae4ca2a7f7a9e3b2f77047475c5dd35f54a3394b4481c2f452a46e983c35e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744270"
---
# <a name="expertmemorysize-function"></a>ExpertMemorySize-Funktion

Die **ExpertMemorySize-Funktion** gibt die Menge an Arbeitsspeicher zurück, die von der [ExpertAllocMemory-Funktion](expertallocmemory.md) belegt wird.

## <a name="syntax"></a>Syntax


```C++
SIZE_T WINAPI ExpertMemorySize(
  _In_ HEXPERTKEY hExpertKey,
  _In_ LPVOID     pOriginalMemory
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hExpertKey* \[ In\]
</dt> <dd>

Eindeutiger Expertenbezeichner. Netzwerkmonitor übergibt *hExpertKey* an den Experten, wenn er die [Run-Funktion](run.md) aufruft.

</dd> <dt>

*pOriginalMemory* \[ In\]
</dt> <dd>

Zeiger auf die Speicheradresse des Experten, der von [ExpertAllocMemory](expertallocmemory.md)zugeordnet wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt die Menge des zugeordneten Arbeitsspeichers in Bytes zurück.

## <a name="remarks"></a>Hinweise

Informationen zum **SIZE \_ T-Datentyp,** den **ExpertMemorySize** zurückgibt, finden Sie unter Datentypen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




