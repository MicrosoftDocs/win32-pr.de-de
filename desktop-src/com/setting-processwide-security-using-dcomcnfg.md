---
title: Festlegen der Process-Wide Sicherheit mithilfe von DCOMCNFG
description: Möglicherweise möchten Sie die Sicherheit für eine bestimmte Anwendung aktivieren, wenn eine Anwendung Sicherheitsanforderungen hat, die sich von den für andere Anwendungen auf dem Computer benötigten Sicherheitsanforderungen unterscheiden.
ms.assetid: 04a7f688-78a3-490a-bcfa-862824a05422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03174dd66e83a88724ff5d421d7b0dcb0c17699e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311615"
---
# <a name="setting-process-wide-security-using-dcomcnfg"></a>Festlegen der Process-Wide Sicherheit mithilfe von DCOMCNFG

Möglicherweise möchten Sie die Sicherheit für eine bestimmte Anwendung aktivieren, wenn eine Anwendung Sicherheitsanforderungen hat, die sich von den für andere Anwendungen auf dem Computer benötigten Sicherheitsanforderungen unterscheiden. Beispielsweise können Sie sich entscheiden, systemweite Einstellungen für Ihre Anwendungen zu verwenden, die ein niedriges Maß an Sicherheit erfordern, während Sie ein höheres Maß an Sicherheit für eine bestimmte Anwendung festlegen.

Sicherheitseinstellungen in der Registrierung, die für eine bestimmte Anwendung gelten, werden jedoch manchmal nicht verwendet. Beispielsweise werden die Prozess weiten Einstellungen, die Sie in der Registrierung mithilfe Dcomcnfg.exe festlegen, überschrieben, wenn ein Client [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) aufruft, um die Sicherheit für einen bestimmten Schnittstellen Proxy festzulegen. Ebenso gilt: Wenn ein Client oder Server (oder beides) [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) aufruft, um die Sicherheit für einen Prozess festzulegen, werden die Einstellungen in der Registrierung ignoriert, und die für **CoInitializeSecurity** angegebenen Parameter werden stattdessen verwendet.

Wenn Sie die Sicherheit für eine Anwendung aktivieren, müssen möglicherweise mehrere Einstellungen geändert werden. Hierzu zählen die Authentifizierungs Ebene, der Speicherort, Start Berechtigungen, Zugriffsberechtigungen und die Identität. Schritt-für-Schritt-Anleitungen finden Sie in den folgenden Bereichen:

-   [Festlegen der Authentifizierungs Ebene für eine Anwendung](#setting-the-authentication-level-for-an-application)
-   [Festlegen des Speicher Orts für eine Anwendung](#setting-the-location-for-an-application)
-   [Festlegen von Start Berechtigungen für eine Anwendung](#setting-launch-permissions-for-an-application)
-   [Festlegen von Zugriffsberechtigungen für eine Anwendung](#setting-access-permissions-for-an-application)
-   [Festlegen der Identität für eine Anwendung](#setting-the-identity-for-an-application)
-   [Durchsuchen der Benutzerdatenbank](#browsing-the-user-database)
-   [Dcomcnfg.exe-und 64-Bit-Anwendungen](#dcomcnfgexe-and-64-bit-applications)
-   [Zugehörige Themen](#related-topics)

## <a name="setting-the-authentication-level-for-an-application"></a>Festlegen der Authentifizierungs Ebene für eine Anwendung

Um die Sicherheit für eine Anwendung zu aktivieren, müssen Sie eine andere Authentifizierungs Ebene als None festlegen. Die Authentifizierungs Ebene teilt com mit, wie viel Authentifizierungs Schutz erforderlich ist, und kann vom Authentifizieren des Clients beim ersten Methoden aufrufen zum vollständigen Verschlüsseln von Parameter Zuständen reichen.

**So legen Sie die Authentifizierungs Ebene einer Anwendung fest**

1.  Wählen Sie auf der Eigenschaften **Seite der Anwendung in Dcomcnfg.exe die Anwendung** aus, und klicken Sie auf die Schaltfläche mit den **Eigenschaften** (oder Doppelklicken Sie auf die ausgewählte Anwendung).

2.  Wählen Sie auf der Seite **Allgemein** im Listenfeld **Authentifizierungs Ebene** eine andere Authentifizierungs Ebene als **(keine)** aus.

3.  Wenn Sie andere Eigenschaften für diese Anwendung festlegen, klicken Sie auf die Schaltfläche **anwenden** , um die neue Authentifizierungs Ebene anzuwenden. Klicken Sie auf **OK** , wenn Sie das Festlegen der Eigenschaften für diese Anwendung abgeschlossen haben und die Änderungen übernehmen möchten.

## <a name="setting-the-location-for-an-application"></a>Festlegen des Speicher Orts für eine Anwendung

Der Speicherort, den Sie für Ihre Anwendung festlegen, bestimmt den Computer, auf dem die Anwendung ausgeführt wird. Sie können auswählen, ob Sie die Anwendung auf dem Computer, auf dem sich die Daten befinden, auf dem Computer, den Sie zum Festlegen des Speicher Orts verwenden, oder auf einem angegebenen Computer ausführen möchten.

**So legen Sie den Speicherort einer Anwendung fest**

1.  Wenn Dcomcnfg.exe ausgeführt wird, wählen Sie die Anwendung auf der Seite **Anwendungen** aus, und klicken Sie auf die Schaltfläche **Eigenschaften** (oder Doppelklicken Sie auf die ausgewählte Anwendung).

2.  Aktivieren Sie auf der Seite **Speicherort** mindestens ein Kontrollkästchen, das den Orten entspricht, an denen die Anwendung ausgeführt werden soll. Wenn Sie mehr als ein Kontrollkästchen aktivieren, verwendet com das erste Kontrollkästchen, das angewendet wird. Wenn Dcomcnfg.exe auf dem Server Computer ausgeführt wird, wählen Sie immer **Anwendung auf diesem Computer ausführen aus**.

3.  Wenn Sie andere Eigenschaften für diese Anwendung festlegen, klicken Sie auf die Schaltfläche **anwenden** , um den neuen Speicherort zu übernehmen. Wählen Sie **OK** aus, wenn Sie das Festlegen der Eigenschaften für diese Anwendung abgeschlossen haben und die Änderungen übernehmen möchten.

## <a name="setting-launch-permissions-for-an-application"></a>Festlegen von Start Berechtigungen für eine Anwendung

Mit Dcomcnfg.exe können Sie Start Berechtigungen festlegen, um die Liste der Benutzer zu steuern, denen die Berechtigung zum Starten eines bestimmten Servers erteilt oder verweigert wird. Sie können der Liste Benutzer oder Gruppen hinzufügen und dabei angeben, ob die Zugriffsberechtigung gewährt oder verweigert wird. Sie können Benutzer auch aus der Liste entfernen.

**So legen Sie Start Berechtigungen für eine Anwendung fest**

1.  Wenn Dcomcnfg.exe ausgeführt wird, wählen Sie die Anwendung auf der Seite **Anwendungen** aus, und klicken Sie auf die Schaltfläche **Eigenschaften** (oder Doppelklicken Sie auf die ausgewählte Anwendung).

2.  Wählen Sie auf der Eigenschaften Seite **Sicherheit** die Options Schaltfläche **benutzerdefinierte Start Berechtigungen verwenden** aus, und klicken Sie auf die Schaltfläche **Bearbeiten** im gleichen Bereich.

3.  Um Benutzer oder Gruppen zu entfernen, wählen Sie den Benutzer oder die Gruppe aus, den Sie entfernen möchten, und wählen Sie die Schaltfläche **Entfernen** . Der ausgewählte Benutzer oder die ausgewählte Gruppe wird nicht mehr im Listenfeld angezeigt. Wenn Sie das Entfernen von Benutzer und Gruppen abgeschlossen haben, klicken Sie auf **OK**.

4.  Wenn Sie Benutzer oder Gruppen hinzufügen möchten, klicken Sie auf die Schaltfläche **Hinzufügen** .

5.  Wenn Sie den voll qualifizierten Benutzernamen kennen, den Sie hinzufügen möchten, geben Sie ihn in das Textfeld **Namen hinzufügen** ein. Wenn Sie den Benutzernamen nicht kennen, können Sie die Benutzerdatenbank durchsuchen, um Sie zu finden (Weitere Informationen finden Sie unten in der Benutzerdatenbank). Wenn Sie den Benutzernamen gefunden haben, wählen Sie im Listenfeld **Namen** den Benutzer oder die Gruppe aus, und klicken Sie auf die Schaltfläche **Hinzufügen** .

6.  Wählen Sie im Listenfeld **Zugriffstyp** den Zugriffstyp aus ( **starten** oder **verweigern starten**). Wiederholen Sie Schritt 5, um weitere Benutzer hinzuzufügen, die den ausgewählten Zugriffstyp haben werden. Wenn Sie das Hinzufügen von Benutzern für den ausgewählten Zugriffstyp abgeschlossen haben, klicken Sie auf die Schaltfläche **OK** .

7.  Wiederholen Sie die Schritte 5 und 6, um Benutzer hinzuzufügen, die einen anderen Zugriffstyp haben werden. Wählen Sie andernfalls **OK** aus, um die Änderungen zu übernehmen.

## <a name="setting-access-permissions-for-an-application"></a>Festlegen von Zugriffsberechtigungen für eine Anwendung

Mit Dcomcnfg.exe können Sie die Liste der Benutzer verwalten, denen der Zugriff auf die Methoden eines bestimmten Servers durch Festlegen von Zugriffsberechtigungen gewährt oder verweigert wird. Sie können der Liste Benutzer oder Gruppen hinzufügen und dabei angeben, ob die Zugriffsberechtigung gewährt oder verweigert wird. Sie können Benutzer auch aus der Liste entfernen.

Beim Festlegen von Zugriffsberechtigungen müssen Sie sicherstellen, dass das System in der Liste der Benutzer enthalten ist, denen der Zugriff gewährt wird. Wenn Sie allen Benutzern Zugriffsberechtigungen erteilt haben, wird das System implizit eingeschlossen.

Der Vorgang zum Festlegen von Zugriffsberechtigungen für eine Anwendung ähnelt dem Festlegen von Start Berechtigungen. Die Schritte werden im Folgenden beschrieben.

**So legen Sie die Zugriffsberechtigungen für eine Anwendung fest**

1.  Wenn Dcomcnfg.exe ausgeführt wird, wählen Sie die Anwendung auf der Seite **Anwendungen** aus, und klicken Sie auf die Schaltfläche **Eigenschaften** (oder Doppelklicken Sie auf die ausgewählte Anwendung).

2.  Wählen Sie auf der Eigenschaften Seite **Sicherheit** die Options Schaltfläche **Benutzerdefinierte Zugriffsberechtigungen verwenden** aus, und klicken Sie auf die Schaltfläche **Bearbeiten** im gleichen Bereich.

3.  Um Benutzer oder Gruppen zu entfernen, wählen Sie den Benutzer oder die Gruppe aus, den Sie entfernen möchten, und wählen Sie die Schaltfläche **Entfernen** . Der ausgewählte Benutzer oder die ausgewählte Gruppe wird nicht mehr im Listenfeld angezeigt. Wenn Sie das Entfernen von Benutzer und Gruppen abgeschlossen haben, klicken Sie auf **OK**.

4.  Wenn Sie einen Benutzer oder eine Gruppe hinzufügen möchten, klicken Sie auf die Schaltfläche **Hinzufügen** .

5.  Wenn Sie den voll qualifizierten Benutzernamen kennen, den Sie hinzufügen möchten, geben Sie ihn in das Textfeld **Namen hinzufügen** ein. Wenn Sie den Benutzernamen nicht kennen, können Sie die Benutzerdatenbank durchsuchen, um Sie zu finden. Wenn Sie den Benutzernamen gefunden haben, wählen Sie im Listenfeld **Namen** den Benutzer oder die Gruppe aus, und klicken Sie auf die Schaltfläche **Hinzufügen** .

6.  Wählen Sie im Listenfeld **Zugriffstyp** den Zugriffstyp aus (entweder **Zugriff zulassen** oder **Zugriff verweigern**). Wiederholen Sie Schritt 5, um weitere Benutzer hinzuzufügen, die den ausgewählten Zugriffstyp haben werden. Wenn Sie das Hinzufügen von Benutzern für den ausgewählten Zugriffstyp abgeschlossen haben, klicken Sie auf die Schaltfläche **OK** .

7.  Wiederholen Sie die Schritte 5 und 6, um Benutzer hinzuzufügen, die einen anderen Zugriffstyp haben werden. Wählen Sie andernfalls **OK** aus, um die Änderungen zu übernehmen.

## <a name="setting-the-identity-for-an-application"></a>Festlegen der Identität für eine Anwendung

Die Identität einer Anwendung ist das Konto, das zum Ausführen der Anwendung verwendet wird. Dabei kann es sich um die Identität des aktuell angemeldeten Benutzers (interaktiver Benutzer), das Benutzerkonto des Client Prozesses, der den Server gestartet hat, einen angegebenen Benutzer oder einen Dienst. Mit Dcomcnfg.exe können Sie eine dieser Identitäten für die Anwendung auswählen. Hilfe bei der Entscheidung, welche Identität für Ihre Anwendung festgelegt werden soll, finden Sie unter [Anwendungs Identität](application-identity.md).

**So legen Sie die Identität für eine Anwendung fest**

1.  Wenn Dcomcnfg.exe ausgeführt wird, wählen Sie die Anwendung auf der Seite **Anwendungen** aus, und klicken Sie auf die Schaltfläche **Eigenschaften** (oder Doppelklicken Sie auf die ausgewählte Anwendung).

2.  Wählen Sie auf der Eigenschaften Seite **Identität** die Options Schaltfläche für die gewünschte Identität aus. Wenn Sie **diesen Benutzer** auswählen, müssen Sie den Benutzernamen, das Kennwort und das bestätigte Kennwort eingeben.

3.  Wenn Sie andere Eigenschaften für diese Anwendung festlegen, klicken Sie auf die Schaltfläche **anwenden** , um die neue Identität anzuwenden. Wählen Sie **OK** aus, wenn Sie das Festlegen der Eigenschaften für diese Anwendung abgeschlossen haben und die Änderungen übernehmen möchten.

## <a name="browsing-the-user-database"></a>Durchsuchen der Benutzerdatenbank

Wenn Sie den voll qualifizierten Benutzernamen für einen bestimmten Benutzer suchen müssen, suchen Sie in der Benutzerdatenbank Dcomcnfg.exe. Beispielsweise können Sie die Benutzerdatenbank durchsuchen, um einen Benutzer zu finden, den Sie für Zugriffs-oder Start Berechtigungen hinzufügen möchten.

**So durchsuchen Sie die Benutzerdatenbank**

1.  Wählen Sie im Listenfeld **Listennamen aus** die Domäne aus, die den Benutzer oder die Gruppe enthält, den bzw. die Sie hinzufügen möchten.

2.  Um die Benutzer anzuzeigen, die der ausgewählten Domäne angehören, klicken Sie auf die Schaltfläche **Benutzer anzeigen** .

3.  Wenn Sie die Mitglieder einer bestimmten Gruppe anzeigen möchten, wählen Sie die Gruppe im Listenfeld **Namen** aus, und wählen Sie dann die Schaltfläche **Mitglieder anzeigen** aus.

4.  Wenn Sie den Benutzer oder die Gruppe, die Sie hinzufügen möchten, nicht finden können, klicken Sie auf die Schaltfläche **Suchen** , um das Dialogfeld **Konto** suchen zu erhalten. Wählen Sie die zu durchsuchende Domäne aus, oder wählen Sie **Alle suchen** aus, geben Sie den Benutzernamen ein, den Sie suchen möchten, und klicken Sie auf die Schaltfläche **Suchen** .

## <a name="dcomcnfgexe-and-64-bit-applications"></a>Dcomcnfg.exe-und 64-Bit-Anwendungen

Auf x64-Betriebssystemen von Windows XP auf Windows Server 2008 konfiguriert die 64-Bit-Version von DCOMCNFG.EXE nicht ordnungsgemäß die 32-Bit-DCOM-Anwendungen für die Remote Aktivierung. Dieses Verhalten bewirkt, dass Komponenten, die Remote aktiviert werden sollen, stattdessen lokal aktiviert werden. Dieses Verhalten tritt nicht in Windows 7 und Windows Server 2008 R2 und höheren Versionen auf.

Die Problem Umgehung besteht in der Verwendung der 32-Bit-Version von DCOMCNFG. Führen Sie die 32-Bit-Version von mmc.exe aus, und laden Sie mithilfe der folgenden Befehlszeile die 32-Bit-Version des Snap-Ins "Komponenten Dienste".

C: \\ Windows \\ syswow64>**MMC comexp. msc/32**

Die 32-Bit-Version der Komponenten Dienste registriert 32-Bit-DCOM-Anwendungen ordnungsgemäß für die Remote Aktivierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen Process-Wide Sicherheit](setting-processwide-security.md)
</dt> </dl>

 

 




