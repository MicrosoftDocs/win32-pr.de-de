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
ms.openlocfilehash: 7a2feda23d6e1759e1c0be27805fefbb6b592df7
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840751"
---
# <a name="shellfolderviewpopupitemmenu-method"></a><span data-ttu-id="1c7fe-103">ShellFolderView.PopupItemMenu-Methode</span><span class="sxs-lookup"><span data-stu-id="1c7fe-103">ShellFolderView.PopupItemMenu method</span></span>

<span data-ttu-id="1c7fe-104">Erstellt ein Kontextmenü für das angegebene Element und gibt die ausgewählte Befehlszeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="1c7fe-104">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c7fe-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c7fe-105">Syntax</span></span>


```JScript
retVal = ShellFolderView.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="1c7fe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c7fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c7fe-107">*vItem* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1c7fe-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c7fe-108">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="1c7fe-108">Type: **Variant**</span></span>

<span data-ttu-id="1c7fe-109">Das [**FolderItem-Objekt,**](folderitem.md) für das das Kontextmenü erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1c7fe-109">The [**FolderItem**](folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="1c7fe-110">*vx* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="1c7fe-110">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1c7fe-111">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="1c7fe-111">Type: **Variant**</span></span>

<span data-ttu-id="1c7fe-112">Die horizontale Position des Menüs in Bildschirmkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="1c7fe-112">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="1c7fe-113">*vy* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="1c7fe-113">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1c7fe-114">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="1c7fe-114">Type: **Variant**</span></span>

<span data-ttu-id="1c7fe-115">Die vertikale Position des Menüs in Bildschirmkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="1c7fe-115">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c7fe-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c7fe-116">Return value</span></span>

<span data-ttu-id="1c7fe-117">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)\***</span><span class="sxs-lookup"><span data-stu-id="1c7fe-117">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)\***</span></span>

<span data-ttu-id="1c7fe-118">Die **Zeichenfolge,** die die Befehlszeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="1c7fe-118">The **String** that receives the command string.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c7fe-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c7fe-119">Requirements</span></span>



| <span data-ttu-id="1c7fe-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c7fe-120">Requirement</span></span> | <span data-ttu-id="1c7fe-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1c7fe-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c7fe-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1c7fe-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1c7fe-123">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c7fe-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1c7fe-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1c7fe-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1c7fe-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c7fe-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1c7fe-126">Header</span><span class="sxs-lookup"><span data-stu-id="1c7fe-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c7fe-127"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="1c7fe-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="1c7fe-128">Idl</span><span class="sxs-lookup"><span data-stu-id="1c7fe-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1c7fe-129"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="1c7fe-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="1c7fe-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1c7fe-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c7fe-131"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="1c7fe-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
