---
description: Die VSS-Infrastruktur erfordert Writerprozesse, um sowohl als COM-Clients als auch als Server funktionieren zu können.
ms.assetid: 59bb7a86-e874-45ce-abd6-cafd18802c4d
title: Sicherheitsüberlegungen für Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 601b981613636a571c204acdfac78ada778bb19b16a3d2677c4e56ff3ee099cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767680"
---
# <a name="security-considerations-for-writers"></a>Sicherheitsüberlegungen für Writer

Die VSS-Infrastruktur erfordert Writerprozesse, um sowohl als COM-Clients als auch als Server funktionieren zu können.

Wenn VSS-Writer als Server fungieren, machen SIE COM-Schnittstellen verfügbar (z. B. die VSS-Ereignishandler wie [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)) und empfangen eingehende COM-Aufrufe von VSS-Prozessen (z. B. Anforderer und den VSS-Dienst) oder RPC-Aufrufe von Prozessen, die sich außerhalb von VSS befinden, in der Regel, wenn diese Prozesse VSS-Ereignisse generieren (z. B. wenn ein Anforderer [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)aufruft). Daher muss ein VSS Writer sicher verwalten, welche COM-Clients eingehende COM-Aufrufe in den Prozess durchführen können.

Auf ähnliche Weise können VSS-Writer auch als COM-Clients fungieren und ausgehende COM-Aufrufe von Rückrufen vornehmen, die von der VSS-Infrastruktur bereitgestellt werden, oder RPC-Aufrufe an Prozesse außerhalb von VSS. Diese Rückrufe, die entweder von einer Sicherungsanwendung oder vom VSS-Dienst bereitgestellt werden, ermöglichen es dem Writer, Aufgaben wie das Aktualisieren des Sicherungskomponentendokuments über die [**IVssComponent-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) auszuführen. Daher müssen VSS-Sicherheitseinstellungen Writern ermöglichen, ausgehende COM-Aufrufe an andere VSS-Prozesse zu senden.

Der einfachste Mechanismus zum Verwalten von Schreibsicherheitsproblemen umfasst die richtige Auswahl des Benutzerkontos, unter dem es ausgeführt wird. Ein Writer muss in der Regel unter einem Benutzer ausgeführt werden, der Mitglied der Gruppe Administratoren oder sicherungsoperatoren ist, oder er muss als lokales Systemkonto ausgeführt werden.

Wenn ein Writer als COM-Client fungiert und nicht unter diesen Konten ausgeführt wird, wird jeder COM-Aufruf, den er vornimmt, standardmäßig automatisch mit **E \_ ACCESSDENIED** abgelehnt, ohne die IMPLEMENTIERUNG der COM-Methode zu durchlaufen.

## <a name="disabling-com-exception-handling"></a>Deaktivieren der COM-Ausnahmebehandlung

Legen Sie beim Entwickeln eines Writers das globale Optionsflag COMGLB \_ EXCEPTION \_ DONOT \_ HANDLE fest, um die COM-Ausnahmebehandlung zu deaktivieren. Dies ist wichtig, da die COM-Ausnahmebehandlung schwerwiegende Fehler in einer VSS-Anwendung maskieren kann. Der maskierte Fehler kann den Prozess in einem instabilen und unvorhersehbaren Zustand belassen, was zu Beschädigungen und Hängen führen kann. Weitere Informationen zu diesem Flag finden Sie unter [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).

## <a name="setting-writer-default-com-access-check-permission"></a>Festlegen der STANDARDMÄßIGEN COM-Zugriffsüberprüfungsberechtigung für Writer

Writer müssen beachten, dass sie eingehende Aufrufe von anderen VSS-Teilnehmern wie Anforderern oder dem VSS-Dienst zulassen müssen, wenn ihre Prozesse als Server fungieren (z. B. zur Behandlung von VSS-Ereignissen).

Standardmäßig lässt ein Prozess jedoch nur COM-Clients zu, die unter derselben Anmeldesitzung (SELF SID) oder unter dem lokalen Systemkonto ausgeführt werden. Dies ist ein potenzielles Problem, da diese Standardwerte nicht ausreichen, um die VSS-Infrastruktur zu unterstützen. Anforderer können beispielsweise als "Sicherungsoperator"-Benutzerkonto ausgeführt werden, das sich weder in derselben Anmeldesitzung wie der Writerprozess noch in einem lokalen Systemkonto befindet.

Um diese Art von Problem zu behandeln, kann jeder COM-Serverprozess weitere Kontrolle darüber haben, ob ein RPC- oder COM-Client eine COM-Methode ausführen darf, die der Server (in diesem Fall ein Writer) implementiert, indem [**coInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) verwendet wird, um eine prozessweite STANDARDMÄßIGe COM-Zugriffsüberprüfungsberechtigung festzulegen.

Writer können folgende Schritte explizit ausführen:

-   Ermöglicht allen Prozessen den Zugriff, um den Writerprozess aufzurufen.

    Diese Option ist möglicherweise für viele Writer geeignet und wird von anderen COM-Servern verwendet, z. B. verwenden alle SVCHOST-basierten Windows Dienste diese Option bereits, ebenso wie alle COM+-Dienste standardmäßig.

    Das Zulassen von eingehenden COM-Aufrufen durch alle Prozesse ist nicht unbedingt eine Sicherheitsrisiko. Ein Writer, der wie alle anderen COM-Server als COM-Server fungiert, behält immer die Möglichkeit, seine Clients für jede com-Methode zu autorisieren, die in seinem Prozess implementiert ist.

    Um allen Prozessen COM-Zugriff auf einen  Writer zu gewähren, können Sie einen NULL-Sicherheitsdeskriptor als ersten Parameter von [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)übergeben. (Beachten Sie, dass **CoInitializeSecurity** für den gesamten Prozess höchstens einmal aufgerufen werden muss. Weitere Informationen zu **CoInitializeSecurity** finden Sie in der COM-Dokumentation.)

    Im Folgenden finden Sie ein Codebeispiel, das einen Aufruf von [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)enthält:

    ``` syntax
    // Initialize COM security.
    hr = CoInitializeSecurity(
           NULL,                          // PSECURITY_DESCRIPTOR          pSecDesc,
           -1,                            // LONG                          cAuthSvc,
           NULL,                          // SOLE_AUTHENTICATION_SERVICE  *asAuthSvc,
           NULL,                          // void                         *pReserved1,
           RPC_C_AUTHN_LEVEL_PKT_PRIVACY, // DWORD                         dwAuthnLevel,
           RPC_C_IMP_LEVEL_IDENTIFY,      // DWORD                         dwImpLevel,
           NULL,                          // void                         *pAuthList,
           EOAC_NONE,                     // DWORD                         dwCapabilities,
           NULL                           // void                         *pReserved3
        );
    ```

    Wenn Sie die Sicherheit auf COM-Ebene eines Writers explizit mit [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)festlegen, sollten Sie folgende Schritte ausführen:

    -   Legen Sie die Authentifizierungsebene auf mindestens **RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT** fest.

        Um die Sicherheit zu erhöhen, sollten Sie **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY** verwenden.

    -   Legen Sie die Identitätswechselebene auf **RPC \_ C \_ IMP LEVEL \_ \_ IDENTIFY** fest, es sei denn, der Writerprozess muss den Identitätswechsel für bestimmte RPC- oder COM-Aufrufe zulassen, die nicht mit VSS in Zusammenhang stehen.

-   Lassen Sie nur angegebenen Prozessen den Zugriff auf den Writer-Prozess zu.

    Ein COM-Server (z. B. ein Writer), der [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) mit einem Nicht-NULL-Sicherheitsdeskriptor aufruft, kann den Deskriptor verwenden, um sich so zu konfigurieren, dass er nur eingehende Aufrufe von Benutzern akzeptiert, die zu einer bestimmten Gruppe von Konten gehören.

    Ein Writer muss sicherstellen, dass COM-Clients, die unter gültigen Benutzern ausgeführt werden, berechtigt sind, den Prozess aufzurufen. Ein Writer, der einen Sicherheitsdeskriptor im ersten Parameter angibt, muss es den folgenden Benutzern ermöglichen, eingehende Aufrufe im Anfordererprozess auszuführen:

    -   Lokales System
    -   Mitglieder der lokalen Gruppe "Administratoren"
    -   Mitglieder der lokalen Gruppe Sicherungsoperatoren
    -   Das Konto, unter dem der Writer ausgeführt wird

## <a name="explicitly-controlling-user-account-access-to-a-writer"></a>Explizites Steuern des Benutzerkontozugriffs auf einen Writer

Es gibt Fälle, in denen das Einschränken des Zugriffs auf einen Writer auf Prozesse, die als lokales System oder unter den lokalen Administratoren oder lokalen Sicherungsoperatoren ausgeführt werden, zu restriktiv ist.

Beispielsweise muss ein Writerprozess (z. B. ein Nicht-Systemwriter eines Drittanbieters) normalerweise nicht unter einem Administrator- oder Sicherungsoperatorkonto ausgeführt werden. Aus Sicherheitsgründen empfiehlt es sich, die Berechtigungen des Prozesses zur Unterstützung von VSS nicht auf künstliche Weise heraufzustufen.

In diesen Fällen muss der **Registrierungsschlüssel HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **VSS** \\ **VssAccessControl** geändert werden, um VSS anzuweisen, dass ein angegebener Benutzer sicher ist, einen VSS Writer auszuführen.

Unter diesem Schlüssel müssen Sie einen Unterschlüssel erstellen, der den gleichen Namen wie das Konto hat, dem der Zugriff gewährt oder verweigert werden soll. Dieser Unterschlüssel muss auf einen der Werte in der folgenden Tabelle festgelegt werden.

| Wert | Bedeutung                                             |
|-------|-----------------------------------------------------|
| 0     | Verweigern Sie dem Benutzer den Zugriff auf Ihren Writer und Anforderer.  |
| 1     | Gewähren Sie dem Benutzer Zugriff auf Ihren Writer.               |
| 2     | Gewähren Sie dem Benutzer Zugriff auf Ihren Anforderer.            |
| 3     | Gewähren Sie dem Benutzer Zugriff auf Ihren Writer und Anforderer. |



 

Im folgenden Beispiel wird Zugriff auf das Konto "MyDomain \\ MyUser" gewährt:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  MyDomain\MyUser = 1<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

Dieser Mechanismus kann auch verwendet werden, um einem andernfalls zugelassenen Benutzer explizit die Ausführung eines VSS Writer einzuschränken. Im folgenden Beispiel wird der Zugriff auf das Konto "ThatDomain \\ Administrator" eingeschränkt:

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

Der Benutzer ThatDomain \\ Administrator kann keinen VSS Writer ausführen.

 

 
