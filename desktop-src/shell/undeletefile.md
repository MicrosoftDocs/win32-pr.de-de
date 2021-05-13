---
description: Gibt eine anwendungsdefinierte Rückruffunktion an, die vom Datei-Manager aufgerufen wird, wenn der Benutzer im Menü Datei den Befehl Undelete ausgibt.
title: FM_UNDELETE_PROC Funktionszeiger (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_UNDELETE_PROC
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 456b053e-e83d-43af-9691-57e1d4fd3f8f
ms.openlocfilehash: b7549b521c241429f1c5c7edb7f83eadf25f5d37
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842421"
---
# <a name="fm_undelete_proc-function-pointer"></a><span data-ttu-id="68de2-103">FM \_ UNDELETE \_ PROC-Funktionszeiger</span><span class="sxs-lookup"><span data-stu-id="68de2-103">FM\_UNDELETE\_PROC function pointer</span></span>

<span data-ttu-id="68de2-104">Gibt eine anwendungsdefinierte Rückruffunktion an, die vom Datei-Manager aufgerufen wird, wenn der Benutzer im Menü **Datei** den Befehl **Wiederherstellen** ausgibt.</span><span class="sxs-lookup"><span data-stu-id="68de2-104">Specifies an application-defined callback function called by File Manager when the user chooses the **Undelete** command from the **File** menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="68de2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="68de2-105">Syntax</span></span>


```C++
typedef DWORD ( APIENTRY *FM_UNDELETE_PROC)(
   HWND  hwndOwner,
   LPSTR lpszDir
);
```



## <a name="parameters"></a><span data-ttu-id="68de2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="68de2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68de2-107">*hwndOwner*</span><span class="sxs-lookup"><span data-stu-id="68de2-107">*hwndOwner*</span></span> 
</dt> <dd>

<span data-ttu-id="68de2-108">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="68de2-108">Type: **HWND**</span></span>

<span data-ttu-id="68de2-109">Das Fensterhandle für den Datei-Manager.</span><span class="sxs-lookup"><span data-stu-id="68de2-109">The window handle to File Manager.</span></span> <span data-ttu-id="68de2-110">Eine wiederherstellende DLL sollte dieses Handle verwenden, um das Besitzerfenster für jedes Dialogfeld oder Meldungsfeld anzugeben, das die DLL möglicherweise anzeigt.</span><span class="sxs-lookup"><span data-stu-id="68de2-110">An undelete DLL should use this handle to specify the owner window for any dialog box or message box the DLL might display.</span></span>

</dd> <dt>

<span data-ttu-id="68de2-111">*lpszDir*</span><span class="sxs-lookup"><span data-stu-id="68de2-111">*lpszDir*</span></span> 
</dt> <dd>

<span data-ttu-id="68de2-112">Typ: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="68de2-112">Type: **LPSTR**</span></span>

<span data-ttu-id="68de2-113">Die Adresse einer auf NULL endende Zeichenfolge, die den Namen des ursprünglichen Verzeichnisses enthält.</span><span class="sxs-lookup"><span data-stu-id="68de2-113">The address of a null-terminated string that contains the name of the initial directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68de2-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68de2-114">Return value</span></span>

<span data-ttu-id="68de2-115">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="68de2-115">Type: **DWORD**</span></span>

<span data-ttu-id="68de2-116">Gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="68de2-116">Returns one of the following values.</span></span>



| <span data-ttu-id="68de2-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="68de2-117">Return code</span></span>                                                                             | <span data-ttu-id="68de2-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68de2-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="68de2-119"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="68de2-119"><dt>**-1**</dt></span></span> </dl>       | <span data-ttu-id="68de2-120">Ein Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="68de2-120">An error occurred.</span></span><br/>                                      |
| <dl> <span data-ttu-id="68de2-121"><dt>**IDOK**</dt></span><span class="sxs-lookup"><span data-stu-id="68de2-121"><dt>**IDOK**</dt></span></span> </dl>     | <span data-ttu-id="68de2-122">Eine Datei wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="68de2-122">A file was undeleted.</span></span> <span data-ttu-id="68de2-123">Der Datei-Manager bemalt das Fenster neu.</span><span class="sxs-lookup"><span data-stu-id="68de2-123">File Manager repaints its window.</span></span><br/> |
| <dl> <span data-ttu-id="68de2-124"><dt>**IDCANCEL**</dt></span><span class="sxs-lookup"><span data-stu-id="68de2-124"><dt>**IDCANCEL**</dt></span></span> </dl> | <span data-ttu-id="68de2-125">Es wurde keine Datei gelöscht.</span><span class="sxs-lookup"><span data-stu-id="68de2-125">No file was undeleted.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="68de2-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68de2-126">Requirements</span></span>



| <span data-ttu-id="68de2-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68de2-127">Requirement</span></span> | <span data-ttu-id="68de2-128">Wert</span><span class="sxs-lookup"><span data-stu-id="68de2-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68de2-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68de2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="68de2-130">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68de2-130">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="68de2-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68de2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="68de2-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68de2-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="68de2-133">Header</span><span class="sxs-lookup"><span data-stu-id="68de2-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="68de2-134"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="68de2-134"><dt>Wfext.h</dt></span></span> </dl> |



 

 




