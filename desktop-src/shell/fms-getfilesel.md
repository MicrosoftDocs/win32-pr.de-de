---
description: Enthält Informationen zu einer ausgewählten Datei im aktiven Datei-Manager-Fenster (im Verzeichnis Fenster oder im Fenster "Suchergebnisse").
title: FMS_GETFILESEL-Struktur (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d8339f87-ba05-40bf-b7d1-a9de29eb15a4
ms.openlocfilehash: e7ae92350e88e050b1208eed6e08f8faba811fee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958644"
---
# <a name="fms_getfilesel-structure"></a><span data-ttu-id="6761a-103">Fims \_ getfilesel-Struktur</span><span class="sxs-lookup"><span data-stu-id="6761a-103">FMS\_GETFILESEL structure</span></span>

<span data-ttu-id="6761a-104">Enthält Informationen zu einer ausgewählten Datei im aktiven Datei-Manager-Fenster (im Verzeichnis Fenster oder im Fenster "Suchergebnisse").</span><span class="sxs-lookup"><span data-stu-id="6761a-104">Contains information about a selected file in the active File Manager window (the directory window or the Search Results window).</span></span>

## <a name="syntax"></a><span data-ttu-id="6761a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6761a-105">Syntax</span></span>


```C++
typedef struct _FMS_GETFILESEL {
  FILETIME ftTime;
  DWORD    dwSize;
  BYTE     bAttr;
  TCHAR    szName;
} FMS_GETFILESEL;
```



## <a name="members"></a><span data-ttu-id="6761a-106">Member</span><span class="sxs-lookup"><span data-stu-id="6761a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6761a-107">**fttime**</span><span class="sxs-lookup"><span data-stu-id="6761a-107">**ftTime**</span></span>
</dt> <dd>

<span data-ttu-id="6761a-108">Typ: **FILETIME**</span><span class="sxs-lookup"><span data-stu-id="6761a-108">Type: **FILETIME**</span></span>

</dd> <dd>

<span data-ttu-id="6761a-109">Das Datum und die Uhrzeit, zu der die Datei erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6761a-109">The time and date the file was created.</span></span>

</dd> <dt>

<span data-ttu-id="6761a-110">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="6761a-110">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="6761a-111">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="6761a-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="6761a-112">Die Größe der Datei in Bytes.</span><span class="sxs-lookup"><span data-stu-id="6761a-112">The size, in bytes, of the file.</span></span>

</dd> <dt>

<span data-ttu-id="6761a-113">**battr**</span><span class="sxs-lookup"><span data-stu-id="6761a-113">**bAttr**</span></span>
</dt> <dd>

<span data-ttu-id="6761a-114">Type: **Byte**</span><span class="sxs-lookup"><span data-stu-id="6761a-114">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="6761a-115">Die Attribute der Datei.</span><span class="sxs-lookup"><span data-stu-id="6761a-115">The attributes of the file.</span></span>

</dd> <dt>

<span data-ttu-id="6761a-116">**szName**</span><span class="sxs-lookup"><span data-stu-id="6761a-116">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="6761a-117">Typ: **TCHAR**</span><span class="sxs-lookup"><span data-stu-id="6761a-117">Type: **TCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="6761a-118">Der durch Null beendete vollständige Pfad und Dateiname der ausgewählten Datei.</span><span class="sxs-lookup"><span data-stu-id="6761a-118">The null-terminated full path and file name of the selected file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6761a-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="6761a-119">Requirements</span></span>



| <span data-ttu-id="6761a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6761a-120">Requirement</span></span> | <span data-ttu-id="6761a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="6761a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6761a-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6761a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6761a-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6761a-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="6761a-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6761a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6761a-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6761a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6761a-126">Header</span><span class="sxs-lookup"><span data-stu-id="6761a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6761a-127"><dt>WF. h</dt></span><span class="sxs-lookup"><span data-stu-id="6761a-127"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6761a-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6761a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6761a-129">**"F"**</span><span class="sxs-lookup"><span data-stu-id="6761a-129">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




