---
description: Die VSS-Infrastruktur erfordert, dass VSS-Anforderer (z. b. Sicherungs Anwendungen) sowohl als com-Clients als auch als Server fungieren kann.
ms.assetid: b01145c6-76ba-4a81-bca6-59c4ca488dac
title: Sicherheitsüberlegungen für anfordernde Personen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e989793dbf5a5dd1fac3224cf6f06958564de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345009"
---
# <a name="security-considerations-for-requesters"></a>Sicherheitsüberlegungen für anfordernde Personen

Die VSS-Infrastruktur erfordert, dass VSS-Anforderer (z. b. Sicherungs Anwendungen) sowohl als com-Clients als auch als Server fungieren kann.

Wenn ein Anforderer als Server fungiert, macht er einen Satz von com-Rückruf Schnittstellen verfügbar, die von externen Prozessen (z. b. Writer oder VSS-Dienst) aufgerufen werden können. Daher müssen Anforderer sicher verwalten, welche com-Clients eingehende com-Aufrufe in seinem Prozess durchführen können.

Ebenso können Anforderer als com-Client für die COM-APIs fungieren, die von einem VSS Writer oder vom VSS-Dienst bereitgestellt werden. Die requestspezifischen Sicherheitseinstellungen müssen ausgehende com-Aufrufe von der anfordernden Person an diese anderen Prozesse zulassen.

Der einfachste Mechanismus zur Verwaltung der Sicherheitsprobleme eines Anforderers umfasst die richtige Auswahl des Benutzerkontos, unter dem es ausgeführt wird.

Ein Anforderer muss in der Regel unter einem Benutzer ausgeführt werden, der Mitglied der Gruppe "Administratoren" oder der Gruppe "Sicherungs-Operatoren" ist oder als lokales System Konto ausgeführt wird.

Wenn eine anfordernde Person als com-Client fungiert und diese nicht unter diesen Konten ausgeführt wird, wird jeder com-Befehl standardmäßig automatisch mit **E \_ AccessDenied** abgelehnt, ohne dass die Implementierung der com-Methode erfolgt.

## <a name="disabling-com-exception-handling"></a>Deaktivieren der com-Ausnahmebehandlung

Legen Sie beim Entwickeln eines Anforderers das Flag com-comglb \_ Exception \_ donot \_ handle Global Options fest, um die com-Ausnahmebehandlung zu deaktivieren. Dies ist wichtig, da durch die com-Ausnahmebehandlung schwerwiegende Fehler in einer VSS-Anwendung maskiert werden können. Der Fehler, der maskiert wird, kann den Prozess in einem instabilen und unvorhersehbaren Zustand belassen, was zu Beschädigungen und hängen von Beschädigungen führen kann. Weitere Informationen zu diesem Flag finden Sie unter [iglobaloptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).

## <a name="setting-requester-default-com-access-check-permission"></a>Festlegen der Berechtigung "Requester default com Access Check"

Die anfordernde Person muss beachten, dass bei Ihrem Prozess als Server (z. b. zum Ändern des Dokuments der Sicherungs Komponenten) eingehende Anrufe von anderen VSS-Teilnehmern (z. b. Writer oder VSS-Dienst) zugelassen werden.

Standardmäßig lässt ein Windows-Prozess jedoch nur com-Clients zu, die in derselben Anmelde Sitzung (der Self-sid) ausgeführt werden oder unter dem lokalen System Konto ausgeführt werden. Dies ist ein potenzielles Problem, da diese Standardwerte für die VSS-Infrastruktur nicht ausreichen. Writer können z. b. als "Sicherungs Operator"-Benutzerkonto ausgeführt werden, das sich weder in derselben Anmelde Sitzung wie der requestprozess noch in einem lokalen System Konto befindet.

Um diese Art von Problem zu behandeln, kann jeder com-Server Prozess besser steuern, ob ein RPC-oder com-Client eine durch den Server implementierte com-Methode (in diesem Fall eine anfordernde Person) ausführen darf (in diesem Fall ein Anforderer), indem er [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) verwendet, um eine Prozess weite "Standard-com-Zugriffs Überprüfung"

Anforderer kann explizit folgende Aktionen ausführen:

-   Ermöglicht allen Prozessen den Zugriff, um den Anforderer Prozess aufzurufen.

    Diese Option ist möglicherweise für die Mehrheit der Anforderer geeignet und wird von anderen com-Servern verwendet – beispielsweise verwenden alle svchost-basierten Windows-Dienste diese Option bereits, ebenso wie alle com+-Dienste standardmäßig.

    Das zulassen, dass alle Prozesse eingehende com-Aufrufe durchführen, ist nicht notwendigerweise eine Sicherheits Schwachstelle. Ein Anforderer, der als com-Server fungiert, wie alle anderen com-Server, behält immer die Option bei, seine Clients für jede com-Methode zu autorisieren, die in seinem Prozess implementiert ist.

    Beachten Sie, dass die von VSS implementierten internen com-Rückrufe standardmäßig gesichert werden.

    Um allen Prozessen den com-Zugriff auf einen Anforderer zuzulassen, können Sie einen **null** -Sicherheits Deskriptor als ersten Parameter von [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)übergeben. (Beachten Sie, dass **CoInitializeSecurity** höchstens einmal für den gesamten Prozess aufgerufen werden muss. Weitere Informationen zu **CoInitializeSecurity** -aufrufen finden Sie in der com-Dokumentation oder in MSDN.

    Im folgenden Codebeispiel wird gezeigt, wie ein Anforderer [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 8 und Windows Server 2012 und höher aufruft, um mit VSS für Remote Dateifreigaben (rvss) kompatibel zu sein:

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

    Wenn Sie die Sicherheit der com-Ebene eines Anforderers mit [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)explizit festlegen, sollten Sie die folgenden Schritte ausführen:

    -   Legen Sie für die Authentifizierungs Stufe mindestens **die \_ \_ \_ \_ Pkt- \_ Integrität der RPC-C-authn-Ebene** fest. Um die Sicherheit zu erhöhen, sollten Sie die Verwendung von **RPC \_ C \_ authn \_ Level \_ Pkt \_ Privacy** in Erwägung gezogen
    -   Legen Sie die Identitätswechsel Ebene auf **RPC- \_ C- \_ IMP- \_ Ebene \_** Identitätswechsel fest.
    -   Legen Sie die Sicherheitsfunktionen für die Sicherheit auf " **eoac \_ static**" fest. Weitere Informationen zum verzippen der Sicherheit finden Sie unter [Cloaking (Cloaking](../com/cloaking.md)).

    Im folgenden Codebeispiel wird gezeigt, wie ein Anforderer [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 7 und Windows Server 2008 R2 und früher aufruft (oder in Windows 8 und Windows Server 2012 und höher, wenn keine rvss-Kompatibilität erforderlich ist):

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

    Wenn Sie die Sicherheit der com-Ebene eines Anforderers mit [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)explizit festlegen, sollten Sie die folgenden Schritte ausführen:

    -   Legen Sie die Authentifizierungs Ebene auf mindestens **RPC \_ C \_ authn \_ Level \_ Connect** fest. Um die Sicherheit zu erhöhen, sollten Sie die Verwendung von **RPC \_ C \_ authn \_ Level \_ Pkt \_ Privacy** in Erwägung gezogen
    -   Legen Sie die Identitätswechsel Ebene auf **RPC \_ C \_ IMP- \_ Ebene \_ identifizieren** fest, es sei denn, der requestprozess muss den Identitätswechsel für bestimmte RPC-oder COM-Aufrufe zulassen, die nicht mit VSS verknüpft sind.

-   Erlauben Sie nur angegebenen Prozessen den Zugriff, um den requestprozess aufzurufen.

    Ein com-Server (z. b. ein Anforderer), der [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) mit einem Sicherheits Deskriptor ungleich **null** als ersten Parameter aufruft, kann den Deskriptor verwenden, um nur eingehende Aufrufe von Benutzern zu akzeptieren, die zu einem bestimmten Satz von Konten gehören.

    Ein Anforderer muss sicherstellen, dass com-Clients, die unter gültigen Benutzern ausgeführt werden, autorisiert sind, seinen Prozess aufzurufen. Ein Anforderer, der eine Sicherheits Beschreibung im ersten Parameter angibt, muss den folgenden Benutzern erlauben, eingehende Aufrufe in den requestprozess auszuführen:

    -   Lokales System
    -   Lokaler Dienst

        **Windows XP:** Dieser Wert wird bis Windows Server 2003 nicht unterstützt.

    -   Netzwerkdienst

        **Windows XP:** Dieser Wert wird bis Windows Server 2003 nicht unterstützt.

    -   Mitglieder der lokalen Gruppe "Administratoren"
    -   Mitglieder der Gruppe der lokalen Sicherungs Operatoren
    -   Besondere Benutzer, die am folgenden Registrierungs Speicherort angegeben sind, mit "1" als reg \_ DWORD-Wert

## <a name="explicitly-controlling-user-account-access-to-a-requester"></a>Explizites Steuern des Benutzerkonto Zugriffs auf einen Anforderer

Es gibt Fälle, in denen der Zugriff auf einen Anforderer auf Prozesse beschränkt wird, die als lokales System oder unter den Gruppen "lokale Administratoren" oder "lokale Sicherungs Operatoren" ausgeführt werden.

Beispielsweise muss ein angegebener Anforderer Prozess normalerweise nicht unter einem Administrator Konto oder einem Sicherungs Operator Konto ausgeführt werden. Aus Sicherheitsgründen wäre es am besten, die Prozess Privilegien nicht künstlich herauf zusetzen, um VSS zu unterstützen.

In diesen Fällen muss der **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VSS** \\ **VssAccessControl** -Registrierungsschlüssel geändert werden, um VSS anzuweisen, dass ein angegebener Benutzer sicher ist, einen VSS-Anforderer auszuführen.

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
                  MyDomain\MyUser = 2<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

Dieser Mechanismus kann auch verwendet werden, um einen anderweitig zugelassenen Benutzer explizit daran zu hindern, eine VSS-Anforderer zu verwenden. Im folgenden Beispiel wird der Zugriff auf das Konto "das Domänen \\ Administrator Konto" beschränkt:

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

Der Benutzer, der Domänen \\ Administrator ist, kann keine VSS-Anforderer ausführen.

## <a name="performing-a-file-backup-of-the-system-state"></a>Ausführen einer Datei Sicherung des System Status

Wenn ein Anforderer die Systemstatus Sicherung durch Sicherung einzelner Dateien durchführt, anstatt ein Volumeabbild für die Sicherung zu verwenden, muss er die Funktionen [**findfirstdateinamew**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) und [**FindNextFile amew**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) zum Auflisten von festen Links für Dateien, die sich in den folgenden Verzeichnissen befinden, aufzählen:

-   Windows \\ system32 \\ WDI \\ perftrack\\
-   Windows- \\ WinSxS\\

Auf diese Verzeichnisse kann nur von Mitgliedern der Gruppe "Administratoren" zugegriffen werden. Aus diesem Grund muss ein solcher Anforderer unter dem Systemkonto oder einem Benutzerkonto ausgeführt werden, das Mitglied der Gruppe "Administratoren" ist.

**Windows XP und Windows Server 2003:** Die Funktionen [**findfirstdateinamew**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) und [**FindNextFile amew**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) werden bis Windows Vista und Windows Server 2008 nicht unterstützt.

 

 
