---
title: Der com-Erhöhungs Moniker.
description: Mit dem com-Erweiterungs Moniker können Anwendungen, die unter der Benutzerkontensteuerung (User Account Control, UAC) ausgeführt werden, com-Klassen mit erhöhten Rechten aktivieren. Weitere Informationen finden Sie unter Fokus auf die geringsten Berechtigungen.
ms.assetid: 1595ebb8-65af-4609-b3e7-a21209e64391
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc80774764cb99e63ed3334a8c0f9c8cedd2500
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474437"
---
# <a name="the-com-elevation-moniker"></a><span data-ttu-id="b57cb-104">Der com-Erhöhungs Moniker.</span><span class="sxs-lookup"><span data-stu-id="b57cb-104">The COM Elevation Moniker</span></span>

<span data-ttu-id="b57cb-105">Mit dem com-Erweiterungs Moniker können Anwendungen, die unter der Benutzerkontensteuerung (User Account Control, UAC) ausgeführt werden, com-Klassen mit erhöhten Rechten aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b57cb-105">The COM elevation moniker allows applications that are running under user account control (UAC) to activate COM classes with elevated privileges.</span></span> <span data-ttu-id="b57cb-106">Weitere Informationen finden Sie unter [Fokus auf die geringsten Berechtigungen](/previous-versions/dotnet/articles/aa480194(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="b57cb-106">For more information, see [Focus on Least Privilege](/previous-versions/dotnet/articles/aa480194(v=msdn.10)).</span></span>

## <a name="when-to-use-the-elevation-moniker"></a><span data-ttu-id="b57cb-107">Verwendung des Erhöhungs Monikers</span><span class="sxs-lookup"><span data-stu-id="b57cb-107">When to Use the Elevation Moniker</span></span>

<span data-ttu-id="b57cb-108">Der Erweiterungs-Moniker wird zum Aktivieren einer com-Klasse verwendet, um eine bestimmte und eingeschränkte Funktion zu erreichen, die erhöhte Berechtigungen erfordert, z. b. das Ändern des Systemdatums und der Systemzeit.</span><span class="sxs-lookup"><span data-stu-id="b57cb-108">The elevation moniker is used to activate a COM class to accomplish a specific and limited function that requires elevated privileges, such as changing the system date and time.</span></span>

<span data-ttu-id="b57cb-109">Erhöhung erfordert die Teilnahme an einer com-Klasse und Ihrem Client.</span><span class="sxs-lookup"><span data-stu-id="b57cb-109">Elevation requires participation from both a COM class and its client.</span></span> <span data-ttu-id="b57cb-110">Die com-Klasse muss so konfiguriert werden, dass Sie eine Erhöhung der Rechte unterstützt, indem Sie Ihren Registrierungs Eintrag kommentiert, wie im Abschnitt "Anforderungen" beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b57cb-110">The COM class must be configured to support elevation by annotating its registry entry, as described in the Requirements section.</span></span> <span data-ttu-id="b57cb-111">Der com-Client muss mit dem Erhöhungs Moniker eine Erhöhung anfordern.</span><span class="sxs-lookup"><span data-stu-id="b57cb-111">The COM client must request elevation by using the elevation moniker.</span></span>

<span data-ttu-id="b57cb-112">Der Erhöhungs Moniker ist nicht für die Bereitstellung der Anwendungs Kompatibilität vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="b57cb-112">The elevation moniker is not intended to provide application compatibility.</span></span> <span data-ttu-id="b57cb-113">Wenn Sie z. b. eine Legacy-COM-Anwendung, z. b. WinWord, als erweiterten Server ausführen möchten, sollten Sie die ausführbare com-Client Datei so konfigurieren, dass Sie eine Erhöhung erfordert, anstatt die Klasse der Legacy Anwendung mit dem Erhöhungs Moniker zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b57cb-113">For example, if you want to run a legacy COM application such as WinWord as an elevated server, you should configure the COM client executable to require elevation, rather than activating the legacy application's class with the elevation moniker.</span></span> <span data-ttu-id="b57cb-114">Wenn der com-Client mit erhöhten Rechten mit der CLSID der Legacy Anwendung [**cokreatanstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) aufruft, wird der Status des Clients mit erhöhten Rechten an den Server Prozess weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="b57cb-114">When the elevated COM client calls [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) using the legacy application's CLSID, the client's elevated state will flow to the server process.</span></span>

<span data-ttu-id="b57cb-115">Nicht alle com-Funktionen sind mit der Erhöhung der Rechte kompatibel.</span><span class="sxs-lookup"><span data-stu-id="b57cb-115">Not all COM functionality is compatible with elevation.</span></span> <span data-ttu-id="b57cb-116">Zu den Funktionen, die nicht funktionieren, gehören:</span><span class="sxs-lookup"><span data-stu-id="b57cb-116">The functionality that will not work includes:</span></span>

-   <span data-ttu-id="b57cb-117">Die Erhöhung der Rechte erfolgt nicht von einem Client zu einem com-Remote Server.</span><span class="sxs-lookup"><span data-stu-id="b57cb-117">Elevation does not flow from a client to a remote COM server.</span></span> <span data-ttu-id="b57cb-118">Wenn ein Client einen com-Remote Server mit dem Erhöhungs Moniker aktiviert, wird der Server nicht erhöht, auch wenn er eine Erhöhung der Rechte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b57cb-118">If a client activates a remote COM server with the elevation moniker, the server will not be elevated, even if it supports elevation.</span></span>
-   <span data-ttu-id="b57cb-119">Wenn eine COM-Klasse mit erhöhten Rechten während eines com-Aufrufes einen Identitätswechsel verwendet, verliert sie während des Identitäts Wechsels möglicherweise ihre erhöhten Rechte.</span><span class="sxs-lookup"><span data-stu-id="b57cb-119">If an elevated COM class uses impersonation during a COM call, it might lose its elevated privileges during the impersonation.</span></span>
-   <span data-ttu-id="b57cb-120">Wenn ein com-Server mit erhöhten Rechten eine Klasse in der Running Object Table (rot) registriert, ist die Klasse nicht für Clients ohne erhöhte Rechte verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b57cb-120">If an elevated COM server registers a class in the running object table (ROT), the class will not be available to non-elevated clients.</span></span>
-   <span data-ttu-id="b57cb-121">Ein Prozess, der mit dem UAC-Mechanismus erhöht wurde, lädt während der com-Aktivierungen keine benutzerspezifischen Klassen.</span><span class="sxs-lookup"><span data-stu-id="b57cb-121">A process elevated by using the UAC mechanism does not load per-user classes during COM activations.</span></span> <span data-ttu-id="b57cb-122">Bei com-Anwendungen bedeutet dies, dass die com-Klassen der Anwendung in der Registrierungs Struktur des **\_ lokalen \_ HKEY** -Computers installiert werden müssen, wenn die Anwendung sowohl von nicht privilegierten als auch von privilegierten Konten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b57cb-122">For COM applications, this means that the application's COM classes must be installed in the **HKEY\_LOCAL\_MACHINE** registry hive if the application is to be used both by non-privileged and privileged accounts.</span></span> <span data-ttu-id="b57cb-123">Die com-Klassen der Anwendung müssen nur in der **HKEY \_ Users** -Struktur installiert werden, wenn die Anwendung nie von privilegierten Konten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b57cb-123">The application's COM classes need only be installed in the **HKEY\_USERS** hive if the application is never used by privileged accounts.</span></span>
-   <span data-ttu-id="b57cb-124">Drag & Drop ist in Anwendungen mit erhöhten Rechten nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="b57cb-124">Drag and drop is not allowed from non-elevated to elevated applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="b57cb-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b57cb-125">Requirements</span></span>

<span data-ttu-id="b57cb-126">Um den Erhöhungs Moniker zum Aktivieren einer com-Klasse zu verwenden, muss die Klasse so konfiguriert werden, dass Sie als Start Benutzer oder als Anwendungs Identität "aktivieren als Activator" ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b57cb-126">In order to use the elevation moniker to activate a COM class, the class must be configured to run as the launching user or the 'Activate as Activator' application identity.</span></span> <span data-ttu-id="b57cb-127">Wenn die Klasse für die Ausführung unter einer anderen Identität konfiguriert ist, gibt die Aktivierung den Fehler Co \_ E \_ runas- \_ Wert \_ muss \_ \_ AAA lauten.</span><span class="sxs-lookup"><span data-stu-id="b57cb-127">If the class is configured to run under any other identity, the activation returns the error CO\_E\_RUNAS\_VALUE\_MUST\_BE\_AAA.</span></span>

<span data-ttu-id="b57cb-128">Die Klasse muss auch mit einem Anzeige Namen versehen werden, der mehrsprachige Benutzeroberfläche (MUI) kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="b57cb-128">The class must also be annotated with a "friendly" display name that is multilingual user interface (MUI) compatible.</span></span> <span data-ttu-id="b57cb-129">Dies erfordert den folgenden Registrierungs Eintrag:</span><span class="sxs-lookup"><span data-stu-id="b57cb-129">This requires the following registry entry:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      LocalizedString = displayName
```

<span data-ttu-id="b57cb-130">Wenn dieser Eintrag fehlt, gibt die Aktivierung den Fehler Co \_ E " \_ Display Name Missing" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="b57cb-130">If this entry is missing, the activation returns the error CO\_E\_MISSING\_DISPLAYNAME.</span></span> <span data-ttu-id="b57cb-131">Wenn die MUI-Datei fehlt, wird der Fehlercode der [**regloadmuistringw**](/windows/desktop/api/winreg/nf-winreg-regloadmuistringa) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b57cb-131">If the MUI file is missing, the error code from the [**RegLoadMUIStringW**](/windows/desktop/api/winreg/nf-winreg-regloadmuistringa) function is returned.</span></span>

<span data-ttu-id="b57cb-132">Fügen Sie optional den folgenden Registrierungsschlüssel hinzu, um ein Anwendungssymbol anzugeben, das von der UAC-Benutzeroberfläche angezeigt werden soll:</span><span class="sxs-lookup"><span data-stu-id="b57cb-132">Optionally, to specify an application icon to be displayed by the UAC user interface, add the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         IconReference = applicationIcon
```

<span data-ttu-id="b57cb-133">**IconReference** verwendet das gleiche Format wie **LocalizedString**:</span><span class="sxs-lookup"><span data-stu-id="b57cb-133">**IconReference** uses the same format as **LocalizedString**:</span></span>

<span data-ttu-id="b57cb-134">@*pathrebinary*,*-resourcenumber*</span><span class="sxs-lookup"><span data-stu-id="b57cb-134">@*pathtobinary*,*-resourcenumber*</span></span>

<span data-ttu-id="b57cb-135">Außerdem muss die COM-Komponente signiert sein, damit das Symbol angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b57cb-135">In addition, the COM component must be signed for the icon to be displayed.</span></span>

<span data-ttu-id="b57cb-136">Die com-Klasse muss auch als Lua-fähig kommentiert werden.</span><span class="sxs-lookup"><span data-stu-id="b57cb-136">The COM class must also be annotated as LUA-Enabled.</span></span> <span data-ttu-id="b57cb-137">Dies erfordert den folgenden Registrierungs Eintrag:</span><span class="sxs-lookup"><span data-stu-id="b57cb-137">This requires the following registry entry:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         Enabled = 1
```

<span data-ttu-id="b57cb-138">Wenn dieser Eintrag fehlt, gibt die Aktivierung die \_ \_ Deaktivierte Fehler-E/a zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="b57cb-138">If this entry is missing, then the activation returns the error CO\_E\_ELEVATION\_DISABLED.</span></span>

<span data-ttu-id="b57cb-139">Beachten Sie, dass diese Einträge in der HKEY-Struktur des lokalen Computers vorhanden sein müssen \_ \_ , nicht in der Hive-Datei des aktuellen HKEY- \_ \_ Benutzers oder HKEY \_</span><span class="sxs-lookup"><span data-stu-id="b57cb-139">Note that these entries must exist in the HKEY\_LOCAL\_MACHINE hive, not the HKEY\_CURRENT\_USER or HKEY\_USERS hive.</span></span> <span data-ttu-id="b57cb-140">Dadurch wird verhindert, dass Benutzer com-Klassen herauf Stufen, die nicht auch über die Berechtigungen zum Registrieren verfügen.</span><span class="sxs-lookup"><span data-stu-id="b57cb-140">This prevents users from elevating COM classes that they did not also have the privileges to register.</span></span>

## <a name="the-elevation-moniker-and-the-elevation-ui"></a><span data-ttu-id="b57cb-141">Der Erhöhungs Moniker und die Benutzeroberfläche für Rechte Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="b57cb-141">The Elevation Moniker and the Elevation UI</span></span>

<span data-ttu-id="b57cb-142">Wenn der Client bereits hochgestuft wurde, bewirkt die Verwendung des Erhöhungs Monikers nicht, dass die Benutzeroberfläche für die Rechte Erweiterung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b57cb-142">If the client is already elevated, using the elevation moniker will not cause the Elevation UI to display.</span></span>

## <a name="how-to-use-the-elevation-moniker"></a><span data-ttu-id="b57cb-143">Verwenden des Erhöhungs Monikers</span><span class="sxs-lookup"><span data-stu-id="b57cb-143">How to Use the Elevation Moniker</span></span>

<span data-ttu-id="b57cb-144">Der Erweiterungs-Moniker ist ein standardmäßiger com-Moniker, ähnlich dem Sitzungs-, Partitions-oder warteschlangenmoniker.</span><span class="sxs-lookup"><span data-stu-id="b57cb-144">The elevation moniker is a standard COM moniker, similar to the session, partition, or queue monikers.</span></span> <span data-ttu-id="b57cb-145">Er leitet eine Aktivierungs Anforderung an einen angegebenen Server mit der angegebenen Erweiterungs Ebene.</span><span class="sxs-lookup"><span data-stu-id="b57cb-145">It directs an activation request to a specified server with the specified elevation level.</span></span> <span data-ttu-id="b57cb-146">Die zu aktivierende CLSID wird in der Monikerzeichenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b57cb-146">The CLSID to be activated appears in the moniker string.</span></span>

<span data-ttu-id="b57cb-147">Der Erhöhungs Moniker unterstützt die folgenden Token auf der Laufebene:</span><span class="sxs-lookup"><span data-stu-id="b57cb-147">The elevation moniker supports the following Run level tokens:</span></span>

1.  <span data-ttu-id="b57cb-148">Administrator</span><span class="sxs-lookup"><span data-stu-id="b57cb-148">Administrator</span></span>
2.  <span data-ttu-id="b57cb-149">Maximal</span><span class="sxs-lookup"><span data-stu-id="b57cb-149">Highest</span></span>

<span data-ttu-id="b57cb-150">Die Syntax hierfür sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="b57cb-150">The syntax for this is as follows:</span></span>

``` syntax
Elevation:Administrator!new:{guid}
Elevation:Highest!new:{guid}
```

<span data-ttu-id="b57cb-151">Die vorangehende Syntax verwendet den "New"-Moniker, um eine Instanz der com-Klasse zurückzugeben, die durch *GUID* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b57cb-151">The preceding syntax uses the "new" moniker to return an instance of the COM class specified by *guid*.</span></span> <span data-ttu-id="b57cb-152">Beachten Sie, dass der "neue" Moniker intern die [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) -Schnittstelle verwendet, um ein Class-Objekt abzurufen, und dann [**IClassFactory:: anateinstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) darauf aufruft.</span><span class="sxs-lookup"><span data-stu-id="b57cb-152">Note that the "new" moniker internally uses the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface to obtain a class object and then calls [**IClassFactory::CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) on it.</span></span>

<span data-ttu-id="b57cb-153">Der Erhöhungs Moniker kann auch verwendet werden, um ein Klassenobjekt zu erhalten, das [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)implementiert.</span><span class="sxs-lookup"><span data-stu-id="b57cb-153">The elevation moniker can also be used to get a class object, which implements [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span></span> <span data-ttu-id="b57cb-154">Der Aufrufer ruft dann mit " [**kreateinstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) " eine Objektinstanz ab.</span><span class="sxs-lookup"><span data-stu-id="b57cb-154">The caller then calls [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) to get an object instance.</span></span> <span data-ttu-id="b57cb-155">Die Syntax hierfür sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="b57cb-155">The syntax for this is as follows:</span></span>

``` syntax
Elevation:Administrator!clsid:{guid}
```

## <a name="sample-code"></a><span data-ttu-id="b57cb-156">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="b57cb-156">Sample code</span></span>

<span data-ttu-id="b57cb-157">Im folgenden Codebeispiel wird die Verwendung des Erhöhungs Monikers veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="b57cb-157">The following code example shows how to use the elevation moniker.</span></span> <span data-ttu-id="b57cb-158">Es wird vorausgesetzt, dass Sie bereits com für den aktuellen Thread initialisiert haben.</span><span class="sxs-lookup"><span data-stu-id="b57cb-158">It assumes that you have already initialized COM on the current thread.</span></span>


```C++
HRESULT CoCreateInstanceAsAdmin(HWND hwnd, REFCLSID rclsid, REFIID riid, __out void ** ppv)
{
    BIND_OPTS3 bo;
    WCHAR  wszCLSID[50];
    WCHAR  wszMonikerName[300];

    StringFromGUID2(rclsid, wszCLSID, sizeof(wszCLSID)/sizeof(wszCLSID[0])); 
    HRESULT hr = StringCchPrintf(wszMonikerName, sizeof(wszMonikerName)/sizeof(wszMonikerName[0]), L"Elevation:Administrator!new:%s", wszCLSID);
    if (FAILED(hr))
        return hr;
    memset(&bo, 0, sizeof(bo));
    bo.cbStruct = sizeof(bo);
    bo.hwnd = hwnd;
    bo.dwClassContext  = CLSCTX_LOCAL_SERVER;
    return CoGetObject(wszMonikerName, &bo, riid, ppv);
}
```



<span data-ttu-id="b57cb-159">[**Binden \_ OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) ist neu in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b57cb-159">[**BIND\_OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) is new in Windows Vista.</span></span> <span data-ttu-id="b57cb-160">Sie wird von [**Bind \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b57cb-160">It is derived from [**BIND\_OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1).</span></span>

<span data-ttu-id="b57cb-161">Die einzige Addition ist ein **HWND** -Feld ( **HWND**).</span><span class="sxs-lookup"><span data-stu-id="b57cb-161">The only addition is an **HWND** field, **hwnd**.</span></span> <span data-ttu-id="b57cb-162">Dieses Handle stellt ein Fenster dar, das zum Besitzer der Benutzeroberfläche für die Rechte Erweiterung wird, falls zutreffend.</span><span class="sxs-lookup"><span data-stu-id="b57cb-162">This handle represents a window that becomes the owner of the Elevation UI, if applicable.</span></span>

<span data-ttu-id="b57cb-163">Wenn **HWND** **null** ist, ruft com [GetActiveWindow](/windows/win32/api/winuser/nf-winuser-getactivewindow) auf, um ein Fenster Handle zu finden, das dem aktuellen Thread zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b57cb-163">If **hwnd** is **NULL**, COM will call [GetActiveWindow](/windows/win32/api/winuser/nf-winuser-getactivewindow) to find a window handle associated with the current thread.</span></span> <span data-ttu-id="b57cb-164">Dieser Fall kann auftreten, wenn es sich bei dem Client um ein Skript handelt, das keine [**Bind \_ OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) -Struktur ausfüllen kann.</span><span class="sxs-lookup"><span data-stu-id="b57cb-164">This case might occur if the client is a script, which cannot fill in a [**BIND\_OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) structure.</span></span> <span data-ttu-id="b57cb-165">In diesem Fall versucht com, das Fenster zu verwenden, das mit dem Skript Thread verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="b57cb-165">In this case, COM will try to use the window associated with the script thread.</span></span>

## <a name="over-the-shoulder-ots-elevation"></a><span data-ttu-id="b57cb-166">Over-the-Shoulder-Höhe (OTS)</span><span class="sxs-lookup"><span data-stu-id="b57cb-166">Over-The-Shoulder (OTS) Elevation</span></span>

<span data-ttu-id="b57cb-167">Die Erhöhung der Rechte (over-the-Shoulder, OTS) bezieht sich auf das Szenario, in dem ein Client einen com-Server mit den Anmelde Informationen eines Administrators anstelle seiner eigenen ausführt.</span><span class="sxs-lookup"><span data-stu-id="b57cb-167">Over-the-shoulder (OTS) elevation refers to the scenario in which a client runs a COM server with an administrator's credentials rather than his or her own.</span></span> <span data-ttu-id="b57cb-168">(Der Begriff "über der Schulter" bedeutet, dass der Administrator die Schulter des Clients überwacht, während der Client den Server ausführt.)</span><span class="sxs-lookup"><span data-stu-id="b57cb-168">(The term "over the shoulder" means that the administrator is watching over the client's shoulder as the client runs the server.)</span></span>

<span data-ttu-id="b57cb-169">Dieses Szenario kann ein Problem für COM-Aufrufe an den Server verursachen, da der Server [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) entweder nicht explizit (d. h. Programm gesteuert) oder implizit (d. h. deklarativ, mithilfe der Registrierung) aufruft.</span><span class="sxs-lookup"><span data-stu-id="b57cb-169">This scenario might cause a problem for COM calls into the server, because the server might not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) either explicitly (that is, programmatically) or implicitly (that is, declaratively, using the registry).</span></span> <span data-ttu-id="b57cb-170">Bei solchen Servern berechnet com eine Sicherheits Beschreibung, die nur selbst-, System-und buildadministratoren ermöglicht, \\ com-Aufrufe an den Server zu tätigen.</span><span class="sxs-lookup"><span data-stu-id="b57cb-170">For such servers, COM computes a security descriptor that allows only SELF, SYSTEM, and Builtin\\Administrators to makes COM calls into the server.</span></span> <span data-ttu-id="b57cb-171">Diese Anordnung funktioniert nicht in OTS-Szenarios.</span><span class="sxs-lookup"><span data-stu-id="b57cb-171">This arrangement will not work in OTS scenarios.</span></span> <span data-ttu-id="b57cb-172">Stattdessen muss der Server entweder explizit oder implizit **CoInitializeSecurity** anrufen und eine ACL angeben, die die interaktive Gruppen-SID und das System enthält.</span><span class="sxs-lookup"><span data-stu-id="b57cb-172">Instead, the server must call **CoInitializeSecurity**, either explicitly or implicitly, and specify an ACL that includes the INTERACTIVE group SID and SYSTEM.</span></span>

<span data-ttu-id="b57cb-173">Im folgenden Codebeispiel wird gezeigt, wie eine Sicherheits Beschreibung (Security Deskriptor, SD) mit der interaktiven Gruppen-SID erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b57cb-173">The following code example shows how to create a security descriptor (SD) with the INTERACTIVE group SID.</span></span>

``` syntax
BOOL GetAccessPermissionsForLUAServer(SECURITY_DESCRIPTOR **ppSD)
{
// Local call permissions to IU, SY
    LPWSTR lpszSDDL = L"O:BAG:BAD:(A;;0x3;;;IU)(A;;0x3;;;SY)";
    SECURITY_DESCRIPTOR *pSD;
    *ppSD = NULL;

    if (ConvertStringSecurityDescriptorToSecurityDescriptorW(lpszSDDL, SDDL_REVISION_1, (PSECURITY_DESCRIPTOR *)&pSD, NULL))
    {
        *ppSD = pSD;
        return TRUE;
    }

    return FALSE;
}
```

<span data-ttu-id="b57cb-174">Im folgenden Codebeispiel wird gezeigt, wie [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) implizit mit der SD aus dem vorherigen Codebeispiel aufgerufen wird:</span><span class="sxs-lookup"><span data-stu-id="b57cb-174">The following code example shows how to call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) implicitly with the SD from the previous code example:</span></span>


```C++
// hKey is the HKCR\AppID\{GUID} key
BOOL SetAccessPermissions(HKEY hkey, PSECURITY_DESCRIPTOR pSD)
{
    BOOL bResult = FALSE;
    DWORD dwLen = GetSecurityDescriptorLength(pSD);
    LONG lResult;
    lResult = RegSetValueExA(hkey, 
        "AccessPermission",
        0,
        REG_BINARY,
        (BYTE*)pSD,
        dwLen);
    if (lResult != ERROR_SUCCESS) goto done;
    bResult = TRUE;
done:
    return bResult;
}
```



<span data-ttu-id="b57cb-175">Im folgenden Codebeispiel wird gezeigt, wie [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) explizit mit der obigen SD aufgerufen wird:</span><span class="sxs-lookup"><span data-stu-id="b57cb-175">The following code example shows how to call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) explicitly with the above SD:</span></span>


```C++
// Absolute SD values
PSECURITY_DESCRIPTOR pAbsSD = NULL;
DWORD AbsSdSize = 0;
PACL  pAbsAcl = NULL;
DWORD AbsAclSize = 0;
PACL  pAbsSacl = NULL;
DWORD AbsSaclSize = 0;
PSID  pAbsOwner = NULL;
DWORD AbsOwnerSize = 0;
PSID  pAbsGroup = NULL;
DWORD AbsGroupSize = 0;

MakeAbsoluteSD (
    pSD,
    pAbsSD,
    &AbsSdSize,
    pAbsAcl,
    &AbsAclSize,
    pAbsSacl,
    &AbsSaclSize,
    pAbsOwner,
    &AbsOwnerSize,
    pAbsGroup,
    &AbsGroupSize
);

if (ERROR_INSUFFICIENT_BUFFER == GetLastError())
{
    pAbsSD = (PSECURITY_DESCRIPTOR)LocalAlloc(LMEM_FIXED, AbsSdSize);
    pAbsAcl = (PACL)LocalAlloc(LMEM_FIXED, AbsAclSize);
    pAbsSacl = (PACL)LocalAlloc(LMEM_FIXED, AbsSaclSize);
    pAbsOwner = (PSID)LocalAlloc(LMEM_FIXED, AbsOwnerSize);
    pAbsGroup = (PSID)LocalAlloc(LMEM_FIXED, AbsGroupSize);

    if ( ! (pAbsSD && pAbsAcl && pAbsSacl && pAbsOwner && pAbsGroup))
    {
        hr = E_OUTOFMEMORY;
        goto Cleanup;
    }
    if ( ! MakeAbsoluteSD(
        pSD,
        pAbsSD,
        &AbsSdSize,
        pAbsAcl,
        &AbsAclSize,
        pAbsSacl,
        &AbsSaclSize,
        pAbsOwner,
        &AbsOwnerSize,
        pAbsGroup,
        &AbsGroupSize
        ))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        goto Cleanup;
    }
}
else
{
    hr = HRESULT_FROM_WIN32(GetLastError());
    goto Cleanup;
}

// Call CoinitilizeSecurity.
```



## <a name="com-permissions-and-mandatory-access-labels"></a><span data-ttu-id="b57cb-176">COM-Berechtigungen und obligatorische Zugriffs Bezeichnungen</span><span class="sxs-lookup"><span data-stu-id="b57cb-176">COM Permissions and Mandatory Access Labels</span></span>

<span data-ttu-id="b57cb-177">In Windows Vista wird das Konzept der *obligatorischen Zugriffs Bezeichnungen* in Sicherheits Beschreibungen eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b57cb-177">Windows Vista introduces the notion of *mandatory access labels* in security descriptors.</span></span> <span data-ttu-id="b57cb-178">Die Bezeichnung bestimmt, ob Clients Ausführungs Zugriff auf ein COM-Objekt erhalten können.</span><span class="sxs-lookup"><span data-stu-id="b57cb-178">The label dictates whether clients can get execute access to a COM object.</span></span> <span data-ttu-id="b57cb-179">Die Bezeichnung wird im SACL-Teil (System Access Control List) der Sicherheits Beschreibung angegeben.</span><span class="sxs-lookup"><span data-stu-id="b57cb-179">The label is specified in the system access control list (SACL) portion of the security descriptor.</span></span> <span data-ttu-id="b57cb-180">In Windows Vista unterstützt com die Bezeichnung "System \_ obligatorisch \_ Label \_ No \_ Execute \_ up".</span><span class="sxs-lookup"><span data-stu-id="b57cb-180">In Windows Vista, COM supports the SYSTEM\_MANDATORY\_LABEL\_NO\_EXECUTE\_UP label.</span></span> <span data-ttu-id="b57cb-181">SACLs in den COM-Berechtigungen werden auf Betriebssystemen vor Windows Vista ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b57cb-181">SACLs in the COM permissions are ignored on operating systems prior to Windows Vista.</span></span>

<span data-ttu-id="b57cb-182">Ab Windows Vista unterstützt dcomcnfg.exe das Ändern der Integritäts Stufe (IL) in com-Berechtigungen nicht.</span><span class="sxs-lookup"><span data-stu-id="b57cb-182">As of Windows Vista, dcomcnfg.exe does not support changing the integrity level (IL) in COM permissions.</span></span> <span data-ttu-id="b57cb-183">Er muss Programm gesteuert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b57cb-183">It must be set programmatically.</span></span>

<span data-ttu-id="b57cb-184">Im folgenden Codebeispiel wird gezeigt, wie Sie eine com-Sicherheits Beschreibung mit einer Bezeichnung erstellen, die Start-/Aktivierungs Anforderungen von allen Clients mit niedriger Il zulässt.</span><span class="sxs-lookup"><span data-stu-id="b57cb-184">The following code example shows how to create a COM security descriptor with a label that allows launch/activation requests from all LOW IL clients.</span></span> <span data-ttu-id="b57cb-185">Beachten Sie, dass die Bezeichnungen für das starten/aktivieren und Aufrufen von Berechtigungen gültig sind.</span><span class="sxs-lookup"><span data-stu-id="b57cb-185">Note that the labels are valid for Launch/Activation and Call permissions.</span></span> <span data-ttu-id="b57cb-186">Daher ist es möglich, einen com-Server zu schreiben, der das starten, aktivieren oder Aufrufen von Clients mit einer bestimmten Il nicht zulässt.</span><span class="sxs-lookup"><span data-stu-id="b57cb-186">Thus, it is possible to write a COM server that disallows launch, activation or calls from clients with a certain IL.</span></span> <span data-ttu-id="b57cb-187">Weitere Informationen zu Integritäts Ebenen finden Sie im Abschnitt "Grundlegendes zum Integritäts Mechanismus von Windows Vista" im [Internet Explorer im geschützten Modus](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b57cb-187">For more information about integrity levels, see the section "Understanding Windows Vista's Integrity Mechanism" in [Understanding and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/).</span></span>


```C++
BOOL GetLaunchActPermissionsWithIL (SECURITY_DESCRIPTOR **ppSD)
{
// Allow World Local Launch/Activation permissions. Label the SD for LOW IL Execute UP
    LPWSTR lpszSDDL = L"O:BAG:BAD:(A;;0xb;;;WD)S:(ML;;NX;;;LW)";
    if (ConvertStringSecurityDescriptorToSecurityDescriptorW(lpszSDDL, SDDL_REVISION_1, (PSECURITY_DESCRIPTOR *)&pSD, NULL))
    {
        *ppSD = pSD;
        return TRUE;
    }
}

BOOL SetLaunchActPermissions(HKEY hkey, PSECURITY_DESCRIPTOR pSD)
{
    
    BOOL bResult = FALSE;
    DWORD dwLen = GetSecurityDescriptorLength(pSD);
    LONG lResult;
    lResult = RegSetValueExA(hkey, 
        "LaunchPermission",
        0,
        REG_BINARY,
        (BYTE*)pSD,
        dwLen);
    if (lResult != ERROR_SUCCESS) goto done;
    bResult = TRUE;
done:
    return bResult;
};
```



## <a name="cocreateinstance-and-integrity-levels"></a><span data-ttu-id="b57cb-188">Cokreateingestance-und Integritäts Ebenen</span><span class="sxs-lookup"><span data-stu-id="b57cb-188">CoCreateInstance and Integrity Levels</span></span>

<span data-ttu-id="b57cb-189">Das Verhalten von [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) wurde in Windows Vista geändert, um zu verhindern, dass Low-Il-Clients standardmäßig an com-Server gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="b57cb-189">The behavior of [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) has changed in Windows Vista, to prevent Low IL clients from binding to COM servers by default.</span></span> <span data-ttu-id="b57cb-190">Der Server muss solche Bindungen explizit zulassen, indem er die SACL angibt.</span><span class="sxs-lookup"><span data-stu-id="b57cb-190">The server must explicitly allow such bindings by specifying the SACL.</span></span> <span data-ttu-id="b57cb-191">Die Änderungen an **cokreatanstance** lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b57cb-191">The changes to **CoCreateInstance** are as follows:</span></span>

1.  <span data-ttu-id="b57cb-192">Beim Starten eines COM-Server Prozesses wird die Il im Server Prozess Token auf das Client-oder Server Token Il festgelegt, je nachdem, welcher Wert niedriger ist.</span><span class="sxs-lookup"><span data-stu-id="b57cb-192">When launching a COM server process, the IL in the server process token is set to the client or server token IL, whichever is lower.</span></span>
2.  <span data-ttu-id="b57cb-193">Standardmäßig verhindert com, dass Low-Il-Clients an die laufenden Instanzen von beliebigen COM-Servern gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="b57cb-193">By default, COM will prevent Low IL clients from binding to running instances of any COM servers.</span></span> <span data-ttu-id="b57cb-194">Um die Bindung zuzulassen, muss die Sicherheits Beschreibung für den Start/die Aktivierung eines COM-Servers eine SACL enthalten, die die Low-Il-Bezeichnung angibt (Weitere Informationen finden Sie im vorherigen Abschnitt für den Beispielcode zum Erstellen einer solchen Sicherheits Beschreibung).</span><span class="sxs-lookup"><span data-stu-id="b57cb-194">To allow the bind, a COM server's Launch/Activation security descriptor must contain a SACL that specifies the Low IL label (see the previous section for the sample code to create such a security descriptor).</span></span>

## <a name="elevated-servers-and-rot-registrations"></a><span data-ttu-id="b57cb-195">Erweiterte Server und rot-Registrierungen</span><span class="sxs-lookup"><span data-stu-id="b57cb-195">Elevated Servers and ROT Registrations</span></span>

<span data-ttu-id="b57cb-196">Wenn ein com-Server in der laufenden Objekttabelle (rot) registriert werden soll und jedem Client der Zugriff auf die Registrierung gestattet werden soll, muss das Flag "rotflags \_ zugsclient" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b57cb-196">If a COM server wishes to register in the running object table (ROT) and allow any client to access the registration, it must use the ROTFLAGS\_ALLOWANYCLIENT flag.</span></span> <span data-ttu-id="b57cb-197">Der com-Server "aktivieren als Aktivator" kann "rotflags Zuordnungs Client" nicht angeben, \_ da der DCOM-Dienststeuerungs-Manager (dcomscm) eine spodüberprüfung für dieses Flag erzwingt.</span><span class="sxs-lookup"><span data-stu-id="b57cb-197">An "Activate As Activator" COM server cannot specify ROTFLAGS\_ALLOWANYCLIENT because the DCOM service control manager (DCOMSCM) enforces a spoof check against this flag.</span></span> <span data-ttu-id="b57cb-198">In Windows Vista fügt com daher Unterstützung für einen neuen Registrierungs Eintrag hinzu, der es dem Server ermöglicht, festzulegen, dass seine rot-Registrierungen für jeden Client verfügbar gemacht werden:</span><span class="sxs-lookup"><span data-stu-id="b57cb-198">Therefore, in Windows Vista, COM adds support for a new registry entry that allows the server to stipulate that its ROT registrations be made available to any client:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\AppID
   {APPID}
      ROTFlags
```

<span data-ttu-id="b57cb-199">Der einzige gültige Wert für diesen reg \_ DWORD-Eintrag ist:</span><span class="sxs-lookup"><span data-stu-id="b57cb-199">The only valid value for this REG\_DWORD entry is:</span></span>

``` syntax
ROTREGFLAGS_ALLOWANYCLIENT 0x1
```

<span data-ttu-id="b57cb-200">Der Eintrag muss in der Hive des **\_ lokalen \_ HKEY** -Computers vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="b57cb-200">The entry must exist in the **HKEY\_LOCAL\_MACHINE** hive.</span></span>

<span data-ttu-id="b57cb-201">Dieser Eintrag bietet den Server "aktivieren als Aktivator" mit derselben Funktionalität, die von "rotflags" \_ für einen runas-Server bereitstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b57cb-201">This entry provides an "Activate As Activator" server with the same functionality that ROTFLAGS\_ALLOWANYCLIENT provides for a RunAs server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b57cb-202">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b57cb-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b57cb-203">Sicherheit in com</span><span class="sxs-lookup"><span data-stu-id="b57cb-203">Security in COM</span></span>](security-in-com.md)
</dt> <dt>

[<span data-ttu-id="b57cb-204">Das Verstehen des geschützten Modus des Internet Explorer und das Arbeiten damit</span><span class="sxs-lookup"><span data-stu-id="b57cb-204">Understanding and Working in Protected Mode Internet Explorer</span></span>](/previous-versions/windows/internet-explorer/ie-developer/)
</dt> </dl>

 

 