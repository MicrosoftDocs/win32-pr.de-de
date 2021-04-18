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
# <a name="dfm_invokecommand-message"></a><span data-ttu-id="32a45-103">DFM \_ InvokeCommand-Meldung</span><span class="sxs-lookup"><span data-stu-id="32a45-103">DFM\_INVOKECOMMAND message</span></span>

<span data-ttu-id="32a45-104">Wird von der standardmäßigen Kontextmenü Implementierung gesendet, um die Rückruffunktion anzufordern, die das Menü ([**lpfndfmcallback**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)) zum Aufrufen eines Menübefehls aufruft.</span><span class="sxs-lookup"><span data-stu-id="32a45-104">Sent by the default context menu implementation to request the callback function that handles the menu ([**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)) to invoke a menu command.</span></span>


```C++
DFM_INVOKECOMMAND
    wParam = (WPARAM)(int) id;          
    lParam = (LPARAM)(LPWSTR) args;
            
```



## <a name="parameters"></a><span data-ttu-id="32a45-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="32a45-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32a45-106">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32a45-106">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32a45-107">Die Befehls-ID des ausgewählten Menübefehls.</span><span class="sxs-lookup"><span data-stu-id="32a45-107">The command ID of the selected menu command.</span></span> <span data-ttu-id="32a45-108">Die folgenden Flags werden erkannt:</span><span class="sxs-lookup"><span data-stu-id="32a45-108">The following flags are recognized:</span></span>

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span data-ttu-id="32a45-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM- \_ cmd \_ Löschen**</span><span class="sxs-lookup"><span data-stu-id="32a45-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM\_CMD\_DELETE**</span></span>


</dt> <dd>

<span data-ttu-id="32a45-110">**Windows Vista und** höher.</span><span class="sxs-lookup"><span data-stu-id="32a45-110">**Windows Vista and later**.</span></span> <span data-ttu-id="32a45-111">Löschen Sie das aktuelle Element.</span><span class="sxs-lookup"><span data-stu-id="32a45-111">Delete the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span data-ttu-id="32a45-112"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM- \_ cmd- \_ Verschiebung**</span><span class="sxs-lookup"><span data-stu-id="32a45-112"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM\_CMD\_MOVE**</span></span>


</dt> <dd>

<span data-ttu-id="32a45-113">**Windows Vista und** höher.</span><span class="sxs-lookup"><span data-stu-id="32a45-113">**Windows Vista and later**.</span></span> <span data-ttu-id="32a45-114">Verschieben Sie das aktuelle Element.</span><span class="sxs-lookup"><span data-stu-id="32a45-114">Move the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span data-ttu-id="32a45-115"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**DFM- \_ cmd- \_ Kopie**</span><span class="sxs-lookup"><span data-stu-id="32a45-115"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**DFM\_CMD\_COPY**</span></span>


</dt> <dd>

<span data-ttu-id="32a45-116">**Windows Vista und** höher.</span><span class="sxs-lookup"><span data-stu-id="32a45-116">**Windows Vista and later**.</span></span> <span data-ttu-id="32a45-117">Kopieren Sie das aktuelle Element.</span><span class="sxs-lookup"><span data-stu-id="32a45-117">Copy the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span data-ttu-id="32a45-118"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM- \_ cmd- \_ Link**</span><span class="sxs-lookup"><span data-stu-id="32a45-118"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM\_CMD\_LINK**</span></span>


</dt> <dd>

<span data-ttu-id="32a45-119">**Windows Vista und** höher.</span><span class="sxs-lookup"><span data-stu-id="32a45-119">**Windows Vista and later**.</span></span> <span data-ttu-id="32a45-120">Erstellen Sie einen Link zum aktuellen Element.</span><span class="sxs-lookup"><span data-stu-id="32a45-120">Create a link to the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span data-ttu-id="32a45-121"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM- \_ cmd- \_ Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="32a45-121"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM\_CMD\_PROPERTIES**</span></span>


</dt> <dd>

<span data-ttu-id="32a45-122">Zeigt die **Eigenschaften** Benutzeroberfläche für das Element an, auf dem das Menü aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="32a45-122">Show the **Properties** UI for the item on which the menu was invoked.</span></span>

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span data-ttu-id="32a45-123"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM- \_ cmd \_ NewFolder**</span><span class="sxs-lookup"><span data-stu-id="32a45-123"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM\_CMD\_NEWFOLDER**</span></span>


</dt> <dd>

<span data-ttu-id="32a45-124">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="32a45-124">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span data-ttu-id="32a45-125"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM- \_ cmd \_ Einfügen**</span><span class="sxs-lookup"><span data-stu-id="32a45-125"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM\_CMD\_PASTE**</span></span>


</dt> <dd>

<span data-ttu-id="32a45-126">**Windows Vista und** höher.</span><span class="sxs-lookup"><span data-stu-id="32a45-126">**Windows Vista and later**.</span></span> <span data-ttu-id="32a45-127">Fügt ein Element an der aktuellen Position ein.</span><span class="sxs-lookup"><span data-stu-id="32a45-127">Paste an item to the current location.</span></span>

</dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span data-ttu-id="32a45-128"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM- \_ cmd- \_ viewlist**</span><span class="sxs-lookup"><span data-stu-id="32a45-128"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM\_CMD\_VIEWLIST**</span></span>


</dt> <dd>

<span data-ttu-id="32a45-129">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="32a45-129">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span data-ttu-id="32a45-130"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM- \_ cmd- \_ ViewDetails**</span><span class="sxs-lookup"><span data-stu-id="32a45-130"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM\_CMD\_VIEWDETAILS**</span></span>


</dt> <dd>

<span data-ttu-id="32a45-131">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="32a45-131">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span data-ttu-id="32a45-132"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM- \_ cmd- \_ pstelink**</span><span class="sxs-lookup"><span data-stu-id="32a45-132"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM\_CMD\_PASTELINK**</span></span>


</dt> <dd>

<span data-ttu-id="32a45-133">**Windows Vista und** höher.</span><span class="sxs-lookup"><span data-stu-id="32a45-133">**Windows Vista and later**.</span></span> <span data-ttu-id="32a45-134">Fügen Sie einen Link an der aktuellen Position ein.</span><span class="sxs-lookup"><span data-stu-id="32a45-134">Paste a link at the current location.</span></span>

</dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span data-ttu-id="32a45-135"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM \_ cmd \_ PasteSpecial**</span><span class="sxs-lookup"><span data-stu-id="32a45-135"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM\_CMD\_PASTESPECIAL**</span></span>


</dt> <dd>

<span data-ttu-id="32a45-136">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="32a45-136">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span data-ttu-id="32a45-137"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM- \_ cmd \_ modalprop**</span><span class="sxs-lookup"><span data-stu-id="32a45-137"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM\_CMD\_MODALPROP**</span></span>


</dt> <dd>

<span data-ttu-id="32a45-138">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="32a45-138">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span data-ttu-id="32a45-139"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**Umbenennen von DFM- \_ cmd \_**</span><span class="sxs-lookup"><span data-stu-id="32a45-139"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**DFM\_CMD\_RENAME**</span></span>


</dt> <dd>

<span data-ttu-id="32a45-140">**Windows Vista und** höher.</span><span class="sxs-lookup"><span data-stu-id="32a45-140">**Windows Vista and later**.</span></span> <span data-ttu-id="32a45-141">Benennen Sie das aktuelle Element um.</span><span class="sxs-lookup"><span data-stu-id="32a45-141">Rename the current item.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="32a45-142">*args* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32a45-142">*args* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32a45-143">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die zusätzliche Argumente für den ausgewählten Menübefehl enthält.</span><span class="sxs-lookup"><span data-stu-id="32a45-143">A pointer to a null-terminated string that contains additional arguments to the selected menu command.</span></span> <span data-ttu-id="32a45-144">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="32a45-144">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32a45-145">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="32a45-145">Return value</span></span>

<span data-ttu-id="32a45-146">Der Handler für diese Nachricht muss S false zurückgeben, \_ Wenn die Standard Implementierung den Standard Handler für den Befehl aufrufen soll.</span><span class="sxs-lookup"><span data-stu-id="32a45-146">The handler for this message needs to return S\_FALSE if you want the default implementation to invoke the default handler for the command.</span></span> <span data-ttu-id="32a45-147">Gibt "S OK" zurück, \_ Wenn die Meldung behandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="32a45-147">Return S\_OK if the message was handled.</span></span> <span data-ttu-id="32a45-148">Andernfalls wird ein Standard-HRESULT-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="32a45-148">Otherwise, return a standard HRESULT error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="32a45-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32a45-149">Remarks</span></span>

<span data-ttu-id="32a45-150">Diese Meldung wird abhängig von der Implementierung des Rückrufs entweder an die Rückruffunktion oder an das Rückruf Objekt gesendet.</span><span class="sxs-lookup"><span data-stu-id="32a45-150">This message is sent to either the callback function or the callback object depending on how the callback is implemented.</span></span> <span data-ttu-id="32a45-151">Es gibt zwei APIs für die Rückruf Erstellung, [**cdeffoldermenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) , die einen Zeiger auf eine Rückruffunktion annimmt, oder [**shkreatedefaultcontextmenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) , das ein Rückruf Objekt verwendet, das [**icontextmenucb**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="32a45-151">There are two APIs for callback construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) that takes a pointer to a callback function, or [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) that uses a callback object that supports [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).</span></span>

<span data-ttu-id="32a45-152">Die Elemente, für die der Befehl aufgerufen wird, werden in einem Datenobjekt bereitgestellt, das an die Rückruffunktion oder an die [**icontextmenucb:: callback**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) -Methode weitergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="32a45-152">The items on which the command is being invoked are provided in a data object passed to the callback function or to the [**IContextMenuCB::CallBack**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) method.</span></span> <span data-ttu-id="32a45-153">Dieses Datenobjekt wird von der Datenquelle bereitgestellt, die den Rückruf implementiert.</span><span class="sxs-lookup"><span data-stu-id="32a45-153">This data object is provided by the data source that implements the callback.</span></span> <span data-ttu-id="32a45-154">Um die Elemente aus dem Datenobjekt zu extrahieren, verwenden Sie [**shkreateshellitemarrayfromdataobject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span><span class="sxs-lookup"><span data-stu-id="32a45-154">To extract the items from the data object, use [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span></span>

<span data-ttu-id="32a45-155">[**DFM \_ Invokecommandex**](dfm-invokecommandex.md) ist eine erweiterte Version dieser Nachricht und bietet weitere Informationen für den Rückruf.</span><span class="sxs-lookup"><span data-stu-id="32a45-155">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="32a45-156">Verwenden Sie **DFM \_ invokecommandex** , wenn die zusätzlichen Informationen, die von dieser Schnittstelle bereitgestellt werden, in der Implementierung benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="32a45-156">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="32a45-157">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="32a45-157">Requirements</span></span>



| <span data-ttu-id="32a45-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32a45-158">Requirement</span></span> | <span data-ttu-id="32a45-159">Wert</span><span class="sxs-lookup"><span data-stu-id="32a45-159">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="32a45-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="32a45-160">Minimum supported client</span></span><br/> | <span data-ttu-id="32a45-161">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32a45-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="32a45-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="32a45-162">Minimum supported server</span></span><br/> | <span data-ttu-id="32a45-163">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32a45-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="32a45-164">Header</span><span class="sxs-lookup"><span data-stu-id="32a45-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="32a45-165"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="32a45-165"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
