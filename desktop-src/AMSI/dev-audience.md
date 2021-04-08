---
title: Entwickler Audience und Beispielcode
description: In diesem Thema werden die Gruppen von Entwicklern beschrieben, für die die Antimalware-Scan Schnittstelle entworfen wurde.
ms.topic: article
ms.date: 03/20/2019
ms.openlocfilehash: 22cf1156a8fa0aedc212b2ab70e34b984d13470f
ms.sourcegitcommit: 272ba17a215d0d27bb7918fee1192d4954ccc576
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2020
ms.locfileid: "104038479"
---
# <a name="developer-audience-and-sample-code"></a>Entwickler Audience und Beispielcode

Die Antimalware-Scan Schnittstelle ist für die Verwendung durch zwei Gruppen von Entwicklern konzipiert.

- Anwendungsentwickler, die in ihren apps Anforderungen an antischadsoftwareprodukte stellen möchten.
- Ersteller von Antischadsoftware-Produkten von Drittanbietern, die ihren Produkten die besten Features für Anwendungen anbieten sollen.

## <a name="application-developers"></a>Anwendungsentwickler

AMSI wurde speziell entwickelt, um "nicht filterlos Schadsoftware" zu bekämpfen. Anwendungs Typen, die die AMSI-Technologie optimal nutzen können, sind Skript-Engines, Anwendungen, die vor der Verwendung von Speicher Puffern gescannt werden müssen, und Anwendungen, die Dateien verarbeiten, die ausführbaren Code enthalten können (z. b. Microsoft Word-und Excel-Makros oder PDF-Dokumente). Die Nützlichkeit der AMSI-Technologie ist jedoch nicht auf diese Beispiele beschränkt.

Es gibt zwei Möglichkeiten, wie Sie in Ihrer Anwendung mit AMSI verbinden können.

- Mithilfe der AMSI-Win32-APIs. Weitere Informationen finden Sie unter [Antimalware Scan Interface (AMSI)-Funktionen](/windows/desktop/amsi/antimalware-scan-interface-functions).
- Mithilfe der AMSI-com-Schnittstellen. Siehe [ **iamsistream** -Schnittstelle](/windows/desktop/api/amsi/nn-amsi-iamsistream).

Beispielcode, der zeigt, wie AMSI in ihrer com-Anwendung verwendet wird, finden Sie in der [Beispielanwendung für die iamsistream-Schnittstelle](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiStream).

## <a name="third-party-creators-of-antimalware-products"></a>Ersteller von Antischadsoftware-Produkten von Drittanbietern

Als Ersteller von Antischadsoftware-Produkten können Sie entscheiden, ihren eigenen Prozess internen com-Server (eine DLL) zu erstellen und zu registrieren, der als AMSI-Anbieter fungiert. Dieser AMSI-Anbieter muss die [ **iantimalwareprovider** -Schnittstelle](/windows/desktop/api/amsi/nn-amsi-iantimalwareprovider)implementieren, und er muss in-Process ausgeführt werden.

Beachten Sie, dass die AMSI-Anbieter-DLL nach Windows 10, Version 1709 (Fall 2017 Creators ' Update), möglicherweise nicht funktioniert, wenn Sie davon abhängt, dass andere DLLs im Pfad gleichzeitig geladen werden müssen. Um dll-Hijacking zu verhindern, wird empfohlen, dass die Anbieter-DLL ihre Abhängigkeiten explizit (mit einem vollständigen Pfad) mithilfe von sicheren [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryw) -aufrufen oder einer ähnlichen Version lädt. Dies wird empfohlen, anstatt sich auf das **LoadLibrary** -Suchverhalten zu verlassen.

Der folgende Abschnitt zeigt, wie Sie Ihren AMSI-Anbieter registrieren. Vollständigen Beispielcode, der zeigt, wie Sie eine eigene AMSI-Anbieter-DLL erstellen, finden Sie in der [Beispielanwendung iantimalwareprovider Interface](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiProvider).

### <a name="register-your-provider-dll-with-amsi"></a>Registrieren der Anbieter-DLL bei AMSI

Zunächst müssen Sie sicherstellen, dass diese Windows-Registrierungsschlüssel vorhanden sind.

- Hklm\software\microsoft\amsi\providers
- Hklm\software\classes\clsid

Ein AMSI-Anbieter ist ein Prozess interner com-Server. Folglich muss Sie sich bei com registrieren. COM-Klassen werden in registriert `HKLM\SOFTWARE\Classes\CLSID` .

Der folgende Code zeigt, wie Sie einen AMSI-Anbieter registrieren, dessen GUID (in diesem Beispiel) angenommen wird `2E5D8A62-77F9-4F7B-A90C-2744820139B2` .

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

Wenn die dll die [DllRegisterServer-Funktion](/windows/desktop/api/olectl/nf-olectl-dllregisterserver)implementiert, wie im obigen Beispiel gezeigt, können Sie Sie mit der von Windows bereitgestellten ausführbaren Datei registrieren `regsvr32.exe` . Geben Sie an einer Eingabeaufforderung mit erhöhten Rechten einen Befehl in diesem Formular aus.

```cmd
C:>C:\Windows\System32\regsvr32.exe SampleAmsiProvider.dll
```

In diesem Beispiel erstellt der Befehl die folgenden Einträge.

**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2e5d8a62-77 B2).**

&nbsp;&nbsp;&nbsp;&nbsp;**Vorgegebene    REG_SZ Beispiel für die AMSI-Anbieter Implementierung**


**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2e5d8a62-77F 9-4b2} \InprocServer32**

&nbsp;&nbsp;&nbsp;&nbsp;**Vorgegebene    REG_EXPAND_SZ% Program Files% \TestProvider\SampleAmsiProvider.dll**

&nbsp;&nbsp;&nbsp;&nbsp;**ThreadingModel-REG_SZ beides**

Zusätzlich zur regulären com-Registrierung müssen Sie den Anbieter auch bei AMSI registrieren. Hierzu fügen Sie einen Eintrag zum folgenden Schlüssel hinzu.

**Hklm\software\microsoft\amsi\providers**

Beispiel:

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AMSI\Providers\\ {2e5d8a62-77 B2).**
