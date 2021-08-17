---
description: Wird während der Erstellung von der Standardmäßigen Kontextmenüimplementierung gesendet, wobei der Standardmenübefehl angegeben wird und eine alternative Auswahl getroffen werden kann. Wird von LPFNDFMCALLBACK verwendet.
title: DFM_GETDEFSTATICID Meldung (Shlobj.h)
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
ms.openlocfilehash: 4d987e085779fd58f16c2534b517c39ebb4b7e3c6e2829982881015bb3a59a92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094371"
---
# <a name="dfm_getdefstaticid-message"></a>DFM \_ GETDEFSTATICID-Meldung

Wird während der Erstellung von der Standardmäßigen Kontextmenüimplementierung gesendet, wobei der Standardmenübefehl angegeben wird und eine alternative Auswahl getroffen werden kann. Wird von [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)verwendet.


```C++
DFM_GETDEFSTATICID
    lParam = (LPARAM)(int*) defaultID;          
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*defaultID* \[ in, out\]
</dt> <dd>

Ein Zeiger auf die ID des ausgewählten Menübefehls. Das folgende Flag wird erkannt.

<dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM \_ CMD \_ PROPERTIES**


</dt> <dd>

Zeigt die **Eigenschaftenbenutzeroberfläche** für das Element an, für das das Menü aufgerufen wurde.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Um die Standardbefehlsauswahl außer Kraft zu setzen, sollte Ihr Handler nach Erhalt dieser Meldung den Wert, auf den als *defaultID* verwiesen wird, auf die ID des Ersetzungsbefehls festlegen und S \_ OK zurückgeben. Gibt andernfalls einen Fehlercode zurück.

Diese Meldung wird entweder an die Rückruffunktion oder das Rückrufobjekt gesendet, je nachdem, wie das Standardkontextmenüobjekt erstellt wird. Es gibt zwei APIs für die Erstellung: [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) ist eine erweiterte Version dieser Nachricht und stellt weitere Informationen zum Rückruf bereit. Verwenden Sie **DFM \_ INVOKECOMMANDEX,** wenn die zusätzlichen Informationen, die von dieser Schnittstelle bereitgestellt werden, in Ihrer Implementierung benötigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
