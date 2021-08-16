---
title: Festlegen Process-Wide-Sicherheit mithilfe von DCOMCNFG
description: Möglicherweise möchten Sie die Sicherheit für eine bestimmte Anwendung aktivieren, wenn für eine Anwendung Sicherheitsanforderungen gelten, die sich von denen unterscheiden, die von anderen Anwendungen auf dem Computer benötigt werden.
ms.assetid: 04a7f688-78a3-490a-bcfa-862824a05422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5ace37c685748983d36b8a1e27a406fb8a81034d82ab793e77c4def960dfa2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309105"
---
# <a name="setting-process-wide-security-using-dcomcnfg"></a>Festlegen Process-Wide-Sicherheit mithilfe von DCOMCNFG

Möglicherweise möchten Sie die Sicherheit für eine bestimmte Anwendung aktivieren, wenn für eine Anwendung Sicherheitsanforderungen gelten, die sich von denen unterscheiden, die von anderen Anwendungen auf dem Computer benötigt werden. Beispielsweise können Sie sich entscheiden, systemweite Einstellungen für Ihre Anwendungen zu verwenden, die ein niedriges Maß an Sicherheit erfordern, und gleichzeitig ein höheres Maß an Sicherheit für eine bestimmte Anwendung festlegen.

Sicherheitseinstellungen in der Registrierung, die für eine bestimmte Anwendung gelten, werden jedoch manchmal nicht verwendet. Beispielsweise werden die prozessweiten Einstellungen, die Sie in der Registrierung mithilfe von Dcomcnfg.exe festlegen, überschrieben, wenn ein Client [**CoSetProxyBlanket aufruft,**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) um die Sicherheit für einen bestimmten Schnittstellenproxy zu erhöhen. Wenn ein Client oder Server (oder beides) [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) aufruft, um die Sicherheit für einen Prozess festzulegen, werden die Einstellungen in der Registrierung ignoriert, und stattdessen werden die für **CoInitializeSecurity** angegebenen Parameter verwendet.

Beim Aktivieren der Sicherheit für eine Anwendung müssen möglicherweise mehrere Einstellungen geändert werden. Dazu gehören Authentifizierungsebene, Standort, Startberechtigungen, Zugriffsberechtigungen und Identität. Schritt-für-Schritt-Verfahren finden Sie in den folgenden Themen:

-   [Festlegen der Authentifizierungsebene für eine Anwendung](#setting-the-authentication-level-for-an-application)
-   [Festlegen des Speicherorts für eine Anwendung](#setting-the-location-for-an-application)
-   [Festlegen von Startberechtigungen für eine Anwendung](#setting-launch-permissions-for-an-application)
-   [Festlegen von Zugriffsberechtigungen für eine Anwendung](#setting-access-permissions-for-an-application)
-   [Festlegen der Identität für eine Anwendung](#setting-the-identity-for-an-application)
-   [Durchsuchen der Benutzerdatenbank](#browsing-the-user-database)
-   [Dcomcnfg.exe und 64-Bit-Anwendungen](#dcomcnfgexe-and-64-bit-applications)
-   [Zugehörige Themen](#related-topics)

## <a name="setting-the-authentication-level-for-an-application"></a>Festlegen der Authentifizierungsebene für eine Anwendung

Um die Sicherheit für eine Anwendung zu aktivieren, müssen Sie eine andere Authentifizierungsebene als Keine festlegen. Die Authentifizierungsebene teilt COM mit, wie viel Authentifizierungsschutz erforderlich ist, und kann von der Authentifizierung des Clients beim ersten Methodenaufruf bis hin zur vollständigen Verschlüsselung von Parameterzuständen reichen.

**So legen Sie die Authentifizierungsebene einer Anwendung fest**

1.  Wählen Sie **auf der** Eigenschaftenseite Anwendungen in Dcomcnfg.exe  die Anwendung aus, und klicken Sie auf die Schaltfläche Eigenschaften (oder doppelklicken Sie auf die ausgewählte Anwendung).

2.  Wählen Sie **auf der** Seite Allgemein im Listenfeld Authentifizierungsebene eine andere Authentifizierungsebene als **(Keine)** aus. 

3.  Wenn Sie andere Eigenschaften für diese Anwendung festlegen möchten, wählen Sie **die** Schaltfläche Anwenden aus, um die neue Authentifizierungsebene anzuwenden. Klicken **Sie auf OK,** wenn Sie mit dem Festlegen der Eigenschaften für diese Anwendung fertig sind und die Änderungen anwenden möchten.

## <a name="setting-the-location-for-an-application"></a>Festlegen des Speicherorts für eine Anwendung

Der Speicherort, den Sie für Ihre Anwendung festlegen, bestimmt den Computer, auf dem die Anwendung ausgeführt wird. Sie können die Anwendung auf dem Computer, auf dem sich die Daten befinden, auf dem Computer, den Sie zum Festlegen des Speicherorts verwenden, oder auf einem angegebenen Computer ausführen.

**So legen Sie den Speicherort einer Anwendung fest**

1.  Wenn Dcomcnfg.exe ausgeführt wird, wählen Sie  die Anwendung auf der Seite Anwendungen und dann die Schaltfläche **Eigenschaften** aus (oder doppelklicken Sie auf die ausgewählte Anwendung).

2.  Aktivieren Sie **auf der** Seite Standort mindestens ein Kontrollkästchen, das den Speicherorten entspricht, an denen die Anwendung ausgeführt werden soll. Wenn Sie mehrere Kontrollkästchen aktivieren, verwendet COM das erste Kontrollkästchen, das angewendet wird. Wenn Dcomcnfg.exe Servercomputer ausgeführt wird, wählen Sie **immer Anwendung auf diesem Computer ausführen aus.**

3.  Wenn Sie andere Eigenschaften für diese Anwendung  festlegen möchten, klicken Sie auf die Schaltfläche Anwenden, um den neuen Speicherort anzuwenden. Wählen **Sie OK** aus, wenn Sie mit dem Festlegen der Eigenschaften für diese Anwendung fertig sind und die Änderungen übernehmen möchten.

## <a name="setting-launch-permissions-for-an-application"></a>Festlegen von Startberechtigungen für eine Anwendung

Mit Dcomcnfg.exe können Sie Startberechtigungen festlegen, um die Liste der Benutzer zu steuern, denen die Berechtigung zum Starten eines bestimmten Servers erteilt oder verweigert wurde. Sie können der Liste Benutzer oder Gruppen hinzufügen und angeben, ob die Zugriffsberechtigung erteilt oder verweigert wird. Sie können Benutzer auch aus der Liste entfernen.

**So legen Sie Startberechtigungen für eine Anwendung fest**

1.  Wenn Dcomcnfg.exe ausgeführt wird, wählen Sie  die Anwendung auf der Seite Anwendungen und dann die Schaltfläche **Eigenschaften** aus (oder doppelklicken Sie auf die ausgewählte Anwendung).

2.  Wählen Sie **auf der**  Eigenschaftenseite Sicherheit die Optionsschaltfläche Benutzerdefinierte Startberechtigungen verwenden aus, und wählen Sie im gleichen Bereich die Schaltfläche Bearbeiten aus. 

3.  Um Benutzer oder Gruppen zu entfernen, wählen Sie den Benutzer oder die Gruppe aus, den bzw. die Sie entfernen möchten, und wählen Sie die **Schaltfläche Entfernen** aus. Der ausgewählte Benutzer oder die ausgewählte Gruppe wird nicht mehr im Listenfeld angezeigt. Wenn Sie das Entfernen von Benutzer und Gruppen abgeschlossen haben, wählen Sie **OK aus.**

4.  Wenn Sie Benutzer oder Gruppen hinzufügen möchten, wählen Sie die **Schaltfläche Hinzufügen** aus.

5.  Wenn Sie den vollqualifizierten Benutzernamen kennen, den Sie hinzufügen möchten, geben Sie ihn in das Textfeld **Namen** hinzufügen ein. Wenn Sie den Benutzernamen nicht kennen, können Sie die Benutzerdatenbank durchsuchen, um sie zu finden (siehe Durchsuchen der Benutzerdatenbank weiter unten). Wenn Sie den Benutzernamen gefunden haben, wählen  Sie den Benutzer oder die Gruppe aus dem Listenfeld Namen und dann die **Schaltfläche Hinzufügen** aus.

6.  Wählen Sie **im Listenfeld Zugriffstyp** den Zugriffstyp aus (entweder Start **zulassen** **oder Start verweigern).** Wiederholen Sie Schritt 5, um weitere Benutzer hinzuzufügen, die über den ausgewählten Zugriffstyp verfügen. Wenn Sie das Hinzufügen von Benutzern für den ausgewählten Zugriffstyp abgeschlossen haben, wählen Sie die Schaltfläche **OK** aus.

7.  Um Benutzer hinzuzufügen, die einen anderen Zugriffstyp haben, wiederholen Sie die Schritte 5 und 6. Wählen Sie andernfalls **OK aus,** um die Änderungen zu übernehmen.

## <a name="setting-access-permissions-for-an-application"></a>Festlegen von Zugriffsberechtigungen für eine Anwendung

Mit Dcomcnfg.exe können Sie die Liste der Benutzer verwalten, denen der Zugriff auf die Methoden eines bestimmten Servers gewährt oder verweigert wird, indem Sie Zugriffsberechtigungen festlegen. Sie können der Liste Benutzer oder Gruppen hinzufügen und angeben, ob die Zugriffsberechtigung erteilt oder verweigert wird. Sie können Benutzer auch aus der Liste entfernen.

Beim Festlegen von Zugriffsberechtigungen müssen Sie sicherstellen, dass SYSTEM in der Liste der Benutzer enthalten ist, denen Zugriff gewährt wird. Wenn Sie jedem Benutzer Zugriffsberechtigungen erteilt haben, wird SYSTEM implizit eingeschlossen.

Das Festlegen von Zugriffsberechtigungen für eine Anwendung ähnelt dem Festlegen von Startberechtigungen. Die Schritte werden im Folgenden beschrieben.

**So legen Sie Zugriffsberechtigungen für eine Anwendung fest**

1.  Wenn Dcomcnfg.exe ausgeführt wird, wählen Sie  die Anwendung auf der Seite Anwendungen und dann die Schaltfläche **Eigenschaften** aus (oder doppelklicken Sie auf die ausgewählte Anwendung).

2.  Wählen Sie **auf der**  Eigenschaftenseite Sicherheit die Optionsschaltfläche Benutzerdefinierte Zugriffsberechtigungen verwenden aus, und wählen Sie im gleichen Bereich die Schaltfläche Bearbeiten aus. 

3.  Um Benutzer oder Gruppen zu entfernen, wählen Sie den Benutzer oder die Gruppe aus, den bzw. die Sie entfernen möchten, und wählen Sie die **Schaltfläche Entfernen** aus. Der ausgewählte Benutzer oder die ausgewählte Gruppe wird nicht mehr im Listenfeld angezeigt. Wenn Sie das Entfernen von Benutzer und Gruppen abgeschlossen haben, wählen Sie **OK aus.**

4.  Wenn Sie einen Benutzer oder eine Gruppe hinzufügen möchten, wählen Sie die **Schaltfläche Hinzufügen** aus.

5.  Wenn Sie den vollqualifizierten Benutzernamen kennen, den Sie hinzufügen möchten, geben Sie ihn in das Textfeld **Namen** hinzufügen ein. Wenn Sie den Benutzernamen nicht kennen, können Sie die Benutzerdatenbank durchsuchen, um sie zu finden. Wenn Sie den Benutzernamen gefunden haben, wählen  Sie den Benutzer oder die Gruppe aus dem Listenfeld Namen und dann die **Schaltfläche Hinzufügen** aus.

6.  Wählen Sie **im Listenfeld Zugriffstyp** den Zugriffstyp aus (entweder **Zugriff zulassen** oder **Zugriff verweigern).** Wiederholen Sie Schritt 5, um weitere Benutzer hinzuzufügen, die über den ausgewählten Zugriffstyp verfügen. Wenn Sie das Hinzufügen von Benutzern für den ausgewählten Zugriffstyp abgeschlossen haben, wählen Sie die Schaltfläche **OK** aus.

7.  Um Benutzer hinzuzufügen, die einen anderen Zugriffstyp haben, wiederholen Sie die Schritte 5 und 6. Wählen Sie andernfalls **OK aus,** um die Änderungen zu übernehmen.

## <a name="setting-the-identity-for-an-application"></a>Festlegen der Identität für eine Anwendung

Die Identität einer Anwendung ist das Konto, das zum Ausführen der Anwendung verwendet wird. Bei der Identität kann es sich um den Benutzer, der derzeit angemeldet ist (der interaktive Benutzer), um das Benutzerkonto des Clientprozesses, der den Server gestartet hat, um einen angegebenen Benutzer oder einen Dienst handelt. Sie können Dcomcnfg.exe verwenden, um eine dieser Identitäten für die Anwendung zu wählen. Hilfe bei der Entscheidung, welche Identität für Ihre Anwendung festgelegt werden soll, finden Sie unter [Anwendungsidentität](application-identity.md).

**So legen Sie die Identität für eine Anwendung fest**

1.  Wenn Dcomcnfg.exe ausgeführt wird, wählen Sie  die Anwendung auf der Seite Anwendungen und dann die Schaltfläche **Eigenschaften** aus (oder doppelklicken Sie auf die ausgewählte Anwendung).

2.  Wählen Sie **auf der** Eigenschaftenseite Identität die Optionsschaltfläche für die identität aus, die Sie wünschen. Wenn Sie Diesen **Benutzer auswählen,** müssen Sie den Benutzernamen, das Kennwort und das bestätigte Kennwort eingeben.

3.  Wenn Sie andere Eigenschaften für diese Anwendung festlegen möchten, wählen Sie **die** Schaltfläche Anwenden aus, um die neue Identität anzuwenden. Wählen **Sie OK** aus, wenn Sie mit dem Festlegen der Eigenschaften für diese Anwendung fertig sind und die Änderungen übernehmen möchten.

## <a name="browsing-the-user-database"></a>Durchsuchen der Benutzerdatenbank

Sie durchsuchen die Benutzerdatenbank in Dcomcnfg.exe, wenn Sie den vollqualifizierten Benutzernamen für einen bestimmten Benutzer suchen müssen. Beispielsweise können Sie die Benutzerdatenbank durchsuchen, um einen Benutzer zu suchen, den Sie für Zugriffs- oder Startberechtigungen hinzufügen möchten.

**So durchsuchen Sie die Benutzerdatenbank**

1.  Wählen Sie **im Listenfeld Listennamen** aus die Domäne aus, die den Benutzer oder die Gruppe enthält, den bzw. die Sie hinzufügen möchten.

2.  Klicken Sie auf die Schaltfläche Benutzer anzeigen, um die Benutzer zu sehen, die **zur ausgewählten Domäne** gehören.

3.  Um die Mitglieder einer bestimmten Gruppe zu sehen, wählen Sie die Gruppe im Listenfeld **Namen** und dann die **Schaltfläche Mitglieder** anzeigen aus.

4.  Wenn Sie den Benutzer oder die Gruppe,  den bzw. die Sie hinzufügen möchten, nicht finden können, wählen Sie die Schaltfläche Suchen aus, die das Dialogfeld **Konto** suchen öffnet. Wählen Sie die Domäne aus, die Sie durchsuchen möchten (oder wählen Sie Alle suchen **aus),** geben Sie den Benutzernamen ein, nach dem Sie suchen möchten, und wählen Sie die **Schaltfläche Suchen** aus.

## <a name="dcomcnfgexe-and-64-bit-applications"></a>Dcomcnfg.exe und 64-Bit-Anwendungen

Unter x64-Betriebssystemen von Windows XP bis Windows Server 2008 konfiguriert die 64-Bit-Version von DCOMCNFG.EXE 32-Bit-DCOM-Anwendungen nicht ordnungsgemäß für die Remoteaktivierung. Dieses Verhalten bewirkt, dass Komponenten, die remote aktiviert werden sollen, anstatt lokal aktiviert werden. Dieses Verhalten tritt in version Windows 7 und Windows Server 2008 R2 und höheren Versionen nicht auf.

Die Problemumgehung besteht in der Verwendung der 32-Bit-Version von DCOMCNFG. Führen Sie die 32-Bit-Version von mmc.exe und laden Sie die 32-Bit-Version des Komponentendienste-Snap-Ins über die folgende Befehlszeile.

C: \\ WINDOWS \\ SysWOW64>**mmc comexp.msc /32**

Die 32-Bit-Version von Component Services registriert ordnungsgemäß 32-Bit-DCOM-Anwendungen für die Remoteaktivierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen Process-Wide Sicherheit](setting-processwide-security.md)
</dt> </dl>

 

 




