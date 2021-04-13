---
description: Die Funktion FilterAddObject fügt einem Anzeige Filter ein einzelnes Objekt hinzu.
ms.assetid: 796216f4-a407-4a8c-98b3-8c3761d91913
title: FilterAddObject-Funktion (Netmon. h)
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
ms.openlocfilehash: 7fc6c41a675bfe560c060e271e4f9f48f88cd58c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484331"
---
# <a name="filteraddobject-function"></a>FilterAddObject-Funktion

Die Funktion **FilterAddObject** fügt einem [*Anzeige Filter*](d.md)ein einzelnes Objekt hinzu.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI FilterAddObject(
  _In_  HFILTER        hFilter,
  _Out_ LPFILTEROBJECT lpFilterObject
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hfilter* \[ in\]
</dt> <dd>

Handle für den Anzeige Filter.

</dd> <dt>

*lpfilterobject* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [filterobject](filterobject.md) -Struktur, die das Objekt definiert, das dem Filter hinzugefügt werden soll. Jedes Objekt kann ein Operator, ein Wert oder eine Eigenschaft sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode.



| Rückgabecode                                                                                              | Beschreibung                                                                  |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**Ungültiger nmerr- \_ \_ Parameter**</dt> </dl> | Der *hfilter* -Parameter weist einen ungültigen Wert auf.<br/>                     |
| <dl> <dt>**nicht genügend Arbeits \_ \_ Speicher für nmerr \_**</dt> </dl>    | Netzwerkmonitor verfügt nicht über genügend Arbeitsspeicher, um das Objekt zu erstellen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

[*Experten*](e.md) und [*Parser*](p.md) können die Funktion **FilterAddObject** aufzurufen.

Die **FilterAddObject** -Funktion wird jedes Mal aufgerufen, wenn dem Anzeige Filter ein Filter Objekt hinzugefügt wird. Der Anzeige Filter ist ein postfix Stapel von Objekten, bei denen es sich um einen Operator, einen Wert oder eine Eigenschaft handeln kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Filter Object](filterobject.md)
</dt> </dl>

 

 




