---
description: Ruft die Eigenschaften der Ansicht ab.
title: IShellFolderViewType::GetViewTypeProperties-Methode
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
ms.openlocfilehash: f5c7c6b75c89711a69ac578b3d04a72362b1eac9
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842701"
---
# <a name="ishellfolderviewtypegetviewtypeproperties-method"></a><span data-ttu-id="834fa-103">IShellFolderViewType::GetViewTypeProperties-Methode</span><span class="sxs-lookup"><span data-stu-id="834fa-103">IShellFolderViewType::GetViewTypeProperties method</span></span>

<span data-ttu-id="834fa-104">Ruft die Eigenschaften der Ansicht ab.</span><span class="sxs-lookup"><span data-stu-id="834fa-104">Gets the properties of the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="834fa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="834fa-105">Syntax</span></span>


```C++
HRESULT GetViewTypeProperties(
  [in]  PCUITEMID_CHILD pidl,
  [out] DWORD           *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="834fa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="834fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="834fa-107">*pidl* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="834fa-107">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="834fa-108">Typ: **PCUITEMID \_ CHILD**</span><span class="sxs-lookup"><span data-stu-id="834fa-108">Type: **PCUITEMID\_CHILD**</span></span>

<span data-ttu-id="834fa-109">EINE PIDL.</span><span class="sxs-lookup"><span data-stu-id="834fa-109">A PIDL.</span></span>

</dd> <dt>

<span data-ttu-id="834fa-110">*pdwFlags* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="834fa-110">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="834fa-111">Typ: **DWORD \***</span><span class="sxs-lookup"><span data-stu-id="834fa-111">Type: **DWORD\***</span></span>

<span data-ttu-id="834fa-112">Ein Zeiger auf eine ganzzahlige Variable ohne Vorzeichen, die die Ansichtseigenschaften empfängt, die angeben, was bei Auswahl der Ansicht zu tun ist.</span><span class="sxs-lookup"><span data-stu-id="834fa-112">A pointer to an unsigned integer variable that receives the view properties, which indicate what to do when the view is selected.</span></span> <span data-ttu-id="834fa-113">Flags können eine beliebige Kombination der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="834fa-113">Flags may be any combination of the following values.</span></span>

<dt>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>

<span data-ttu-id="834fa-114"><span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>**SFVTFLAG \_ NOTIFY \_ CREATE** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="834fa-114"><span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>**SFVTFLAG\_NOTIFY\_CREATE** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="834fa-115">Erstellen Sie ein Ansichtselement, falls es nicht dort ist.</span><span class="sxs-lookup"><span data-stu-id="834fa-115">Create view item if not there.</span></span>

</dd> <dt>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>

<span data-ttu-id="834fa-116"><span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG \_ NOTIFY \_ RESORT** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="834fa-116"><span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG\_NOTIFY\_RESORT** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="834fa-117">Erneutes Einreihen von PIDL und neu sortieren.</span><span class="sxs-lookup"><span data-stu-id="834fa-117">Reinsert PIDL and re-sort.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="834fa-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="834fa-118">Return value</span></span>

<span data-ttu-id="834fa-119">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="834fa-119">Type: **HRESULT**</span></span>

<span data-ttu-id="834fa-120">Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="834fa-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="834fa-121">Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="834fa-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="834fa-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="834fa-122">Requirements</span></span>



| <span data-ttu-id="834fa-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="834fa-123">Requirement</span></span> | <span data-ttu-id="834fa-124">Wert</span><span class="sxs-lookup"><span data-stu-id="834fa-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="834fa-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="834fa-125">Minimum supported client</span></span><br/> | <span data-ttu-id="834fa-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="834fa-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="834fa-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="834fa-127">Minimum supported server</span></span><br/> | <span data-ttu-id="834fa-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="834fa-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="834fa-129">DLL</span><span class="sxs-lookup"><span data-stu-id="834fa-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="834fa-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="834fa-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




