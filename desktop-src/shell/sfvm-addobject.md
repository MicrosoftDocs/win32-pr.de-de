---
description: Fügt der shellansicht ein Objekt hinzu. Wird von der shshellfolderview- \_ Nachricht verwendet.
title: SFVM_ADDOBJECT Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 90394af6-3809-457c-b2f2-5f35187ed45b
api_name:
- SFVM_ADDOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0e5b3f0a5b1aed634ab8929b0501d2e23ba40352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994887"
---
# <a name="sfvm_addobject-message"></a><span data-ttu-id="c55cf-104">Sfvm- \_ AddObject-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c55cf-104">SFVM\_ADDOBJECT message</span></span>

<span data-ttu-id="c55cf-105">Fügt der shellansicht ein Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="c55cf-105">Adds an object to the Shell view.</span></span> <span data-ttu-id="c55cf-106">Wird von der [**shshellfolderview- \_ Nachricht**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)verwendet.</span><span class="sxs-lookup"><span data-stu-id="c55cf-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_ADDOBJECT 

    lParam = (LPARAM) pidl;

            
```



## <a name="parameters"></a><span data-ttu-id="c55cf-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c55cf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c55cf-108">*PIDL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c55cf-108">*pidl* \[in\]</span></span>
</dt> <dd><span data-ttu-id="c55cf-109">Ein Zeiger auf das hinzu zufügende Objekt.</span><span class="sxs-lookup"><span data-stu-id="c55cf-109">A pointer to the object of interest to add.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c55cf-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c55cf-110">Return value</span></span>

<span data-ttu-id="c55cf-111">Gibt die neue ListView-Element-ID des hinzugefügten Objekts zurück, wenn der Prozess erfolgreich war. Andernfalls wird-1 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c55cf-111">Returns the new listview item ID of the added object if the process was successful; otherwise, returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="c55cf-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c55cf-112">Requirements</span></span>



| <span data-ttu-id="c55cf-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c55cf-113">Requirement</span></span> | <span data-ttu-id="c55cf-114">Wert</span><span class="sxs-lookup"><span data-stu-id="c55cf-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c55cf-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c55cf-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c55cf-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c55cf-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c55cf-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c55cf-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c55cf-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c55cf-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c55cf-119">Header</span><span class="sxs-lookup"><span data-stu-id="c55cf-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c55cf-120"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="c55cf-120"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




