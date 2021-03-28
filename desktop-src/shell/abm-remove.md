---
description: Hebt die Registrierung einer appbar auf, indem Sie aus der internen Liste des Systems entfernt wird. Das System sendet keine Benachrichtigungs Meldungen mehr an die appbar oder verhindert, dass andere Anwendungen den von der appbar verwendeten Bildschirmbereich verwenden.
title: ABM_REMOVE Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3da73a52-3dbb-4133-a9bd-86540e1c4154
api_name:
- ABM_REMOVE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7f4530869b9f68772c28fefd6130ff8e4b6ffbec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862139"
---
# <a name="abm_remove-message"></a>ABM \_ Entfernungs Meldung

Hebt die Registrierung einer appbar auf, indem Sie aus der internen Liste des Systems entfernt wird. Das System sendet keine Benachrichtigungs Meldungen mehr an die appbar oder verhindert, dass andere Anwendungen den von der appbar verwendeten Bildschirmbereich verwenden.


```C++
                SHAppBarMessage(ABM_REMOVE, pabd); 
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pabd* 
</dt> <dd>

Ein Zeiger auf eine [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur, die das Handle für die APP-Leiste enthält, deren Registrierung aufgehoben werden soll. Beim Senden dieser Nachricht müssen Sie die **CBSIZE** -und **HWND** -Elemente angeben. alle anderen Member werden ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt immer **true** zurück.

## <a name="remarks"></a>Bemerkungen

Diese Meldung bewirkt, dass das System die [**ABN \_**](abn-poschanged.md) -Benachrichtigungs Meldung an alle appbars sendet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




