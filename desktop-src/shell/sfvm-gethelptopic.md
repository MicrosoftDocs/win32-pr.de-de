---
description: 'Ermöglicht dem Rückruf Objekt, eine HTML-Hilfedatei und ein Thema darin anzugeben. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
title: SFVM_GETHELPTOPIC Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bbe92e9f-4074-4101-a945-072866ab20a8
api_name:
- SFVM_GETHELPTOPIC
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7ebe078934f467407710f0ad493b6088b34d0c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866779"
---
# <a name="sfvm_gethelptopic-message"></a><span data-ttu-id="6b30f-104">Sfvm \_ GetHelpTopic-Nachricht</span><span class="sxs-lookup"><span data-stu-id="6b30f-104">SFVM\_GETHELPTOPIC message</span></span>

<span data-ttu-id="6b30f-105">Ermöglicht dem Rückruf Objekt, eine HTML-Hilfedatei und ein Thema darin anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6b30f-105">Allows the callback object to specify an HTML Help file and a topic within it.</span></span> <span data-ttu-id="6b30f-106">Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b30f-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETHELPTOPIC 

    lParam = (LPARAM)(SFVM_HELPTOPIC_DATA*) phtd;

            
```



## <a name="parameters"></a><span data-ttu-id="6b30f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b30f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b30f-108">*phtd* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6b30f-108">*phtd* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b30f-109">Die Adresse einer [**sfvm- \_ HelpTopic- \_ Daten**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data) Struktur, die die HTML-Hilfedatei und das Thema angibt.</span><span class="sxs-lookup"><span data-stu-id="6b30f-109">The address of a [**SFVM\_HELPTOPIC\_DATA**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data) structure that specifies the HTML Help file and topic.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6b30f-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="6b30f-110">Requirements</span></span>



| <span data-ttu-id="6b30f-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b30f-111">Requirement</span></span> | <span data-ttu-id="6b30f-112">Wert</span><span class="sxs-lookup"><span data-stu-id="6b30f-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6b30f-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b30f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="6b30f-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b30f-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6b30f-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b30f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="6b30f-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b30f-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6b30f-117">Header</span><span class="sxs-lookup"><span data-stu-id="6b30f-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b30f-118"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b30f-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
