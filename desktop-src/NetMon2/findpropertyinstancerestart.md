---
description: Sucht die nächste Instanz der Eigenschaft, die durch den hproperty-Parameter angegeben wird.
ms.assetid: f77cb92b-5936-4349-bf66-643c16e9e0df
title: Findpropertyinstancerestart-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstanceRestart
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: d1e731bb00b28bb62862dd18fbd6031fa973fe38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346489"
---
# <a name="findpropertyinstancerestart-function"></a>Findpropertyinstancerestart-Funktion

Die **findpropertyinstancerestart** -Funktion sucht die nächste Instanz der Eigenschaft, die durch den *hproperty* -Parameter angegeben wird.

## <a name="syntax"></a>Syntax


```C++
LPPROPERTYINST WINAPI FindPropertyInstanceRestart(
  _In_ HFRAME         hFrame,
  _In_ HPROPERTY      hProperty,
  _In_ LPPROPERTYINST *lpRestartKey,
  _In_ BOOL           DirForward
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hframe* \[ in\]
</dt> <dd>

Ein Handle für den Frame. Das Frame Handle kann durch einen Aufrufen der [GetFrame](getframe.md) -Funktion abgerufen werden.

</dd> <dt>

*hproperty* \[ in\]
</dt> <dd>

Ein Handle für die zu suchende Eigenschaft. Das Eigenschafts Handle kann durch einen Aufrufen der [GetProperty](getproperty.md) -Funktion abgerufen werden.

</dd> <dt>

*lprestartkey* \[ in\]
</dt> <dd>

Ein Zeiger auf die Eigenschaften Instanz, die als Ausgangspunkt für die Suche verwendet wird. Wenn der *lprestartkey* -Parameter auf **null** festgelegt ist, beginnt die Suche am Anfang des Frames oder am Ende des Frames, abhängig vom Wert des *dirforward* -Parameters.

Wenn *lprestartkey* auf **null** zeigt, beginnt die Suche am Anfang des Frames, wenn *dirforward* den Wert **true** hat, oder am Ende des Frames, wenn der-Parameter **false** ist.

</dd> <dt>

*Dirforward* \[ in\]
</dt> <dd>

Ein Indikator der Suchrichtung. Wenn der Wert **true** ist, wechselt die Suche von der aktuellen Position bis zum Ende des Frames. Wenn der Wert **false** ist, wird die Suche von der aktuellen Position bis zum Anfang des Frames verschoben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert das nächste gültige **lppropertyinst**.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.

## <a name="remarks"></a>Bemerkungen

[*Experten*](e.md) und [*Parser*](p.md) können die **findpropertyinstancerestart** -Funktion aufrufen.

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

[GetFrame](getframe.md)
</dt> <dt>

[GetProperty](getproperty.md)
</dt> </dl>

 

 




