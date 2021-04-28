---
title: WebViewFolderContents.PopupItemMenu-Methode (Shldisp.h)
description: 'WebViewFolderContents.PopupItemMenu-Methode: Erstellt ein Kontextmenü für das angegebene Element und gibt die ausgewählte Befehlszeichenfolge zurück.'
ms.assetid: 3c07500c-2fe9-4976-a1a8-b128e75f9325
keywords:
- PopupItemMenu-Methode Legacy-Windows-Umgebungsfeatures
- PopupItemMenu-Methode Legacy-Windows-Umgebungsfeatures , WebViewFolderContents-Objekt
- WebViewFolderContents-Objekt Legacy-Windows-Umgebungsfeatures , PopupItemMenu-Methode
topic_type:
- apiref
api_name:
- WebViewFolderContents.PopupItemMenu
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c879e10097b334f0c2d4f98b1b76289d20ee4a93
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102638"
---
# <a name="webviewfoldercontentspopupitemmenu-method"></a><span data-ttu-id="2c54a-106">WebViewFolderContents.PopupItemMenu-Methode</span><span class="sxs-lookup"><span data-stu-id="2c54a-106">WebViewFolderContents.PopupItemMenu method</span></span>

<span data-ttu-id="2c54a-107">Erstellt ein Kontextmenü für das angegebene Element und gibt die ausgewählte Befehlszeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="2c54a-107">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c54a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c54a-108">Syntax</span></span>


```JScript
retVal = WebViewFolderContents.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="2c54a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c54a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c54a-110">*vItem* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2c54a-110">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c54a-111">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="2c54a-111">Type: **Variant**</span></span>

<span data-ttu-id="2c54a-112">Das [**FolderItem-Objekt,**](../shell/folderitem.md) für das das Kontextmenü erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2c54a-112">The [**FolderItem**](../shell/folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="2c54a-113">*vx* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="2c54a-113">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2c54a-114">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="2c54a-114">Type: **Variant**</span></span>

<span data-ttu-id="2c54a-115">Die horizontale Position des Menüs in Bildschirmkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="2c54a-115">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="2c54a-116">*vy* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="2c54a-116">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2c54a-117">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="2c54a-117">Type: **Variant**</span></span>

<span data-ttu-id="2c54a-118">Die vertikale Position des Menüs in Bildschirmkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="2c54a-118">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c54a-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c54a-119">Return value</span></span>

<span data-ttu-id="2c54a-120">Typ: **[BSTR](/previous-versions/windows/desktop/automat/bstr)\***</span><span class="sxs-lookup"><span data-stu-id="2c54a-120">Type: **[BSTR](/previous-versions/windows/desktop/automat/bstr)\***</span></span>

<span data-ttu-id="2c54a-121">Diese Methode gibt die Befehlszeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="2c54a-121">When this method returns, contains the command string.</span></span>

## <a name="examples"></a><span data-ttu-id="2c54a-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c54a-122">Examples</span></span>

<span data-ttu-id="2c54a-123">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung von **PopupItemMenu** für JScript, das in HTML eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="2c54a-123">The following example shows the proper use of **PopupItemMenu** for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsPopupItemMenuJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            var szCommand;

            szCommand = FileList.PopupItemMenu(objFolderItem);
        }
    }
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="2c54a-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c54a-124">Requirements</span></span>



| <span data-ttu-id="2c54a-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c54a-125">Requirement</span></span> | <span data-ttu-id="2c54a-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2c54a-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c54a-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c54a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2c54a-128">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c54a-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2c54a-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c54a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2c54a-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c54a-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2c54a-131">Header</span><span class="sxs-lookup"><span data-stu-id="2c54a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c54a-132"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="2c54a-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2c54a-133">Idl</span><span class="sxs-lookup"><span data-stu-id="2c54a-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2c54a-134"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="2c54a-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2c54a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2c54a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c54a-136"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="2c54a-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

