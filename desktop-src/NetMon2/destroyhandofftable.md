---
description: Die Funktion "destroyhandofftable" zerstört eine mit "" von "" "" "" "mit" "" erstelltes Tabelle
ms.assetid: 01ae9899-4f7c-4706-a2ce-9f55b112351d
title: Destroyhandofftable-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7afccfd1932c57b2a0d77dbb5467afc31726c6fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959648"
---
# <a name="destroyhandofftable-function"></a>Destroyhandofftable-Funktion

Die Funktion " **destroyhandofftable** " zerstört **eine mit "" von "**" "" "" "mit" "" erstelltes Tabelle

## <a name="syntax"></a>Syntax


```C++
VOID WINAPI DestroyHandoffTable(
  _In_ LPHANDOFFTABLE hTable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*htable* \[ in\]
</dt> <dd>

Handle für die zerstörte Übergabe-Tabelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




