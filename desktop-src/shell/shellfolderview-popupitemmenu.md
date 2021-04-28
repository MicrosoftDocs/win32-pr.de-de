---
description: 'ShellFolderView.PopupItemMenu-Methode: Erstellt ein Kontextmenü für das angegebene Element und gibt die ausgewählte Befehlszeichenfolge zurück.'
title: ShellFolderView.PopupItemMenu-Methode (Shldisp.h)
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
ms.openlocfilehash: cb862ba159f55d3ab82495ddeb32a87f3ce1901b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083388"
---
# <a name="shellfolderviewpopupitemmenu-method"></a><span data-ttu-id="ced3b-103">ShellFolderView.PopupItemMenu-Methode</span><span class="sxs-lookup"><span data-stu-id="ced3b-103">ShellFolderView.PopupItemMenu method</span></span>

<span data-ttu-id="ced3b-104">Erstellt ein Kontextmenü für das angegebene Element und gibt die ausgewählte Befehlszeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="ced3b-104">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="ced3b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ced3b-105">Syntax</span></span>


```JScript
retVal = ShellFolderView.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="ced3b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ced3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ced3b-107">*vItem* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ced3b-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ced3b-108">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="ced3b-108">Type: **Variant**</span></span>

<span data-ttu-id="ced3b-109">Das [**FolderItem-Objekt,**](folderitem.md) für das das Kontextmenü erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ced3b-109">The [**FolderItem**](folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="ced3b-110">*vx* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ced3b-110">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ced3b-111">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="ced3b-111">Type: **Variant**</span></span>

<span data-ttu-id="ced3b-112">Die horizontale Position des Menüs in Bildschirmkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="ced3b-112">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="ced3b-113">*vy* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ced3b-113">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ced3b-114">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="ced3b-114">Type: **Variant**</span></span>

<span data-ttu-id="ced3b-115">Die vertikale Position des Menüs in Bildschirmkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="ced3b-115">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ced3b-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ced3b-116">Return value</span></span>

<span data-ttu-id="ced3b-117">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)\***</span><span class="sxs-lookup"><span data-stu-id="ced3b-117">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)\***</span></span>

<span data-ttu-id="ced3b-118">Die **Zeichenfolge,** die die Befehlszeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="ced3b-118">The **String** that receives the command string.</span></span>

## <a name="requirements"></a><span data-ttu-id="ced3b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ced3b-119">Requirements</span></span>



| <span data-ttu-id="ced3b-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ced3b-120">Requirement</span></span> | <span data-ttu-id="ced3b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ced3b-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ced3b-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ced3b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ced3b-123">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ced3b-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ced3b-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ced3b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ced3b-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ced3b-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ced3b-126">Header</span><span class="sxs-lookup"><span data-stu-id="ced3b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ced3b-127"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="ced3b-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="ced3b-128">Idl</span><span class="sxs-lookup"><span data-stu-id="ced3b-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ced3b-129"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="ced3b-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="ced3b-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ced3b-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ced3b-131"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="ced3b-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
