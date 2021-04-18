---
description: Die VSS-Infrastruktur erfordert, dass Writer-Prozesse sowohl als com-Clients als auch als Server fungieren können.
ms.assetid: 59bb7a86-e874-45ce-abd6-cafd18802c4d
title: Sicherheitsüberlegungen für Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea6f88243adbd62d928170a86ed57b91cbebe134
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347107"
---
# <a name="security-considerations-for-writers"></a>Sicherheitsüberlegungen für Writer

Die VSS-Infrastruktur erfordert, dass Writer-Prozesse sowohl als com-Clients als auch als Server fungieren können.

Wenn Sie als Server fungieren, machen VSS Writer com-Schnittstellen verfügbar (z. b. die VSS-Ereignishandler wie [**CVssWriter: onidentifizieren**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)) und empfangen von eingehenden com-Aufrufen von VSS-Prozessen (z. b. anfordernde Personen und VSS-Dienst) oder RPC-Aufrufen von Prozessen, die sich außerhalb von VSS befinden, normalerweise wenn diese Prozesse VSS-Ereignisse generieren (z. b. Wenn ein Anforderer [**IVssBackupComponents:: gatherbeschreimetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)aufruft) Aus diesem Grund muss ein VSS Writer sicher verwalten, welche com-Clients eingehende com-Aufrufe in seinem Prozess durchführen können.

Ebenso können VSS-Writer auch als com-Clients fungieren und ausgehende com-Aufrufe von Rückrufen, die von der VSS-Infrastruktur bereitgestellt werden, oder RPC-Aufrufe an externe Prozesse von VSS ausführen. Diese Rückrufe, die entweder von einer Sicherungs Anwendung oder vom VSS-Dienst bereitgestellt werden, ermöglichen es dem Writer, Aufgaben auszuführen, z. b. das Aktualisieren des Sicherungs Komponenten Dokuments über die [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle. Daher müssen die VSS-Sicherheitseinstellungen Writer das Ausführen von ausgehenden com-aufrufen in andere VSS-Prozesse ermöglichen.

Der einfachste Mechanismus zum Verwalten von Writer-Sicherheitsproblemen umfasst die richtige Auswahl des Benutzerkontos, unter dem es ausgeführt wird. Ein Writer muss in der Regel unter einem Benutzer ausgeführt werden, der Mitglied der Gruppe "Administratoren" oder der Gruppe "Sicherungs-Operatoren" ist, oder er muss als lokales System Konto ausgeführt werden.

Wenn ein Writer als com-Client fungiert und dieser nicht unter diesen Konten ausgeführt wird, wird ein beliebiger com-Befehl standardmäßig automatisch mit **E \_ AccessDenied** abgelehnt, ohne dass die Implementierung der com-Methode erfolgt.

## <a name="disabling-com-exception-handling"></a>Deaktivieren der com-Ausnahmebehandlung

Wenn Sie einen Writer entwickeln, legen Sie das Flag com comglb \_ Exception \_ donot \_ handle Global Options fest, um die com-Ausnahmebehandlung zu deaktivieren. Dies ist wichtig, da durch die com-Ausnahmebehandlung schwerwiegende Fehler in einer VSS-Anwendung maskiert werden können. Der Fehler, der maskiert wird, kann den Prozess in einem instabilen und unvorhersehbaren Zustand belassen, was zu Beschädigungen und hängen von Beschädigungen führen kann. Weitere Informationen zu diesem Flag finden Sie unter [iglobaloptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).

## <a name="setting-writer-default-com-access-check-permission"></a>Festlegen der com-Standard Zugriffs Überprüfung-Berechtigung für Writer

Writer müssen sich bewusst sein, dass Sie, wenn Ihre Prozesse als Server fungieren (z. b. zum Verarbeiten von VSS-Ereignissen), eingehende Aufrufe von anderen VSS-Teilnehmern zulassen müssen, z. b. Anforderer oder VSS-Dienst.

Standardmäßig lässt ein Prozess jedoch nur com-Clients zu, die in derselben Anmelde Sitzung ausgeführt werden, oder unter dem lokalen System Konto. Dies ist ein potenzielles Problem, da diese Standardwerte nicht ausreichen, um die VSS-Infrastruktur zu unterstützen. Beispielsweise können Anforderer als Benutzerkonto "Sicherungs Operator" ausgeführt werden, das sich weder in derselben Anmelde Sitzung wie der Schreiber Prozess noch in einem lokalen System Konto befindet.

Um diese Art von Problem zu behandeln, kann jeder com-Server Prozess besser steuern, ob ein RPC-oder com-Client eine com-Methode ausführen darf (in diesem Fall ein Writer), indem er [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) zum Festlegen einer Prozess weiten Standard-com-Zugriffs Überprüfung-Berechtigung verwendet.

Writer können explizit folgende Aktionen ausführen:

-   Ermöglicht allen Prozessen den Zugriff, um den Schreibprozess aufzurufen.

    Diese Option ist möglicherweise für viele Writer geeignet und wird von anderen com-Servern verwendet – z. b. werden alle svchost-basierten Windows-Dienste diese Option bereits verwenden, ebenso wie alle com+-Dienste standardmäßig.

    Das zulassen, dass alle Prozesse eingehende com-Aufrufe durchführen, ist nicht notwendigerweise eine Sicherheits Schwachstelle. Ein Writer, der als com-Server fungiert, wie alle anderen com-Server, behält immer die Option bei, seine Clients für jede in seinem Prozess implementierte com-Methode zu autorialisieren.

    Um allen Prozessen den com-Zugriff auf einen Writer zu ermöglichen, können Sie einen **null** -Sicherheits Deskriptor als ersten Parameter von [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)übergeben. (Beachten Sie, dass **CoInitializeSecurity** höchstens einmal für den gesamten Prozess aufgerufen werden muss. Weitere Informationen zu **CoInitializeSecurity** finden Sie in der com-Dokumentation.)

    Im folgenden finden Sie ein Codebeispiel, das einen [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)-aufrufswert enthält:

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

    Wenn Sie die Sicherheit eines Writers auf com-Ebene mit [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)explizit festlegen, sollten Sie die folgenden Schritte ausführen:

    -   Legen Sie die Authentifizierungs Ebene auf mindestens **RPC \_ C \_ authn \_ Level \_ Connect** fest.

        Um die Sicherheit zu erhöhen, sollten Sie die Verwendung von **RPC \_ C \_ authn \_ Level \_ Pkt \_ Privacy** in Erwägung gezogen

    -   Legen Sie die Identitätswechsel Ebene auf **RPC \_ C \_ IMP- \_ Ebene \_ identifizieren** fest, es sei denn, der Schreiber Prozess muss den Identitätswechsel für bestimmte RPC-oder COM-Aufrufe zulassen, die nicht mit VSS verknüpft sind.

-   Erlauben Sie nur angegebenen Prozessen den Zugriff, um den Writer-Prozess aufzurufen.

    Ein com-Server (z. b. ein Writer), der [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) mit einem Sicherheits Deskriptor ungleich **null** aufruft, kann den Deskriptor verwenden, um nur eingehende Aufrufe von Benutzern zu akzeptieren, die zu einem bestimmten Satz von Konten gehören.

    Ein Writer muss sicherstellen, dass com-Clients, die unter gültigen Benutzern ausgeführt werden, autorisiert sind, den Prozess aufzurufen. Ein Writer, der eine Sicherheits Beschreibung im ersten Parameter angibt, muss den folgenden Benutzern erlauben, eingehende Aufrufe in den requestprozess auszuführen:

    -   Lokales System
    -   Mitglieder der lokalen Gruppe "Administratoren"
    -   Mitglieder der Gruppe der lokalen Sicherungs Operatoren
    -   Das Konto, unter dem der Writer ausgeführt wird.

## <a name="explicitly-controlling-user-account-access-to-a-writer"></a>Explizites Steuern des Benutzerkonto Zugriffs auf einen Writer

Es gibt Fälle, in denen der Zugriff auf einen Writer auf Prozesse beschränkt wird, die als lokales System oder unter den lokalen Gruppen Administratoren oder lokale Sicherungs Operatoren ausgeführt werden, möglicherweise zu restriktiv.

Ein Writer-Prozess (z. b. ein nicht-System-Writer von Drittanbietern) muss normalerweise nicht unter einem Administrator-oder Sicherungs Operator Konto ausgeführt werden. Aus Sicherheitsgründen wäre es am besten, die Berechtigungen des Prozesses zur Unterstützung von VSS nicht künstlich zu fördern.

In diesen Fällen muss der **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VSS** \\ **VssAccessControl** -Registrierungsschlüssel geändert werden, um VSS anzuweisen, dass ein bestimmter Benutzer sicher eine VSS Writer ausführen kann.

Unter diesem Schlüssel müssen Sie einen Unterschlüssel erstellen, der denselben Namen hat wie das Konto, dem der Zugriff gewährt oder verweigert werden soll. Dieser Unterschlüssel muss auf einen der Werte in der folgenden Tabelle festgelegt werden.

| Wert | Bedeutung                                             |
|-------|-----------------------------------------------------|
| 0     | Verweigern Sie dem Benutzer den Zugriff auf Ihren Writer und den Anforderer.  |
| 1     | Gewähren Sie dem Benutzer Zugriff auf Ihren Writer.               |
| 2     | Gewähren Sie dem Benutzer Zugriff auf Ihre Anforderer.            |
| 3     | Gewähren Sie dem Benutzer Zugriff auf Ihren Writer und Anforderer. |



 

Im folgenden Beispiel wird der Zugriff auf das Konto "mydomain \\ myuser" gewährt:

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

Dieser Mechanismus kann auch verwendet werden, um einen anderweitig zugelassenen Benutzer explizit auf die Ausführung einer VSS Writer zu beschränken. Im folgenden Beispiel wird der Zugriff auf das Konto "das Domänen \\ Administrator Konto" beschränkt:

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

Der Benutzer, der Domänen \\ Administrator ist, kann keine VSS Writer ausführen.

 

 
