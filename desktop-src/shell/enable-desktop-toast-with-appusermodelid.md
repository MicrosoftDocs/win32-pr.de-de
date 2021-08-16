---
description: In diesem Thema erfahren Sie, wie Sie eine Verknüpfung für Ihre App erstellen, ihr eine AppUserModelID zuweisen und sie im Startbildschirm.
title: Aktivieren von Desktoppopupbenachrichtigungen über eine AppUserModelID
ms.topic: article
ms.date: 05/31/2018
ms.assetid: BB32CD0A-99E6-47dc-A913-39A7B3027314
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbSyntax
ms.openlocfilehash: 517c2b72e830c00b105048adc63923291f896cd5d0d77569c91b1aa12e034e60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459792"
---
# <a name="how-to-enable-desktop-toast-notifications-through-an-appusermodelid"></a>Aktivieren von Desktoppopupbenachrichtigungen über eine AppUserModelID

In diesem Thema erfahren Sie, wie Sie eine Verknüpfung für Ihre App erstellen, ihr eine [AppUserModelID](appids.md)zuweisen und sie im Startbildschirm. Es wird dringend empfohlen, dies im Windows Installer und nicht im Code Ihrer App zu tun. Ohne eine gültige Verknüpfung, die im Startbildschirm oder **unter** Alle Programme installiert ist, können Sie keine Popupbenachrichtigung von einer Desktop-App aus erstellen.

> [!Note]  
> Die in diesem Thema verwendeten Beispielmethoden sind aus dem [Desktop-Popupbeispiel entnommen.](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts)

 

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   COM

### <a name="prerequisites"></a>Voraussetzungen

-   Bibliotheken
    -   C++: Runtime.object.lib
    -   C \# : Windows. Winmd
-   C \# : Windows API Code Pack für Microsoft .NET Framework
-   Eine Version von Microsoft Visual Studio, die mindestens Windows 8

## <a name="instructions"></a>Anweisungen

### <a name="step-1-prepare-the-shortcut-to-be-created"></a>Schritt 1: Vorbereiten der zu erstellenden Verknüpfung

In diesem Beispiel wird zunächst der Pfad des App-Datenordners des Benutzers über die [**GetEnvironmentVariable-Funktion**](/windows/win32/api/processenv/nf-processenv-getenvironmentvariablea) bestimmt. Anschließend wird der vollständige Pfad zur Verknüpfung erstellt, es wird ermittelt, dass an diesem Speicherort noch keine Verknüpfung mit diesem Namen vorhanden ist, und diese Informationen werden an eine andere Methode übertragen, die die Verknüpfung erstellt und installiert.

Beachten Sie, dass die Verknüpfung pro Benutzer oder pro App bereitgestellt werden kann.


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



### <a name="step-2-create-the-shortcut-and-install-it-in-the-start-screen"></a>Schritt 2: Erstellen Sie die Verknüpfung, und installieren Sie sie im Startbildschirm

In diesem Beispiel wird auch der Eigenschaftenspeicher der Verknüpfung abgerufen und die erforderliche [System.AppUserModel.ID-Eigenschaft](../properties/props-system-appusermodel-id.md) aus einer zuvor definierten Variablen `AppID` festgelegt.


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



## <a name="remarks"></a>Hinweise

Als Alternative zu dem in diesem Thema gezeigten Ansatz können Sie ein Framework wie das Windows Installer XML (WiX) verwenden, um die Verknüpfung zu generieren und als Teil des Windows-Installers bereitzustellen. In diesem Fall sollte dieser Code in der MSI und nicht im Code der App enthalten sein. Weitere Informationen finden Sie in der WiX-Beispielkonfigurationsdatei, die im Beispiel [Senden von Popupbenachrichtigungen von Desktop-Apps enthalten](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208)) ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schnellstart: Senden einer Popupbenachrichtigung vom Desktop](quickstart-sending-desktop-toast.md)
</dt> <dt>

[Beispiel zum Senden von Toastbenachrichtigungen aus Desktop-Apps](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208))
</dt> <dt>

[Anwendungsbenutzermodell-IDs (AppUserModelIDs)](appids.md)
</dt> <dt>

[How to: Install the Windows Installer XML (WiX) Tools](/previous-versions/windows/server-essentials/gg513936(v=msdn.10))
</dt> <dt>

[Popup-XML-Schema](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

[Übersicht über Popupbenachrichtigungen](/previous-versions/windows/apps/hh779727(v=win.10))
</dt> <dt>

[Schnellstart: Senden einer Popupbenachrichtigung](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Schnellstart: Senden einer Popup-Pushbenachrichtigung](/previous-versions/windows/hh761487(v=win.10))
</dt> <dt>

[Richtlinien und Checkliste für Popupbenachrichtigungen](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[Hinzufügen von Bildern zu einer Popupvorlage](/previous-versions/windows/)
</dt> <dt>

[Überprüfen der Einstellungen für Popupbenachrichtigungen](/previous-versions/windows/)
</dt> <dt>

[Auswählen und Verwenden einer Popupvorlage](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Behandeln der Aktivierung von Popupbenachrichtigungen](/previous-versions/windows/apps/hh761468(v=win.10))
</dt> <dt>

[Aktivieren von Popupbenachrichtigungen](/previous-versions/windows/apps/hh781238(v=win.10))
</dt> <dt>

[Auswählen einer Popupvorlage](/previous-versions/windows/apps/hh761494(v=win.10))
</dt> <dt>

[Audiooptionen für Popups](/previous-versions/windows/apps/hh761492(v=win.10))
</dt> </dl>

 

 
