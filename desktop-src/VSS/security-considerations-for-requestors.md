---
description: Die VSS-Infrastruktur erfordert, dass VSS-Anforderer, z. B. Sicherungsanwendungen, sowohl als COM-Clients als auch als Server funktionieren können.
ms.assetid: b01145c6-76ba-4a81-bca6-59c4ca488dac
title: Sicherheitsüberlegungen für Anfordernde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d64a5c817a8c45951d56d3fa12e78a03d8bee9dd742f67755f949d1f90a0e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590951"
---
# <a name="security-considerations-for-requesters"></a>Sicherheitsüberlegungen für Anfordernde

Die VSS-Infrastruktur erfordert, dass VSS-Anforderer, z. B. Sicherungsanwendungen, sowohl als COM-Clients als auch als Server funktionieren können.

Als Server macht ein An anfordernde Benutzer eine Reihe von COM-Rückrufschnittstellen verfügbar, die von externen Prozessen (z. B. Writern oder dem VSS-Dienst) aufgerufen werden können. Daher müssen Anfordernde sicher verwalten, welche COM-Clients in der Lage sind, eingehende COM-Aufrufe in ihren Prozess zu tätigen.

Ebenso können Anfordernde als COM-Client für die COM-APIs fungieren, die von einem VSS Writer oder vom VSS-Dienst bereitgestellt werden. Die sicherheitsspezifischen Sicherheitseinstellungen des Anfordernden müssen ausgehende COM-Aufrufe des Anfordernden an diese anderen Prozesse zulassen.

Der einfachste Mechanismus zum Verwalten der Sicherheitsprobleme eines An anfordernden Benutzers umfasst die richtige Auswahl des Benutzerkontos, unter dem es ausgeführt wird.

Ein Anfordernde muss in der Regel unter einem Benutzer ausgeführt werden, der entweder Mitglied der Gruppe Administratoren oder der Gruppe Sicherungsoperatoren ist, oder als lokales Systemkonto ausführen.

Wenn ein Anfordernde als COM-Client agiert und nicht unter diesen Konten ausgeführt wird, wird standardmäßig jeder COM-Aufruf automatisch mit **E \_ ACCESSDENIED** abgelehnt, ohne dass sogar die COM-Methodenimplementierung verwendet wird.

## <a name="disabling-com-exception-handling"></a>Deaktivieren der COM-Ausnahmebehandlung

Legen Sie beim Entwickeln eines Anfordernden das globale OPTIONSflag COM COMGLB EXCEPTION DONOT HANDLE fest, \_ \_ um die \_ COM-Ausnahmebehandlung zu deaktivieren. Dies ist wichtig, da die COM-Ausnahmebehandlung schwerwiegende Fehler in einer VSS-Anwendung maskieren kann. Der maskierte Fehler kann dazu führen, dass der Prozess in einem instabilen und unvorhersehbaren Zustand bleibt, was zu Beschädigungen und Hängen führen kann. Weitere Informationen zu diesem Flag finden Sie unter [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).

## <a name="setting-requester-default-com-access-check-permission"></a>Festlegen der STANDARDMÄßIGEN COM-Zugriffsüberprüfungsberechtigung des Anfordernden

Anfordernde müssen beachten, dass sie eingehende Aufrufe von anderen VSS-Teilnehmern wie Writern oder dem VSS-Dienst zulassen müssen, wenn ihr Prozess als Server fungiert (z. B. das Ändern des Sicherungskomponentendokuments durch Writer).

Standardmäßig lässt ein Windows jedoch nur COM-Clients zu, die unter derselben Anmeldesitzung (der SELF-SID) oder unter dem lokalen Systemkonto ausgeführt werden. Dies ist ein potenzielles Problem, da diese Standardwerte für die VSS-Infrastruktur nicht geeignet sind. Writer können beispielsweise als "Sicherungsoperator"-Benutzerkonto ausgeführt werden, das sich weder in derselben Anmeldesitzung wie der anfordernde Prozess noch in einem lokalen Systemkonto befindet.

Um diese Art von Problem zu behandeln, kann jeder COM-Serverprozess weitere Kontrolle darüber übernehmen, ob ein RPC- oder COM-Client eine vom Server implementierte COM-Methode (in diesem Fall eine Anfordernde) mithilfe von [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ausführen darf, um eine prozessweite "Standardmäßige COM-Zugriffsüberprüfungsberechtigung" zu festlegen.

An anfordernde Benutzer können explizit folgende Schritte unternehmen:

-   Erlauben Sie allen Prozessen den Zugriff auf den Aufruf des An anfordernden Prozesses.

    Diese Option kann für die überwiegende Mehrheit der Anfordernden geeignet sein und wird von anderen COM-Servern verwendet, z. B. verwenden alle SVCHOST-basierten Windows-Dienste diese Option bereits, ebenso wie alle COM+-Dienste standardmäßig.

    Das Zulassen, dass alle Prozesse eingehende COM-Aufrufe ausführen, ist nicht notwendigerweise eine Sicherheitsschwäche. Ein Anfordernde, der wie alle anderen COM-Server als COM-Server agiert, behält immer die Option bei, seine Clients für jede COM-Methode zu autorisieren, die in seinem Prozess implementiert ist.

    Beachten Sie, dass interne COM-Rückrufe, die von VSS implementiert werden, standardmäßig geschützt sind.

    Um allen Prozessen COM-Zugriff auf einen anfordernden Benutzer zu ermöglichen, können Sie einen NULL-Sicherheitsdeskriptor als ersten Parameter von [**CoInitializeSecurity übergeben.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)  (Beachten **Sie, dass CoInitializeSecurity** für den gesamten Prozess mindestens einmal aufgerufen werden muss. Weitere Informationen zu **CoInitializeSecurity-Aufrufen** finden Sie in der COM-Dokumentation oder in MSDN.)

    Im folgenden Codebeispiel wird gezeigt, wie ein Anfinger [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 8 und Windows Server 2012 und höher aufrufen sollte, um mit VSS für Remotedateifreigaben (RVSS) kompatibel zu sein:

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IMPERSONATE,   //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_STATIC,                   //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    Wenn Sie die COM-Sicherheit einer Anfordernden mit [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)explizit festlegen, sollten Sie folgende Schritte unternehmen:

    -   Legen Sie die Authentifizierungsebene auf mindestens **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT INTEGRITY \_ fest.** Für eine bessere Sicherheit sollten Sie die **Verwendung von RPC C \_ \_ AUTHN \_ LEVEL \_ PKT PRIVACY in Betracht \_ ziehen.**
    -   Legen Sie die Identitätswechselebene auf **RPC C IMP LEVEL \_ \_ \_ \_ IMPERSONATE fest.**
    -   Legen Sie die Sicherheitsfunktionen für die Verkleinerung auf **EOAC \_ STATIC fest.** Weitere Informationen zum Verkleinern der Sicherheit finden Sie unter [Cloaking](../com/cloaking.md).

    Im folgenden Codebeispiel wird gezeigt, wie ein an anfordernde Mitarbeiter [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 7 und Windows Server 2008 R2 und früher aufrufen soll (oder in Windows 8 und Windows Server 2012 und höher, wenn keine RVSS-Kompatibilität erforderlich ist):

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IDENTIFY,      //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_NONE,                     //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    Wenn Sie die COM-Sicherheit einer Anfordernden mit [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)explizit festlegen, sollten Sie folgende Schritte unternehmen:

    -   Legen Sie die Authentifizierungsebene auf mindestens **RPC \_ C \_ AUTHN \_ LEVEL CONNECT \_ fest.** Für eine bessere Sicherheit sollten Sie die **Verwendung von RPC C \_ \_ AUTHN \_ LEVEL \_ PKT PRIVACY in Betracht \_ ziehen.**
    -   Legen Sie die Identitätswechselebene auf **RPC C IMP LEVEL IDENTIFY \_ \_ \_ \_ fest,** es sei denn, der An anfordernde Prozess muss den Identitätswechsel für bestimmte RPC- oder COM-Aufrufe zulassen, die nicht mit VSS in Zusammenhang stehen.

-   Lassen Sie nur den Zugriff auf angegebene Prozesse zu, um den Prozess des Anfordernden aufrufen zu können.

    Ein COM-Server (z. B. ein An anfordernder Server), der [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) mit einem Nicht-NULL-Sicherheitsdeskriptor als ersten Parameter aufruft, kann den Deskriptor verwenden, um sich selbst so zu konfigurieren, dass eingehende Aufrufe nur von Benutzern akzeptiert werden, die zu einem bestimmten Satz von Konten gehören.

    Ein An anfordernde Benutzer muss sicherstellen, dass COM-Clients, die unter gültigen Benutzern ausgeführt werden, berechtigt sind, in seinen Prozess auf zu rufen. Ein An anfordernder Benutzer, der im ersten Parameter einen Sicherheitsdeskriptor angibt, muss den folgenden Benutzern ermöglichen, eingehende Aufrufe an den Anfordernden Prozess durchzuführen:

    -   Lokales System
    -   Lokaler Dienst

        **Windows XP:** Dieser Wert wird erst ab Windows Server 2003 unterstützt.

    -   Netzwerkdienst

        **Windows XP:** Dieser Wert wird erst ab Windows Server 2003 unterstützt.

    -   Mitglieder der lokalen Administratorgruppe
    -   Mitglieder der lokalen Gruppe "Sicherungsoperatoren"
    -   Spezielle Benutzer, die unten am Registrierungsspeicherort angegeben sind, mit "1" als REG \_ DWORD-Wert

## <a name="explicitly-controlling-user-account-access-to-a-requester"></a>Explizites Steuern des Benutzerkontozugriffs auf einen anfordernden Benutzer

Es gibt Fälle, in denen das Einschränken des Zugriffs auf einen Anfordernden auf Prozesse, die als lokales System oder unter den lokalen Administratoren oder lokalen Sicherungsoperatoren-Gruppen ausgeführt werden, möglicherweise zu restriktiv ist.

Beispielsweise muss ein angegebener Prozess des Anfordernden normalerweise nicht unter einem Administrator- oder Sicherungsoperatorkonto ausgeführt werden. Aus Sicherheitsgründen ist es am besten, die Prozessberechtigungen zur Unterstützung von VSS nicht künstlicher Art zu fördern.

In diesen Fällen muss der **\_ \_** \\  \\  \\  \\ **VSS** \\ **VssAccessControl-Registrierungsschlüssel** von HKEY LOCAL MACHINE SYSTEM CurrentControlSet Services geändert werden, um VSS anweisen zu können, dass ein angegebener Benutzer sicher ist, einen VSS-Anfordernden ausführen zu können.

Unter diesem Schlüssel müssen Sie einen Unterschlüssel erstellen, der denselben Namen wie das Konto hat, dem der Zugriff gewährt oder verweigert werden soll. Dieser Unterschlüssel muss auf einen der Werte in der folgenden Tabelle festgelegt werden.

| Wert | Bedeutung                                             |
|-------|-----------------------------------------------------|
| 0     | Verweigern Sie dem Benutzer den Zugriff auf Ihren Writer und an anfordernden Benutzer.  |
| 1     | Gewähren Sie dem Benutzer Zugriff auf Ihren Writer.               |
| 2     | Gewähren Sie dem Benutzer Zugriff auf Den Anfordernden.            |
| 3     | Gewähren Sie dem Benutzer Zugriff auf Ihren Writer und an anfordernden Benutzer. |



 

Im folgenden Beispiel wird Zugriff auf das Konto "MyDomain \\ MyUser" gewährt:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  MyDomain\MyUser = 2<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

Dieser Mechanismus kann auch verwendet werden, um explizit zu verhindern, dass ein ansonsten zugelassener Benutzer einen VSS-Anfordernden ausführen kann. Im folgenden Beispiel wird der Zugriff über das Konto "ThatDomain \\ Administrator" beschränkt:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  ThatDomain\Administrator = 0<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

Der Benutzer ThatDomain \\ Administrator kann keine VSS-Anfordernde ausführen.

## <a name="performing-a-file-backup-of-the-system-state"></a>Ausführen einer Dateisicherung des Systemstatus

Wenn eine Anfordernde eine Systemstatussicherung durch Sichern einzelner Dateien ausführt, anstatt ein Volumeimage für die Sicherung zu verwenden, muss sie die [**Funktionen FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) und [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) aufrufen, um harte Links für Dateien aufzuzählen, die sich in den folgenden Verzeichnissen befinden:

-   \\Windows system32 \\ WDI \\ perftrack\\
-   \\Windows Winsxs\\

Auf diese Verzeichnisse kann nur von Mitgliedern der Gruppe Administratoren zugegriffen werden. Aus diesem Grund muss eine solche Anfordernde unter dem Systemkonto oder einem Benutzerkonto ausgeführt werden, das Mitglied der Gruppe Administratoren ist.

**Windows XP und Windows Server 2003:** Die [**Funktionen FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) und [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) werden erst nach Windows Vista und Windows Server 2008 unterstützt.

 

 
