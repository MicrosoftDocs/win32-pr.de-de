---
description: Sucht die nächste Instanz der -Eigenschaft, die durch den hProperty-Parameter angegeben wird.
ms.assetid: f77cb92b-5936-4349-bf66-643c16e9e0df
title: FindPropertyInstanceRestart-Funktion (Netmon.h)
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
ms.openlocfilehash: 0699cb37165e9181bf78bc3a86ad68c07dbbd589469e3e0bca6a1cd0228573f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890810"
---
# <a name="findpropertyinstancerestart-function"></a>FindPropertyInstanceRestart-Funktion

Die **FindPropertyInstanceRestart-Funktion** sucht die nächste Instanz der Eigenschaft, die durch den *hProperty-Parameter angegeben* wird.

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

*hFrame* \[ In\]
</dt> <dd>

Ein Handle für den Frame. Das Framehand handle kann durch einen Aufruf der [GetFrame-Funktion abgerufen](getframe.md) werden.

</dd> <dt>

*hProperty* \[ In\]
</dt> <dd>

Ein Handle für die zu suchende Eigenschaft. Das Eigenschaftenhand handle kann durch einen Aufruf der [GetProperty-Funktion abgerufen](getproperty.md) werden.

</dd> <dt>

*lpRestartKey* \[ In\]
</dt> <dd>

Ein Zeiger auf die Eigenschafteninstanz, die als Ausgangspunkt der Suche verwendet wird. Wenn *der lpRestartKey-Parameter* auf **NULL** festgelegt ist, beginnt die Suche am Anfang des Frames oder am Ende des Frames, abhängig vom Wert des *DirForward-Parameters.*

Wenn *lpRestartKey* auf **NULL** zeigt, beginnt die Suche am Anfang des Frames, wenn *DirForward* **TRUE** ist, oder am Ende des Frames, wenn der Parameter **FALSE ist.**

</dd> <dt>

*DirForward* \[ In\]
</dt> <dd>

Ein Indikator für die Suchrichtung. Wenn der Wert **TRUE ist,** wird die Suche von der aktuellen Position an das Ende des Frames bewegt. Wenn der Wert **FALSE ist,** wird die Suche von der aktuellen Position an den Anfang des Frames bewegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert der nächste gültige **LPPROPERTYINST**.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **NULL.**

## <a name="remarks"></a>Hinweise

[*Experten*](e.md) und [*Parser*](p.md) können die **Funktion FindPropertyInstanceRestart** aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Getframe](getframe.md)
</dt> <dt>

[GetProperty](getproperty.md)
</dt> </dl>

 

 




