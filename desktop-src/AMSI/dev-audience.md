---
title: Zielgruppe für Entwickler und Beispielcode
description: In diesem Thema werden die Entwicklergruppen beschrieben, für die die Antimalware Scan Interface entworfen wurde.
ms.topic: article
ms.date: 03/20/2019
ms.openlocfilehash: 4ac11c75d5714d0706bed28264f9fa1bf03432af82107826178007e2c42243c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579910"
---
# <a name="developer-audience-and-sample-code"></a>Zielgruppe für Entwickler und Beispielcode

Die Antimalware Scan Interface ist für die Verwendung durch zwei Gruppen von Entwicklern konzipiert.

- Anwendungsentwickler, die Anforderungen an Antischadsoftwareprodukte aus ihren Apps stellen möchten.
- Ersteller von Antischadsoftwareprodukten von Drittanbietern, die möchten, dass ihre Produkte anwendungen die besten Features bieten.

## <a name="application-developers"></a>Anwendungsentwickler

AMSI ist insbesondere dafür konzipiert, "dateilose Schadsoftware" zu schützen. Zu den Anwendungstypen, die am besten die AMSI-Technologie nutzen können, gehören Skript-Engines, Anwendungen, die Speicherpuffer vor der Verwendung scannen müssen, und Anwendungen, die Dateien verarbeiten, die ausführbaren Code enthalten können, der nicht peinlich ist (z. B. Microsoft Word- und Excel-Makros oder PDF-Dokumente). Die Nützlichkeit der AMSI-Technologie ist jedoch nicht auf diese Beispiele beschränkt.

Es gibt zwei Möglichkeiten, wie Sie eine Schnittstelle mit AMSI in Ihrer Anwendung verwenden können.

- Mithilfe der AMSI Win32-APIs. Siehe [Antimalware Scan Interface (AMSI)-Funktionen](/windows/desktop/amsi/antimalware-scan-interface-functions).
- Mithilfe der AMSI COM-Schnittstellen. Siehe [ **IAmsiStream-Schnittstelle**](/windows/desktop/api/amsi/nn-amsi-iamsistream).

Beispielcode, der zeigt, wie AMSI in Ihrer COM-Anwendung verwendet wird, finden Sie in der [IAmsiStream-Schnittstellenbeispielanwendung](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiStream).

## <a name="third-party-creators-of-antimalware-products"></a>Ersteller von Antischadsoftwareprodukten von Drittanbietern

Als Ersteller von Antischadsoftwareprodukten können Sie ihren eigenen Prozess-COM-Server (eine DLL) erstellen und registrieren, um als AMSI-Anbieter zu arbeiten. Dieser AMSI-Anbieter muss die [ **IAntimalwareProvider-Schnittstelle** implementieren](/windows/desktop/api/amsi/nn-amsi-iantimalwareprovider)und prozessintern ausgeführt werden.

Beachten Sie, dass ihre AMSI-Anbieter-DLL nach Windows 10 Version 1709 (Creators Update vom Fall 2017) möglicherweise nicht funktioniert, wenn sie von anderen DLLs in ihrem Pfad abhängig ist, die gleichzeitig geladen werden. Um DLL-Hijacking zu verhindern, empfiehlt es sich, dass Ihre Anbieter-DLL ihre Abhängigkeiten explizit (mit einem vollständigen Pfad) mithilfe sicherer [**LoadLibrary-Aufrufe**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryw) oder entsprechender Aufrufe geladen. Dies wird empfohlen, anstatt sich auf das **Suchverhalten von LoadLibrary** zu verlassen.

Im folgenden Abschnitt wird gezeigt, wie Sie Ihren AMSI-Anbieter registrieren. Den vollständigen Beispielcode, der zeigt, wie Sie Ihre eigene AMSI-Anbieter-DLL erstellen, finden Sie in der [IAntimalwareProvider-Schnittstellenbeispielanwendung](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiProvider).

### <a name="register-your-provider-dll-with-amsi"></a>Registrieren Ihrer Anbieter-DLL bei AMSI

Zunächst müssen Sie sicherstellen, dass diese Windows Registrierungsschlüssel vorhanden sind.

- HKLM\SOFTWARE\Microsoft\AMSI\Providers
- HKLM\SOFTWARE\Classes\CLSID

Ein AMSI-Anbieter ist ein In-Process-COM-Server. Daher muss es sich selbst bei COM registrieren. COM-Klassen werden in `HKLM\SOFTWARE\Classes\CLSID` registriert.

Der folgende Code zeigt, wie Sie einen AMSI-Anbieter registrieren, dessen GUID (in diesem Beispiel) angenommen `2E5D8A62-77F9-4F7B-A90C-2744820139B2` wird.

```cpp
#include <strsafe.h>
...
HRESULT SetKeyStringValue(_In_ HKEY key, _In_opt_ PCWSTR subkey, _In_opt_ PCWSTR valueName, _In_ PCWSTR stringValue)
{
    LONG status = RegSetKeyValue(key, subkey, valueName, REG_SZ, stringValue, (wcslen(stringValue) + 1) * sizeof(wchar_t));
    return HRESULT_FROM_WIN32(status);
}

STDAPI DllRegisterServer()
{
    wchar_t modulePath[MAX_PATH];
    if (GetModuleFileName(g_currentModule, modulePath, ARRAYSIZE(modulePath)) >= ARRAYSIZE(modulePath))
    {
        return E_UNEXPECTED;
    }

    // Create a standard COM registration for our CLSID.
    // The class must be registered as "Both" threading model,
    // and support multithreaded access.
    wchar_t clsidString[40];
    if (StringFromGUID2(__uuidof(SampleAmsiProvider), clsidString, ARRAYSIZE(clsidString)) == 0)
    {
        return E_UNEXPECTED;
    }

    wchar_t keyPath[200];
    HRESULT hr = StringCchPrintf(keyPath, ARRAYSIZE(keyPath), L"Software\\Classes\\CLSID\\%ls", clsidString);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, nullptr, L"SampleAmsiProvider");
    if (FAILED(hr)) return hr;

    hr = StringCchPrintf(keyPath, ARRAYSIZE(keyPath), L"Software\\Classes\\CLSID\\%ls\\InProcServer32", clsidString);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, nullptr, modulePath);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, L"ThreadingModel", L"Both");
    if (FAILED(hr)) return hr;

    // Register this CLSID as an anti-malware provider.
    hr = StringCchPrintf(keyPath, ARRAYSIZE(keyPath), L"Software\\Microsoft\\AMSI\\Providers\\%ls", clsidString);
    if (FAILED(hr)) return hr;

    hr = SetKeyStringValue(HKEY_LOCAL_MACHINE, keyPath, nullptr, L"SampleAmsiProvider");
    if (FAILED(hr)) return hr;

    return S_OK;
}
```

Wenn Ihre DLL wie im obigen Beispiel die [DllRegisterServer-Funktion](/windows/desktop/api/olectl/nf-olectl-dllregisterserver)implementiert, können Sie sie mithilfe der Windows ausführbaren Datei `regsvr32.exe` registrieren. Geben Sie an einer Eingabeaufforderung mit erhöhten Rechten einen Befehl dieses Formulars aus.

```cmd
C:>C:\Windows\System32\regsvr32.exe SampleAmsiProvider.dll
```

In diesem Beispiel erstellt der Befehl die folgenden Einträge.

**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**

&nbsp;&nbsp;&nbsp;&nbsp;**(Standard)    REG_SZ Amsi-Beispielanbieterimplementierung**


**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}\InprocServer32**

&nbsp;&nbsp;&nbsp;&nbsp;**(Standard)    REG_EXPAND_SZ %ProgramFiles%\TestProvider\SampleAmsiProvider.dll**

&nbsp;&nbsp;&nbsp;&nbsp;**ThreadingModel REG_SZ Beides**

Zusätzlich zur regulären COM-Registrierung müssen Sie den Anbieter auch bei AMSI registrieren. Dazu fügen Sie dem folgenden Schlüssel einen Eintrag hinzu.

**HKLM\SOFTWARE\Microsoft\AMSI\Providers**

Beispiel:

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AMSI\Providers\\ {2E5D8A62-77F9-4F7B-A90C-2744820139B2}**
