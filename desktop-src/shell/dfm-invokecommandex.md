---
description: Wird von der Standard Implementierung des Kontextmenüs gesendet, um lpfndfmcallback zum Aufrufen eines erweiterten Menübefehls anzufordern.
title: DFM_INVOKECOMMANDEX Meldung (shlobj. h)
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
ms.openlocfilehash: dc96e9d0e4c27be8dee3ed7742874de4a3fb97e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525361"
---
# <a name="dfm_invokecommandex-message"></a>DFM \_ invokecommandex-Meldung

Wird von der Standard Implementierung des Kontextmenüs gesendet, um [**lpfndfmcallback**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback) zum Aufrufen eines erweiterten Menübefehls anzufordern.


```C++
                DFM_INVOKECOMMANDEX
    wParam = (WPARAM)(int) idCmd;           
    lParam = (LPARAM)(DFMICS) PDFMICS;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*idcmd* \[ in\]
</dt> <dd>

Die Befehls-ID des ausgewählten Menübefehls. Die folgenden Flags werden erkannt.

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM- \_ cmd \_ Löschen**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM- \_ cmd- \_ Verschiebung**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**DFM- \_ cmd- \_ Kopie**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM- \_ cmd- \_ Link**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM- \_ cmd- \_ Eigenschaften**


</dt> <dd>

Zeigt die **Eigenschaften** Benutzeroberfläche für das Element an, für das das Menü aufgerufen wurde.

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM- \_ cmd \_ NewFolder**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM- \_ cmd \_ Einfügen**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM- \_ cmd- \_ viewlist**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM- \_ cmd- \_ ViewDetails**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM- \_ cmd- \_ pstelink**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM \_ cmd \_ PasteSpecial**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM- \_ cmd \_ modalprop**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**Umbenennen von DFM- \_ cmd \_**


</dt> <dd></dd> </dl> </dd> <dt>

*Pdfmics* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**dfmics**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics) -Struktur, die zusätzliche Argumente für den ausgewählten Menübefehl enthält. Dieser Parameter kann **NULL** sein.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beim Empfang dieser Nachricht sollte die Funktion "S false" zurückgeben, \_ Wenn die Standard Implementierung den Standard Handler für den Befehl aufrufen soll. Gibt "S OK" zurück, \_ Wenn die Meldung behandelt wurde. Andernfalls wird ein Standard-HRESULT-Fehlercode zurückgegeben.

Diese Meldung wird abhängig von der Implementierung des Rückrufs entweder an die Rückruffunktion oder an das Rückruf Objekt gesendet. Es gibt zwei APIs für die Rückruf Erstellung, [**cdeffoldermenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) , die einen Zeiger auf eine Rückruffunktion annimmt, oder [**shkreatedefaultcontextmenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) , das ein Rückruf Objekt verwendet, das [**icontextmenucb**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb)unterstützt.

Die Elemente, für die der Befehl aufgerufen wird, werden in einem Datenobjekt bereitgestellt, das an die Rückruffunktion oder an die [**icontextmenucb:: callback**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) -Methode weitergegeben wird. Dieses Datenobjekt wird von der Datenquelle bereitgestellt, die den Rückruf implementiert. Um die Elemente aus dem Datenobjekt zu extrahieren, verwenden Sie [**shkreateshellitemarrayfromdataobject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).

[**DFM \_ InvokeCommand**](dfm-invokecommand.md) ist eine einfachere Version dieser Nachricht, die dem Rückruf nicht so viele Informationen bereitstellt. Verwenden Sie **DFM \_ InvokeCommand** , wenn die zusätzlichen Informationen von **DFM \_ invokecommandex** in ihrer Implementierung nicht benötigt werden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
