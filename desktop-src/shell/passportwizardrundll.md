---
description: Startet den Passport-Assistenten bei Verwendung mit Rundll32.exe.
title: PassportWizardRunDll-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PassportWizardRunDll
api_type:
- DllExport
api_location:
- Netplwiz.dll
ms.assetid: 015c3875-698e-4d80-bbfc-4fc8a71197b7
ms.openlocfilehash: 1678677bcb305b7e5c47d28f5168d1e596ca3e26
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842511"
---
# <a name="passportwizardrundll-function"></a><span data-ttu-id="88eaa-103">PassportWizardRunDll-Funktion</span><span class="sxs-lookup"><span data-stu-id="88eaa-103">PassportWizardRunDll function</span></span>

<span data-ttu-id="88eaa-104">\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="88eaa-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="88eaa-105">Sie kann in nachfolgenden Versionen von Windows geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="88eaa-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="88eaa-106">Startet den Passport-Assistenten bei Verwendung mit Rundll32.exe.</span><span class="sxs-lookup"><span data-stu-id="88eaa-106">Launches the Passport Wizard when used with Rundll32.exe.</span></span>

## <a name="syntax"></a><span data-ttu-id="88eaa-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="88eaa-107">Syntax</span></span>


```C++
void PassportWizardRunDll(
  _In_ HWND      hwndStub,
  _In_ HINSTANCE hAppInstance,
  _In_ LPTSTR    lpszCmdLine,
  _In_ int       nCmdShow
);
```



## <a name="parameters"></a><span data-ttu-id="88eaa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="88eaa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88eaa-109">*hwndStub* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="88eaa-109">*hwndStub* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88eaa-110">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="88eaa-110">Type: **HWND**</span></span>

<span data-ttu-id="88eaa-111">Ein Handle für ein Besitzerfenster.</span><span class="sxs-lookup"><span data-stu-id="88eaa-111">A handle to an owner window.</span></span> <span data-ttu-id="88eaa-112">Dieser Parameter wird in der Regel auf **NULL festgelegt.**</span><span class="sxs-lookup"><span data-stu-id="88eaa-112">This parameter is typically set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="88eaa-113">*hAppInstance* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="88eaa-113">*hAppInstance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88eaa-114">Typ: **HINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="88eaa-114">Type: **HINSTANCE**</span></span>

<span data-ttu-id="88eaa-115">Ein Handle für die Bibliotheksdatei, das als Rückgabewert von [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("netplwiz") erhalten wird.</span><span class="sxs-lookup"><span data-stu-id="88eaa-115">A handle to the library file, obtained as a return value from [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("netplwiz").</span></span>

</dd> <dt>

<span data-ttu-id="88eaa-116">*lpszCmdLine* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="88eaa-116">*lpszCmdLine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88eaa-117">Typ: **LPTSTR**</span><span class="sxs-lookup"><span data-stu-id="88eaa-117">Type: **LPTSTR**</span></span>

<span data-ttu-id="88eaa-118">Argumentdaten.</span><span class="sxs-lookup"><span data-stu-id="88eaa-118">Argument data.</span></span> <span data-ttu-id="88eaa-119">Dieser Wert ist immer leer.</span><span class="sxs-lookup"><span data-stu-id="88eaa-119">This value will always be empty.</span></span>

</dd> <dt>

<span data-ttu-id="88eaa-120">*nCmdShow* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="88eaa-120">*nCmdShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88eaa-121">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="88eaa-121">Type: **int**</span></span>

<span data-ttu-id="88eaa-122">Legt den Anzeigemodus für das Fenster fest.</span><span class="sxs-lookup"><span data-stu-id="88eaa-122">Sets the display mode for the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88eaa-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="88eaa-123">Return value</span></span>

<span data-ttu-id="88eaa-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="88eaa-124">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="88eaa-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="88eaa-125">Remarks</span></span>

<span data-ttu-id="88eaa-126">Der Passport-Assistent wird verwendet, um einen Standardpass für Windows zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="88eaa-126">The Passport Wizard is used to obtain a default Passport for Windows.</span></span> <span data-ttu-id="88eaa-127">Ein Passport gewährt dem Benutzer personalisierten Zugriff auf alle MSN-Websites und andere Passport-fähige Websites unter Verwendung der E-Mail-Adresse des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="88eaa-127">A Passport gives the user personalized access to all MSN websites and other Passport-enabled sites using the user's email address.</span></span> <span data-ttu-id="88eaa-128">Wenn Sie **PassportWizardRunDll** als Einstiegspunkt in die Netplwiz.dll-Datei über einen Rundll32-Befehl verwenden, können Sie den Passport-Assistenten über eine Befehlszeile starten, als wäre es eine ausführbare Datei.</span><span class="sxs-lookup"><span data-stu-id="88eaa-128">Using **PassportWizardRunDll** as an entry point into the Netplwiz.dll file through a Rundll32 command allows you to launch the Passport Wizard from a command line as though it were an executable file.</span></span>

<span data-ttu-id="88eaa-129">**PassportWizardRunDll** wird ausschließlich im Kontext eines Rundll32.exe Befehls wie folgt verwendet:</span><span class="sxs-lookup"><span data-stu-id="88eaa-129">**PassportWizardRunDll** is used solely in the context of a Rundll32.exe command as follows:</span></span>

<span data-ttu-id="88eaa-130">**rundll32.exe netplwiz.dll, PassportWizardRunDll**</span><span class="sxs-lookup"><span data-stu-id="88eaa-130">**rundll32.exe netplwiz.dll, PassportWizardRunDll**</span></span>

<span data-ttu-id="88eaa-131">Die Verwendung einer Einstiegspunktfunktion mit Rundll32.exe ähnelt keinem normalen Funktionsaufruf.</span><span class="sxs-lookup"><span data-stu-id="88eaa-131">Using an entry point function with Rundll32.exe does not resemble a normal function call.</span></span> <span data-ttu-id="88eaa-132">Der Funktionsname und der Name der DLL-Datei, in der sie gespeichert ist, werden nur als Befehlszeilenparameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="88eaa-132">The function name and the name of the .dll file where it is stored are used only as command-line parameters.</span></span> <span data-ttu-id="88eaa-133">Die unter Syntax gezeigte Funktionsdefinition ist nur ein Standardprototyp für alle Funktionen, die Sie mit Rundll32 aufrufen können.</span><span class="sxs-lookup"><span data-stu-id="88eaa-133">The function definition shown under Syntax is only a standard prototype for all functions that you can call using Rundll32.</span></span> <span data-ttu-id="88eaa-134">Die spezifischen Werte für *hwndStub,* *hAppInstance* und *nCmdShow* werden nicht vom Benutzer bereitgestellt, sondern im Hintergrund von Rundll32 verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="88eaa-134">The specific values for *hwndStub*, *hAppInstance*, and *nCmdShow* are not provided by the user, but are handled behind the scenes by Rundll32.</span></span> <span data-ttu-id="88eaa-135">**PassportWizardRunDll** verwendet nicht den *LpszCmdLine-Wert, sodass* keine zusätzlichen Daten erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="88eaa-135">**PassportWizardRunDll** does not use the *lpszCmdLine* value, so no additional data is required.</span></span>

## <a name="requirements"></a><span data-ttu-id="88eaa-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88eaa-136">Requirements</span></span>



| <span data-ttu-id="88eaa-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88eaa-137">Requirement</span></span> | <span data-ttu-id="88eaa-138">Wert</span><span class="sxs-lookup"><span data-stu-id="88eaa-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88eaa-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88eaa-139">Minimum supported client</span></span><br/> | <span data-ttu-id="88eaa-140">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88eaa-140">Windows XP \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="88eaa-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88eaa-141">Minimum supported server</span></span><br/> | <span data-ttu-id="88eaa-142">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88eaa-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="88eaa-143">Header</span><span class="sxs-lookup"><span data-stu-id="88eaa-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="88eaa-144"><dt>Keine</dt></span><span class="sxs-lookup"><span data-stu-id="88eaa-144"><dt>None</dt></span></span> </dl>                                 |
| <span data-ttu-id="88eaa-145">DLL</span><span class="sxs-lookup"><span data-stu-id="88eaa-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88eaa-146"><dt>Netplwiz.dll (Version 5.60 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="88eaa-146"><dt>Netplwiz.dll (version 5.60 or later)</dt></span></span> </dl> |



 

 
