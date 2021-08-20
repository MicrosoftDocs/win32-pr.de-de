---
description: Wird von der Standardimplementierung des Kontextmenüs gesendet, um die Rückruffunktion anfordern, die das Menü (LPFNDFMCALLBACK) zum Aufrufen eines Menübefehls verarbeitet.
title: DFM_INVOKECOMMAND (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bd3200a6-b9e7-414c-9a01-c432cb306dba
api_name:
- DFM_INVOKECOMMAND
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6730de1e0c66093c0382b9b8fd04c05b5ea3dab4e151d581b155c1704bf26f58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118050760"
---
# <a name="dfm_invokecommand-message"></a>DFM \_ INVOKECOMMAND-Nachricht

Wird von der Standardimplementierung des Kontextmenüs gesendet, um die Rückruffunktion anfordern, die das Menü ([**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)) verarbeitet, um einen Menübefehl auf aufruft.


```C++
DFM_INVOKECOMMAND
    wParam = (WPARAM)(int) id;          
    lParam = (LPARAM)(LPWSTR) args;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*id* \[ in\]
</dt> <dd>

Die Befehls-ID des ausgewählten Menübefehls. Die folgenden Flags werden erkannt:

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM \_ CMD \_ DELETE**


</dt> <dd>

**Windows Vista und höher.** Löschen Sie das aktuelle Element.

</dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM \_ CMD \_ MOVE**


</dt> <dd>

**Windows Vista und höher.** Verschieben Sie das aktuelle Element.

</dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**DFM \_ CMD \_ COPY**


</dt> <dd>

**Windows Vista und höher.** Kopieren Sie das aktuelle Element.

</dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM \_ CMD \_ LINK**


</dt> <dd>

**Windows Vista und höher.** Erstellen Sie einen Link zum aktuellen Element.

</dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**\_DFM-CMD-EIGENSCHAFTEN \_**


</dt> <dd>

Zeigt die **Eigenschaftenbenutzeroberfläche** für das Element an, für das das Menü aufgerufen wurde.

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM \_ CMD \_ NEWFOLDER**


</dt> <dd>

Wird nicht unterstützt.

</dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM \_ CMD \_ PASTE**


</dt> <dd>

**Windows Vista und höher.** Fügen Sie ein Element an der aktuellen Position ein.

</dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM \_ CMD \_ VIEWLIST**


</dt> <dd>

Wird nicht unterstützt.

</dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM \_ CMD \_ VIEWDETAILS**


</dt> <dd>

Wird nicht unterstützt.

</dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM \_ CMD \_ PASTELINK**


</dt> <dd>

**Windows Vista und höher.** Fügen Sie einen Link an der aktuellen Position ein.

</dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM \_ CMD \_ PASTESPECIAL**


</dt> <dd>

Wird nicht unterstützt.

</dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM \_ CMD \_ MODALPROP**


</dt> <dd>

Wird nicht unterstützt.

</dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**\_ \_ DFM-CMD-UMBENENNUNG**


</dt> <dd>

**Windows Vista und höher.** Benennen Sie das aktuelle Element um.

</dd> </dl> </dd> <dt>

*args* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die zusätzliche Argumente für den ausgewählten Menübefehl enthält. Dieser Parameter kann **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Handler für diese Meldung muss S FALSE zurückgeben, wenn die Standardimplementierung den Standardhandler für \_ den Befehl aufrufen soll. Gibt S \_ OK zurück, wenn die Nachricht behandelt wurde. Andernfalls wird ein HRESULT-Standardfehlercode zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Nachricht wird entweder an die Rückruffunktion oder das Rückrufobjekt gesendet, je nachdem, wie der Rückruf implementiert wird. Es gibt zwei APIs für die Rückrufkonstruktion: [**CDefFolderMenu \_ Create2,**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) die einen Zeiger auf eine Rückruffunktion verwenden, oder [**SHCreateDefaultContextMenu,**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) das ein Rückrufobjekt verwendet, das [**IContextMenuCB unterstützt.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb)

Die Elemente, für die der Befehl aufgerufen wird, werden in einem Datenobjekt bereitgestellt, das an die Rückruffunktion oder die [**IContextMenuCB::CallBack-Methode übergeben**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) wird. Dieses Datenobjekt wird von der Datenquelle bereitgestellt, die den Rückruf implementiert. Um die Elemente aus dem Datenobjekt zu extrahieren, verwenden Sie [**SHCreateShellItemArrayFromDataObject.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject)

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) ist eine erweiterte Version dieser Nachricht und stellt weitere Informationen für den Rückruf zur Verfügung. Verwenden **Sie DFM \_ INVOKECOMMANDEX,** wenn die zusätzlichen Informationen, die von dieser Schnittstelle bereitgestellt werden, in Ihrer Implementierung benötigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
