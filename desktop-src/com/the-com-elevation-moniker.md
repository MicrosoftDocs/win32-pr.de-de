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
# <a name="the-com-elevation-moniker"></a>Der com-Erhöhungs Moniker.

Mit dem com-Erweiterungs Moniker können Anwendungen, die unter der Benutzerkontensteuerung (User Account Control, UAC) ausgeführt werden, com-Klassen mit erhöhten Rechten aktivieren. Weitere Informationen finden Sie unter [Fokus auf die geringsten Berechtigungen](/previous-versions/dotnet/articles/aa480194(v=msdn.10)).

## <a name="when-to-use-the-elevation-moniker"></a>Verwendung des Erhöhungs Monikers

Der Erweiterungs-Moniker wird zum Aktivieren einer com-Klasse verwendet, um eine bestimmte und eingeschränkte Funktion zu erreichen, die erhöhte Berechtigungen erfordert, z. b. das Ändern des Systemdatums und der Systemzeit.

Erhöhung erfordert die Teilnahme an einer com-Klasse und Ihrem Client. Die com-Klasse muss so konfiguriert werden, dass Sie eine Erhöhung der Rechte unterstützt, indem Sie Ihren Registrierungs Eintrag kommentiert, wie im Abschnitt "Anforderungen" beschrieben. Der com-Client muss mit dem Erhöhungs Moniker eine Erhöhung anfordern.

Der Erhöhungs Moniker ist nicht für die Bereitstellung der Anwendungs Kompatibilität vorgesehen. Wenn Sie z. b. eine Legacy-COM-Anwendung, z. b. WinWord, als erweiterten Server ausführen möchten, sollten Sie die ausführbare com-Client Datei so konfigurieren, dass Sie eine Erhöhung erfordert, anstatt die Klasse der Legacy Anwendung mit dem Erhöhungs Moniker zu aktivieren. Wenn der com-Client mit erhöhten Rechten mit der CLSID der Legacy Anwendung [**cokreatanstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) aufruft, wird der Status des Clients mit erhöhten Rechten an den Server Prozess weitergeleitet.

Nicht alle com-Funktionen sind mit der Erhöhung der Rechte kompatibel. Zu den Funktionen, die nicht funktionieren, gehören:

-   Die Erhöhung der Rechte erfolgt nicht von einem Client zu einem com-Remote Server. Wenn ein Client einen com-Remote Server mit dem Erhöhungs Moniker aktiviert, wird der Server nicht erhöht, auch wenn er eine Erhöhung der Rechte unterstützt.
-   Wenn eine COM-Klasse mit erhöhten Rechten während eines com-Aufrufes einen Identitätswechsel verwendet, verliert sie während des Identitäts Wechsels möglicherweise ihre erhöhten Rechte.
-   Wenn ein com-Server mit erhöhten Rechten eine Klasse in der Running Object Table (rot) registriert, ist die Klasse nicht für Clients ohne erhöhte Rechte verfügbar.
-   Ein Prozess, der mit dem UAC-Mechanismus erhöht wurde, lädt während der com-Aktivierungen keine benutzerspezifischen Klassen. Bei com-Anwendungen bedeutet dies, dass die com-Klassen der Anwendung in der Registrierungs Struktur des **\_ lokalen \_ HKEY** -Computers installiert werden müssen, wenn die Anwendung sowohl von nicht privilegierten als auch von privilegierten Konten verwendet werden soll. Die com-Klassen der Anwendung müssen nur in der **HKEY \_ Users** -Struktur installiert werden, wenn die Anwendung nie von privilegierten Konten verwendet wird.
-   Drag & Drop ist in Anwendungen mit erhöhten Rechten nicht zulässig.

## <a name="requirements"></a>Anforderungen

Um den Erhöhungs Moniker zum Aktivieren einer com-Klasse zu verwenden, muss die Klasse so konfiguriert werden, dass Sie als Start Benutzer oder als Anwendungs Identität "aktivieren als Activator" ausgeführt wird. Wenn die Klasse für die Ausführung unter einer anderen Identität konfiguriert ist, gibt die Aktivierung den Fehler Co \_ E \_ runas- \_ Wert \_ muss \_ \_ AAA lauten.

Die Klasse muss auch mit einem Anzeige Namen versehen werden, der mehrsprachige Benutzeroberfläche (MUI) kompatibel ist. Dies erfordert den folgenden Registrierungs Eintrag:

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      LocalizedString = displayName
```

Wenn dieser Eintrag fehlt, gibt die Aktivierung den Fehler Co \_ E " \_ Display Name Missing" zurück \_ . Wenn die MUI-Datei fehlt, wird der Fehlercode der [**regloadmuistringw**](/windows/desktop/api/winreg/nf-winreg-regloadmuistringa) -Funktion zurückgegeben.

Fügen Sie optional den folgenden Registrierungsschlüssel hinzu, um ein Anwendungssymbol anzugeben, das von der UAC-Benutzeroberfläche angezeigt werden soll:

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         IconReference = applicationIcon
```

**IconReference** verwendet das gleiche Format wie **LocalizedString**:

@*pathrebinary*,*-resourcenumber*

Außerdem muss die COM-Komponente signiert sein, damit das Symbol angezeigt wird.

Die com-Klasse muss auch als Lua-fähig kommentiert werden. Dies erfordert den folgenden Registrierungs Eintrag:

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         Enabled = 1
```

Wenn dieser Eintrag fehlt, gibt die Aktivierung die \_ \_ Deaktivierte Fehler-E/a zurück \_ .

Beachten Sie, dass diese Einträge in der HKEY-Struktur des lokalen Computers vorhanden sein müssen \_ \_ , nicht in der Hive-Datei des aktuellen HKEY- \_ \_ Benutzers oder HKEY \_ Dadurch wird verhindert, dass Benutzer com-Klassen herauf Stufen, die nicht auch über die Berechtigungen zum Registrieren verfügen.

## <a name="the-elevation-moniker-and-the-elevation-ui"></a>Der Erhöhungs Moniker und die Benutzeroberfläche für Rechte Erweiterungen

Wenn der Client bereits hochgestuft wurde, bewirkt die Verwendung des Erhöhungs Monikers nicht, dass die Benutzeroberfläche für die Rechte Erweiterung angezeigt wird.

## <a name="how-to-use-the-elevation-moniker"></a>Verwenden des Erhöhungs Monikers

Der Erweiterungs-Moniker ist ein standardmäßiger com-Moniker, ähnlich dem Sitzungs-, Partitions-oder warteschlangenmoniker. Er leitet eine Aktivierungs Anforderung an einen angegebenen Server mit der angegebenen Erweiterungs Ebene. Die zu aktivierende CLSID wird in der Monikerzeichenfolge angezeigt.

Der Erhöhungs Moniker unterstützt die folgenden Token auf der Laufebene:

1.  Administrator
2.  Maximal

Die Syntax hierfür sieht wie folgt aus:

``` syntax
Elevation:Administrator!new:{guid}
Elevation:Highest!new:{guid}
```

Die vorangehende Syntax verwendet den "New"-Moniker, um eine Instanz der com-Klasse zurückzugeben, die durch *GUID* angegeben wird. Beachten Sie, dass der "neue" Moniker intern die [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) -Schnittstelle verwendet, um ein Class-Objekt abzurufen, und dann [**IClassFactory:: anateinstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) darauf aufruft.

Der Erhöhungs Moniker kann auch verwendet werden, um ein Klassenobjekt zu erhalten, das [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)implementiert. Der Aufrufer ruft dann mit " [**kreateinstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) " eine Objektinstanz ab. Die Syntax hierfür sieht wie folgt aus:

``` syntax
Elevation:Administrator!clsid:{guid}
```

## <a name="sample-code"></a>Beispielcode

Im folgenden Codebeispiel wird die Verwendung des Erhöhungs Monikers veranschaulicht. Es wird vorausgesetzt, dass Sie bereits com für den aktuellen Thread initialisiert haben.


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



[**Binden \_ OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) ist neu in Windows Vista. Sie wird von [**Bind \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1)abgeleitet.

Die einzige Addition ist ein **HWND** -Feld ( **HWND**). Dieses Handle stellt ein Fenster dar, das zum Besitzer der Benutzeroberfläche für die Rechte Erweiterung wird, falls zutreffend.

Wenn **HWND** **null** ist, ruft com [GetActiveWindow](/windows/win32/api/winuser/nf-winuser-getactivewindow) auf, um ein Fenster Handle zu finden, das dem aktuellen Thread zugeordnet ist. Dieser Fall kann auftreten, wenn es sich bei dem Client um ein Skript handelt, das keine [**Bind \_ OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) -Struktur ausfüllen kann. In diesem Fall versucht com, das Fenster zu verwenden, das mit dem Skript Thread verknüpft ist.

## <a name="over-the-shoulder-ots-elevation"></a>Over-the-Shoulder-Höhe (OTS)

Die Erhöhung der Rechte (over-the-Shoulder, OTS) bezieht sich auf das Szenario, in dem ein Client einen com-Server mit den Anmelde Informationen eines Administrators anstelle seiner eigenen ausführt. (Der Begriff "über der Schulter" bedeutet, dass der Administrator die Schulter des Clients überwacht, während der Client den Server ausführt.)

Dieses Szenario kann ein Problem für COM-Aufrufe an den Server verursachen, da der Server [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) entweder nicht explizit (d. h. Programm gesteuert) oder implizit (d. h. deklarativ, mithilfe der Registrierung) aufruft. Bei solchen Servern berechnet com eine Sicherheits Beschreibung, die nur selbst-, System-und buildadministratoren ermöglicht, \\ com-Aufrufe an den Server zu tätigen. Diese Anordnung funktioniert nicht in OTS-Szenarios. Stattdessen muss der Server entweder explizit oder implizit **CoInitializeSecurity** anrufen und eine ACL angeben, die die interaktive Gruppen-SID und das System enthält.

Im folgenden Codebeispiel wird gezeigt, wie eine Sicherheits Beschreibung (Security Deskriptor, SD) mit der interaktiven Gruppen-SID erstellt wird.

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

Im folgenden Codebeispiel wird gezeigt, wie [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) implizit mit der SD aus dem vorherigen Codebeispiel aufgerufen wird:


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



Im folgenden Codebeispiel wird gezeigt, wie [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) explizit mit der obigen SD aufgerufen wird:


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



## <a name="com-permissions-and-mandatory-access-labels"></a>COM-Berechtigungen und obligatorische Zugriffs Bezeichnungen

In Windows Vista wird das Konzept der *obligatorischen Zugriffs Bezeichnungen* in Sicherheits Beschreibungen eingeführt. Die Bezeichnung bestimmt, ob Clients Ausführungs Zugriff auf ein COM-Objekt erhalten können. Die Bezeichnung wird im SACL-Teil (System Access Control List) der Sicherheits Beschreibung angegeben. In Windows Vista unterstützt com die Bezeichnung "System \_ obligatorisch \_ Label \_ No \_ Execute \_ up". SACLs in den COM-Berechtigungen werden auf Betriebssystemen vor Windows Vista ignoriert.

Ab Windows Vista unterstützt dcomcnfg.exe das Ändern der Integritäts Stufe (IL) in com-Berechtigungen nicht. Er muss Programm gesteuert festgelegt werden.

Im folgenden Codebeispiel wird gezeigt, wie Sie eine com-Sicherheits Beschreibung mit einer Bezeichnung erstellen, die Start-/Aktivierungs Anforderungen von allen Clients mit niedriger Il zulässt. Beachten Sie, dass die Bezeichnungen für das starten/aktivieren und Aufrufen von Berechtigungen gültig sind. Daher ist es möglich, einen com-Server zu schreiben, der das starten, aktivieren oder Aufrufen von Clients mit einer bestimmten Il nicht zulässt. Weitere Informationen zu Integritäts Ebenen finden Sie im Abschnitt "Grundlegendes zum Integritäts Mechanismus von Windows Vista" im [Internet Explorer im geschützten Modus](/previous-versions/windows/internet-explorer/ie-developer/).


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



## <a name="cocreateinstance-and-integrity-levels"></a>Cokreateingestance-und Integritäts Ebenen

Das Verhalten von [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) wurde in Windows Vista geändert, um zu verhindern, dass Low-Il-Clients standardmäßig an com-Server gebunden werden. Der Server muss solche Bindungen explizit zulassen, indem er die SACL angibt. Die Änderungen an **cokreatanstance** lauten wie folgt:

1.  Beim Starten eines COM-Server Prozesses wird die Il im Server Prozess Token auf das Client-oder Server Token Il festgelegt, je nachdem, welcher Wert niedriger ist.
2.  Standardmäßig verhindert com, dass Low-Il-Clients an die laufenden Instanzen von beliebigen COM-Servern gebunden werden. Um die Bindung zuzulassen, muss die Sicherheits Beschreibung für den Start/die Aktivierung eines COM-Servers eine SACL enthalten, die die Low-Il-Bezeichnung angibt (Weitere Informationen finden Sie im vorherigen Abschnitt für den Beispielcode zum Erstellen einer solchen Sicherheits Beschreibung).

## <a name="elevated-servers-and-rot-registrations"></a>Erweiterte Server und rot-Registrierungen

Wenn ein com-Server in der laufenden Objekttabelle (rot) registriert werden soll und jedem Client der Zugriff auf die Registrierung gestattet werden soll, muss das Flag "rotflags \_ zugsclient" verwendet werden. Der com-Server "aktivieren als Aktivator" kann "rotflags Zuordnungs Client" nicht angeben, \_ da der DCOM-Dienststeuerungs-Manager (dcomscm) eine spodüberprüfung für dieses Flag erzwingt. In Windows Vista fügt com daher Unterstützung für einen neuen Registrierungs Eintrag hinzu, der es dem Server ermöglicht, festzulegen, dass seine rot-Registrierungen für jeden Client verfügbar gemacht werden:

```
HKEY_LOCAL_MACHINE\Software\Classes\AppID
   {APPID}
      ROTFlags
```

Der einzige gültige Wert für diesen reg \_ DWORD-Eintrag ist:

``` syntax
ROTREGFLAGS_ALLOWANYCLIENT 0x1
```

Der Eintrag muss in der Hive des **\_ lokalen \_ HKEY** -Computers vorhanden sein.

Dieser Eintrag bietet den Server "aktivieren als Aktivator" mit derselben Funktionalität, die von "rotflags" \_ für einen runas-Server bereitstellt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheit in com](security-in-com.md)
</dt> <dt>

[Das Verstehen des geschützten Modus des Internet Explorer und das Arbeiten damit](/previous-versions/windows/internet-explorer/ie-developer/)
</dt> </dl>

 

 