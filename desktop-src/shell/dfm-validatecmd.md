---
description: Wird gesendet, um zu überprüfen, ob ein Menübefehl vorhanden ist.
title: DFM_VALIDATECMD Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 97ff3cdf-ed0c-4813-8d5a-b5141636d32c
api_name:
- DFM_VALIDATECMD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5aa171f19d4d08c3ba3088676a4ae5364f0826f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128453"
---
# <a name="dfm_validatecmd-message"></a>DFM- \_ validatecmd-Meldung

Wird gesendet, um zu überprüfen, ob ein Menübefehl vorhanden ist.


```C++
DFM_INVOKECOMMAND

    wParam = (WPARAM)(WPARAM) idCmd;            

    lParam = (LPARAM)(LPARAM) lParam = 0;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*idcmd* 
</dt> <dd>Der Offset des Menübefehls Bezeichners.</dd> <dt>

*lParam* 
</dt> <dd>Nicht verwendet. Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt "s OK" zurück \_ , wenn der Befehl vorhanden ist, \_ andernfalls "false".

## <a name="remarks"></a>Bemerkungen

Diese Nachricht wird entweder an die Rückruffunktion oder an das Rückruf Objekt gesendet, je nachdem, wie das standardmäßige Kontextmenü Objekt erstellt wird. Es gibt zwei APIs für die Erstellung, [**cdeffoldermenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**shkreatedefaultcontextmenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ Invokecommandex**](dfm-invokecommandex.md) ist eine erweiterte Version dieser Nachricht und bietet weitere Informationen für den Rückruf. Verwenden Sie **DFM \_ invokecommandex** , wenn die zusätzlichen Informationen, die von dieser Schnittstelle bereitgestellt werden, in der Implementierung benötigt werden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




