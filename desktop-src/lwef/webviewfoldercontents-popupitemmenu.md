---
title: Webviewfoldercontents. popupitemmenu-Methode (Shldisp. h)
description: Erstellt ein Kontextmenü für das angegebene Element und gibt die ausgewählte Befehls Zeichenfolge zurück.
ms.assetid: 3c07500c-2fe9-4976-a1a8-b128e75f9325
keywords:
- Popupitemmenu-Methode Legacy-Windows-Umgebungs Features
- Popupitemmenu-Methode Legacy-Windows-Umgebungs Funktionen, webviewfoldercontents-Objekt
- Webviewfoldercontents-Objekt Legacy Funktionen der Windows-Umgebung, Methode "popupitemmenu"
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
ms.openlocfilehash: 41753814f103998185acc798a37447f22356d2aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740128"
---
# <a name="webviewfoldercontentspopupitemmenu-method"></a><span data-ttu-id="7232f-106">Webviewfoldercontents. popupitemmenu-Methode</span><span class="sxs-lookup"><span data-stu-id="7232f-106">WebViewFolderContents.PopupItemMenu method</span></span>

<span data-ttu-id="7232f-107">Erstellt ein Kontextmenü für das angegebene Element und gibt die ausgewählte Befehls Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="7232f-107">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="7232f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7232f-108">Syntax</span></span>


```JScript
retVal = WebViewFolderContents.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="7232f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7232f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7232f-110">*vitem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7232f-110">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7232f-111">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="7232f-111">Type: **Variant**</span></span>

<span data-ttu-id="7232f-112">Das [**folderItem**](../shell/folderitem.md) -Objekt, für das das Kontextmenü erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7232f-112">The [**FolderItem**](../shell/folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="7232f-113">*VX* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="7232f-113">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7232f-114">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="7232f-114">Type: **Variant**</span></span>

<span data-ttu-id="7232f-115">Die horizontale Position des Menüs in Bildschirm Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="7232f-115">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="7232f-116">*Vy* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="7232f-116">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7232f-117">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="7232f-117">Type: **Variant**</span></span>

<span data-ttu-id="7232f-118">Die vertikale Position des Menüs in Bildschirm Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="7232f-118">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7232f-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7232f-119">Return value</span></span>

<span data-ttu-id="7232f-120">Geben Sie Folgendes ein: \**[BSTR](/previous-versions/windows/desktop/automat/bstr) \** _</span><span class="sxs-lookup"><span data-stu-id="7232f-120">Type: \**[BSTR](/previous-versions/windows/desktop/automat/bstr)\** _</span></span>

<span data-ttu-id="7232f-121">Wenn diese Methode zurückgegeben wird, enthält Sie die Befehls Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="7232f-121">When this method returns, contains the command string.</span></span>

## <a name="examples"></a><span data-ttu-id="7232f-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7232f-122">Examples</span></span>

<span data-ttu-id="7232f-123">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung von _ *popupitemmenu*\* für JScript Embedded in HTML.</span><span class="sxs-lookup"><span data-stu-id="7232f-123">The following example shows the proper use of _ *PopupItemMenu*\* for JScript embedded in HTML.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="7232f-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7232f-124">Requirements</span></span>



| <span data-ttu-id="7232f-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7232f-125">Requirement</span></span> | <span data-ttu-id="7232f-126">Wert</span><span class="sxs-lookup"><span data-stu-id="7232f-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7232f-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7232f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7232f-128">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7232f-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7232f-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7232f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7232f-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7232f-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7232f-131">Header</span><span class="sxs-lookup"><span data-stu-id="7232f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7232f-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7232f-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7232f-133">IDL</span><span class="sxs-lookup"><span data-stu-id="7232f-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7232f-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7232f-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7232f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="7232f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7232f-136"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="7232f-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

