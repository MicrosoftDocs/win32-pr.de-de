---
description: Gibt eine Anwendungs definierte Rückruffunktion an, die vom Datei-Manager aufgerufen wird, wenn der Benutzer den Befehl "Undelete" aus dem Menü Datei auswählt.
title: FM_UNDELETE_PROC Funktionszeiger (WF. h)
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
ms.openlocfilehash: 3bed8995954cdfe05bcc8eea82dc47415033e205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218057"
---
# <a name="fm_undelete_proc-function-pointer"></a><span data-ttu-id="0e07b-103">FM \_ Undelete \_ proc-Funktionszeiger</span><span class="sxs-lookup"><span data-stu-id="0e07b-103">FM\_UNDELETE\_PROC function pointer</span></span>

<span data-ttu-id="0e07b-104">Gibt eine Anwendungs definierte Rückruffunktion an, die vom Datei-Manager aufgerufen wird, wenn der Benutzer den Befehl " **Undelete** " aus dem Menü **Datei** auswählt.</span><span class="sxs-lookup"><span data-stu-id="0e07b-104">Specifies an application-defined callback function called by File Manager when the user chooses the **Undelete** command from the **File** menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e07b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e07b-105">Syntax</span></span>


```C++
typedef DWORD ( APIENTRY *FM_UNDELETE_PROC)(
   HWND  hwndOwner,
   LPSTR lpszDir
);
```



## <a name="parameters"></a><span data-ttu-id="0e07b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e07b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e07b-107">*hwndOwner*</span><span class="sxs-lookup"><span data-stu-id="0e07b-107">*hwndOwner*</span></span> 
</dt> <dd>

<span data-ttu-id="0e07b-108">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="0e07b-108">Type: **HWND**</span></span>

<span data-ttu-id="0e07b-109">Das Fenster Handle für den Datei-Manager.</span><span class="sxs-lookup"><span data-stu-id="0e07b-109">The window handle to File Manager.</span></span> <span data-ttu-id="0e07b-110">Eine wiederherstellen-dll sollte dieses Handle verwenden, um das Besitzer Fenster für ein beliebiges Dialogfeld oder Meldungs Feld anzugeben, das die dll möglicherweise anzeigt.</span><span class="sxs-lookup"><span data-stu-id="0e07b-110">An undelete DLL should use this handle to specify the owner window for any dialog box or message box the DLL might display.</span></span>

</dd> <dt>

<span data-ttu-id="0e07b-111">*lpszdir*</span><span class="sxs-lookup"><span data-stu-id="0e07b-111">*lpszDir*</span></span> 
</dt> <dd>

<span data-ttu-id="0e07b-112">Typ: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="0e07b-112">Type: **LPSTR**</span></span>

<span data-ttu-id="0e07b-113">Die Adresse einer auf NULL endenden Zeichenfolge, die den Namen des ursprünglichen Verzeichnisses enthält.</span><span class="sxs-lookup"><span data-stu-id="0e07b-113">The address of a null-terminated string that contains the name of the initial directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e07b-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e07b-114">Return value</span></span>

<span data-ttu-id="0e07b-115">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0e07b-115">Type: **DWORD**</span></span>

<span data-ttu-id="0e07b-116">Gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="0e07b-116">Returns one of the following values.</span></span>



| <span data-ttu-id="0e07b-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0e07b-117">Return code</span></span>                                                                             | <span data-ttu-id="0e07b-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e07b-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="0e07b-119"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="0e07b-119"><dt>**-1**</dt></span></span> </dl>       | <span data-ttu-id="0e07b-120">Ein Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="0e07b-120">An error occurred.</span></span><br/>                                      |
| <dl> <span data-ttu-id="0e07b-121"><dt>**IDOK**</dt></span><span class="sxs-lookup"><span data-stu-id="0e07b-121"><dt>**IDOK**</dt></span></span> </dl>     | <span data-ttu-id="0e07b-122">Eine Datei wurde wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="0e07b-122">A file was undeleted.</span></span> <span data-ttu-id="0e07b-123">Das Fenster wird vom Datei-Manager neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0e07b-123">File Manager repaints its window.</span></span><br/> |
| <dl> <span data-ttu-id="0e07b-124"><dt>**IDCANCEL**</dt></span><span class="sxs-lookup"><span data-stu-id="0e07b-124"><dt>**IDCANCEL**</dt></span></span> </dl> | <span data-ttu-id="0e07b-125">Es wurde keine Datei wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="0e07b-125">No file was undeleted.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="0e07b-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0e07b-126">Requirements</span></span>



| <span data-ttu-id="0e07b-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e07b-127">Requirement</span></span> | <span data-ttu-id="0e07b-128">Wert</span><span class="sxs-lookup"><span data-stu-id="0e07b-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0e07b-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0e07b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0e07b-130">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e07b-130">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0e07b-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0e07b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0e07b-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e07b-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0e07b-133">Header</span><span class="sxs-lookup"><span data-stu-id="0e07b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e07b-134"><dt>WF. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e07b-134"><dt>Wfext.h</dt></span></span> </dl> |



 

 




