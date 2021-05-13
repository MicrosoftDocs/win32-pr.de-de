---
description: Gibt eine anwendungsdefinierte Rückruffunktion an, die vom Datei-Manager für die Kommunikation mit einer Datei-Manager-Erweiterung aufgerufen wird.
title: FMExtensionProc-Rückruffunktion (Wfext.h)
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
ms.openlocfilehash: 5e7b1f0142ea77967af15087131d3036aaec505e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842241"
---
# <a name="fmextensionproc-callback-function"></a><span data-ttu-id="ea47b-103">RÜCKRUFFUNKTION "FMExtensionProc"</span><span class="sxs-lookup"><span data-stu-id="ea47b-103">FMExtensionProc callback function</span></span>

<span data-ttu-id="ea47b-104">Gibt eine anwendungsdefinierte Rückruffunktion an, die vom Datei-Manager aufgerufen wird, um mit einer Datei-Manager-Erweiterung zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="ea47b-104">Specifies an application-defined callback function called by File Manager to communicate with a File Manager extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea47b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea47b-105">Syntax</span></span>


```C++
LONG CALLBACK FMExtensionProc(
   HWND hwnd,
   WORD wMsg,
   LONG lParam
);
```



## <a name="parameters"></a><span data-ttu-id="ea47b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea47b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea47b-107">*Hwnd*</span><span class="sxs-lookup"><span data-stu-id="ea47b-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="ea47b-108">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="ea47b-108">Type: **HWND**</span></span>

<span data-ttu-id="ea47b-109">Ein Fensterhandle für den Datei-Manager.</span><span class="sxs-lookup"><span data-stu-id="ea47b-109">A window handle to File Manager.</span></span> <span data-ttu-id="ea47b-110">Eine Erweiterung verwendet dieses Handle, um das übergeordnete Fenster für jedes Dialogfeld oder Meldungsfeld anzugeben, das angezeigt werden muss, und um Abfragemeldungen an den Datei-Manager zu senden.</span><span class="sxs-lookup"><span data-stu-id="ea47b-110">An extension uses this handle to specify the parent window for any dialog box or message box it must display, and to send query messages to File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="ea47b-111">*wMsg*</span><span class="sxs-lookup"><span data-stu-id="ea47b-111">*wMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="ea47b-112">Typ: **WORD**</span><span class="sxs-lookup"><span data-stu-id="ea47b-112">Type: **WORD**</span></span>

<span data-ttu-id="ea47b-113">Eine der folgenden Datei-Manager-Meldungen.</span><span class="sxs-lookup"><span data-stu-id="ea47b-113">One of the following File Manager messages.</span></span>

<dt>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>

<span data-ttu-id="ea47b-114"><span id="1_through_99"></span><span id="1_THROUGH_99"></span>**1 bis 99**</span><span class="sxs-lookup"><span data-stu-id="ea47b-114"><span id="1_through_99"></span><span id="1_THROUGH_99"></span>**1 through 99**</span></span>


</dt> <dd>

<span data-ttu-id="ea47b-115">Der Benutzer hat im durch die Erweiterung bereitgestellten Menü ein Element ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="ea47b-115">User selected an item from the extension-supplied menu.</span></span> <span data-ttu-id="ea47b-116">Der Wert ist der Bezeichner des ausgewählten Menüelements.</span><span class="sxs-lookup"><span data-stu-id="ea47b-116">The value is the identifier of the selected menu item.</span></span>

</dd> <dt>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>

<span data-ttu-id="ea47b-117"><span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**FMEVENT \_ HELPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="ea47b-117"><span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**FMEVENT\_HELPMENUITEM**</span></span>


</dt> <dd>

<span data-ttu-id="ea47b-118">Der Benutzer hat F1 gedrückt, während er ein Erweiterungsmenü oder ein Symbolleistenbefehlselement auswählte.</span><span class="sxs-lookup"><span data-stu-id="ea47b-118">User pressed F1 while selecting an extension menu or toolbar command item.</span></span> <span data-ttu-id="ea47b-119">Gibt an, dass die Erweiterung **WinHelp** entsprechend für das Befehlselement aufrufen soll.</span><span class="sxs-lookup"><span data-stu-id="ea47b-119">Indicates that the extension should call **WinHelp** appropriately for the command item.</span></span>

</dd> <dt>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>

<span data-ttu-id="ea47b-120"><span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**FMEVENT \_ HELPSTRING**</span><span class="sxs-lookup"><span data-stu-id="ea47b-120"><span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**FMEVENT\_HELPSTRING**</span></span>


</dt> <dd>

<span data-ttu-id="ea47b-121">Der Benutzer hat ein Erweiterungsmenü oder ein Symbolleistenbefehlselement ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="ea47b-121">User selected an extension menu or toolbar command item.</span></span> <span data-ttu-id="ea47b-122">Gibt an, dass die Erweiterung eine Hilfezeichenfolge bereitstellen soll.</span><span class="sxs-lookup"><span data-stu-id="ea47b-122">Indicates that the extension should supply a Help string.</span></span>

</dd> <dt>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>

<span data-ttu-id="ea47b-123"><span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**FMEVENT \_ INITMENU**</span><span class="sxs-lookup"><span data-stu-id="ea47b-123"><span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**FMEVENT\_INITMENU**</span></span>


</dt> <dd>

<span data-ttu-id="ea47b-124">Der Benutzer hat das Menü der Erweiterung ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="ea47b-124">User selected the extension's menu.</span></span> <span data-ttu-id="ea47b-125">Die Erweiterung sollte Elemente im Menü initialisieren.</span><span class="sxs-lookup"><span data-stu-id="ea47b-125">The extension should initialize items in the menu.</span></span>

</dd> <dt>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>

<span data-ttu-id="ea47b-126"><span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**FMEVENT \_ LOAD**</span><span class="sxs-lookup"><span data-stu-id="ea47b-126"><span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**FMEVENT\_LOAD**</span></span>


</dt> <dd>

<span data-ttu-id="ea47b-127">Der Datei-Manager lädt die Erweiterungs-DLL und fordert die DLL auf, Informationen über das von der DLL zur Verfügung zu stellende Menü zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ea47b-127">File Manager is loading the extension DLL and prompts the DLL for information about the menu that the DLL supplies.</span></span>

</dd> <dt>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>

<span data-ttu-id="ea47b-128"><span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**FMEVENT \_ SELCHANGE**</span><span class="sxs-lookup"><span data-stu-id="ea47b-128"><span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**FMEVENT\_SELCHANGE**</span></span>


</dt> <dd>

<span data-ttu-id="ea47b-129">Die Auswahl im **Datei-Manager-Verzeichnisfenster** oder **im Fenster Suchergebnisse** wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="ea47b-129">Selection in the **File Manager** directory window or **Search Results** window has changed.</span></span>

</dd> <dt>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>

<span data-ttu-id="ea47b-130"><span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**FMEVENT \_ TOOLBARLOAD**</span><span class="sxs-lookup"><span data-stu-id="ea47b-130"><span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**FMEVENT\_TOOLBARLOAD**</span></span>


</dt> <dd>

<span data-ttu-id="ea47b-131">Der Datei-Manager erstellt die Symbolleiste und fordert die Erweiterungs-DLL auf, Informationen zu schaltflächen zu erhalten, die die DLL der Symbolleiste hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="ea47b-131">File Manager is creating the toolbar and prompts the extension DLL for information about any buttons the DLL adds to the toolbar.</span></span>

</dd> <dt>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>

<span data-ttu-id="ea47b-132"><span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**FMEVENT \_ UNLOAD**</span><span class="sxs-lookup"><span data-stu-id="ea47b-132"><span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**FMEVENT\_UNLOAD**</span></span>


</dt> <dd>

<span data-ttu-id="ea47b-133">Der Datei-Manager entlädt die Erweiterungs-DLL.</span><span class="sxs-lookup"><span data-stu-id="ea47b-133">File Manager is unloading the extension DLL.</span></span>

</dd> <dt>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>

<span data-ttu-id="ea47b-134"><span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**\_FMEVENT-BENUTZERAKTUALISIERUNG \_**</span><span class="sxs-lookup"><span data-stu-id="ea47b-134"><span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**FMEVENT\_USER\_REFRESH**</span></span>


</dt> <dd>

<span data-ttu-id="ea47b-135">Der Benutzer hat im **Menü** Fenster den Befehl **Aktualisieren** ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="ea47b-135">User selected the **Refresh** command from the **Window** menu.</span></span> <span data-ttu-id="ea47b-136">Die Erweiterung sollte bei Bedarf Elemente im Menü aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ea47b-136">The extension should update items in the menu, if necessary.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ea47b-137">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea47b-137">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea47b-138">Typ: **LONG**</span><span class="sxs-lookup"><span data-stu-id="ea47b-138">Type: **LONG**</span></span>

<span data-ttu-id="ea47b-139">Nachrichtenspezifischer Wert.</span><span class="sxs-lookup"><span data-stu-id="ea47b-139">Message-specific value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea47b-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea47b-140">Return value</span></span>

<span data-ttu-id="ea47b-141">Typ: **LONG**</span><span class="sxs-lookup"><span data-stu-id="ea47b-141">Type: **LONG**</span></span>

<span data-ttu-id="ea47b-142">Gibt einen Wert zurück, der von der *wMsg-Parametermeldung* abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="ea47b-142">Returns a value dependent upon the *wMsg* parameter message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea47b-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea47b-143">Requirements</span></span>



| <span data-ttu-id="ea47b-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea47b-144">Requirement</span></span> | <span data-ttu-id="ea47b-145">Wert</span><span class="sxs-lookup"><span data-stu-id="ea47b-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ea47b-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea47b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="ea47b-147">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea47b-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="ea47b-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea47b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="ea47b-149">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea47b-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ea47b-150">Header</span><span class="sxs-lookup"><span data-stu-id="ea47b-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea47b-151"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="ea47b-151"><dt>Wfext.h</dt></span></span> </dl> |
| <span data-ttu-id="ea47b-152">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="ea47b-152">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ea47b-153">**FMExtensionProcW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="ea47b-153">**FMExtensionProcW** (Unicode)</span></span><br/>                                          |



 

 




