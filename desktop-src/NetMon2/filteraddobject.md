---
description: Die FilterAddObject-Funktion fügt einem Anzeigefilter ein einzelnes Objekt hinzu.
ms.assetid: 796216f4-a407-4a8c-98b3-8c3761d91913
title: FilterAddObject-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilterAddObject
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2c7d814efbbc77816836d437161390b1e2af60e8bbf4932322dcbd606920be5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938733"
---
# <a name="filteraddobject-function"></a>FilterAddObject-Funktion

Die **FilterAddObject-Funktion** fügt einem [*Anzeigefilter*](d.md)ein einzelnes -Objekt hinzu.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI FilterAddObject(
  _In_  HFILTER        hFilter,
  _Out_ LPFILTEROBJECT lpFilterObject
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hFilter* \[ In\]
</dt> <dd>

Handle für den Anzeigefilter.

</dd> <dt>

*lpFilterObject* \[ out\]
</dt> <dd>

Zeiger auf eine [FILTEROBJECT-Struktur,](filterobject.md) die das Objekt definiert, das dem Filter hinzugefügt werden soll. Jedes Objekt kann ein Operator, ein Wert oder eine Eigenschaft sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode.



| Rückgabecode                                                                                              | Beschreibung                                                                  |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ – UNGÜLTIGER \_ PARAMETER**</dt> </dl> | Der *hFilter-Parameter* weist einen ungültigen Wert auf.<br/>                     |
| <dl> <dt>**NMERR \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**</dt> </dl>    | Netzwerkmonitor verfügt nicht über genügend Arbeitsspeicher, um das Objekt zu erstellen.<br/> |



 

## <a name="remarks"></a>Hinweise

[*Experten*](e.md) und [*Parser*](p.md) können die **FilterAddObject-Funktion** aufrufen.

Die **FilterAddObject-Funktion** wird jedes Mal aufgerufen, wenn dem Anzeigefilter ein Filterobjekt hinzugefügt wird. Der Anzeigefilter ist ein Postfixstapel von Objekten, bei denen es sich um einen Operator, einen Wert oder eine Eigenschaft handelt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[FILTEROBJECT](filterobject.md)
</dt> </dl>

 

 




