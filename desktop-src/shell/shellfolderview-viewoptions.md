---
description: Ruft einen Satz von Flags ab, die die aktuellen Optionen der Ansicht angeben.
ms.assetid: 83a17033-bd7f-44de-a0c8-460d12c4825d
title: Shellfolderview. viewoptions-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.ViewOptions
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e336034e7d5037b8037c6fd0ef549fe5f87da312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994991"
---
# <a name="shellfolderviewviewoptions-property"></a><span data-ttu-id="94a9c-103">Shellfolderview. viewoptions (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="94a9c-103">ShellFolderView.ViewOptions property</span></span>

<span data-ttu-id="94a9c-104">Ruft einen Satz von Flags ab, die die aktuellen Optionen der Ansicht angeben.</span><span class="sxs-lookup"><span data-stu-id="94a9c-104">Gets a set of flags that indicate the current options of the view.</span></span>

<span data-ttu-id="94a9c-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="94a9c-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="94a9c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="94a9c-106">Syntax</span></span>


```JScript
objViewOptions = ShellFolderView.ViewOptions
```



## <a name="property-value"></a><span data-ttu-id="94a9c-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="94a9c-107">Property value</span></span>

<span data-ttu-id="94a9c-108">Eine Variable vom Typ [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , die das Ansichts Options Objekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="94a9c-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the view options object.</span></span> <span data-ttu-id="94a9c-109">Enthält einen oder mehrere der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="94a9c-109">Contains one or more of the following values:</span></span>

<dt>

<span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>

<span data-ttu-id="94a9c-110"><span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>**Sfvvo \_ Showallobjects** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="94a9c-110"><span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>**SFVVO\_SHOWALLOBJECTS** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="94a9c-111">Die Option **alle Dateien anzeigen** ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="94a9c-111">The **Show All Files** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>

<span data-ttu-id="94a9c-112"><span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>**Sfvvo \_ Showextensions** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="94a9c-112"><span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>**SFVVO\_SHOWEXTENSIONS** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="94a9c-113">Die Option **Erweiterungen für bekannte Dateitypen ausblenden** ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="94a9c-113">The **Hide extensions for known file types** option is disabled.</span></span>

</dd> <dt>

<span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>

<span data-ttu-id="94a9c-114"><span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>**Sfvvo \_ Showcompcolor** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="94a9c-114"><span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>**SFVVO\_SHOWCOMPCOLOR** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="94a9c-115">Die Option **komprimierte Dateien und Ordner mit alternativer Farbe anzeigen** ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="94a9c-115">The **Display Compressed Files and Folders with Alternate Color** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>

<span data-ttu-id="94a9c-116"><span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>**Sfvvo \_ Showsysfiles** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="94a9c-116"><span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>**SFVVO\_SHOWSYSFILES** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="94a9c-117">Die Option Ausgeblendete **Dateien nicht anzeigen** ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="94a9c-117">The **Do Not Show Hidden Files** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>

<span data-ttu-id="94a9c-118"><span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>**Sfvvo \_ WIN95CLASSIC** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="94a9c-118"><span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>**SFVVO\_WIN95CLASSIC** (0x00000040)</span></span>


</dt> <dd>

<span data-ttu-id="94a9c-119">Die Option für den **klassischen Stil** ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="94a9c-119">The **Classic Style** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>

<span data-ttu-id="94a9c-120"><span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>**Sfvvo \_ Doubleclickinwebview** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="94a9c-120"><span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>**SFVVO\_DOUBLECLICKINWEBVIEW** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="94a9c-121">Das **doppelklicken, um eine Element Option zu öffnen,** ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="94a9c-121">The **Double-Click to Open an Item** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>

<span data-ttu-id="94a9c-122"><span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>**Sfvvo \_ Desktophtml** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="94a9c-122"><span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>**SFVVO\_DESKTOPHTML** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="94a9c-123">Die Option **Active Desktop – View as Web Page** ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="94a9c-123">The **Active Desktop – View as Web Page** option is enabled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94a9c-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94a9c-124">Remarks</span></span>

<span data-ttu-id="94a9c-125">[**FocusedItem**](shellfolderview-focuseditem.md) kann nur auf dem lokalen System aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="94a9c-125">[**FocusedItem**](shellfolderview-focuseditem.md) can only be called on the local system.</span></span> <span data-ttu-id="94a9c-126">Es funktioniert nicht, wenn es auf einer Webseite über HTTP oder UNC ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="94a9c-126">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="94a9c-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="94a9c-127">Examples</span></span>

<span data-ttu-id="94a9c-128">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode in JScript Embedded in HTML.</span><span class="sxs-lookup"><span data-stu-id="94a9c-128">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewViewOptionsJ()
    {
        var objOptions;
        
        objOptions = WebOC.Document.ViewOptions;
        if (objOptions != null)
        {
            alert(objOptions);
        }
    }
    
    function fnLoad()
    {
        var webOC;
        
        webOC = document.all("WebOC");
        webOC.Navigate("C:\\");
    }
</script>

</head>
<body onload="fnLoad()">
<object id="WebOC"
        classid="clsid:8856F961-340A-11D0-A96B-00C04FD705A2"
        width=400
        height=400>
</object>
<br><br>
<INPUT id=ViewOptions 
       type=button 
       value=ViewOptions 
       name=ViewOptions 
       onclick="fnShellFolderViewViewOptionsJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="94a9c-129">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="94a9c-129">Requirements</span></span>



| <span data-ttu-id="94a9c-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94a9c-130">Requirement</span></span> | <span data-ttu-id="94a9c-131">Wert</span><span class="sxs-lookup"><span data-stu-id="94a9c-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94a9c-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94a9c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="94a9c-133">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94a9c-133">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="94a9c-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94a9c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="94a9c-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94a9c-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="94a9c-136">Header</span><span class="sxs-lookup"><span data-stu-id="94a9c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="94a9c-137"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="94a9c-137"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="94a9c-138">IDL</span><span class="sxs-lookup"><span data-stu-id="94a9c-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="94a9c-139"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="94a9c-139"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="94a9c-140">DLL</span><span class="sxs-lookup"><span data-stu-id="94a9c-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94a9c-141"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="94a9c-141"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
