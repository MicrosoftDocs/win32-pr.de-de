---
description: Ruft die Eigenschaften der Ansicht ab.
title: 'Ishellfolderviewtype:: getviewtypeproperties-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetViewTypeProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 82be6bd5-a46c-48b3-a1f0-a92b9454c35e
ms.openlocfilehash: f4368edf6eae3e6892a3d81147401e061548f6e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977928"
---
# <a name="ishellfolderviewtypegetviewtypeproperties-method"></a><span data-ttu-id="866a3-103">Ishellfolderviewtype:: getviewtypeproperties-Methode</span><span class="sxs-lookup"><span data-stu-id="866a3-103">IShellFolderViewType::GetViewTypeProperties method</span></span>

<span data-ttu-id="866a3-104">Ruft die Eigenschaften der Ansicht ab.</span><span class="sxs-lookup"><span data-stu-id="866a3-104">Gets the properties of the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="866a3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="866a3-105">Syntax</span></span>


```C++
HRESULT GetViewTypeProperties(
  [in]  PCUITEMID_CHILD pidl,
  [out] DWORD           *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="866a3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="866a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="866a3-107">*PIDL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="866a3-107">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="866a3-108">Type: **pcuitemid \_ Child**</span><span class="sxs-lookup"><span data-stu-id="866a3-108">Type: **PCUITEMID\_CHILD**</span></span>

<span data-ttu-id="866a3-109">eine PIDL.</span><span class="sxs-lookup"><span data-stu-id="866a3-109">A PIDL.</span></span>

</dd> <dt>

<span data-ttu-id="866a3-110">*pdwflags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="866a3-110">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="866a3-111">Typ: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="866a3-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="866a3-112">Ein Zeiger auf eine ganzzahlige Variable ohne Vorzeichen, die die Ansichts Eigenschaften empfängt und angibt, was beim Auswählen der Sicht geschehen soll.</span><span class="sxs-lookup"><span data-stu-id="866a3-112">A pointer to an unsigned integer variable that receives the view properties, which indicate what to do when the view is selected.</span></span> <span data-ttu-id="866a3-113">Flags können eine beliebige Kombination der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="866a3-113">Flags may be any combination of the following values.</span></span>

<dt>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>

<span data-ttu-id="866a3-114"><span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>_ *Sfvtflag \_ Notify \_ Create*\* (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="866a3-114"><span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>_ *SFVTFLAG\_NOTIFY\_CREATE*\* (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="866a3-115">Erstellen Sie ein Ansichts Element, wenn nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="866a3-115">Create view item if not there.</span></span>

</dd> <dt>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>

<span data-ttu-id="866a3-116"><span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**Sfvtflag \_ \_Ressort Benachrichtigen** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="866a3-116"><span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG\_NOTIFY\_RESORT** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="866a3-117">Resert PIDL und resortieren.</span><span class="sxs-lookup"><span data-stu-id="866a3-117">Reinsert PIDL and re-sort.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="866a3-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="866a3-118">Return value</span></span>

<span data-ttu-id="866a3-119">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="866a3-119">Type: **HRESULT**</span></span>

<span data-ttu-id="866a3-120">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="866a3-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="866a3-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="866a3-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="866a3-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="866a3-122">Requirements</span></span>



| <span data-ttu-id="866a3-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="866a3-123">Requirement</span></span> | <span data-ttu-id="866a3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="866a3-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="866a3-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="866a3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="866a3-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="866a3-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="866a3-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="866a3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="866a3-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="866a3-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="866a3-129">DLL</span><span class="sxs-lookup"><span data-stu-id="866a3-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="866a3-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="866a3-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




