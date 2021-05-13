---
description: Wird von einer Datei-Manager-Erweiterung gesendet, um den Typ des Datei-Manager-Fensters abzurufen, das den Eingabefokus besitzt.
title: FM_GETFOCUS (Wfext.h)
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
ms.openlocfilehash: e5f6470ea1217485b401387150cae786b44ccca1
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841411"
---
# <a name="fm_getfocus-message"></a><span data-ttu-id="44eb9-103">FM \_ GETFOCUS-Nachricht</span><span class="sxs-lookup"><span data-stu-id="44eb9-103">FM\_GETFOCUS message</span></span>

<span data-ttu-id="44eb9-104">Wird von einer Datei-Manager-Erweiterung gesendet, um den Typ des Datei-Manager-Fensters abzurufen, das den Eingabefokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="44eb9-104">Sent by a File Manager extension to retrieve the type of File Manager window that has the input focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="44eb9-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="44eb9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44eb9-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="44eb9-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="44eb9-107">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="44eb9-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="44eb9-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="44eb9-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="44eb9-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="44eb9-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44eb9-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44eb9-110">Return value</span></span>

<span data-ttu-id="44eb9-111">Gibt den Typ des Datei-Manager-Fensters zurück, das den Eingabefokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="44eb9-111">Returns the type of File Manager window that has the input focus.</span></span> <span data-ttu-id="44eb9-112">Dieses Argument einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="44eb9-112">It can be one of the following values.</span></span>



| <span data-ttu-id="44eb9-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="44eb9-113">Return code</span></span>                                                                                    | <span data-ttu-id="44eb9-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44eb9-114">Description</span></span>                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="44eb9-115"><dt>**FMFOCUS \_ DIR**</dt></span><span class="sxs-lookup"><span data-stu-id="44eb9-115"><dt>**FMFOCUS\_DIR**</dt></span></span> </dl>    | <span data-ttu-id="44eb9-116">Verzeichnisteil eines Verzeichnisfensters.</span><span class="sxs-lookup"><span data-stu-id="44eb9-116">Directory portion of a directory window.</span></span><br/> |
| <dl> <span data-ttu-id="44eb9-117"><dt>**\_FMFOCUS-STRUKTUR**</dt></span><span class="sxs-lookup"><span data-stu-id="44eb9-117"><dt>**FMFOCUS\_TREE**</dt></span></span> </dl>   | <span data-ttu-id="44eb9-118">Strukturteil eines Verzeichnisfensters.</span><span class="sxs-lookup"><span data-stu-id="44eb9-118">Tree portion of a directory window.</span></span><br/>      |
| <dl> <span data-ttu-id="44eb9-119"><dt>**\_FMFOCUS-LAUFWERKE**</dt></span><span class="sxs-lookup"><span data-stu-id="44eb9-119"><dt>**FMFOCUS\_DRIVES**</dt></span></span> </dl> | <span data-ttu-id="44eb9-120">Die Laufwerkleiste eines Verzeichnisfensters.</span><span class="sxs-lookup"><span data-stu-id="44eb9-120">Drive bar of a directory window.</span></span><br/>         |
| <dl> <span data-ttu-id="44eb9-121"><dt>**\_FMFOCUS-SUCHE**</dt></span><span class="sxs-lookup"><span data-stu-id="44eb9-121"><dt>**FMFOCUS\_SEARCH**</dt></span></span> </dl> | <span data-ttu-id="44eb9-122">Suchergebnisfenster.</span><span class="sxs-lookup"><span data-stu-id="44eb9-122">Search Results window.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="44eb9-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44eb9-123">Requirements</span></span>



| <span data-ttu-id="44eb9-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44eb9-124">Requirement</span></span> | <span data-ttu-id="44eb9-125">Wert</span><span class="sxs-lookup"><span data-stu-id="44eb9-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="44eb9-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44eb9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="44eb9-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44eb9-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="44eb9-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44eb9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="44eb9-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44eb9-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="44eb9-130">Header</span><span class="sxs-lookup"><span data-stu-id="44eb9-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="44eb9-131"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="44eb9-131"><dt>Wfext.h</dt></span></span> </dl> |



 

 




