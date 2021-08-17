---
description: Um mithilfe von WMI eine Verbindung mit einem Remotecomputer herzustellen, stellen Sie sicher, dass die richtigen DCOM-Einstellungen und WMI-Namespacesicherheitseinstellungen für die Verbindung aktiviert sind.
ms.assetid: 96ebaa9b-a062-4300-a637-8eb71cb80d1c
ms.tgt_platform: multiple
title: Sichern einer WMI-Remoteverbindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8650ee47c549121a51e5d131055a84c176da944c6146f0532ffc86f1d2f9e4c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739514"
---
# <a name="securing-a-remote-wmi-connection"></a>Sichern einer WMI-Remoteverbindung

Um mithilfe von WMI eine Verbindung mit einem Remotecomputer herzustellen, stellen Sie sicher, dass die richtigen DCOM-Einstellungen und WMI-Namespacesicherheitseinstellungen für die Verbindung aktiviert sind.

WMI verfügt über Standardeinstellungen für Identitätswechsel, Authentifizierung und Authentifizierungsdienst (NTLM oder Kerberos), die der Zielcomputer in einer Remoteverbindung erfordert. Ihr lokaler Computer verwendet möglicherweise andere Standardwerte, die das Zielsystem nicht akzeptiert. Sie können diese Einstellungen im Verbindungsaufruf ändern.

Die folgenden Abschnitte werden in diesem Thema erläutert:

-   [DCOM-Identitätswechsel und Authentifizierungs-Einstellungen für WMI](#dcom-impersonation-and-authentication-settings-for-wmi)
-   [Festlegen der DCOM-Sicherheit, sodass ein Benutzer remote auf einen Computer zugreifen kann](#setting-dcom-security-to-allow-a-user-to-access-a-computer-remotely)
-   [Zulassen des Zugriffs auf einen bestimmten WMI-Namespace für Benutzer](#allowing-users-access-to-a-specific-wmi-namespace)
-   [Festlegen der Namespacesicherheit auf Datenverschlüsselung für Remoteverbindungen erforderlich](#setting-namespace-security-to-require-data-encryption-for-remote-connections)
-   [Zugehörige Themen](#related-topics)

## <a name="dcom-impersonation-and-authentication-settings-for-wmi"></a>DCOM-Identitätswechsel und Authentifizierungs-Einstellungen für WMI

WMI verfügt über standardeinstellungen für DCOM-Identitätswechsel, Authentifizierung und Authentifizierungsdienst (NTLM oder Kerberos), die für ein Remotesystem erforderlich sind. Ihr lokales System verwendet möglicherweise andere Standardwerte, die das Ziel-Remotesystem nicht akzeptiert. Sie können diese Einstellungen im Verbindungsaufruf ändern. Weitere Informationen finden Sie unter [Setting Client Application Process Security](setting-client-application-process-security.md). Für den Authentifizierungsdienst wird jedoch empfohlen, **RPC \_ C \_ AUTHN \_ DEFAULT** anzugeben und DCOM die Auswahl des geeigneten Diensts für den Zielcomputer zu erlauben.

Sie können Einstellungen in Parametern für die Aufrufe von [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) oder [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) in C++ angeben. In Skripts können Sie Sicherheitseinstellungen in Aufrufen von [**SWbemLocator.ConnectServer,**](swbemlocator-connectserver.md)in einem [**SWbemSecurity-Objekt**](swbemsecurity.md) oder in der [Skriptmonikerzeichenfolge](constructing-a-moniker-string.md) einrichten.

Eine Liste aller C++-Identitätswechselkonstanten finden Sie unter [Festlegen der Standardprozesssicherheitsstufe mit C++](setting-the-default-process-security-level-using-c-.md). Informationen zu den Visual Basic Konstanten und Skriptzeichenfolgen für die Verwendung der Monikerverbindung finden Sie unter [Festlegen der Standardprozesssicherheitsstufe mit VBScript.](setting-the-default-process-security-level-using-vbscript.md)

In der folgenden Tabelle sind die Standardeinstellungen für DCOM-Identitätswechsel, Authentifizierung und Authentifizierungsdienst aufgeführt, die für den Zielcomputer (Computer B) in einer Remoteverbindung erforderlich sind. Weitere Informationen finden Sie unter Sichern einer WMI-Remoteverbindung.



| Betriebssystem "Computer B" | Skriptzeichenfolge auf Identitätswechselebene | Skriptzeichenfolge auf Authentifizierungsebene | Authentifizierungsdienst |
|-----------------------------|--------------------------------------|---------------------------------------|------------------------|
| Windows Vista oder höher      | Impersonate                          | Pkt                                   | Kerberos               |



 

WMI-Remoteverbindungen sind von [benutzerkontensteuerung (User Account Control, UAC)](/previous-versions/aa905108(v=msdn.10)) und [Windows Firewall](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx)betroffen. Weitere Informationen finden Sie unter [Connecting to WMI Remotely Starting with Vista (Remoteverbindung mit WMI ab Vista)](connecting-to-wmi-remotely-starting-with-vista.md) und [Connecting Through Windows Firewall (Herstellen einer Verbindung über Windows Firewall).](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista)

Beachten Sie, dass das Herstellen einer Verbindung mit WMI auf dem lokalen Computer über die Standardauthentifizierungsebene **PktPrivacy verfügt.**

## <a name="setting-dcom-security-to-allow-a-user-to-access-a-computer-remotely"></a>Festlegen der DCOM-Sicherheit, sodass ein Benutzer remote auf einen Computer zugreifen kann

Die Sicherheit in WMI bezieht sich auf das Herstellen einer Verbindung mit einem WMI-Namespace. WMI verwendet DCOM, um Remoteaufrufe zu verarbeiten. Ein Grund für das Fehlschlagen der Verbindung mit einem Remotecomputer ist ein DCOM-Fehler (Fehler "DCOM Access Denied" decimal -2147024891 oder hex 0x80070005). Weitere Informationen zur DCOM-Sicherheit in WMI für C++-Anwendungen finden Sie unter [Setting Client Application Process Security](setting-client-application-process-security.md).

Sie können die DCOM-Einstellungen für WMI mithilfe des DCOM-Konfigurationshilfsprogramms (**DCOMCnfg.exe**) konfigurieren, das sich unter **Verwaltung** in **Systemsteuerung**. Dieses Hilfsprogramm macht die Einstellungen verfügbar, die es bestimmten Benutzern ermöglichen, eine Remoteverbindung mit dem Computer über DCOM herzustellen. Mitglieder der Gruppe Administratoren dürfen standardmäßig eine Remoteverbindung mit dem Computer herstellen. Mit diesem Hilfsprogramm können Sie die Sicherheit festlegen, um den WMI-Dienst zu starten, darauf zuzugreifen und diesen zu konfigurieren.

Im folgenden Verfahren wird beschrieben, wie Sie bestimmten Benutzern und Gruppen DCOM-Remotestart- und Aktivierungsberechtigungen erteilen. Wenn Computer A eine Remoteverbindung mit Computer B herstellt, können Sie diese Berechtigungen auf Computer B festlegen, damit ein Benutzer oder eine Gruppe, der bzw. die nicht Teil der Gruppe Administratoren auf Computer B ist, DCOM-Start- und Aktivierungsaufrufe auf Computer B ausführen kann.

**So erteilen Sie einem Benutzer oder einer Gruppe Remotestart- und Aktivierungsberechtigungen für DCOM**

1.  Klicken Sie auf **Start**, klicken Sie auf **Ausführen**, geben **Sie DCOMCNFG** ein, und klicken Sie dann auf **OK.**
2.  Erweitern Sie im Dialogfeld **Komponentendienste** den Bereich **Komponentendienste**, erweitern Sie **Computer**, und klicken Sie dann mit der rechten Maustaste auf **Arbeitsplatz,** und klicken Sie auf **Eigenschaften.**
3.  Klicken Sie im Dialogfeld **Arbeitsplatz Eigenschaften** auf die Registerkarte **COM-Sicherheit.**
4.  Klicken Sie unter **Start- und Aktivierungsberechtigungen** auf **Limits bearbeiten**.
5.  Führen Sie im Dialogfeld **Startberechtigung** die folgenden Schritte aus, wenn Ihr Name oder Ihre Gruppe nicht in der **Liste Gruppen oder Benutzernamen** angezeigt wird:

    1.  Klicken Sie im Dialogfeld **Startberechtigung** auf **Hinzufügen.**
    2.  Fügen Sie im Dialogfeld **Benutzer, Computer oder Gruppen auswählen** Ihren Namen und die Gruppe im Feld Geben Sie die **auszuwählende Objektnamen ein** , und klicken Sie dann auf **OK.**

6.  Wählen Sie im Dialogfeld **Startberechtigung** den Benutzer und die Gruppe im Feld **Gruppe oder Benutzernamen** aus. Wählen Sie in der Spalte **Zulassen** unter **Berechtigungen für Benutzer** die Option **Remotestart** aus, und wählen Sie **Remoteaktivierung** aus, und klicken Sie dann auf **OK.**

Im folgenden Verfahren wird beschrieben, wie Sie DCOM-Remotezugriffsberechtigungen für bestimmte Benutzer und Gruppen gewähren. Wenn Computer A eine Remoteverbindung mit Computer B herstellt, können Sie diese Berechtigungen auf Computer B festlegen, damit ein Benutzer oder eine Gruppe, der bzw. die nicht Teil der Gruppe Administratoren auf Computer B ist, eine Verbindung mit Computer B herstellen kann.

**So erteilen Sie DCOM-Remotezugriffsberechtigungen**

1.  Klicken Sie auf **Start**, klicken Sie auf **Ausführen**, geben **Sie DCOMCNFG** ein, und klicken Sie dann auf **OK.**
2.  Erweitern Sie im Dialogfeld **Komponentendienste** den Bereich **Komponentendienste**, erweitern Sie **Computer**, und klicken Sie dann mit der rechten Maustaste auf **Arbeitsplatz,** und klicken Sie auf **Eigenschaften.**
3.  Klicken Sie im Dialogfeld **Arbeitsplatz Eigenschaften** auf die Registerkarte **COM-Sicherheit.**
4.  Klicken Sie unter **Zugriffsberechtigungen** auf **Limits bearbeiten**.
5.  Wählen Sie im Dialogfeld **Zugriffsberechtigung** im Feld **Gruppen- oder Benutzernamen** die Option **ANONYMER ANMELDENAME** aus. Wählen **Sie** in der Spalte Zulassen unter **Berechtigungen für Benutzer** die Option **Remotezugriff** aus, und klicken Sie dann auf **OK.**

## <a name="allowing-users-access-to-a-specific-wmi-namespace"></a>Zulassen des Zugriffs auf einen bestimmten WMI-Namespace für Benutzer

Sie können Benutzern den Zugriff auf einen bestimmten WMI-Namespace erlauben oder nicht erlauben, indem Sie die Berechtigung "Remote enable" im WMI-Steuerelement für einen Namespace festlegen. Wenn ein Benutzer versucht, eine Verbindung mit einem Namespace herzustellen, auf den er keinen Zugriff hat, erhält er einen Fehler 0x80041003. Standardmäßig ist diese Berechtigung nur für Administratoren aktiviert. Ein Administrator kann den Remotezugriff auf bestimmte WMI-Namespaces für einen Nichtadministratorbenutzer aktivieren.

Mit dem folgenden Verfahren werden Remoteberechtigungen für Benutzer ohne Administratorrechte festgelegt.

**So legen Sie Remoteberechtigungen für die Aktivierung fest**

1.  Verbinden mithilfe des WMI-Steuerelements zum Remotecomputer.

    Weitere Informationen zum WMI-Steuerelement finden Sie unter Festlegen der [Namespacesicherheit mit dem WMI-Steuerelement.](setting-namespace-security-with-the-wmi-control.md)

2.  Wählen Sie auf der Registerkarte **Sicherheit** den Namespace aus, und klicken Sie auf **Sicherheit.**
3.  Suchen Sie das entsprechende Konto, und aktivieren **Sie Remote aktivieren** in der Liste **Berechtigungen.**

## <a name="setting-namespace-security-to-require-data-encryption-for-remote-connections"></a>Festlegen der Namespacesicherheit auf Datenverschlüsselung für Remoteverbindungen erforderlich

Ein Administrator oder eine MOF-Datei kann einen WMI-Namespace so konfigurieren, dass keine Daten zurückgegeben werden, es sei denn, Sie verwenden Paketdatenschutz **(RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY** oder **PktPrivacy** als Moniker in einem Skript) in einer Verbindung mit diesem Namespace. Dadurch wird sichergestellt, dass Daten verschlüsselt werden, während sie das Netzwerk passieren. Wenn Sie versuchen, eine niedrigere Authentifizierungsebene festzulegen, erhalten Sie die Meldung Zugriff verweigert. Weitere Informationen finden Sie unter [Erfordern einer verschlüsselten Verbindung mit einem Namespace.](requiring-an-encrypted-connection-to-a-namespace.md)

Das folgende VBScript-Codebeispiel zeigt, wie Sie mithilfe von "pktPrivacy" eine Verbindung mit einem verschlüsselten Namespace herstellen.


```VB
strComputer = "RemoteComputer"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktPrivacy}!\\" _
                              & strComputer & "\root\EncryptedNamespace")
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Delegieren mit WMI](connecting-to-a-3rd-computer-delegation.md)
</dt> <dt>

[Remoteerstellung von Prozessen mit WMI](creating-processes-remotely.md)
</dt> <dt>

[Sichern von C++-Clients und -Anbietern](securing-c---clients-and-providers.md)
</dt> <dt>

[Sichern von Skriptclients](securing-scripting-clients.md)
</dt> </dl>

 

 
