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
# <a name="how-to-enable-desktop-toast-notifications-through-an-appusermodelid"></a>Aktivieren von Desktoppopupbenachrichtigungen über eine AppUserModelID

In diesem Thema erfahren Sie, wie Sie eine Verknüpfung für Ihre APP erstellen, ihr eine [appusermodelid](appids.md)zuweisen und Sie auf dem Start Bildschirm installieren. Es wird dringend empfohlen, dass Sie dies in der Windows Installer statt im Code Ihrer APP tun. Wenn keine gültige Verknüpfung auf dem Start Bildschirm oder in **allen Programmen** installiert ist, können Sie keine Popup Benachrichtigung von einer Desktop-App aus aufrichten.

> [!Note]  
> Die in diesem Thema verwendeten Beispiel Methoden stammen aus dem [Desktop-Popup Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts).

 

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   COM

### <a name="prerequisites"></a>Voraussetzungen

-   Bibliotheken
    -   C++: Runtime. Object. lib
    -   C \# : Windows. winmd
-   C \# : Windows-API-Code Paket für Microsoft .NET Framework
-   Eine Version von Microsoft Visual Studio, die mindestens Windows 8 unterstützt.

## <a name="instructions"></a>Instructions

### <a name="step-1-prepare-the-shortcut-to-be-created"></a>Schritt 1: Vorbereiten der zu erstellenden Verknüpfung

In diesem Beispiel wird zuerst der Pfad des Ordners für App-Daten des Benutzers über die [**GetEnvironmentVariable**](/windows/win32/api/processenv/nf-processenv-getenvironmentvariablea) -Funktion bestimmt. Anschließend wird der vollständige Pfad zur Verknüpfung erstellt, es wird festgelegt, dass an diesem Speicherort noch keine Verknüpfung dieses Namens vorhanden ist, und diese Informationen werden an eine andere Methode weitergeleitet, die die Verknüpfung erstellt und installiert.

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



### <a name="step-2-create-the-shortcut-and-install-it-in-the-start-screen"></a>Schritt 2: Erstellen Sie die Verknüpfung, und installieren Sie Sie auf dem Start Bildschirm.

In diesem Beispiel wird auch der Eigenschaften Speicher der Verknüpfung abgerufen, und die erforderliche [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) -Eigenschaft wird von einer zuvor definierten Variablen,, festgelegt `AppID` .


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



## <a name="remarks"></a>Bemerkungen

Als Alternative zu dem in diesem Thema gezeigten Ansatz können Sie ein Framework, wie z. b. das Windows Installer-XML (WiX), verwenden, um die Verknüpfung zu generieren und als Teil der Windows Installer bereitzustellen. In diesem Fall sollte dieser Code in der MSI-Datei statt im Code der App enthalten sein. Weitere Informationen finden Sie in der WiX-Beispielkonfigurationsdatei im Beispiel zum [Senden von Popup Benachrichtigungen aus Desktop-Apps](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208)) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schnellstart: Senden einer Popup Benachrichtigung vom Desktop](quickstart-sending-desktop-toast.md)
</dt> <dt>

[Beispiel zum Senden von Toastbenachrichtigungen aus Desktop-Apps](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208))
</dt> <dt>

[Anwendungs Benutzer Modell-IDs (appusermudelids)](appids.md)
</dt> <dt>

[Gewusst wie: Installieren der WiX-Tools (Windows Installer XML)](/previous-versions/windows/server-essentials/gg513936(v=msdn.10))
</dt> <dt>

[Popup-XML-Schema](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

[Übersicht über Popup Benachrichtigungen](/previous-versions/windows/apps/hh779727(v=win.10))
</dt> <dt>

[Schnellstart: Senden einer Popup Benachrichtigung](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Schnellstart: Senden einer Popup-Pushbenachrichtigung](/previous-versions/windows/hh761487(v=win.10))
</dt> <dt>

[Richtlinien und Prüfliste für Popup Benachrichtigungen](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[Hinzufügen von Bildern zu einer Popup Vorlage](/previous-versions/windows/)
</dt> <dt>

[Überprüfen der Popup Benachrichtigungseinstellungen](/previous-versions/windows/)
</dt> <dt>

[Auswählen und Verwenden einer Popup Vorlage](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Behandeln der Aktivierung über eine Popup Benachrichtigung](/previous-versions/windows/apps/hh761468(v=win.10))
</dt> <dt>

[Abonnieren von Popup Benachrichtigungen](/previous-versions/windows/apps/hh781238(v=win.10))
</dt> <dt>

[Auswählen einer Popup Vorlage](/previous-versions/windows/apps/hh761494(v=win.10))
</dt> <dt>

[Popup-Audiooptionen](/previous-versions/windows/apps/hh761492(v=win.10))
</dt> </dl>

 

 
