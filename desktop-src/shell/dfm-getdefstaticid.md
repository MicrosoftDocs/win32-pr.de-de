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
# <a name="dfm_getdefstaticid-message"></a><span data-ttu-id="cf490-104">DFM \_ getdefstaticid-Meldung</span><span class="sxs-lookup"><span data-stu-id="cf490-104">DFM\_GETDEFSTATICID message</span></span>

<span data-ttu-id="cf490-105">Wird von der standardmäßigen Kontextmenü Implementierung während der Erstellung gesendet, wobei der Standardmenü Befehl angegeben und eine Alternative Auswahl getroffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="cf490-105">Sent by the default context menu implementation during creation, specifying the default menu command and allowing an alternate choice to be made.</span></span> <span data-ttu-id="cf490-106">Wird von [**lpfndfmcallback**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)verwendet.</span><span class="sxs-lookup"><span data-stu-id="cf490-106">Used by [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback).</span></span>


```C++
DFM_GETDEFSTATICID
    lParam = (LPARAM)(int*) defaultID;          
            
```



## <a name="parameters"></a><span data-ttu-id="cf490-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf490-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf490-108">*DefaultID* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cf490-108">*defaultID* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf490-109">Ein Zeiger auf die ID des ausgewählten Menübefehls.</span><span class="sxs-lookup"><span data-stu-id="cf490-109">A pointer to the ID of the selected menu command.</span></span> <span data-ttu-id="cf490-110">Das folgende Flag wird erkannt.</span><span class="sxs-lookup"><span data-stu-id="cf490-110">The following flag is recognized.</span></span>

<dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span data-ttu-id="cf490-111"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM- \_ cmd- \_ Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="cf490-111"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM\_CMD\_PROPERTIES**</span></span>


</dt> <dd>

<span data-ttu-id="cf490-112">Zeigt die **Eigenschaften** Benutzeroberfläche für das Element an, für das das Menü aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="cf490-112">Show the **Properties** UI for the item the menu was invoked on.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf490-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf490-113">Remarks</span></span>

<span data-ttu-id="cf490-114">Wenn Sie die standardmäßige Befehls Auswahl überschreiben möchten, sollte Ihr Handler beim Empfang dieser Nachricht den Wert, auf den von *DefaultID* verwiesen wird, auf die ID des Ersetzungs Befehls festlegen und S OK zurückgeben \_ .</span><span class="sxs-lookup"><span data-stu-id="cf490-114">To override the default command choice, your handler should, upon receipt of this message, set the value pointed to by *defaultID* to the ID of the replacement command and return S\_OK.</span></span> <span data-ttu-id="cf490-115">Andernfalls wird ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cf490-115">Return a failure code otherwise.</span></span>

<span data-ttu-id="cf490-116">Diese Nachricht wird entweder an die Rückruffunktion oder an das Rückruf Objekt gesendet, je nachdem, wie das standardmäßige Kontextmenü Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="cf490-116">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="cf490-117">Es gibt zwei APIs für die Erstellung, [**cdeffoldermenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**shkreatedefaultcontextmenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="cf490-117">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="cf490-118">[**DFM \_ Invokecommandex**](dfm-invokecommandex.md) ist eine erweiterte Version dieser Nachricht und bietet weitere Informationen für den Rückruf.</span><span class="sxs-lookup"><span data-stu-id="cf490-118">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="cf490-119">Verwenden Sie **DFM \_ invokecommandex** , wenn die zusätzlichen Informationen, die von dieser Schnittstelle bereitgestellt werden, in der Implementierung benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="cf490-119">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf490-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="cf490-120">Requirements</span></span>



| <span data-ttu-id="cf490-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf490-121">Requirement</span></span> | <span data-ttu-id="cf490-122">Wert</span><span class="sxs-lookup"><span data-stu-id="cf490-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cf490-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf490-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cf490-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf490-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="cf490-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf490-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cf490-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf490-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cf490-127">Header</span><span class="sxs-lookup"><span data-stu-id="cf490-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf490-128"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf490-128"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
