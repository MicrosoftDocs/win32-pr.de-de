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
# <a name="dfm_invokecommandex-message"></a><span data-ttu-id="10a14-103">DFM \_ invokecommandex-Meldung</span><span class="sxs-lookup"><span data-stu-id="10a14-103">DFM\_INVOKECOMMANDEX message</span></span>

<span data-ttu-id="10a14-104">Wird von der Standard Implementierung des Kontextmenüs gesendet, um [**lpfndfmcallback**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback) zum Aufrufen eines erweiterten Menübefehls anzufordern.</span><span class="sxs-lookup"><span data-stu-id="10a14-104">Sent by the default context menu implementation to request [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback) to invoke an extended menu command.</span></span>


```C++
                DFM_INVOKECOMMANDEX
    wParam = (WPARAM)(int) idCmd;           
    lParam = (LPARAM)(DFMICS) PDFMICS;
            
```



## <a name="parameters"></a><span data-ttu-id="10a14-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="10a14-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10a14-106">*idcmd* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10a14-106">*idCmd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10a14-107">Die Befehls-ID des ausgewählten Menübefehls.</span><span class="sxs-lookup"><span data-stu-id="10a14-107">The command ID of the selected menu command.</span></span> <span data-ttu-id="10a14-108">Die folgenden Flags werden erkannt.</span><span class="sxs-lookup"><span data-stu-id="10a14-108">The following flags are recognized.</span></span>

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span data-ttu-id="10a14-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM- \_ cmd \_ Löschen**</span><span class="sxs-lookup"><span data-stu-id="10a14-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM\_CMD\_DELETE**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span data-ttu-id="10a14-110"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM- \_ cmd- \_ Verschiebung**</span><span class="sxs-lookup"><span data-stu-id="10a14-110"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM\_CMD\_MOVE**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span data-ttu-id="10a14-111"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**DFM- \_ cmd- \_ Kopie**</span><span class="sxs-lookup"><span data-stu-id="10a14-111"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**DFM\_CMD\_COPY**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span data-ttu-id="10a14-112"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM- \_ cmd- \_ Link**</span><span class="sxs-lookup"><span data-stu-id="10a14-112"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM\_CMD\_LINK**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span data-ttu-id="10a14-113"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM- \_ cmd- \_ Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="10a14-113"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM\_CMD\_PROPERTIES**</span></span>


</dt> <dd>

<span data-ttu-id="10a14-114">Zeigt die **Eigenschaften** Benutzeroberfläche für das Element an, für das das Menü aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="10a14-114">Show the **Properties** UI for the item the menu was invoked on.</span></span>

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span data-ttu-id="10a14-115"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM- \_ cmd \_ NewFolder**</span><span class="sxs-lookup"><span data-stu-id="10a14-115"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM\_CMD\_NEWFOLDER**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span data-ttu-id="10a14-116"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM- \_ cmd \_ Einfügen**</span><span class="sxs-lookup"><span data-stu-id="10a14-116"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM\_CMD\_PASTE**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span data-ttu-id="10a14-117"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM- \_ cmd- \_ viewlist**</span><span class="sxs-lookup"><span data-stu-id="10a14-117"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM\_CMD\_VIEWLIST**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span data-ttu-id="10a14-118"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM- \_ cmd- \_ ViewDetails**</span><span class="sxs-lookup"><span data-stu-id="10a14-118"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM\_CMD\_VIEWDETAILS**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span data-ttu-id="10a14-119"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM- \_ cmd- \_ pstelink**</span><span class="sxs-lookup"><span data-stu-id="10a14-119"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM\_CMD\_PASTELINK**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span data-ttu-id="10a14-120"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM \_ cmd \_ PasteSpecial**</span><span class="sxs-lookup"><span data-stu-id="10a14-120"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM\_CMD\_PASTESPECIAL**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span data-ttu-id="10a14-121"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM- \_ cmd \_ modalprop**</span><span class="sxs-lookup"><span data-stu-id="10a14-121"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM\_CMD\_MODALPROP**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span data-ttu-id="10a14-122"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**Umbenennen von DFM- \_ cmd \_**</span><span class="sxs-lookup"><span data-stu-id="10a14-122"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**DFM\_CMD\_RENAME**</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="10a14-123">*Pdfmics* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10a14-123">*PDFMICS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10a14-124">Ein Zeiger auf eine [**dfmics**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics) -Struktur, die zusätzliche Argumente für den ausgewählten Menübefehl enthält.</span><span class="sxs-lookup"><span data-stu-id="10a14-124">A pointer to a [**DFMICS**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics) structure that contains additional arguments to the selected menu command.</span></span> <span data-ttu-id="10a14-125">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="10a14-125">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10a14-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10a14-126">Remarks</span></span>

<span data-ttu-id="10a14-127">Beim Empfang dieser Nachricht sollte die Funktion "S false" zurückgeben, \_ Wenn die Standard Implementierung den Standard Handler für den Befehl aufrufen soll.</span><span class="sxs-lookup"><span data-stu-id="10a14-127">Upon receipt of this message, your function should return S\_FALSE if you want the default implementation to invoke the default handler for the command.</span></span> <span data-ttu-id="10a14-128">Gibt "S OK" zurück, \_ Wenn die Meldung behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="10a14-128">Return S\_OK if the message was handled.</span></span> <span data-ttu-id="10a14-129">Andernfalls wird ein Standard-HRESULT-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="10a14-129">Otherwise, return a standard HRESULT error code.</span></span>

<span data-ttu-id="10a14-130">Diese Meldung wird abhängig von der Implementierung des Rückrufs entweder an die Rückruffunktion oder an das Rückruf Objekt gesendet.</span><span class="sxs-lookup"><span data-stu-id="10a14-130">This message is sent to either the callback function or the callback object depending on how the callback is implemented.</span></span> <span data-ttu-id="10a14-131">Es gibt zwei APIs für die Rückruf Erstellung, [**cdeffoldermenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) , die einen Zeiger auf eine Rückruffunktion annimmt, oder [**shkreatedefaultcontextmenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) , das ein Rückruf Objekt verwendet, das [**icontextmenucb**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="10a14-131">There are two APIs for callback construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) that takes a pointer to a callback function, or [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) that uses a callback object that supports [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).</span></span>

<span data-ttu-id="10a14-132">Die Elemente, für die der Befehl aufgerufen wird, werden in einem Datenobjekt bereitgestellt, das an die Rückruffunktion oder an die [**icontextmenucb:: callback**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) -Methode weitergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="10a14-132">The items on which the command is being invoked are provided in a data object passed to the callback function or to the [**IContextMenuCB::CallBack**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) method.</span></span> <span data-ttu-id="10a14-133">Dieses Datenobjekt wird von der Datenquelle bereitgestellt, die den Rückruf implementiert.</span><span class="sxs-lookup"><span data-stu-id="10a14-133">This data object is provided by the data source that implements the callback.</span></span> <span data-ttu-id="10a14-134">Um die Elemente aus dem Datenobjekt zu extrahieren, verwenden Sie [**shkreateshellitemarrayfromdataobject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span><span class="sxs-lookup"><span data-stu-id="10a14-134">To extract the items from the data object, use [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span></span>

<span data-ttu-id="10a14-135">[**DFM \_ InvokeCommand**](dfm-invokecommand.md) ist eine einfachere Version dieser Nachricht, die dem Rückruf nicht so viele Informationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="10a14-135">[**DFM\_INVOKECOMMAND**](dfm-invokecommand.md) is a simpler version of this message which does not provide as much information to the callback.</span></span> <span data-ttu-id="10a14-136">Verwenden Sie **DFM \_ InvokeCommand** , wenn die zusätzlichen Informationen von **DFM \_ invokecommandex** in ihrer Implementierung nicht benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="10a14-136">Use **DFM\_INVOKECOMMAND** if the additional information provided by **DFM\_INVOKECOMMANDEX** is not needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="10a14-137">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="10a14-137">Requirements</span></span>



| <span data-ttu-id="10a14-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10a14-138">Requirement</span></span> | <span data-ttu-id="10a14-139">Wert</span><span class="sxs-lookup"><span data-stu-id="10a14-139">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="10a14-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="10a14-140">Minimum supported client</span></span><br/> | <span data-ttu-id="10a14-141">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10a14-141">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="10a14-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="10a14-142">Minimum supported server</span></span><br/> | <span data-ttu-id="10a14-143">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10a14-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="10a14-144">Header</span><span class="sxs-lookup"><span data-stu-id="10a14-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="10a14-145"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="10a14-145"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
