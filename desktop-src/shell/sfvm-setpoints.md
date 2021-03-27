---
description: Legt die Punkte der aktuell ausgewählten Objekte auf das Datenobjekt in den Befehlen zum Kopieren und Ausschneiden fest. Wird von der shshellfolderview- \_ Nachricht verwendet.
title: SFVM_SETPOINTS Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d2c3e06a-19e4-4b78-9b7c-1a256582786e
api_name:
- SFVM_SETPOINTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1df501f162fb19335fcf1672299a74135672db22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218583"
---
# <a name="sfvm_setpoints-message"></a><span data-ttu-id="2c169-104">Sfvm- \_ SetPoints-Meldung</span><span class="sxs-lookup"><span data-stu-id="2c169-104">SFVM\_SETPOINTS message</span></span>

<span data-ttu-id="2c169-105">Legt die Punkte der aktuell ausgewählten Objekte auf das Datenobjekt in den Befehlen zum **Kopieren** und **Ausschneiden** fest.</span><span class="sxs-lookup"><span data-stu-id="2c169-105">Sets the points of the currently selected objects to the data object on **Copy** and **Cut** commands.</span></span> <span data-ttu-id="2c169-106">Wird von der [**shshellfolderview- \_ Nachricht**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)verwendet.</span><span class="sxs-lookup"><span data-stu-id="2c169-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_SETPOINTS 

    lParam = (LPARAM) pdtobj;

            
```



## <a name="parameters"></a><span data-ttu-id="2c169-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c169-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c169-108">*pdtobj* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c169-108">*pdtobj* \[in\]</span></span>
</dt> <dd><span data-ttu-id="2c169-109">Ein Zeiger auf ein <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">**IDataObject**</a> der Befehle zum **Kopieren** und **Ausschneiden** .</span><span class="sxs-lookup"><span data-stu-id="2c169-109">A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">**IDataObject**</a> of the **Copy** and **Cut** commands.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c169-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c169-110">Return value</span></span>

<span data-ttu-id="2c169-111">Es wird immer NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2c169-111">Always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c169-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c169-112">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2c169-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2c169-113">Requirements</span></span>



| <span data-ttu-id="2c169-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c169-114">Requirement</span></span> | <span data-ttu-id="2c169-115">Wert</span><span class="sxs-lookup"><span data-stu-id="2c169-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2c169-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c169-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2c169-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c169-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2c169-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c169-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2c169-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c169-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2c169-120">Header</span><span class="sxs-lookup"><span data-stu-id="2c169-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c169-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c169-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
