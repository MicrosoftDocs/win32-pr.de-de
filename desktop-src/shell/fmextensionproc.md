---
description: Gibt eine Anwendungs definierte Rückruffunktion an, die vom Datei-Manager für die Kommunikation mit einer Datei-Manager-Erweiterung aufgerufen wird.
title: Funktion "f mextensionproc" (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMExtensionProc
- FMExtensionProcW
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 6e02d655-f7d8-460a-97d2-5b369493e941
ms.openlocfilehash: 40e18dfe64c6d2b24b982cdf891cbb63b091a7ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993687"
---
# <a name="fmextensionproc-callback-function"></a><span data-ttu-id="30da2-103">Funktion "f mextensionproc"</span><span class="sxs-lookup"><span data-stu-id="30da2-103">FMExtensionProc callback function</span></span>

<span data-ttu-id="30da2-104">Gibt eine Anwendungs definierte Rückruffunktion an, die vom Datei-Manager für die Kommunikation mit einer Datei-Manager-Erweiterung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="30da2-104">Specifies an application-defined callback function called by File Manager to communicate with a File Manager extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="30da2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="30da2-105">Syntax</span></span>


```C++
LONG CALLBACK FMExtensionProc(
   HWND hwnd,
   WORD wMsg,
   LONG lParam
);
```



## <a name="parameters"></a><span data-ttu-id="30da2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="30da2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30da2-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="30da2-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="30da2-108">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="30da2-108">Type: **HWND**</span></span>

<span data-ttu-id="30da2-109">Ein Fenster Handle für den Datei-Manager.</span><span class="sxs-lookup"><span data-stu-id="30da2-109">A window handle to File Manager.</span></span> <span data-ttu-id="30da2-110">Eine Erweiterung verwendet dieses Handle, um das übergeordnete Fenster für ein beliebiges Dialogfeld oder Meldungs Feld anzugeben, das angezeigt werden muss, und zum Senden von Abfrage Nachrichten an den Datei-Manager.</span><span class="sxs-lookup"><span data-stu-id="30da2-110">An extension uses this handle to specify the parent window for any dialog box or message box it must display, and to send query messages to File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="30da2-111">*wmsg*</span><span class="sxs-lookup"><span data-stu-id="30da2-111">*wMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="30da2-112">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="30da2-112">Type: **WORD**</span></span>

<span data-ttu-id="30da2-113">Eine der folgenden Datei-Manager-Meldungen.</span><span class="sxs-lookup"><span data-stu-id="30da2-113">One of the following File Manager messages.</span></span>

<dt>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>

<span data-ttu-id="30da2-114"><span id="1_through_99"></span><span id="1_THROUGH_99"></span>**1 bis 99**</span><span class="sxs-lookup"><span data-stu-id="30da2-114"><span id="1_through_99"></span><span id="1_THROUGH_99"></span>**1 through 99**</span></span>


</dt> <dd>

<span data-ttu-id="30da2-115">Der Benutzer hat ein Element aus dem von der Erweiterung bereitgestellten Menü ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="30da2-115">User selected an item from the extension-supplied menu.</span></span> <span data-ttu-id="30da2-116">Der Wert ist der Bezeichner des ausgewählten Menü Elements.</span><span class="sxs-lookup"><span data-stu-id="30da2-116">The value is the identifier of the selected menu item.</span></span>

</dd> <dt>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>

<span data-ttu-id="30da2-117"><span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**"helpmenuitem" für "f" \_**</span><span class="sxs-lookup"><span data-stu-id="30da2-117"><span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**FMEVENT\_HELPMENUITEM**</span></span>


</dt> <dd>

<span data-ttu-id="30da2-118">Benutzer hat F1 gedrückt, während ein Erweiterungs Menü oder ein Symbolleisten-Befehls Element ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="30da2-118">User pressed F1 while selecting an extension menu or toolbar command item.</span></span> <span data-ttu-id="30da2-119">Gibt an, dass die Erweiterung **WinHelp** entsprechend für das Befehls Element aufruft.</span><span class="sxs-lookup"><span data-stu-id="30da2-119">Indicates that the extension should call **WinHelp** appropriately for the command item.</span></span>

</dd> <dt>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>

<span data-ttu-id="30da2-120"><span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**-HelpString für "f" \_**</span><span class="sxs-lookup"><span data-stu-id="30da2-120"><span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**FMEVENT\_HELPSTRING**</span></span>


</dt> <dd>

<span data-ttu-id="30da2-121">Der Benutzer hat ein Erweiterungs Menü oder ein Symbolleisten-Befehls Element ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="30da2-121">User selected an extension menu or toolbar command item.</span></span> <span data-ttu-id="30da2-122">Gibt an, dass die Erweiterung eine Hilfe Zeichenfolge bereitstellen soll.</span><span class="sxs-lookup"><span data-stu-id="30da2-122">Indicates that the extension should supply a Help string.</span></span>

</dd> <dt>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>

<span data-ttu-id="30da2-123"><span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**Datei " \_ InitMenu"**</span><span class="sxs-lookup"><span data-stu-id="30da2-123"><span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**FMEVENT\_INITMENU**</span></span>


</dt> <dd>

<span data-ttu-id="30da2-124">Der Benutzer hat das Menü der Erweiterung ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="30da2-124">User selected the extension's menu.</span></span> <span data-ttu-id="30da2-125">Die Erweiterung sollte Elemente im Menü initialisieren.</span><span class="sxs-lookup"><span data-stu-id="30da2-125">The extension should initialize items in the menu.</span></span>

</dd> <dt>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>

<span data-ttu-id="30da2-126"><span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**Laden von "f" \_**</span><span class="sxs-lookup"><span data-stu-id="30da2-126"><span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**FMEVENT\_LOAD**</span></span>


</dt> <dd>

<span data-ttu-id="30da2-127">Der Datei-Manager lädt die Erweiterungs-DLL und fordert die dll zur Eingabe von Informationen über das Menü an, das die dll bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="30da2-127">File Manager is loading the extension DLL and prompts the DLL for information about the menu that the DLL supplies.</span></span>

</dd> <dt>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>

<span data-ttu-id="30da2-128"><span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**"schabvent \_ selChange"**</span><span class="sxs-lookup"><span data-stu-id="30da2-128"><span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**FMEVENT\_SELCHANGE**</span></span>


</dt> <dd>

<span data-ttu-id="30da2-129">Die Auswahl im Verzeichnis Fenster des **Datei-Managers** oder im Fenster " **Suchergebnisse** " wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="30da2-129">Selection in the **File Manager** directory window or **Search Results** window has changed.</span></span>

</dd> <dt>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>

<span data-ttu-id="30da2-130"><span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**"Tool barload" von "f" \_**</span><span class="sxs-lookup"><span data-stu-id="30da2-130"><span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**FMEVENT\_TOOLBARLOAD**</span></span>


</dt> <dd>

<span data-ttu-id="30da2-131">Der Datei-Manager erstellt die Symbolleiste und fordert die Erweiterungs-DLL zur Eingabe von Informationen über alle Schaltflächen auf, die die dll der Symbolleiste hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="30da2-131">File Manager is creating the toolbar and prompts the extension DLL for information about any buttons the DLL adds to the toolbar.</span></span>

</dd> <dt>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>

<span data-ttu-id="30da2-132"><span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**Entladen von "f" \_**</span><span class="sxs-lookup"><span data-stu-id="30da2-132"><span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**FMEVENT\_UNLOAD**</span></span>


</dt> <dd>

<span data-ttu-id="30da2-133">Die Erweiterungs-DLL wird vom Datei-Manager entladen.</span><span class="sxs-lookup"><span data-stu-id="30da2-133">File Manager is unloading the extension DLL.</span></span>

</dd> <dt>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>

<span data-ttu-id="30da2-134"><span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**\_Benutzer Aktualisierung für "Benutzer" \_**</span><span class="sxs-lookup"><span data-stu-id="30da2-134"><span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**FMEVENT\_USER\_REFRESH**</span></span>


</dt> <dd>

<span data-ttu-id="30da2-135">Der Benutzer hat den Befehl " **Aktualisieren** " im Menü " **Fenster** " ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="30da2-135">User selected the **Refresh** command from the **Window** menu.</span></span> <span data-ttu-id="30da2-136">Die Erweiterung sollte bei Bedarf Elemente im Menü aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="30da2-136">The extension should update items in the menu, if necessary.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="30da2-137">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30da2-137">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30da2-138">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="30da2-138">Type: **LONG**</span></span>

<span data-ttu-id="30da2-139">Meldungs spezifischer Wert.</span><span class="sxs-lookup"><span data-stu-id="30da2-139">Message-specific value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30da2-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30da2-140">Return value</span></span>

<span data-ttu-id="30da2-141">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="30da2-141">Type: **LONG**</span></span>

<span data-ttu-id="30da2-142">Gibt einen Wert zurück, der von der *wmsg* -Parameter Nachricht abhängt.</span><span class="sxs-lookup"><span data-stu-id="30da2-142">Returns a value dependent upon the *wMsg* parameter message.</span></span>

## <a name="requirements"></a><span data-ttu-id="30da2-143">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="30da2-143">Requirements</span></span>



| <span data-ttu-id="30da2-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30da2-144">Requirement</span></span> | <span data-ttu-id="30da2-145">Wert</span><span class="sxs-lookup"><span data-stu-id="30da2-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="30da2-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30da2-146">Minimum supported client</span></span><br/> | <span data-ttu-id="30da2-147">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30da2-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="30da2-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30da2-148">Minimum supported server</span></span><br/> | <span data-ttu-id="30da2-149">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30da2-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="30da2-150">Header</span><span class="sxs-lookup"><span data-stu-id="30da2-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="30da2-151"><dt>WF. h</dt></span><span class="sxs-lookup"><span data-stu-id="30da2-151"><dt>Wfext.h</dt></span></span> </dl> |
| <span data-ttu-id="30da2-152">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="30da2-152">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="30da2-153">" **F** " (Unicode)</span><span class="sxs-lookup"><span data-stu-id="30da2-153">**FMExtensionProcW** (Unicode)</span></span><br/>                                          |



 

 




