---
description: Wird von der standardmäßigen Kontextmenü Implementierung gesendet, um die Rückruffunktion anzufordern, die das Menü (lpfndfmcallback) zum Aufrufen eines Menübefehls aufruft.
title: DFM_INVOKECOMMAND Meldung (shlobj. h)
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
ms.openlocfilehash: 168b25833deb6bde2424ea4552f4600b83bc9679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977289"
---
# <a name="dfm_invokecommand-message"></a>DFM \_ InvokeCommand-Meldung

Wird von der standardmäßigen Kontextmenü Implementierung gesendet, um die Rückruffunktion anzufordern, die das Menü ([**lpfndfmcallback**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)) zum Aufrufen eines Menübefehls aufruft.


```C++
DFM_INVOKECOMMAND
    wParam = (WPARAM)(int) id;          
    lParam = (LPARAM)(LPWSTR) args;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ID* \[ in\]
</dt> <dd>

Die Befehls-ID des ausgewählten Menübefehls. Die folgenden Flags werden erkannt:

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM- \_ cmd \_ Löschen**


</dt> <dd>

**Windows Vista und** höher. Löschen Sie das aktuelle Element.

</dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM- \_ cmd- \_ Verschiebung**


</dt> <dd>

**Windows Vista und** höher. Verschieben Sie das aktuelle Element.

</dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**DFM- \_ cmd- \_ Kopie**


</dt> <dd>

**Windows Vista und** höher. Kopieren Sie das aktuelle Element.

</dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM- \_ cmd- \_ Link**


</dt> <dd>

**Windows Vista und** höher. Erstellen Sie einen Link zum aktuellen Element.

</dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM- \_ cmd- \_ Eigenschaften**


</dt> <dd>

Zeigt die **Eigenschaften** Benutzeroberfläche für das Element an, auf dem das Menü aufgerufen wurde.

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM- \_ cmd \_ NewFolder**


</dt> <dd>

Wird nicht unterstützt.

</dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM- \_ cmd \_ Einfügen**


</dt> <dd>

**Windows Vista und** höher. Fügt ein Element an der aktuellen Position ein.

</dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM- \_ cmd- \_ viewlist**


</dt> <dd>

Wird nicht unterstützt.

</dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM- \_ cmd- \_ ViewDetails**


</dt> <dd>

Wird nicht unterstützt.

</dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM- \_ cmd- \_ pstelink**


</dt> <dd>

**Windows Vista und** höher. Fügen Sie einen Link an der aktuellen Position ein.

</dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM \_ cmd \_ PasteSpecial**


</dt> <dd>

Wird nicht unterstützt.

</dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM- \_ cmd \_ modalprop**


</dt> <dd>

Wird nicht unterstützt.

</dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**Umbenennen von DFM- \_ cmd \_**


</dt> <dd>

**Windows Vista und** höher. Benennen Sie das aktuelle Element um.

</dd> </dl> </dd> <dt>

*args* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die zusätzliche Argumente für den ausgewählten Menübefehl enthält. Dieser Parameter kann **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Handler für diese Nachricht muss S false zurückgeben, \_ Wenn die Standard Implementierung den Standard Handler für den Befehl aufrufen soll. Gibt "S OK" zurück, \_ Wenn die Meldung behandelt wurde. Andernfalls wird ein Standard-HRESULT-Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird abhängig von der Implementierung des Rückrufs entweder an die Rückruffunktion oder an das Rückruf Objekt gesendet. Es gibt zwei APIs für die Rückruf Erstellung, [**cdeffoldermenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) , die einen Zeiger auf eine Rückruffunktion annimmt, oder [**shkreatedefaultcontextmenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) , das ein Rückruf Objekt verwendet, das [**icontextmenucb**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb)unterstützt.

Die Elemente, für die der Befehl aufgerufen wird, werden in einem Datenobjekt bereitgestellt, das an die Rückruffunktion oder an die [**icontextmenucb:: callback**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) -Methode weitergegeben wird. Dieses Datenobjekt wird von der Datenquelle bereitgestellt, die den Rückruf implementiert. Um die Elemente aus dem Datenobjekt zu extrahieren, verwenden Sie [**shkreateshellitemarrayfromdataobject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).

[**DFM \_ Invokecommandex**](dfm-invokecommandex.md) ist eine erweiterte Version dieser Nachricht und bietet weitere Informationen für den Rückruf. Verwenden Sie **DFM \_ invokecommandex** , wenn die zusätzlichen Informationen, die von dieser Schnittstelle bereitgestellt werden, in der Implementierung benötigt werden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
