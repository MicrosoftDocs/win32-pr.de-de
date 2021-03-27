---
description: Hiermit wird der Passport-Assistent bei der Verwendung mit Rundll32.exe gestartet.
title: Passportwizardrundll-Funktion
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
ms.openlocfilehash: a858a36caa4af8095fc7023abae5ad918321f53e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216606"
---
# <a name="passportwizardrundll-function"></a><span data-ttu-id="adaa5-103">Passportwizardrundll-Funktion</span><span class="sxs-lookup"><span data-stu-id="adaa5-103">PassportWizardRunDll function</span></span>

<span data-ttu-id="adaa5-104">\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="adaa5-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="adaa5-105">Sie wird möglicherweise in nachfolgenden Versionen von Windows geändert oder ist nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="adaa5-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="adaa5-106">Hiermit wird der Passport-Assistent bei der Verwendung mit Rundll32.exe gestartet.</span><span class="sxs-lookup"><span data-stu-id="adaa5-106">Launches the Passport Wizard when used with Rundll32.exe.</span></span>

## <a name="syntax"></a><span data-ttu-id="adaa5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="adaa5-107">Syntax</span></span>


```C++
void PassportWizardRunDll(
  _In_ HWND      hwndStub,
  _In_ HINSTANCE hAppInstance,
  _In_ LPTSTR    lpszCmdLine,
  _In_ int       nCmdShow
);
```



## <a name="parameters"></a><span data-ttu-id="adaa5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="adaa5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adaa5-109">*hwndstub* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="adaa5-109">*hwndStub* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adaa5-110">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="adaa5-110">Type: **HWND**</span></span>

<span data-ttu-id="adaa5-111">Ein Handle für ein Besitzer Fenster.</span><span class="sxs-lookup"><span data-stu-id="adaa5-111">A handle to an owner window.</span></span> <span data-ttu-id="adaa5-112">Dieser Parameter ist in der Regel auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="adaa5-112">This parameter is typically set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="adaa5-113">*happinstance* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="adaa5-113">*hAppInstance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adaa5-114">Typ: **HINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="adaa5-114">Type: **HINSTANCE**</span></span>

<span data-ttu-id="adaa5-115">Ein Handle für die Bibliotheksdatei, die als Rückgabewert von [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("netplwiz") abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="adaa5-115">A handle to the library file, obtained as a return value from [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("netplwiz").</span></span>

</dd> <dt>

<span data-ttu-id="adaa5-116">*lpszCmdLine* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="adaa5-116">*lpszCmdLine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adaa5-117">Typ: **LPTSTR**</span><span class="sxs-lookup"><span data-stu-id="adaa5-117">Type: **LPTSTR**</span></span>

<span data-ttu-id="adaa5-118">Argument Daten.</span><span class="sxs-lookup"><span data-stu-id="adaa5-118">Argument data.</span></span> <span data-ttu-id="adaa5-119">Dieser Wert ist immer leer.</span><span class="sxs-lookup"><span data-stu-id="adaa5-119">This value will always be empty.</span></span>

</dd> <dt>

<span data-ttu-id="adaa5-120">*nCmdShow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="adaa5-120">*nCmdShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adaa5-121">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="adaa5-121">Type: **int**</span></span>

<span data-ttu-id="adaa5-122">Legt den Anzeigemodus für das Fenster fest.</span><span class="sxs-lookup"><span data-stu-id="adaa5-122">Sets the display mode for the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adaa5-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="adaa5-123">Return value</span></span>

<span data-ttu-id="adaa5-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="adaa5-124">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="adaa5-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="adaa5-125">Remarks</span></span>

<span data-ttu-id="adaa5-126">Der Passport-Assistent wird verwendet, um einen Standard Passport für Windows zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="adaa5-126">The Passport Wizard is used to obtain a default Passport for Windows.</span></span> <span data-ttu-id="adaa5-127">Ein Passport ermöglicht dem Benutzer den personalisierten Zugriff auf alle MSN Websites und anderen Passport-fähigen Websites mithilfe der e-Mail-Adresse des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="adaa5-127">A Passport gives the user personalized access to all MSN websites and other Passport-enabled sites using the user's email address.</span></span> <span data-ttu-id="adaa5-128">Die Verwendung von **passportwizardrundll** als Einstiegspunkt in die Netplwiz.dll Datei über einen rundll32-Befehl ermöglicht es Ihnen, den Passport-Assistenten von einer Befehlszeile aus zu starten, als wäre es eine ausführbare Datei.</span><span class="sxs-lookup"><span data-stu-id="adaa5-128">Using **PassportWizardRunDll** as an entry point into the Netplwiz.dll file through a Rundll32 command allows you to launch the Passport Wizard from a command line as though it were an executable file.</span></span>

<span data-ttu-id="adaa5-129">**Passportwizardrundll** wird nur im Kontext eines Rundll32.exe Befehls wie folgt verwendet:</span><span class="sxs-lookup"><span data-stu-id="adaa5-129">**PassportWizardRunDll** is used solely in the context of a Rundll32.exe command as follows:</span></span>

<span data-ttu-id="adaa5-130">**rundll32.exe netplwiz.dll, passportwizardrundll**</span><span class="sxs-lookup"><span data-stu-id="adaa5-130">**rundll32.exe netplwiz.dll, PassportWizardRunDll**</span></span>

<span data-ttu-id="adaa5-131">Die Verwendung einer Einstiegspunkt Funktion mit Rundll32.exe ähnelt keinem normalen Funktions aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="adaa5-131">Using an entry point function with Rundll32.exe does not resemble a normal function call.</span></span> <span data-ttu-id="adaa5-132">Der Funktionsname und der Name der DLL-Datei, in der er gespeichert ist, werden nur als Befehlszeilenparameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="adaa5-132">The function name and the name of the .dll file where it is stored are used only as command-line parameters.</span></span> <span data-ttu-id="adaa5-133">Die unter Syntax gezeigte Funktionsdefinition ist nur ein Standard Prototyp für alle Funktionen, die Sie mithilfe von rundll32 abrufen können.</span><span class="sxs-lookup"><span data-stu-id="adaa5-133">The function definition shown under Syntax is only a standard prototype for all functions that you can call using Rundll32.</span></span> <span data-ttu-id="adaa5-134">Die spezifischen Werte für *hwndstub*, *happinstance* und *nCmdShow* werden nicht vom Benutzer bereitgestellt, sondern im Hintergrund durch rundll32 behandelt.</span><span class="sxs-lookup"><span data-stu-id="adaa5-134">The specific values for *hwndStub*, *hAppInstance*, and *nCmdShow* are not provided by the user, but are handled behind the scenes by Rundll32.</span></span> <span data-ttu-id="adaa5-135">**Passportwizardrundll** verwendet nicht den *lpszCmdLine* -Wert, sodass keine zusätzlichen Daten erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="adaa5-135">**PassportWizardRunDll** does not use the *lpszCmdLine* value, so no additional data is required.</span></span>

## <a name="requirements"></a><span data-ttu-id="adaa5-136">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="adaa5-136">Requirements</span></span>



| <span data-ttu-id="adaa5-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="adaa5-137">Requirement</span></span> | <span data-ttu-id="adaa5-138">Wert</span><span class="sxs-lookup"><span data-stu-id="adaa5-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adaa5-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="adaa5-139">Minimum supported client</span></span><br/> | <span data-ttu-id="adaa5-140">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="adaa5-140">Windows XP \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="adaa5-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="adaa5-141">Minimum supported server</span></span><br/> | <span data-ttu-id="adaa5-142">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="adaa5-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="adaa5-143">Header</span><span class="sxs-lookup"><span data-stu-id="adaa5-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="adaa5-144"><dt>None</dt></span><span class="sxs-lookup"><span data-stu-id="adaa5-144"><dt>None</dt></span></span> </dl>                                 |
| <span data-ttu-id="adaa5-145">DLL</span><span class="sxs-lookup"><span data-stu-id="adaa5-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adaa5-146"><dt>Netplwiz.dll (Version 5,60 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="adaa5-146"><dt>Netplwiz.dll (version 5.60 or later)</dt></span></span> </dl> |



 

 
