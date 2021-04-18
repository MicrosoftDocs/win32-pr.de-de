---
description: Anpassen des Winlogon-Verhaltens durch Implementieren eines Anmelde Informationsanbieters.
ms.assetid: 70b47e29-c755-4c59-a493-d7fcbbc94b83
title: Anpassen von Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64da4baae9b52dd53e288c631f35d33ea5a3085
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357393"
---
# <a name="customizing-winlogon"></a><span data-ttu-id="72e18-103">Anpassen von Winlogon</span><span class="sxs-lookup"><span data-stu-id="72e18-103">Customizing Winlogon</span></span>

<span data-ttu-id="72e18-104">Anpassen des [*Winlogon*](/windows/desktop/SecGloss/w-gly) -Verhaltens durch Implementieren eines Anmelde Informationsanbieters.</span><span class="sxs-lookup"><span data-stu-id="72e18-104">Customize [*Winlogon*](/windows/desktop/SecGloss/w-gly) behavior by implementing a Credential Provider.</span></span> <span data-ttu-id="72e18-105">Weitere Informationen zu Anmelde Informationsanbietern finden Sie unter [**ikredentialprovider-Schnittstelle**](/windows/win32/api/credentialprovider/nn-credentialprovider-icredentialprovider).</span><span class="sxs-lookup"><span data-stu-id="72e18-105">For information about Credential Providers, see [**ICredentialProvider Interface**](/windows/win32/api/credentialprovider/nn-credentialprovider-icredentialprovider).</span></span>

<span data-ttu-id="72e18-106">**Windows Server 2003 und Windows XP:** Anmelde Informationsanbieter werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="72e18-106">**Windows Server 2003 and Windows XP:** Credential Providers are not supported.</span></span>

<span data-ttu-id="72e18-107">In den folgenden Abschnitten werden Möglichkeiten zum Anpassen von Winlogon in Windows-Versionen vor Windows Vista beschrieben.</span><span class="sxs-lookup"><span data-stu-id="72e18-107">The following sections describe ways to customize Winlogon in Windows versions prior to Windows Vista.</span></span>

> [!Note]  
> <span data-ttu-id="72e18-108">Gina-DLLs und Winlogon-Benachrichtigungs Pakete werden in Windows Vista ignoriert.</span><span class="sxs-lookup"><span data-stu-id="72e18-108">GINA DLLs and Winlogon notification packages are ignored in Windows Vista.</span></span>

 

-   [<span data-ttu-id="72e18-109">Winlogon-Benachrichtigungs Pakete</span><span class="sxs-lookup"><span data-stu-id="72e18-109">Winlogon Notification Packages</span></span>](#winlogon-notification-packages)
-   [<span data-ttu-id="72e18-110">Gina-Stub</span><span class="sxs-lookup"><span data-stu-id="72e18-110">GINA Stubs</span></span>](#gina-stubs)
-   [<span data-ttu-id="72e18-111">Gina-Hooks</span><span class="sxs-lookup"><span data-stu-id="72e18-111">GINA Hooks</span></span>](#gina-hooks)

## <a name="winlogon-notification-packages"></a><span data-ttu-id="72e18-112">Winlogon-Benachrichtigungs Pakete</span><span class="sxs-lookup"><span data-stu-id="72e18-112">Winlogon Notification Packages</span></span>

<span data-ttu-id="72e18-113">Ein Winlogon-Benachrichtigungs Paket ist eine DLL, die Funktionen exportiert, die Winlogon-Ereignisse verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="72e18-113">A Winlogon notification package is a DLL that exports functions that handle Winlogon events.</span></span> <span data-ttu-id="72e18-114">Wenn sich ein Benutzer beispielsweise beim System anmeldet, ruft Winlogon jedes Benachrichtigungs Paket auf, um Informationen zum Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="72e18-114">For example, when a user logs onto the system, Winlogon calls each notification package to provide information about the event.</span></span> <span data-ttu-id="72e18-115">Weitere Informationen finden Sie unter [Winlogon-Benachrichtigungs Pakete](winlogon-notification-packages.md).</span><span class="sxs-lookup"><span data-stu-id="72e18-115">For more information, see [Winlogon Notification Packages](winlogon-notification-packages.md).</span></span>

## <a name="gina-stubs"></a><span data-ttu-id="72e18-116">Gina-Stub</span><span class="sxs-lookup"><span data-stu-id="72e18-116">GINA Stubs</span></span>

<span data-ttu-id="72e18-117">Ein [*Gina*](/windows/desktop/SecGloss/g-gly) Stub ist eine benutzerdefinierte GINA-DLL, die die Export Funktions Implementierungen einer zuvor installierten Gina-DLL verwendet (in der Regel MsGina.dll).</span><span class="sxs-lookup"><span data-stu-id="72e18-117">A [*GINA*](/windows/desktop/SecGloss/g-gly) stub is a custom GINA DLL that uses the export function implementations of a previously installed GINA DLL (typically MsGina.dll).</span></span> <span data-ttu-id="72e18-118">Ein Gina-Stub ruft Zeiger auf jede Funktion ab, die von der zuvor installierten Gina-DLL exportiert wurde.</span><span class="sxs-lookup"><span data-stu-id="72e18-118">A GINA stub gets pointers to each function exported by the previously installed GINA DLL.</span></span> <span data-ttu-id="72e18-119">Jede Gina Stub-Funktion verwendet dann den passenden Funktionszeiger, um die entsprechende Funktion in der zuvor installierten Gina-DLL aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="72e18-119">Each GINA stub function then uses the appropriate function pointer to call the corresponding function in the previously installed GINA DLL.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="72e18-120">Jede Gina Stub-Funktion muss die entsprechende Funktion in der zuvor installierten Gina aufruft.</span><span class="sxs-lookup"><span data-stu-id="72e18-120">Each GINA stub function must call the corresponding function in the previously installed GINA.</span></span>

 

<span data-ttu-id="72e18-121">Eine Gina Stub-Funktion kann zusätzliche Funktionen in einer oder mehreren ihrer Exportfunktionen implementieren.</span><span class="sxs-lookup"><span data-stu-id="72e18-121">A GINA stub function can implement additional functionality in one or more of its export functions.</span></span> <span data-ttu-id="72e18-122">Beispielsweise kann die [**wlxloggedoutsas**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas) -Funktion eines Gina Stub die aktuelle Zeit überprüfen, bevor die **wlxloggedoutsas** -Funktion des MsGina.dll aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="72e18-122">For example, the [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas) function of a GINA stub might check the current time before calling the **WlxLoggedOutSAS** function of the MsGina.dll.</span></span> <span data-ttu-id="72e18-123">Wenn sich die aktuelle Zeit in einem bestimmten Bereich befunden hat, könnte die stubfunktion eine Meldung anzeigen, die angibt, dass die Anmeldung während dieses Zeitraums nicht zulässig ist, und die **wlx- \_ SAS- \_ Aktion " \_ None** " an "Winlogon" zurückgeben</span><span class="sxs-lookup"><span data-stu-id="72e18-123">If the current time was within a specific range, the stub function could display a message that indicates logon is disallowed during that time period and return **WLX\_SAS\_ACTION\_NONE** to Winlogon.</span></span> <span data-ttu-id="72e18-124">Die **wlxloggedoutsas** -Funktion des MsGina.dll würde dann nur während des zulässigen Zeitraums aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="72e18-124">The **WlxLoggedOutSAS** function of the MsGina.dll would then be called only during the allowed time period.</span></span>

<span data-ttu-id="72e18-125">Die Gina Stub-Anwendung ruft über den *pwinlogonfunctions* -Parameter der [**wlxinitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) -Funktion eine dispatchtabelle an die Winlogon-Unterstützungsfunktionen ab.</span><span class="sxs-lookup"><span data-stu-id="72e18-125">The GINA stub application gets a dispatch table to Winlogon support functions through the *pWinlogonFunctions* parameter of the [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) function.</span></span> <span data-ttu-id="72e18-126">Die Gina Stub-Anwendung kann diese Dispatch-Tabelle verwenden, um Winlogon-Unterstützungsfunktionen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="72e18-126">The GINA stub application can use this dispatch table to call Winlogon support functions.</span></span> <span data-ttu-id="72e18-127">Eine Gina Stub-Anwendung kann z. b. die [**wlxsasnotify**](/windows/win32/api/winwlx/nc-winwlx-pwlx_sas_notify) -Funktion aufgerufen werden, um ein Sicherheits Ereignis ( [*Secure Attention Sequence*](/windows/desktop/SecGloss/s-gly) , SAS) auszulösen, wenn eine [*Smartcard*](/windows/desktop/SecGloss/s-gly) in einen [*Reader*](/windows/desktop/SecGloss/r-gly)eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="72e18-127">For example, A GINA stub application can call the [**WlxSasNotify**](/windows/win32/api/winwlx/nc-winwlx-pwlx_sas_notify) function to cause a [*secure attention sequence*](/windows/desktop/SecGloss/s-gly) (SAS) event when a [*smart card*](/windows/desktop/SecGloss/s-gly) is inserted into a [*reader*](/windows/desktop/SecGloss/r-gly).</span></span>

<span data-ttu-id="72e18-128">Weitere Informationen zum Erstellen eines Gina Stub finden Sie im Beispiel "Gina Stubs" im \\ Verzeichnis "Beispiele \\ Security \\ Gina \\ Ginastub" einer Platform Software Development Kit (SDK)-Installation.</span><span class="sxs-lookup"><span data-stu-id="72e18-128">For more information about creating a GINA stub, see the Gina Stubs sample in the \\Samples\\Security\\Gina\\GinaStub directory of a Platform Software Development Kit (SDK) installation.</span></span>

> [!Note]  
> <span data-ttu-id="72e18-129">Alle Aufrufe zwischen einer Gina und Winlogon müssen sich innerhalb eines einzelnen Threads befinden.</span><span class="sxs-lookup"><span data-stu-id="72e18-129">All calls between a GINA and Winlogon must be within a single thread.</span></span>

 

## <a name="gina-hooks"></a><span data-ttu-id="72e18-130">Gina-Hooks</span><span class="sxs-lookup"><span data-stu-id="72e18-130">GINA Hooks</span></span>

<span data-ttu-id="72e18-131">Ein Gina-Hook ist ein Gina-Stub, der in der Implementierung der [**wlxinitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) -Funktion den Zeiger auf die [**wlxdialogboxparam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) -Unterstützungsfunktion in der dispatchtabelle durch einen Zeiger auf seine eigene Implementierung der **wlxdialogboxparam** -Funktion ersetzt.</span><span class="sxs-lookup"><span data-stu-id="72e18-131">A GINA hook is a GINA stub that, in its implementation of the [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) function, replaces the pointer to the [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) support function in the dispatch table with a pointer to its own implementation of the **WlxDialogBoxParam** function.</span></span> <span data-ttu-id="72e18-132">Daher wird jedes Mal, wenn die zuvor installierte Gina (in der Regel MsGina.dll) die **wlxdialogboxparam** -Funktion aufruft, die durch den Gina-Hook implementierte Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="72e18-132">As a result, each time the previously installed GINA (typically MsGina.dll) calls the **WlxDialogBoxParam** function, the function implemented by the GINA hook is called.</span></span>

<span data-ttu-id="72e18-133">Die vom Gina-Hook implementierte [**wlxdialogboxparam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) -Funktion kann die [**DialogProc**](/windows/win32/api/winuser/nc-winuser-dlgproc) -Rückruf Prozedur ersetzen, die auf ein bestimmtes Dialogfeld Ereignis antwortet.</span><span class="sxs-lookup"><span data-stu-id="72e18-133">The [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) function implemented by the GINA hook can replace the [**DialogProc**](/windows/win32/api/winuser/nc-winuser-dlgproc) callback procedure that responds to a specific dialog box event.</span></span>

<span data-ttu-id="72e18-134">Dadurch erhält der Gina-Hook vollständige Kontrolle über die Darstellung und das Verhalten aller Dialogfelder, die von MsGina.dll erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="72e18-134">This gives the GINA hook full control over the appearance and behavior of all of the dialog boxes that MsGina.dll creates.</span></span>

<span data-ttu-id="72e18-135">Weitere Informationen zum Erstellen eines Gina-Hooks finden Sie im Beispiel "Gina Hooks" \\ im \\ Verzeichnis "Beispiele Security \\ Gina \\ ginahook" einer Platform SDK-Installation.</span><span class="sxs-lookup"><span data-stu-id="72e18-135">For more information about creating a GINA hook, see the Gina Hooks sample in the \\Samples\\Security\\Gina\\GinaHook directory of a Platform SDK installation.</span></span>

> [!Note]  
> <span data-ttu-id="72e18-136">Alle Aufrufe zwischen einer Gina und Winlogon müssen sich innerhalb eines einzelnen Threads befinden.</span><span class="sxs-lookup"><span data-stu-id="72e18-136">All calls between a GINA and Winlogon must be within a single thread.</span></span>

 

 

 
