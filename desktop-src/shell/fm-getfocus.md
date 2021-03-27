---
description: Wird von einer Datei-Manager-Erweiterung gesendet, um den Typ des Datei-Manager-Fensters abzurufen, das den Eingabefokus besitzt.
title: FM_GETFOCUS Meldung (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFOCUS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: e2d5f825-5678-4dd7-adad-eec1cbcc7e49
ms.openlocfilehash: af6e0894b3734f976302eacbf0575a017f054f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979736"
---
# <a name="fm_getfocus-message"></a><span data-ttu-id="7517b-103">FM \_ GetFocus-Nachricht</span><span class="sxs-lookup"><span data-stu-id="7517b-103">FM\_GETFOCUS message</span></span>

<span data-ttu-id="7517b-104">Wird von einer Datei-Manager-Erweiterung gesendet, um den Typ des Datei-Manager-Fensters abzurufen, das den Eingabefokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="7517b-104">Sent by a File Manager extension to retrieve the type of File Manager window that has the input focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="7517b-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="7517b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7517b-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7517b-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7517b-107">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="7517b-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7517b-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7517b-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7517b-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="7517b-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7517b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7517b-110">Return value</span></span>

<span data-ttu-id="7517b-111">Gibt den Typ des Datei-Manager-Fensters zurück, das den Eingabefokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="7517b-111">Returns the type of File Manager window that has the input focus.</span></span> <span data-ttu-id="7517b-112">Dieses Argument einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="7517b-112">It can be one of the following values.</span></span>



| <span data-ttu-id="7517b-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7517b-113">Return code</span></span>                                                                                    | <span data-ttu-id="7517b-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7517b-114">Description</span></span>                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="7517b-115"><dt>**fmfocus- \_ dir**</dt></span><span class="sxs-lookup"><span data-stu-id="7517b-115"><dt>**FMFOCUS\_DIR**</dt></span></span> </dl>    | <span data-ttu-id="7517b-116">Verzeichnis Teil eines Verzeichnis Fensters.</span><span class="sxs-lookup"><span data-stu-id="7517b-116">Directory portion of a directory window.</span></span><br/> |
| <dl> <span data-ttu-id="7517b-117"><dt>**fmfocus \_ -Struktur**</dt></span><span class="sxs-lookup"><span data-stu-id="7517b-117"><dt>**FMFOCUS\_TREE**</dt></span></span> </dl>   | <span data-ttu-id="7517b-118">Struktur Teil eines Verzeichnis Fensters.</span><span class="sxs-lookup"><span data-stu-id="7517b-118">Tree portion of a directory window.</span></span><br/>      |
| <dl> <span data-ttu-id="7517b-119"><dt>**fmfocus- \_ Laufwerke**</dt></span><span class="sxs-lookup"><span data-stu-id="7517b-119"><dt>**FMFOCUS\_DRIVES**</dt></span></span> </dl> | <span data-ttu-id="7517b-120">Laufwerk Leiste eines Verzeichnis Fensters.</span><span class="sxs-lookup"><span data-stu-id="7517b-120">Drive bar of a directory window.</span></span><br/>         |
| <dl> <span data-ttu-id="7517b-121"><dt>**fmfocus- \_ Suche**</dt></span><span class="sxs-lookup"><span data-stu-id="7517b-121"><dt>**FMFOCUS\_SEARCH**</dt></span></span> </dl> | <span data-ttu-id="7517b-122">Fenster "Suchergebnisse".</span><span class="sxs-lookup"><span data-stu-id="7517b-122">Search Results window.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="7517b-123">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7517b-123">Requirements</span></span>



| <span data-ttu-id="7517b-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7517b-124">Requirement</span></span> | <span data-ttu-id="7517b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="7517b-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7517b-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7517b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7517b-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7517b-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="7517b-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7517b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7517b-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7517b-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7517b-130">Header</span><span class="sxs-lookup"><span data-stu-id="7517b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7517b-131"><dt>WF. h</dt></span><span class="sxs-lookup"><span data-stu-id="7517b-131"><dt>Wfext.h</dt></span></span> </dl> |



 

 




