---
description: Wird von der Standardimplementierung des Kontextmenüs gesendet, um LPFNDFMCALLBACK zum Aufrufen eines erweiterten Menübefehls anfordern.
title: DFM_INVOKECOMMANDEX (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6ef885e5-2ddd-4a1b-9f8e-016a74e292b1
api_name:
- DFM_INVOKECOMMANDEX
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2b8a7fd63aa4269ee265a4ae147c99fe394e8aad725f7134f8d62daf8ee9984b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943170"
---
# <a name="dfm_invokecommandex-message"></a>DFM \_ INVOKECOMMANDEX-Nachricht

Wird von der Standardimplementierung des Kontextmenüs gesendet, um [**LPFNDFMCALLBACK zum**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback) Aufrufen eines erweiterten Menübefehls anfordern.


```C++
                DFM_INVOKECOMMANDEX
    wParam = (WPARAM)(int) idCmd;           
    lParam = (LPARAM)(DFMICS) PDFMICS;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*idCmd* \[ in\]
</dt> <dd>

Die Befehls-ID des ausgewählten Menübefehls. Die folgenden Flags werden erkannt.

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM \_ CMD \_ DELETE**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM \_ CMD \_ MOVE**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**DFM \_ CMD \_ COPY**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM \_ CMD \_ LINK**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**\_DFM-CMD-EIGENSCHAFTEN \_**


</dt> <dd>

Zeigen Sie **die Eigenschaftenbenutzeroberfläche** für das Element an, für das das Menü aufgerufen wurde.

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM \_ CMD \_ NEWFOLDER**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM \_ CMD \_ PASTE**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM \_ CMD \_ VIEWLIST**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM \_ CMD \_ VIEWDETAILS**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM \_ CMD \_ PASTELINK**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM \_ CMD \_ PASTESPECIAL**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM \_ CMD \_ MODALPROP**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**\_ \_ DFM-CMD-UMBENENNUNG**


</dt> <dd></dd> </dl> </dd> <dt>

*PDFMICS* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**DFMICS-Struktur,**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics) die zusätzliche Argumente für den ausgewählten Menübefehl enthält. Dieser Parameter kann **NULL** sein.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Nach Erhalt dieser Meldung sollte Ihre Funktion S FALSE zurückgeben, wenn die Standardimplementierung den Standardhandler für \_ den Befehl aufrufen soll. Gibt S \_ OK zurück, wenn die Nachricht behandelt wurde. Andernfalls wird ein HRESULT-Standardfehlercode zurückgegeben.

Diese Nachricht wird entweder an die Rückruffunktion oder das Rückrufobjekt gesendet, je nachdem, wie der Rückruf implementiert wird. Es gibt zwei APIs für die Rückrufkonstruktion: [**CDefFolderMenu \_ Create2,**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) die einen Zeiger auf eine Rückruffunktion verwenden, oder [**SHCreateDefaultContextMenu,**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) das ein Rückrufobjekt verwendet, das [**IContextMenuCB unterstützt.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb)

Die Elemente, für die der Befehl aufgerufen wird, werden in einem Datenobjekt bereitgestellt, das an die Rückruffunktion oder die [**IContextMenuCB::CallBack-Methode übergeben**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) wird. Dieses Datenobjekt wird von der Datenquelle bereitgestellt, die den Rückruf implementiert. Um die Elemente aus dem Datenobjekt zu extrahieren, verwenden Sie [**SHCreateShellItemArrayFromDataObject.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject)

[**DFM \_ INVOKECOMMAND ist**](dfm-invokecommand.md) eine einfachere Version dieser Nachricht, die dem Rückruf nicht so viele Informationen zur Verfügung stellt. Verwenden **Sie DFM \_ INVOKECOMMAND,** wenn die zusätzlichen Informationen, die von **DFM \_ INVOKECOMMANDEX** bereitgestellt werden, in Ihrer Implementierung nicht benötigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
