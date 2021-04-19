---
description: Von der sfcgetfiles-Funktion verwendete Struktur.
ms.assetid: 958167e3-3eb3-406a-85bf-ffe2851a95a1
title: PPROTECT_FILE_ENTRY Struktur (sfcfiles. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PPROTECT_FILE_ENTRY
api_type:
- HeaderDef
api_location:
- Sfcfiles.h
ms.openlocfilehash: 98cda570a3677560d51800d58822d93a942847c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349252"
---
# <a name="pprotect_file_entry-structure"></a><span data-ttu-id="bdb3a-103">Pprotect- \_ Datei \_ Eintrags Struktur</span><span class="sxs-lookup"><span data-stu-id="bdb3a-103">PPROTECT\_FILE\_ENTRY structure</span></span>

<span data-ttu-id="bdb3a-104">\[Diese Struktur steht für die Verwendung in den Betriebssystemen zur Verfügung, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="bdb3a-104">\[This structure is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bdb3a-105">Die Unterstützung für diese Struktur wurde in Windows Vista und Windows Server 2008 entfernt.</span><span class="sxs-lookup"><span data-stu-id="bdb3a-105">Support for this structure was removed in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="bdb3a-106">Verwenden Sie stattdessen die in [WRP-Funktionen](wfp-functions.md) aufgeführten unterstützten Funktionen.\]</span><span class="sxs-lookup"><span data-stu-id="bdb3a-106">Use the supported functions listed in [WRP Functions](wfp-functions.md) instead.\]</span></span>

<span data-ttu-id="bdb3a-107">Von der [**sfcgetfiles**](sfcgetfiles.md) -Funktion verwendete Struktur.</span><span class="sxs-lookup"><span data-stu-id="bdb3a-107">Structure used by the [**SfcGetFiles**](sfcgetfiles.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdb3a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdb3a-108">Syntax</span></span>


```C++
typedef struct _PPROTECT_FILE_ENTRY {
  PWSTR SourceFileName;
  PWSTR FileName;
  PWSTR InfName;
} PPROTECT_FILE_ENTRY, *PPPROTECT_FILE_ENTRY;
```



## <a name="members"></a><span data-ttu-id="bdb3a-109">Member</span><span class="sxs-lookup"><span data-stu-id="bdb3a-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="bdb3a-110">**SourceFileName**</span><span class="sxs-lookup"><span data-stu-id="bdb3a-110">**SourceFileName**</span></span>
</dt> <dd>

<span data-ttu-id="bdb3a-111">Ein Zeiger auf einen Zeichen folgen Wert, der den Dateinamen der Quelldatei enthält.</span><span class="sxs-lookup"><span data-stu-id="bdb3a-111">Pointer to a string value containing the filename of the source file.</span></span> <span data-ttu-id="bdb3a-112">Dieser Wert ist **null** , wenn die Datei bei der Installation nicht umbenannt wird.</span><span class="sxs-lookup"><span data-stu-id="bdb3a-112">This will be **NULL** if the file is not renamed on installation.</span></span>

</dd> <dt>

<span data-ttu-id="bdb3a-113">**FileName**</span><span class="sxs-lookup"><span data-stu-id="bdb3a-113">**FileName**</span></span>
</dt> <dd>

<span data-ttu-id="bdb3a-114">Ein Zeiger auf einen Zeichen folgen Wert, der den Ziel Dateinamen sowie den vollständigen Pfad zur Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="bdb3a-114">Pointer to string value containing the destination filename plus the full path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="bdb3a-115">**InfName**</span><span class="sxs-lookup"><span data-stu-id="bdb3a-115">**InfName**</span></span>
</dt> <dd>

<span data-ttu-id="bdb3a-116">Ein Zeiger auf einen Zeichen folgen Wert, der den Dateinamen der INF-Datei mit Layoutinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="bdb3a-116">Pointer to string value containing the filename of the INF file which provides layout information.</span></span> <span data-ttu-id="bdb3a-117">Dieser Parameter kann **null** sein, wenn das Standardlayout verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bdb3a-117">This parameter may be **NULL** when using the default layout.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bdb3a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bdb3a-118">Requirements</span></span>



| <span data-ttu-id="bdb3a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bdb3a-119">Requirement</span></span> | <span data-ttu-id="bdb3a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="bdb3a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bdb3a-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bdb3a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bdb3a-122">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bdb3a-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bdb3a-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bdb3a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bdb3a-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bdb3a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bdb3a-125">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="bdb3a-125">End of client support</span></span><br/>    | <span data-ttu-id="bdb3a-126">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bdb3a-126">Windows XP</span></span><br/>                                                                 |
| <span data-ttu-id="bdb3a-127">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="bdb3a-127">End of server support</span></span><br/>    | <span data-ttu-id="bdb3a-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bdb3a-128">Windows Server 2003</span></span><br/>                                                        |
| <span data-ttu-id="bdb3a-129">Header</span><span class="sxs-lookup"><span data-stu-id="bdb3a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdb3a-130"><dt>Sfcfiles. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdb3a-130"><dt>Sfcfiles.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdb3a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdb3a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdb3a-132">**Sfcgetfiles**</span><span class="sxs-lookup"><span data-stu-id="bdb3a-132">**SfcGetFiles**</span></span>](sfcgetfiles.md)
</dt> </dl>

 

 




