---
description: Um mithilfe von WMI eine Verbindung mit einem Remote Computer herzustellen, stellen Sie sicher, dass die richtigen DCOM-Einstellungen und Sicherheitseinstellungen für den WMI-Namespace für die Verbindung aktiviert sind.
ms.assetid: 96ebaa9b-a062-4300-a637-8eb71cb80d1c
ms.tgt_platform: multiple
title: Sichern einer Remote-WMI-Verbindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2a044e49fed5eaa27fbc246dca3306a6c29650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528496"
---
# <a name="securing-a-remote-wmi-connection"></a>Sichern einer Remote-WMI-Verbindung

Um mithilfe von WMI eine Verbindung mit einem Remote Computer herzustellen, stellen Sie sicher, dass die richtigen DCOM-Einstellungen und Sicherheitseinstellungen für den WMI-Namespace für die Verbindung aktiviert sind.

WMI verfügt über Standardeinstellungen für Identitätswechsel, Authentifizierung und Authentifizierungsdienst (NTLM oder Kerberos), die für den Bereitstellungs Zielcomputer in einer Remote Verbindung erforderlich sind. Auf dem lokalen Computer werden möglicherweise andere Standardwerte verwendet, die vom Zielsystem nicht akzeptiert werden. Sie können diese Einstellungen im Verbindungs Befehl ändern.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [DCOM-Identitätswechsel-und Authentifizierungs Einstellungen für WMI](#dcom-impersonation-and-authentication-settings-for-wmi)
-   [Festlegen der DCOM-Sicherheit, damit ein Benutzer Remote auf einen Computer zugreifen kann](#setting-dcom-security-to-allow-a-user-to-access-a-computer-remotely)
-   [Zulassen des Zugriffs auf einen bestimmten WMI-Namespace für Benutzer](#allowing-users-access-to-a-specific-wmi-namespace)
-   [Festlegen der Namespace Sicherheit, um die Datenverschlüsselung für Remote Verbindungen zu erfordern](#setting-namespace-security-to-require-data-encryption-for-remote-connections)
-   [Zugehörige Themen](#related-topics)

## <a name="dcom-impersonation-and-authentication-settings-for-wmi"></a>DCOM-Identitätswechsel-und Authentifizierungs Einstellungen für WMI

WMI verfügt über die Standardeinstellungen für den DCOM-Identitätswechsel, die Authentifizierung und den Authentifizierungsdienst (NTLM oder Kerberos), die für ein Remote System erforderlich sind. Ihr lokales System verwendet möglicherweise andere Standardwerte, die vom Ziel Remote System nicht akzeptiert werden. Sie können diese Einstellungen im Verbindungs Befehl ändern. Weitere Informationen finden Sie unter [Festlegen der Prozesssicherheit für Client Anwendungen](setting-client-application-process-security.md). Für den Authentifizierungsdienst wird jedoch empfohlen, **RPC \_ C \_ authn \_ default** anzugeben und DCOM die Auswahl des entsprechenden Dienstanbieter für den Zielcomputer zu ermöglichen.

Sie können Einstellungen in den Parametern für die Aufrufe von [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) oder [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) in C++ angeben. In Skripts können Sie Sicherheitseinstellungen in Aufrufen von " [**Swap-Locator. ConnectServer**](swbemlocator-connectserver.md)", in einem " [**Swap Security**](swbemsecurity.md) "-Objekt oder in der Skript- [Monikerzeichenfolge](constructing-a-moniker-string.md) festlegen.

Eine Liste aller C++-Identitätswechsel Konstanten finden [Sie unter Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von C++](setting-the-default-process-security-level-using-c-.md). Informationen zu den Visual Basic Konstanten und Skript Zeichenfolgen für die Verwendung der monikerverbindung finden Sie unter [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md).

In der folgenden Tabelle werden die Standardeinstellungen für den DCOM-Identitätswechsel, die Authentifizierung und den Authentifizierungsdienst aufgelistet, die für den Zielcomputer (Computer B) in einer Remote Verbindung erforderlich sind. Weitere Informationen finden Sie unter Sichern einer Remote-WMI-Verbindung.



| Computer B-Betriebssystem | Skript Zeichenfolge der Identitätswechsel Ebene | Skript Zeichenfolge auf Authentifizierungs Ebene | Authentifizierungsdienst |
|-----------------------------|--------------------------------------|---------------------------------------|------------------------|
| Windows Vista oder höher      | Impersonate                          | Pkt                                   | Kerberos               |



 

WMI-Remote Verbindungen sind von der [Benutzerkontensteuerung (UAC)](/previous-versions/aa905108(v=msdn.10)) und der [Windows-Firewall](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx)betroffen. Weitere Informationen finden Sie unter [Herstellen einer Remote Verbindung mit WMI ab Vista](connecting-to-wmi-remotely-starting-with-vista.md) und [Herstellen einer Verbindung über die Windows-Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).

Beachten Sie, dass das Herstellen einer Verbindung mit WMI auf dem lokalen Computer über eine Standard Authentifizierungs Ebene von **PKTPRIVACY** verfügt.

## <a name="setting-dcom-security-to-allow-a-user-to-access-a-computer-remotely"></a>Festlegen der DCOM-Sicherheit, damit ein Benutzer Remote auf einen Computer zugreifen kann

Die Sicherheit in WMI bezieht sich auf das Herstellen einer Verbindung mit einem WMI-Namespace. WMI verwendet DCOM zum Verarbeiten von Remote aufrufen. Ein Fehler beim Herstellen einer Verbindung mit einem Remote Computer besteht aus einem DCOM-Fehler (Fehler "DCOM-Zugriff verweigert" Decimal-2147024891 oder Hex 0x80070005). Weitere Informationen zur DCOM-Sicherheit in WMI für C++-Anwendungen finden Sie unter [Festlegen der Prozesssicherheit für Client](setting-client-application-process-security.md)Anwendungen.

Sie können DCOM-Einstellungen für WMI mithilfe des DCOM-Konfigurations Hilfsprogramms (**DCOMCnfg.exe**) konfigurieren, das Sie in der **Systemsteuerung** unter **Verwaltung** finden. Dieses Hilfsprogramm macht die Einstellungen verfügbar, mit denen bestimmte Benutzer eine Remote Verbindung mit dem Computer über DCOM herstellen können. Mitglieder der Gruppe "Administratoren" können standardmäßig eine Remote Verbindung mit dem Computer herstellen. Mit diesem Hilfsprogramm können Sie die Sicherheit festlegen, um den WMI-Dienst zu starten, darauf zuzugreifen und ihn zu konfigurieren.

Im folgenden Verfahren wird beschrieben, wie Sie DCOM-Remote Start-und Aktivierungs Berechtigungen für bestimmte Benutzer und Gruppen erteilen. Wenn Computer a eine Remote Verbindung mit Computer b herstellt, können Sie diese Berechtigungen auf Computer b festlegen, um zuzulassen, dass ein Benutzer oder eine Gruppe, der nicht Teil der Administratoren Gruppe auf Computer b ist, DCOM-Start-und Aktivierungs Aufrufe auf Computer b ausführt.

**So erteilen Sie DCOM-Remote Start-und Aktivierungs Berechtigungen für einen Benutzer oder eine Gruppe**

1.  Klicken Sie im **Startmenü** auf **Ausführen**, geben Sie **DCOMCNFG** ein, und klicken Sie dann auf **OK**.
2.  Erweitern Sie im Dialogfeld **Komponenten Dienste** nacheinander **Komponenten Dienste** und **Computer**, und klicken Sie dann mit der rechten Maustaste auf **Arbeitsplatz** und klicken Sie dann auf **Eigenschaften**.
3.  Klicken Sie im Dialogfeld **Eigenschaften von Arbeitsplatz** auf die Registerkarte **com-Sicherheit** .
4.  Klicken Sie unter **Start- und Aktivierungsberechtigungen** auf **Limits bearbeiten**.
5.  Führen Sie im Dialogfeld **Startberechtigung** die folgenden Schritte aus, wenn der Name oder die Gruppe nicht in der **Liste Gruppen oder Benutzernamen** angezeigt wird:

    1.  Klicken Sie im Dialogfeld **Startberechtigung** auf **Hinzufügen**.
    2.  Fügen Sie im Dialogfeld **Benutzer, Computer oder Gruppen auswählen** im Feld **Geben Sie die zu ausgewäfnenden Objektnamen** ein den Namen und die Gruppe ein, und klicken Sie dann auf **OK**.

6.  Wählen Sie im Dialogfeld **Startberechtigung** im Feld **Gruppen-oder Benutzernamen** den Benutzer und die Gruppe aus. Wählen Sie in der Spalte **zulassen** unter **Berechtigungen für Benutzer** die Option **Remote Start** aus, und wählen Sie **Remote Aktivierung** aus, und klicken Sie dann auf **OK**.

Im folgenden Verfahren wird beschrieben, wie Sie DCOM-Remote Zugriffsberechtigungen für bestimmte Benutzer und Gruppen erteilen. Wenn Computer a eine Remote Verbindung mit Computer b herstellt, können Sie diese Berechtigungen auf Computer b festlegen, um zuzulassen, dass ein Benutzer oder eine Gruppe, der nicht Teil der Administratoren Gruppe auf Computer b ist, eine Verbindung mit Computer b herstellt.

**So erteilen Sie DCOM-Remote Zugriffsberechtigungen**

1.  Klicken Sie im **Startmenü** auf **Ausführen**, geben Sie **DCOMCNFG** ein, und klicken Sie dann auf **OK**.
2.  Erweitern Sie im Dialogfeld **Komponenten Dienste** nacheinander **Komponenten Dienste** und **Computer**, und klicken Sie dann mit der rechten Maustaste auf **Arbeitsplatz** und klicken Sie dann auf **Eigenschaften**.
3.  Klicken Sie im Dialogfeld **Eigenschaften von Arbeitsplatz** auf die Registerkarte **com-Sicherheit** .
4.  Klicken Sie unter **Zugriffsberechtigungen** auf **Limits bearbeiten**.
5.  Wählen Sie im Dialogfeld **Zugriffsberechtigung** die Option **Anonymer Anmelde** Name im Feld **Gruppen-oder Benutzernamen** aus. Wählen Sie in der Spalte **zulassen** unter **Berechtigungen für Benutzer** die Option **Remote Zugriff** aus, und klicken Sie dann auf **OK**.

## <a name="allowing-users-access-to-a-specific-wmi-namespace"></a>Zulassen des Zugriffs auf einen bestimmten WMI-Namespace für Benutzer

Sie können Benutzern den Zugriff auf einen bestimmten WMI-Namespace erlauben oder ablehnen, indem Sie im WMI-Steuerelement für einen Namespace die Berechtigung "Remote Aktivierung" festlegen. Wenn ein Benutzer versucht, eine Verbindung mit einem Namespace herzustellen, für den er keinen Zugriff hat, erhalten Sie den Fehler 0x80041003. Diese Berechtigung ist standardmäßig nur für Administratoren aktiviert. Ein Administrator kann den Remote Zugriff auf bestimmte WMI-Namespaces für einen nicht Administrator Benutzer aktivieren.

Mit dem folgenden Verfahren werden Berechtigungen für Remote Aktivierung für einen Benutzer ohne Administratorrechte festgelegt.

**So legen Sie Berechtigungen für Remote Aktivierung fest**

1.  Stellen Sie mithilfe der WMI-Steuerung eine Verbindung mit dem Remote Computer her.

    Weitere Informationen zum WMI-Steuerelement finden Sie unter [Festlegen der Namespace Sicherheit mit dem WMI-Steuer](setting-namespace-security-with-the-wmi-control.md)Element.

2.  Wählen Sie auf der Registerkarte **Sicherheit** den Namespace aus, und klicken Sie auf **Sicherheit**.
3.  Suchen Sie das entsprechende Konto, und überprüfen Sie **Remote Aktivierung** in der Liste der **Berechtigungen** .

## <a name="setting-namespace-security-to-require-data-encryption-for-remote-connections"></a>Festlegen der Namespace Sicherheit, um die Datenverschlüsselung für Remote Verbindungen zu erfordern

Ein Administrator oder eine MOF-Datei kann einen WMI-Namespace so konfigurieren, dass keine Daten zurückgegeben werden, es sei denn, Sie verwenden den Datenschutz für den Datenschutz in einer Verbindung mit diesem Namespace in einem Skript als Moniker für die Datenschutz **\_ Ebene " \_ \_ \_ Pkt \_** " und " **PKTPRIVACY** " in einem Skript Dadurch wird sichergestellt, dass die Daten beim Überschreiten des Netzwerks verschlüsselt werden. Wenn Sie versuchen, eine niedrigere Authentifizierungs Ebene festzulegen, erhalten Sie die Meldung "Zugriff verweigert". Weitere Informationen finden Sie unter [erfordern einer verschlüsselten Verbindung mit einem Namespace](requiring-an-encrypted-connection-to-a-namespace.md).

Im folgenden VBScript-Codebeispiel wird gezeigt, wie mithilfe von "PKTPRIVACY" eine Verbindung mit einem verschlüsselten Namespace hergestellt wird.


```VB
strComputer = "RemoteComputer"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktPrivacy}!\\" _
                              & strComputer & "\root\EncryptedNamespace")
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Delegierung mit WMI](connecting-to-a-3rd-computer-delegation.md)
</dt> <dt>

[Erstellen von Prozessen per Remote Verbindung mit WMI](creating-processes-remotely.md)
</dt> <dt>

[Sichern von C++-Clients und-Anbietern](securing-c---clients-and-providers.md)
</dt> <dt>

[Sichern von Skript Clients](securing-scripting-clients.md)
</dt> </dl>

 

 
