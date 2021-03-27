---
description: Wird von der standardmäßigen Kontextmenü Implementierung während der Erstellung gesendet, wobei der Standardmenü Befehl angegeben und eine Alternative Auswahl getroffen werden kann. Wird von lpfndfmcallback verwendet.
title: DFM_GETDEFSTATICID Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9e4ad96e-7c90-456e-8668-21b347f2915c
api_name:
- DFM_GETDEFSTATICID
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3fb1635b624b4c39e91ad8c31645c9aad598c7fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393441"
---
# <a name="dfm_getdefstaticid-message"></a>DFM \_ getdefstaticid-Meldung

Wird von der standardmäßigen Kontextmenü Implementierung während der Erstellung gesendet, wobei der Standardmenü Befehl angegeben und eine Alternative Auswahl getroffen werden kann. Wird von [**lpfndfmcallback**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)verwendet.


```C++
DFM_GETDEFSTATICID
    lParam = (LPARAM)(int*) defaultID;          
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DefaultID* \[ in, out\]
</dt> <dd>

Ein Zeiger auf die ID des ausgewählten Menübefehls. Das folgende Flag wird erkannt.

<dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM- \_ cmd- \_ Eigenschaften**


</dt> <dd>

Zeigt die **Eigenschaften** Benutzeroberfläche für das Element an, für das das Menü aufgerufen wurde.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie die standardmäßige Befehls Auswahl überschreiben möchten, sollte Ihr Handler beim Empfang dieser Nachricht den Wert, auf den von *DefaultID* verwiesen wird, auf die ID des Ersetzungs Befehls festlegen und S OK zurückgeben \_ . Andernfalls wird ein Fehlercode zurückgegeben.

Diese Nachricht wird entweder an die Rückruffunktion oder an das Rückruf Objekt gesendet, je nachdem, wie das standardmäßige Kontextmenü Objekt erstellt wird. Es gibt zwei APIs für die Erstellung, [**cdeffoldermenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**shkreatedefaultcontextmenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ Invokecommandex**](dfm-invokecommandex.md) ist eine erweiterte Version dieser Nachricht und bietet weitere Informationen für den Rückruf. Verwenden Sie **DFM \_ invokecommandex** , wenn die zusätzlichen Informationen, die von dieser Schnittstelle bereitgestellt werden, in der Implementierung benötigt werden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
