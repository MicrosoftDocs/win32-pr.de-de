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
# <a name="developer-audience-and-sample-code"></a><span data-ttu-id="4749c-103">Entwickler Audience und Beispielcode</span><span class="sxs-lookup"><span data-stu-id="4749c-103">Developer audience, and sample code</span></span>

<span data-ttu-id="4749c-104">Die Antimalware-Scan Schnittstelle ist für die Verwendung durch zwei Gruppen von Entwicklern konzipiert.</span><span class="sxs-lookup"><span data-stu-id="4749c-104">The Antimalware Scan Interface is designed for use by two groups of developers.</span></span>

- <span data-ttu-id="4749c-105">Anwendungsentwickler, die in ihren apps Anforderungen an antischadsoftwareprodukte stellen möchten.</span><span class="sxs-lookup"><span data-stu-id="4749c-105">Application developers who want to make requests to antimalware products from within their apps.</span></span>
- <span data-ttu-id="4749c-106">Ersteller von Antischadsoftware-Produkten von Drittanbietern, die ihren Produkten die besten Features für Anwendungen anbieten sollen.</span><span class="sxs-lookup"><span data-stu-id="4749c-106">Third-party creators of antimalware products who want their products to offer the best features to applications.</span></span>

## <a name="application-developers"></a><span data-ttu-id="4749c-107">Anwendungsentwickler</span><span class="sxs-lookup"><span data-stu-id="4749c-107">Application developers</span></span>

<span data-ttu-id="4749c-108">AMSI wurde speziell entwickelt, um "nicht filterlos Schadsoftware" zu bekämpfen.</span><span class="sxs-lookup"><span data-stu-id="4749c-108">AMSI is designed in particular to combat "fileless malware".</span></span> <span data-ttu-id="4749c-109">Anwendungs Typen, die die AMSI-Technologie optimal nutzen können, sind Skript-Engines, Anwendungen, die vor der Verwendung von Speicher Puffern gescannt werden müssen, und Anwendungen, die Dateien verarbeiten, die ausführbaren Code enthalten können (z. b. Microsoft Word-und Excel-Makros oder PDF-Dokumente).</span><span class="sxs-lookup"><span data-stu-id="4749c-109">Application types that can optimally leverage AMSI technology include script engines, applications that need memory buffers to be scanned before using them, and applications that process files that can contain non-PE executable code (such as Microsoft Word and Excel macros, or PDF documents).</span></span> <span data-ttu-id="4749c-110">Die Nützlichkeit der AMSI-Technologie ist jedoch nicht auf diese Beispiele beschränkt.</span><span class="sxs-lookup"><span data-stu-id="4749c-110">However, the usefulness of AMSI technology is not limited to those examples.</span></span>

<span data-ttu-id="4749c-111">Es gibt zwei Möglichkeiten, wie Sie in Ihrer Anwendung mit AMSI verbinden können.</span><span class="sxs-lookup"><span data-stu-id="4749c-111">There are two ways in which you can interface with AMSI in your application.</span></span>

- <span data-ttu-id="4749c-112">Mithilfe der AMSI-Win32-APIs.</span><span class="sxs-lookup"><span data-stu-id="4749c-112">By using the AMSI Win32 APIs.</span></span> <span data-ttu-id="4749c-113">Weitere Informationen finden Sie unter [Antimalware Scan Interface (AMSI)-Funktionen](/windows/desktop/amsi/antimalware-scan-interface-functions).</span><span class="sxs-lookup"><span data-stu-id="4749c-113">See [Antimalware Scan Interface (AMSI) functions](/windows/desktop/amsi/antimalware-scan-interface-functions).</span></span>
- <span data-ttu-id="4749c-114">Mithilfe der AMSI-com-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="4749c-114">By using the AMSI COM interfaces.</span></span> <span data-ttu-id="4749c-115">Siehe [ **iamsistream** -Schnittstelle](/windows/desktop/api/amsi/nn-amsi-iamsistream).</span><span class="sxs-lookup"><span data-stu-id="4749c-115">See [**IAmsiStream** interface](/windows/desktop/api/amsi/nn-amsi-iamsistream).</span></span>

<span data-ttu-id="4749c-116">Beispielcode, der zeigt, wie AMSI in ihrer com-Anwendung verwendet wird, finden Sie in der [Beispielanwendung für die iamsistream-Schnittstelle](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiStream).</span><span class="sxs-lookup"><span data-stu-id="4749c-116">For sample code showing how to consume AMSI within your COM application, see the [IAmsiStream interface sample application](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiStream).</span></span>

## <a name="third-party-creators-of-antimalware-products"></a><span data-ttu-id="4749c-117">Ersteller von Antischadsoftware-Produkten von Drittanbietern</span><span class="sxs-lookup"><span data-stu-id="4749c-117">Third-party creators of antimalware products</span></span>

<span data-ttu-id="4749c-118">Als Ersteller von Antischadsoftware-Produkten können Sie entscheiden, ihren eigenen Prozess internen com-Server (eine DLL) zu erstellen und zu registrieren, der als AMSI-Anbieter fungiert.</span><span class="sxs-lookup"><span data-stu-id="4749c-118">As a creator of antimalware products, you can choose to author and register your own in-process COM server (a DLL) to function as an AMSI provider.</span></span> <span data-ttu-id="4749c-119">Dieser AMSI-Anbieter muss die [ **iantimalwareprovider** -Schnittstelle](/windows/desktop/api/amsi/nn-amsi-iantimalwareprovider)implementieren, und er muss in-Process ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4749c-119">That AMSI provider must implement the [**IAntimalwareProvider** interface](/windows/desktop/api/amsi/nn-amsi-iantimalwareprovider), and it must run in-process.</span></span>

<span data-ttu-id="4749c-120">Beachten Sie, dass die AMSI-Anbieter-DLL nach Windows 10, Version 1709 (Fall 2017 Creators ' Update), möglicherweise nicht funktioniert, wenn Sie davon abhängt, dass andere DLLs im Pfad gleichzeitig geladen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="4749c-120">Note that, after Windows 10, version 1709 (the Fall 2017 Creators' Update), your AMSI provider DLL may not work if it depends upon other DLLs in its path to be loaded at the same time.</span></span> <span data-ttu-id="4749c-121">Um dll-Hijacking zu verhindern, wird empfohlen, dass die Anbieter-DLL ihre Abhängigkeiten explizit (mit einem vollständigen Pfad) mithilfe von sicheren [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryw) -aufrufen oder einer ähnlichen Version lädt.</span><span class="sxs-lookup"><span data-stu-id="4749c-121">To prevent DLL hijacking, we recommend that your provider DLL load its dependencies explicitly (with a full path) using secure [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryw) calls, or equivalent.</span></span> <span data-ttu-id="4749c-122">Dies wird empfohlen, anstatt sich auf das **LoadLibrary** -Suchverhalten zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="4749c-122">We recommend this instead of relying on the **LoadLibrary** search behavior.</span></span>

<span data-ttu-id="4749c-123">Der folgende Abschnitt zeigt, wie Sie Ihren AMSI-Anbieter registrieren.</span><span class="sxs-lookup"><span data-stu-id="4749c-123">The section below shows how to register your AMSI provider.</span></span> <span data-ttu-id="4749c-124">Vollständigen Beispielcode, der zeigt, wie Sie eine eigene AMSI-Anbieter-DLL erstellen, finden Sie in der [Beispielanwendung iantimalwareprovider Interface](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiProvider).</span><span class="sxs-lookup"><span data-stu-id="4749c-124">For full sample code showing how to author your own AMSI provider DLL, see the [IAntimalwareProvider interface sample application](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/AmsiProvider).</span></span>

### <a name="register-your-provider-dll-with-amsi"></a><span data-ttu-id="4749c-125">Registrieren der Anbieter-DLL bei AMSI</span><span class="sxs-lookup"><span data-stu-id="4749c-125">Register your provider DLL with AMSI</span></span>

<span data-ttu-id="4749c-126">Zunächst müssen Sie sicherstellen, dass diese Windows-Registrierungsschlüssel vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="4749c-126">To begin with, you need to ensure that these Windows Registry keys exist.</span></span>

- <span data-ttu-id="4749c-127">Hklm\software\microsoft\amsi\providers</span><span class="sxs-lookup"><span data-stu-id="4749c-127">HKLM\SOFTWARE\Microsoft\AMSI\Providers</span></span>
- <span data-ttu-id="4749c-128">Hklm\software\classes\clsid</span><span class="sxs-lookup"><span data-stu-id="4749c-128">HKLM\SOFTWARE\Classes\CLSID</span></span>

<span data-ttu-id="4749c-129">Ein AMSI-Anbieter ist ein Prozess interner com-Server.</span><span class="sxs-lookup"><span data-stu-id="4749c-129">An AMSI provider is an in-process COM server.</span></span> <span data-ttu-id="4749c-130">Folglich muss Sie sich bei com registrieren.</span><span class="sxs-lookup"><span data-stu-id="4749c-130">Consequently, it needs to register itself with COM.</span></span> <span data-ttu-id="4749c-131">COM-Klassen werden in registriert `HKLM\SOFTWARE\Classes\CLSID` .</span><span class="sxs-lookup"><span data-stu-id="4749c-131">COM classes are registered in `HKLM\SOFTWARE\Classes\CLSID`.</span></span>

<span data-ttu-id="4749c-132">Der folgende Code zeigt, wie Sie einen AMSI-Anbieter registrieren, dessen GUID (in diesem Beispiel) angenommen wird `2E5D8A62-77F9-4F7B-A90C-2744820139B2` .</span><span class="sxs-lookup"><span data-stu-id="4749c-132">The code below shows how to register an AMSI provider, whose GUID (for this example) we will assume is `2E5D8A62-77F9-4F7B-A90C-2744820139B2`.</span></span>

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

<span data-ttu-id="4749c-133">Wenn die dll die [DllRegisterServer-Funktion](/windows/desktop/api/olectl/nf-olectl-dllregisterserver)implementiert, wie im obigen Beispiel gezeigt, können Sie Sie mit der von Windows bereitgestellten ausführbaren Datei registrieren `regsvr32.exe` .</span><span class="sxs-lookup"><span data-stu-id="4749c-133">If your DLL implements the [DllRegisterServer function](/windows/desktop/api/olectl/nf-olectl-dllregisterserver), as the example above does, then you can register it by using the Windows-supplied executable `regsvr32.exe`.</span></span> <span data-ttu-id="4749c-134">Geben Sie an einer Eingabeaufforderung mit erhöhten Rechten einen Befehl in diesem Formular aus.</span><span class="sxs-lookup"><span data-stu-id="4749c-134">From an elevated command prompt, issue a command of this form.</span></span>

```cmd
C:>C:\Windows\System32\regsvr32.exe SampleAmsiProvider.dll
```

<span data-ttu-id="4749c-135">In diesem Beispiel erstellt der Befehl die folgenden Einträge.</span><span class="sxs-lookup"><span data-stu-id="4749c-135">In this example, the command creates the following entries.</span></span>

<span data-ttu-id="4749c-136">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2e5d8a62-77 B2).**</span><span class="sxs-lookup"><span data-stu-id="4749c-136">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\{2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span></span>

<span data-ttu-id="4749c-137">&nbsp;&nbsp;&nbsp;&nbsp;**Vorgegebene    REG_SZ Beispiel für die AMSI-Anbieter Implementierung**</span><span class="sxs-lookup"><span data-stu-id="4749c-137">&nbsp;&nbsp;&nbsp;&nbsp;**(Default)    REG_SZ    Sample AMSI Provider implementation**</span></span>


<span data-ttu-id="4749c-138">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\ {2e5d8a62-77F 9-4b2} \InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="4749c-138">**HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID\\{2E5D8A62-77F9-4F7B-A90C-2744820139B2}\InprocServer32**</span></span>

<span data-ttu-id="4749c-139">&nbsp;&nbsp;&nbsp;&nbsp;**Vorgegebene    REG_EXPAND_SZ% Program Files% \TestProvider\SampleAmsiProvider.dll**</span><span class="sxs-lookup"><span data-stu-id="4749c-139">&nbsp;&nbsp;&nbsp;&nbsp;**(Default)    REG_EXPAND_SZ    %ProgramFiles%\TestProvider\SampleAmsiProvider.dll**</span></span>

<span data-ttu-id="4749c-140">&nbsp;&nbsp;&nbsp;&nbsp;**ThreadingModel-REG_SZ beides**</span><span class="sxs-lookup"><span data-stu-id="4749c-140">&nbsp;&nbsp;&nbsp;&nbsp;**ThreadingModel    REG_SZ    Both**</span></span>

<span data-ttu-id="4749c-141">Zusätzlich zur regulären com-Registrierung müssen Sie den Anbieter auch bei AMSI registrieren.</span><span class="sxs-lookup"><span data-stu-id="4749c-141">In addition to regular COM registration, you also need to enroll the provider with AMSI.</span></span> <span data-ttu-id="4749c-142">Hierzu fügen Sie einen Eintrag zum folgenden Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="4749c-142">You do that by adding an entry to the following key.</span></span>

<span data-ttu-id="4749c-143">**Hklm\software\microsoft\amsi\providers**</span><span class="sxs-lookup"><span data-stu-id="4749c-143">**HKLM\SOFTWARE\Microsoft\AMSI\Providers**</span></span>

<span data-ttu-id="4749c-144">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="4749c-144">For example,</span></span>

<span data-ttu-id="4749c-145">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AMSI\Providers\\ {2e5d8a62-77 B2).**</span><span class="sxs-lookup"><span data-stu-id="4749c-145">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AMSI\Providers\\{2E5D8A62-77F9-4F7B-A90C-2744820139B2}**</span></span>
