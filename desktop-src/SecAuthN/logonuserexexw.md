---
description: Die logonuserexexw-Funktion versucht, einen Benutzer auf dem lokalen Computer zu protokollieren.
ms.assetid: d90db4c6-a711-4519-8b91-5069cee07738
title: Logonuserexexw-Funktion (winbasep. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogonUserExExW
api_type:
- DllExport
api_location:
- Advapi32.dll
ms.openlocfilehash: 35ec65e7899f45a5222ae12b08992e77ea67f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050285"
---
# <a name="logonuserexexw-function"></a>Logonuserexexw-Funktion

Die **logonuserexexw** -Funktion versucht, einen Benutzer auf dem lokalen Computer zu protokollieren. Der lokale Computer ist der Computer, von dem **logonuserexexw** aufgerufen wurde. Sie können **logonuserexexw** nicht zum Anmelden an einem Remote Computer verwenden. Geben Sie den Benutzer mithilfe eines Benutzernamens und einer Domäne an, und [*Authentifizieren*](../secgloss/a-gly.md) Sie den Benutzer mit einem nur-Text-Kennwort. Wenn die Funktion erfolgreich ausgeführt wird, empfängt Sie ein Handle für ein Token, das den angemeldeten Benutzer darstellt. Anschließend können Sie dieses Tokenhandle verwenden, um die Identität des angegebenen Benutzers anzunehmen oder in den meisten Fällen einen [*Prozess*](../secgloss/p-gly.md) zu erstellen, der im Kontext des angegebenen Benutzers ausgeführt wird.

Diese Funktion ähnelt der [**logonuserex**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa) -Funktion, mit der Ausnahme, dass Sie den zusätzlichen Parameter " *ptokengroups*" annimmt, bei dem es sich um einen Satz von mindestens einem Sicherheits-IDs (SIDs) handelt, die dem Token hinzugefügt werden, das dem Aufrufer zurückgegeben wird, wenn die Anmeldung erfolgreich ist. [](../secgloss/s-gly.md)

Diese Funktion ist nicht in einem öffentlichen Header deklariert und besitzt keine zugehörige Import Bibliothek. Sie müssen die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Advapi32.dll zu verknüpfen.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI LogonUserExExW(
  _In_      LPTSTR        lpszUsername,
  _In_opt_  LPTSTR        lpszDomain,
  _In_opt_  LPTSTR        lpszPassword,
  _In_      DWORD         dwLogonType,
  _In_      DWORD         dwLogonProvider,
  _In_opt_  PTOKEN_GROUPS pTokenGroups,
  _Out_opt_ PHANDLE       phToken,
  _Out_opt_ PSID          *ppLogonSid,
  _Out_opt_ PVOID         *ppProfileBuffer,
  _Out_opt_ LPDWORD       pdwProfileLength,
  _Out_opt_ PQUOTA_LIMITS pQuotaLimits
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszusername* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Benutzers angibt. Dies ist der Name des Benutzerkontos, bei dem Sie sich anmelden möchten. Wenn Sie das UPN-Format ( [*User Principal Name, Benutzer Prinzipal Name*](../secgloss/u-gly.md) ) verwenden, muss der *lpszdomain* -Parameter **null** sein.

</dd> <dt>

*lpszdomain* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen der Domäne oder des Servers angibt, deren Konto Datenbank das *lpszusername* -Konto enthält. Wenn dieser Parameter **null** ist, muss der Benutzername im UPN-Format angegeben werden. Wenn dieser Parameter "." ist, überprüft die Funktion das Konto nur mithilfe der lokalen Konto Datenbank.

</dd> <dt>

*lpszpassword* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die das nur-Text-Kennwort für das durch *lpszusername* angegebene Benutzerkonto angibt. Wenn Sie die Verwendung des Kennworts abgeschlossen haben, löschen Sie das Kennwort aus dem Arbeitsspeicher, indem Sie die [**securezeromemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) -Funktion aufrufen. Weitere Informationen zum Schützen von Kenn Wörtern finden Sie unter [Handling Kennwörter](../secbp/handling-passwords.md).

</dd> <dt>

*dwlogontype* \[ in\]
</dt> <dd>

Der Typ des auszuführenden Anmeldevorgangs. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                                                        | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_LOGON_INTERACTIVE"></span><span id="logon32_logon_interactive"></span><dl> <dt>**LOGON32 \_ \_Interaktiv anmelden**</dt> <dt>2</dt> </dl>                    | Dieser Anmeldetyp richtet sich an Benutzer, die den Computer interaktiv verwenden, z. b. ein Benutzer, der von einem [*Terminal*](../secgloss/t-gly.md) Server, einer Remoteshell oder einem ähnlichen Prozess angemeldet wird. Dieser Anmeldetyp hat zusätzliche Kosten für das Zwischenspeichern von Anmelde Informationen für getrennte Vorgänge. Daher ist es für einige Client/Server-Anwendungen, wie z. b. einen Mailserver, ungeeignet.<br/>                                  |
| <span id="LOGON32_LOGON_NETWORK"></span><span id="logon32_logon_network"></span><dl> <dt>**LOGON32 \_ Anmelde \_ Netzwerk**</dt> <dt>3</dt> </dl>                                | Dieser Anmeldetyp eignet sich für Hochleistungsserver, um nur-Text-Kenn Wörter zu authentifizieren. Die Anmelde Informationen für diesen Anmeldetyp werden von der **logonuserexexw** -Funktion nicht zwischengespeichert.<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_BATCH"></span><span id="logon32_logon_batch"></span><dl> <dt>**LOGON32 \_ Anmelde \_ Batch**</dt> <dt>4</dt> </dl>                                      | Dieser Anmeldetyp ist für Batch Server gedacht, bei denen Prozesse möglicherweise im Auftrag eines Benutzers ohne direkten Eingriff ausgeführt werden. Dieser Typ ist auch für Server mit höherer Leistung vorgesehen, die viele nur-Text-Authentifizierungs Versuche gleichzeitig verarbeiten, z. b. e-Mail-oder Webserver. Die Anmelde Informationen für diesen Anmeldetyp werden von der **logonuserexexw** -Funktion nicht zwischengespeichert.<br/>                                                                                                           |
| <span id="LOGON32_LOGON_SERVICE"></span><span id="logon32_logon_service"></span><dl> <dt>**LOGON32 \_ Anmelde \_ Dienst**</dt> <dt>5</dt> </dl>                                | Gibt die Anmeldung eines Dienst Typs an. Für das angegebene Konto muss die Dienst Berechtigung aktiviert sein.<br/>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_UNLOCK"></span><span id="logon32_logon_unlock"></span><dl> <dt>**LOGON32 \_ Anmelde \_ Sperre**</dt> <dt>7</dt> aufheben </dl>                                   | Bei diesem Anmeldetyp handelt es sich um [*Gina*](../secgloss/g-gly.md) -DLLs, die sich bei Benutzern anmelden, die den Computer interaktiv verwenden werden. Dieser Anmeldetyp kann einen eindeutigen Überwachungsdaten Satz generieren, der anzeigt, wann die Arbeitsstation entsperrt wurde.<br/>                                                                                                                                                                                                                   |
| <span id="LOGON32_LOGON_NETWORK_CLEARTEXT"></span><span id="logon32_logon_network_cleartext"></span><dl> <dt>**LOGON32 \_ Anmelde \_ Netzwerk \_ Klartext**</dt> <dt>8</dt> </dl> | Dieser Anmeldetyp behält den Namen und das Kennwort im [*Authentifizierungs Paket*](../secgloss/a-gly.md)bei, wodurch der Serververbindungen zu anderen Netzwerkservern herstellen kann, während die Identität des Clients angenommen wird. Ein Server kann Klartext-Anmelde Informationen von einem Client akzeptieren, **logonuserexexw** aufrufen, sicherstellen, dass der Benutzer über das Netzwerk auf das System zugreifen kann und weiterhin mit anderen Servern kommunizieren kann. <br/> |
| <span id="LOGON32_LOGON_NEW_CREDENTIALS"></span><span id="logon32_logon_new_credentials"></span><dl> <dt>**LOGON32 \_ \_Neue \_**</dt> Anmelde Informationen anmelden <dt>9</dt> </dl>       | Dieser Anmeldetyp ermöglicht dem Aufrufer das Klonen seines aktuellen Tokens und das Angeben neuer Anmelde Informationen für ausgehende Verbindungen. Die neue Anmelde Sitzung hat denselben lokalen Bezeichner, verwendet jedoch andere Anmelde Informationen für andere Netzwerkverbindungen.<br/> Dieser Anmeldetyp wird nur vom **LOGON32 \_ Provider \_ WINNT50** -Anmelde Anbieter unterstützt.<br/>                                                                                                                                       |



 

</dd> <dt>

*dwlogonprovider* \[ in\]
</dt> <dd>

Der Anmelde Anbieter. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                           | Bedeutung                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_PROVIDER_DEFAULT"></span><span id="logon32_provider_default"></span><dl> <dt>**LOGON32 \_ Provider- \_ Standard**</dt> </dl> | Verwenden Sie den Standard Anmelde Anbieter für das System. Der Standard [*Sicherheitsanbieter*](../secgloss/s-gly.md) ist NTLM.<br/> |
| <span id="LOGON32_PROVIDER_WINNT50"></span><span id="logon32_provider_winnt50"></span><dl> <dt>**LOGON32- \_ Anbieter \_ WINNT50**</dt> </dl> | Verwenden Sie den Logon-Anmelde Anbieter. <br/>                                                                                                                                                         |
| <span id="LOGON32_PROVIDER_WINNT40"></span><span id="logon32_provider_winnt40"></span><dl> <dt>**LOGON32- \_ Anbieter \_ WINNT40**</dt> </dl> | Verwenden Sie den NTLM-Anmelde Anbieter.<br/>                                                                                                                                                               |



 

</dd> <dt>

*ptokengroups* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine [**\_ tokengruppenstruktur**](/windows/win32/api/winnt/ns-winnt-token_groups) , die eine Liste von Gruppen-SIDs angibt, die dem Token hinzugefügt werden, das diese Funktion bei erfolgreicher Anmeldung empfängt. Alle dem Token hinzugefügten SIDs wirken sich auch auf die Gruppen Erweiterung aus. Wenn die hinzugefügten SIDs beispielsweise Mitglieder von lokalen Gruppen sind, werden diese Gruppen auch dem empfangenen Zugriffs Token hinzugefügt.

Wenn dieser Parameter nicht **null** ist, muss dem Aufrufer dieser Funktion die **Berechtigung "SE \_ TCB- \_ Berechtigung** erteilt und aktiviert" zugewiesen sein.

</dd> <dt>

*phtoken* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine Handle-Variable, die ein Handle für ein Token empfängt, das den angegebenen Benutzer darstellt.

Sie können das zurückgegebene Handle in Aufrufen der Funktion "annehmen der Identität des Identitäts [**Benutzers**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) " verwenden.

In den meisten Fällen ist das zurückgegebene Handle ein [*primäres Token*](../secgloss/p-gly.md) , das Sie in Aufrufen der Funktion " [**deateprocessasuser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) " verwenden können. Wenn Sie jedoch das LOGON32 \_ Logon Network- \_ Flag angeben, gibt **logonuserexexw** ein Identitätswechsel [*Token*](../secgloss/i-gly.md) zurück, das Sie nicht in " **kreateprocessasuser** " verwenden können, es sei denn, Sie müssen [**duplicalletokenex**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) aufrufen, um das Identitätswechsel Token in ein primäres Token zu konvertieren.

Wenn Sie dieses Handle nicht mehr benötigen, schließen Sie es, indem Sie die [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) -Funktion aufrufen.

</dd> <dt>

*pplogonsid* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine SID, die die SID des angemeldeten Benutzers empfängt.

Wenn Sie die SID nicht mehr verwenden, können Sie Sie durch Aufrufen der [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) -Funktion freigeben.

</dd> <dt>

*ppprofilebuffer* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf einen Zeiger, der die Adresse eines Puffers empfängt, der das Profil des angemeldeten Benutzers enthält.

</dd> <dt>

*pdwprofilelength* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf ein **DWORD** , das die Länge des Profil Puffers empfängt.

</dd> <dt>

*pquotalimits* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**Kontingent \_ Limits**](/windows/desktop/api/Winnt/ns-winnt-quota_limits) -Struktur, die Informationen über die Kontingente für den angemeldeten Benutzer empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion einen Wert ungleich NULL zurück.

Wenn die Funktion fehlschlägt, gibt Sie 0 (null) zurück. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

Der Anmeldetyp " **LOGON32 \_ Logon \_ Network** " ist am schnellsten, es gelten jedoch die folgenden Einschränkungen:

-   Die-Funktion gibt ein Identitätswechsel [*Token*](../secgloss/i-gly.md)zurück, nicht ein primäres Token. Sie können dieses Token nicht direkt in der [**Funktion "**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) " von "" in der Funktion "|" verwenden. Allerdings können Sie die [**duplicalletokenex**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) -Funktion aufrufen, um das **Token in ein** primäres Token zu konvertieren
-   Wenn Sie das Token in ein primäres Token konvertieren und es in [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) verwenden, um einen Prozess zu starten, kann der neue Prozess nicht auf andere Netzwerkressourcen (z. b. Remote Server oder Drucker) über den Redirector zugreifen. Eine Ausnahme besteht darin, dass der neue Prozess darauf zugreifen kann, wenn der Zugriff auf die Netzwerkressource nicht gesteuert wird.

Das von *lpszusername* angegebene Konto muss über die erforderlichen Konto Rechte verfügen. Wenn Sie z. b. einen Benutzer mit dem " **LOGON32 \_ Logon \_ Interactive** "-Flag anmelden möchten, muss der Benutzer (oder eine Gruppe, zu der der Benutzer gehört) über das Konto "Konto für **\_ interaktive \_ Anmelde \_ Namen** Konto" verfügen. Eine Liste der Konto Rechte, die sich auf die verschiedenen Anmeldevorgänge auswirken, finden Sie unter [Konto Objekt-Zugriffsrechte](../secmgmt/account-object-access-rights.md).

Ein Benutzer gilt als angemeldet, wenn mindestens ein Token vorhanden ist. Wenn Sie " [**kreateprocessasuser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) " aufrufen und dann das Token schließen, ist der Benutzer weiterhin angemeldet, bis der Prozess (und alle untergeordneten Prozesse) beendet wurden.

Wenn der optionale Parameter " *ptokengroups* " angegeben wird, wird die lokale sid oder die Anmelde-SID von LSA nicht automatisch hinzugefügt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                                  |
| Version<br/>                  | Logonuserexexw ist auch unter Windows Server 2003 oder Windows xpmit der allgemeinen Verteilungs Version verfügbar.<br/> |
| Header<br/>                   | <dl> <dt>Winbasep. h</dt> </dl>                                 |
| DLL<br/>                      | <dl> <dt>Advapi32.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Client/Server-Access Control](../secauthz/client-server-access-control.md)
</dt> <dt>

[Client/Server-Access Control Funktionen](../secauthz/authorization-functions.md)
</dt> <dt>

[**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)
</dt> <dt>

[**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)
</dt> <dt>

[**Duplialisietokenex**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)
</dt> <dt>

[**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)
</dt> <dt>

[**Logonuserex**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa)
</dt> <dt>

[**Kontingent \_ Limits**](/windows/desktop/api/Winnt/ns-winnt-quota_limits)
</dt> </dl>

 

 
