---
description: In diesem Thema erfahren Sie, wie Sie eine Verknüpfung für Ihre APP erstellen, ihr eine appusermodelid zuweisen und Sie auf dem Start Bildschirm installieren.
title: Aktivieren von Desktoppopupbenachrichtigungen über eine AppUserModelID
ms.topic: article
ms.date: 05/31/2018
ms.assetid: BB32CD0A-99E6-47dc-A913-39A7B3027314
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbSyntax
ms.openlocfilehash: bd02a0ec6512aa7637f0d6b2b281e1b862e61d3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978856"
---
# <a name="how-to-enable-desktop-toast-notifications-through-an-appusermodelid"></a><span data-ttu-id="7ef21-103">Aktivieren von Desktoppopupbenachrichtigungen über eine AppUserModelID</span><span class="sxs-lookup"><span data-stu-id="7ef21-103">How to enable desktop toast notifications through an AppUserModelID</span></span>

<span data-ttu-id="7ef21-104">In diesem Thema erfahren Sie, wie Sie eine Verknüpfung für Ihre APP erstellen, ihr eine [appusermodelid](appids.md)zuweisen und Sie auf dem Start Bildschirm installieren.</span><span class="sxs-lookup"><span data-stu-id="7ef21-104">This topic shows you how to create a shortcut for your app, assign it an [AppUserModelID](appids.md), and install it in the Start screen.</span></span> <span data-ttu-id="7ef21-105">Es wird dringend empfohlen, dass Sie dies in der Windows Installer statt im Code Ihrer APP tun.</span><span class="sxs-lookup"><span data-stu-id="7ef21-105">We strongly recommend that you do this in the Windows Installer rather than in your app's code.</span></span> <span data-ttu-id="7ef21-106">Wenn keine gültige Verknüpfung auf dem Start Bildschirm oder in **allen Programmen** installiert ist, können Sie keine Popup Benachrichtigung von einer Desktop-App aus aufrichten.</span><span class="sxs-lookup"><span data-stu-id="7ef21-106">Without a valid shortcut installed in the Start screen or in **All Programs**, you cannot raise a toast notification from a desktop app.</span></span>

> [!Note]  
> <span data-ttu-id="7ef21-107">Die in diesem Thema verwendeten Beispiel Methoden stammen aus dem [Desktop-Popup Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts).</span><span class="sxs-lookup"><span data-stu-id="7ef21-107">The example methods used in this topic are taken from the [Desktop toast sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts).</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="7ef21-108">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="7ef21-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7ef21-109">Technologien</span><span class="sxs-lookup"><span data-stu-id="7ef21-109">Technologies</span></span>

-   <span data-ttu-id="7ef21-110">COM</span><span class="sxs-lookup"><span data-stu-id="7ef21-110">COM</span></span>

### <a name="prerequisites"></a><span data-ttu-id="7ef21-111">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="7ef21-111">Prerequisites</span></span>

-   <span data-ttu-id="7ef21-112">Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="7ef21-112">Libraries</span></span>
    -   <span data-ttu-id="7ef21-113">C++: Runtime. Object. lib</span><span class="sxs-lookup"><span data-stu-id="7ef21-113">C++: Runtime.object.lib</span></span>
    -   <span data-ttu-id="7ef21-114">C \# : Windows. winmd</span><span class="sxs-lookup"><span data-stu-id="7ef21-114">C\#: Windows.Winmd</span></span>
-   <span data-ttu-id="7ef21-115">C \# : Windows-API-Code Paket für Microsoft .NET Framework</span><span class="sxs-lookup"><span data-stu-id="7ef21-115">C\#: Windows API Code Pack for Microsoft .NET Framework</span></span>
-   <span data-ttu-id="7ef21-116">Eine Version von Microsoft Visual Studio, die mindestens Windows 8 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7ef21-116">A version of Microsoft Visual Studio that supports at least Windows 8</span></span>

## <a name="instructions"></a><span data-ttu-id="7ef21-117">Instructions</span><span class="sxs-lookup"><span data-stu-id="7ef21-117">Instructions</span></span>

### <a name="step-1-prepare-the-shortcut-to-be-created"></a><span data-ttu-id="7ef21-118">Schritt 1: Vorbereiten der zu erstellenden Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="7ef21-118">Step 1: Prepare the shortcut to be created</span></span>

<span data-ttu-id="7ef21-119">In diesem Beispiel wird zuerst der Pfad des Ordners für App-Daten des Benutzers über die [**GetEnvironmentVariable**](/windows/win32/api/processenv/nf-processenv-getenvironmentvariablea) -Funktion bestimmt.</span><span class="sxs-lookup"><span data-stu-id="7ef21-119">This example first determines the path of the user's app data folder through the [**GetEnvironmentVariable**](/windows/win32/api/processenv/nf-processenv-getenvironmentvariablea) function.</span></span> <span data-ttu-id="7ef21-120">Anschließend wird der vollständige Pfad zur Verknüpfung erstellt, es wird festgelegt, dass an diesem Speicherort noch keine Verknüpfung dieses Namens vorhanden ist, und diese Informationen werden an eine andere Methode weitergeleitet, die die Verknüpfung erstellt und installiert.</span><span class="sxs-lookup"><span data-stu-id="7ef21-120">It then composes the full path to the shortcut, determines that a shortcut of that name does not already exist at that location, and passes that information to another method which creates and installs the shortcut.</span></span>

<span data-ttu-id="7ef21-121">Beachten Sie, dass die Verknüpfung pro Benutzer oder pro App bereitgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7ef21-121">Note that the shortcut can be deployed per-user or per-app.</span></span>


```C++
HRESULT DesktopToastsApp::TryCreateShortcut()
{
    wchar_t shortcutPath[MAX_PATH];
    DWORD charWritten = GetEnvironmentVariable(L"APPDATA", shortcutPath, MAX_PATH);
    HRESULT hr = charWritten > 0 ? S_OK : E_INVALIDARG;

    if (SUCCEEDED(hr))
    {
        errno_t concatError = wcscat_s(shortcutPath, ARRAYSIZE(shortcutPath), L"\\Microsoft\\Windows\\Start Menu\\Programs\\Desktop Toasts App.lnk");
 
        hr = concatError == 0 ? S_OK : E_INVALIDARG;
        if (SUCCEEDED(hr))
        {
            DWORD attributes = GetFileAttributes(shortcutPath);
            bool fileExists = attributes < 0xFFFFFFF;

            if (!fileExists)
            {
                hr = InstallShortcut(shortcutPath);  // See step 2.
            }
            else
            {
                hr = S_FALSE;
            }
        }
    }
    return hr;
}
```



### <a name="step-2-create-the-shortcut-and-install-it-in-the-start-screen"></a><span data-ttu-id="7ef21-122">Schritt 2: Erstellen Sie die Verknüpfung, und installieren Sie Sie auf dem Start Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="7ef21-122">Step 2: Create the shortcut and install it in the Start screen</span></span>

<span data-ttu-id="7ef21-123">In diesem Beispiel wird auch der Eigenschaften Speicher der Verknüpfung abgerufen, und die erforderliche [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) -Eigenschaft wird von einer zuvor definierten Variablen,, festgelegt `AppID` .</span><span class="sxs-lookup"><span data-stu-id="7ef21-123">This example also retrieves the shortcut's property store and sets the required [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) property from a previously defined variable, `AppID`.</span></span>


```C++
HRESULT DesktopToastsApp::InstallShortcut(_In_z_ wchar_t *shortcutPath)
{
    wchar_t exePath[MAX_PATH];
    
    DWORD charWritten = GetModuleFileNameEx(GetCurrentProcess(), nullptr, exePath, ARRAYSIZE(exePath));

    HRESULT hr = charWritten > 0 ? S_OK : E_FAIL;
    
    if (SUCCEEDED(hr))
    {
        ComPtr<IShellLink> shellLink;
        hr = CoCreateInstance(CLSID_ShellLink, nullptr, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&shellLink));

        if (SUCCEEDED(hr))
        {
            hr = shellLink->SetPath(exePath);
            if (SUCCEEDED(hr))
            {
                hr = shellLink->SetArguments(L"");
                if (SUCCEEDED(hr))
                {
                    ComPtr<IPropertyStore> propertyStore;

                    hr = shellLink.As(&propertyStore);
                    if (SUCCEEDED(hr))
                    {
                        PROPVARIANT appIdPropVar;
                        hr = InitPropVariantFromString(AppId, &appIdPropVar);
                        if (SUCCEEDED(hr))
                        {
                            hr = propertyStore->SetValue(PKEY_AppUserModel_ID, appIdPropVar);
                            if (SUCCEEDED(hr))
                            {
                                hr = propertyStore->Commit();
                                if (SUCCEEDED(hr))
                                {
                                    ComPtr<IPersistFile> persistFile;
                                    hr = shellLink.As(&persistFile);
                                    if (SUCCEEDED(hr))
                                    {
                                        hr = persistFile->Save(shortcutPath, TRUE);
                                    }
                                }
                            }
                            PropVariantClear(&appIdPropVar);
                        }
                    }
                }
            }
        }
    }
    return hr;
}
```



## <a name="remarks"></a><span data-ttu-id="7ef21-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ef21-124">Remarks</span></span>

<span data-ttu-id="7ef21-125">Als Alternative zu dem in diesem Thema gezeigten Ansatz können Sie ein Framework, wie z. b. das Windows Installer-XML (WiX), verwenden, um die Verknüpfung zu generieren und als Teil der Windows Installer bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7ef21-125">As an alternative to the approach shown in this topic, you can use a framework such as the Windows Installer XML (WiX) to generate the shortcut and deploy it as part of the Windows Installer.</span></span> <span data-ttu-id="7ef21-126">In diesem Fall sollte dieser Code in der MSI-Datei statt im Code der App enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="7ef21-126">In that case, this code should be included in the MSI rather than in the app's code.</span></span> <span data-ttu-id="7ef21-127">Weitere Informationen finden Sie in der WiX-Beispielkonfigurationsdatei im Beispiel zum [Senden von Popup Benachrichtigungen aus Desktop-Apps](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208)) .</span><span class="sxs-lookup"><span data-stu-id="7ef21-127">For more information, see the sample WiX configuration file included with the [Sending toast notifications from desktop apps](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208)) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ef21-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7ef21-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ef21-129">Schnellstart: Senden einer Popup Benachrichtigung vom Desktop</span><span class="sxs-lookup"><span data-stu-id="7ef21-129">Quickstart: Sending a toast notification from the desktop</span></span>](quickstart-sending-desktop-toast.md)
</dt> <dt>

<span data-ttu-id="7ef21-130">[Beispiel zum Senden von Toastbenachrichtigungen aus Desktop-Apps](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208))</span><span class="sxs-lookup"><span data-stu-id="7ef21-130">[Sending toast notifications from desktop apps sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208))</span></span>
</dt> <dt>

[<span data-ttu-id="7ef21-131">Anwendungs Benutzer Modell-IDs (appusermudelids)</span><span class="sxs-lookup"><span data-stu-id="7ef21-131">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> <dt>

<span data-ttu-id="7ef21-132">[Gewusst wie: Installieren der WiX-Tools (Windows Installer XML)](/previous-versions/windows/server-essentials/gg513936(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="7ef21-132">[How to: Install the Windows Installer XML (WiX) Tools](/previous-versions/windows/server-essentials/gg513936(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="7ef21-133">Popup-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="7ef21-133">Toast XML schema</span></span>](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

<span data-ttu-id="7ef21-134">[Übersicht über Popup Benachrichtigungen](/previous-versions/windows/apps/hh779727(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7ef21-134">[Toast notification overview](/previous-versions/windows/apps/hh779727(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="7ef21-135">[Schnellstart: Senden einer Popup Benachrichtigung](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7ef21-135">[Quickstart: Sending a toast notification](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="7ef21-136">[Schnellstart: Senden einer Popup-Pushbenachrichtigung](/previous-versions/windows/hh761487(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7ef21-136">[Quickstart: Sending a toast push notification](/previous-versions/windows/hh761487(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="7ef21-137">Richtlinien und Prüfliste für Popup Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="7ef21-137">Guidelines and checklist for toast notifications</span></span>](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[<span data-ttu-id="7ef21-138">Hinzufügen von Bildern zu einer Popup Vorlage</span><span class="sxs-lookup"><span data-stu-id="7ef21-138">How to add images to a toast template</span></span>](/previous-versions/windows/)
</dt> <dt>

[<span data-ttu-id="7ef21-139">Überprüfen der Popup Benachrichtigungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="7ef21-139">How to check toast notification settings</span></span>](/previous-versions/windows/)
</dt> <dt>

<span data-ttu-id="7ef21-140">[Auswählen und Verwenden einer Popup Vorlage](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7ef21-140">[How to choose and use a toast template](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="7ef21-141">[Behandeln der Aktivierung über eine Popup Benachrichtigung](/previous-versions/windows/apps/hh761468(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7ef21-141">[How to handle activation from a toast notification](/previous-versions/windows/apps/hh761468(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="7ef21-142">[Abonnieren von Popup Benachrichtigungen](/previous-versions/windows/apps/hh781238(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7ef21-142">[How to opt in for toast notifications](/previous-versions/windows/apps/hh781238(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="7ef21-143">[Auswählen einer Popup Vorlage](/previous-versions/windows/apps/hh761494(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7ef21-143">[Choosing a toast template](/previous-versions/windows/apps/hh761494(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="7ef21-144">[Popup-Audiooptionen](/previous-versions/windows/apps/hh761492(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7ef21-144">[Toast audio options](/previous-versions/windows/apps/hh761492(v=win.10))</span></span>
</dt> </dl>

 

 
