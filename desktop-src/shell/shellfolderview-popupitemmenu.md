---
description: Erstellt ein Kontextmenü für das angegebene Element und gibt die ausgewählte Befehls Zeichenfolge zurück.
title: Shellfolderview. popupitemmenu-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.PopupItemMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 1610d91e-87c3-4ba5-9147-1595eddb2c3a
ms.openlocfilehash: 513f654442361da840cb02089810c814275c5867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217692"
---
# <a name="shellfolderviewpopupitemmenu-method"></a><span data-ttu-id="141c6-103">Shellfolderview. popupitemmenu-Methode</span><span class="sxs-lookup"><span data-stu-id="141c6-103">ShellFolderView.PopupItemMenu method</span></span>

<span data-ttu-id="141c6-104">Erstellt ein Kontextmenü für das angegebene Element und gibt die ausgewählte Befehls Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="141c6-104">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="141c6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="141c6-105">Syntax</span></span>


```JScript
retVal = ShellFolderView.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="141c6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="141c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="141c6-107">*vitem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="141c6-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="141c6-108">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="141c6-108">Type: **Variant**</span></span>

<span data-ttu-id="141c6-109">Das [**folderItem**](folderitem.md) -Objekt, für das das Kontextmenü erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="141c6-109">The [**FolderItem**](folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="141c6-110">*VX* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="141c6-110">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="141c6-111">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="141c6-111">Type: **Variant**</span></span>

<span data-ttu-id="141c6-112">Die horizontale Position des Menüs in Bildschirm Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="141c6-112">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="141c6-113">*Vy* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="141c6-113">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="141c6-114">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="141c6-114">Type: **Variant**</span></span>

<span data-ttu-id="141c6-115">Die vertikale Position des Menüs in Bildschirm Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="141c6-115">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="141c6-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="141c6-116">Return value</span></span>

<span data-ttu-id="141c6-117">Geben Sie Folgendes ein: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr) \** _</span><span class="sxs-lookup"><span data-stu-id="141c6-117">Type: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr)\** _</span></span>

<span data-ttu-id="141c6-118">Die _ \*String\*\*, die die Befehls Zeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="141c6-118">The _ *String*\* that receives the command string.</span></span>

## <a name="requirements"></a><span data-ttu-id="141c6-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="141c6-119">Requirements</span></span>



| <span data-ttu-id="141c6-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="141c6-120">Requirement</span></span> | <span data-ttu-id="141c6-121">Wert</span><span class="sxs-lookup"><span data-stu-id="141c6-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="141c6-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="141c6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="141c6-123">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="141c6-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="141c6-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="141c6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="141c6-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="141c6-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="141c6-126">Header</span><span class="sxs-lookup"><span data-stu-id="141c6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="141c6-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="141c6-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="141c6-128">IDL</span><span class="sxs-lookup"><span data-stu-id="141c6-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="141c6-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="141c6-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="141c6-130">DLL</span><span class="sxs-lookup"><span data-stu-id="141c6-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="141c6-131"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="141c6-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
