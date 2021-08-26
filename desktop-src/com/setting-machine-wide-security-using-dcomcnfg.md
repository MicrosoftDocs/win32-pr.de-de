---
title: Festlegen System-Wide Sicherheit mithilfe von DCOMCNFG
description: Wenn Sie möchten, dass alle Anwendungen auf einem Computer, die keine eigene Sicherheit bieten, die gleichen Standardsicherheitseinstellungen verwenden, legen Sie die Sicherheit systemweit fest.
ms.assetid: 23d1e222-c00b-497c-adc8-4ae14c5bdd98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7914fd3b1561900426e2928a5277cb845918e3b8d1b1ad1569ea8db0d112e218
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954370"
---
# <a name="setting-system-wide-security-using-dcomcnfg"></a>Festlegen System-Wide Sicherheit mithilfe von DCOMCNFG

Das Ändern der systemweiten Sicherheitseinstellungen wirkt sich auf alle COM-Serveranwendungen aus, die keine eigene prozessweite Sicherheit festlegen. Dies kann verhindern, dass solche Anwendungen ordnungsgemäß funktionieren. Wenn Sie die systemweiten Sicherheitseinstellungen so ändern, dass sie sich auf die Sicherheitseinstellungen für eine bestimmte COM-Anwendung auswirken, sollten Sie stattdessen die prozessweiten Sicherheitseinstellungen für diese bestimmte COM-Anwendung ändern. Weitere Informationen zum Festlegen der prozessweiten Sicherheit finden Sie unter [Festlegen der prozessweiten Sicherheit.](setting-processwide-security.md)

Wenn Sie möchten, dass alle Anwendungen auf einem Computer, die keine eigene Sicherheit bieten, die gleichen Standardsicherheitseinstellungen verwenden, legen Sie die Sicherheit systemweit fest. Die Verwendung von Dcomcnfg.exe erleichtert das Festlegen von Standardwerten in der Registrierung, die für alle Anwendungen auf einem Computer gelten.

Es ist wichtig zu verstehen, dass die Standardeinstellungen in der Registrierung ignoriert werden und die Parameter für [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) stattdessen für die Sicherheitseinstellungen für den Prozess verwendet werden, wenn der Client oder Server **CoInitializeSecurity** explizit aufruft, um die prozessweite Sicherheit festzulegen. Wenn Sie Dcomcnfg.exe verwenden, um Sicherheitseinstellungen für einen bestimmten Prozess anzugeben, werden die Standardcomputereinstellungen durch die Einstellungen für den Prozess überschrieben.

Wenn Sie die systemweite Sicherheit aktivieren, müssen Sie die Authentifizierungsebene auf einen anderen Wert als None festlegen, und Sie müssen Start- und Zugriffsberechtigungen festlegen. Sie haben die Möglichkeit, die Standardidentitätswechselebene festzulegen, und Sie können auch die Verweisnachverfolgung aktivieren. Die folgenden Themen enthalten schrittweise Verfahren:

-   [Festlegen System-Wide Standardauthentifizierungsebene](#setting-system-wide-default-authentication-level)
-   [Festlegen System-Wide Startberechtigungen](#setting-system-wide-launch-permissions)
-   [Festlegen System-Wide Zugriffsberechtigungen](#setting-system-wide-access-permissions)
-   [Festlegen System-Wide Identitätswechselebene](#setting-system-wide-impersonation-level)
-   [Festlegen System-Wide Verweisnachverfolgung](#setting-system-wide-reference-tracking)
-   [Aktivieren und Deaktivieren von DCOM](#enabling-and-disabling-dcom)
-   [Zugehörige Themen](#related-topics)

## <a name="setting-system-wide-default-authentication-level"></a>Festlegen System-Wide Standardauthentifizierungsebene

Die Authentifizierungsebene wird verwendet, um COM mitzuteilen, auf welcher Ebene der Client authentifiziert werden soll. Diese Ebenen bieten verschiedene Schutzebenen, von keinem Schutz bis hin zur vollständigen Verschlüsselung. Um die Sicherheit für einen Computer zu aktivieren, müssen Sie eine andere Authentifizierungsebene als Keine auswählen. Sie können eine solche Einstellung mit Dcomcnfg.exe auswählen, indem Sie die folgenden Schritte ausführen.

**So legen Sie die Authentifizierungsebene systemweit fest**

1.  Führen Sie "Dcomcnfg.exe" aus.

2.  Wählen Sie die Registerkarte **Standardeigenschaften** aus.

3.  Wählen Sie im Listenfeld **Standardauthentifizierungsebene** einen anderen Wert als **(Keine)** aus.

4.  Wenn Sie weitere Eigenschaften für den Computer festlegen, klicken Sie auf die Schaltfläche **Anwenden,** um die neue Authentifizierungsebene anzuwenden. Klicken Sie andernfalls auf **OK,** um die Änderungen zu übernehmen und Dcomcnfg.exe zu beenden.

## <a name="setting-system-wide-launch-permissions"></a>Festlegen System-Wide Startberechtigungen

Die Startberechtigungen, die Sie mit Dcomcnfg.exe festlegen, bestimmen eine Liste von Benutzern, von denen jeder explizit die Berechtigung zum Starten eines Servers erteilt oder verweigert wird, der keine eigenen Startberechtigungseinstellungen bereitstellt. Wenn Sie Startberechtigungen festlegen, können Sie mindestens einen Benutzer oder eine Gruppe aus dieser Liste hinzufügen oder daraus entfernen. Für jeden Benutzer, den Sie hinzufügen, müssen Sie angeben, ob dem Benutzer die Startberechtigung erteilt oder verweigert wird.

**So legen Sie Startberechtigungen für einen Computer fest**

1.  Wählen Sie auf der Eigenschaftenseite **Standardsicherheit** in Dcomcnfg.exe im Bereich **Standardstartberechtigungen** die Schaltfläche **Standard bearbeiten** aus.

2.  Um Benutzer oder Gruppen zu entfernen, wählen Sie den Benutzer oder die Gruppe aus, den bzw. die Sie entfernen möchten, und klicken Sie auf die Schaltfläche **Entfernen.** Der ausgewählte Benutzer oder die ausgewählte Gruppe wird nicht mehr im Listenfeld angezeigt. Wenn Sie das Entfernen von Benutzern und Gruppen abgeschlossen haben, wählen Sie **OK** aus.

3.  Wenn Sie einen Benutzer oder eine Gruppe hinzufügen möchten, wählen Sie die Schaltfläche **Hinzufügen** aus.

4.  Wenn Sie den vollqualifizierten Benutzernamen kennen, den Sie hinzufügen möchten, geben Sie ihn in das Textfeld **Namen hinzufügen** ein. Wenn Sie den Benutzernamen nicht kennen, finden Sie weitere Informationen unter **Setting Processwide Security Using DCOMCNFG (Festlegen der prozessweiten Sicherheit mit DCOMCNFG).** Wenn Sie den Benutzernamen gefunden haben, wählen Sie den Benutzer oder die Gruppe aus dem Listenfeld **Namen** und dann die Schaltfläche **Hinzufügen** aus.

5.  Wählen Sie im Listenfeld **Zugriffstyp** den Zugriffstyp aus (start **zulassen** oder **Starten verweigern).** Wiederholen Sie Schritt 4, um andere Benutzer hinzuzufügen, die ebenfalls über den ausgewählten Zugriffstyp verfügen. Wenn Sie das Hinzufügen von Benutzern für den ausgewählten Zugriffstyp abgeschlossen haben, wählen Sie die Schaltfläche **OK** aus.

6.  Wiederholen Sie die Schritte 4 und 5, um Benutzer hinzuzufügen, die über einen anderen Zugriffstyp verfügen. Wählen Sie andernfalls **OK** aus, um die Änderungen zu übernehmen.

## <a name="setting-system-wide-access-permissions"></a>Festlegen System-Wide Zugriffsberechtigungen

Dcomcnfg.exe können Sie Zugriffsberechtigungen festlegen, um die Liste der Benutzer zu steuern, denen der Zugriff auf die Methoden dieser Server gewährt oder verweigert wird, die keine eigenen Zugriffsberechtigungen bereitstellen. Sie können der Liste Benutzer oder Gruppen hinzufügen und angeben, ob die Zugriffsberechtigung erteilt oder verweigert wird. Sie können benutzer auch aus der Liste entfernen.

Wenn Sie Zugriffsberechtigungen festlegen, müssen Sie sicherstellen, dass SYSTEM in der Liste der Benutzer enthalten ist, denen Zugriff gewährt wird. Wenn Sie Allen Zugriffsrechte erteilt haben, wird SYSTEM implizit eingeschlossen.

Das Festlegen von Zugriffsberechtigungen für einen Computer ähnelt dem Festlegen von Startberechtigungen. Die folgenden Schritte sollten ausgeführt werden.

**So legen Sie Zugriffsberechtigungen für einen Computer fest**

1.  Wählen Sie auf der Eigenschaftenseite **Standardsicherheit** in Dcomcnfg.exe im Bereich **Standardzugriffsberechtigungen** die Schaltfläche **Standard bearbeiten** aus.

2.  Um Benutzer oder Gruppen zu entfernen, wählen Sie den Benutzer oder die Gruppe aus, den bzw. die Sie entfernen möchten, und klicken Sie auf die Schaltfläche **Entfernen.** Der ausgewählte Benutzer oder die ausgewählte Gruppe wird nicht mehr im Listenfeld angezeigt. Wenn Sie das Entfernen von Benutzern und Gruppen abgeschlossen haben, wählen Sie **OK** aus.

3.  Wenn Sie einen Benutzer oder eine Gruppe hinzufügen möchten, wählen Sie die Schaltfläche **Hinzufügen** aus.

4.  Wenn Sie den vollqualifizierten Benutzernamen kennen, den Sie hinzufügen möchten, geben Sie ihn in das Textfeld **Namen hinzufügen** ein. Wenn Sie den Benutzernamen nicht kennen, finden Sie weitere Informationen unter [Setting Process-wide Security Using DCOMCNFG (Festlegen der prozessweiten Sicherheit mithilfe von DCOMCNFG).](setting-processwide-security-using-dcomcnfg.md) Wenn Sie den Benutzernamen gefunden haben, wählen Sie den Benutzer oder die Gruppe aus dem Listenfeld **Namen** und dann die Schaltfläche **Hinzufügen** aus.

5.  Wählen Sie im Listenfeld **Zugriffstyp** den Zugriffstyp aus (Zugriff **zulassen** oder **Zugriff verweigern).** Wiederholen Sie Schritt 4, um andere Benutzer hinzuzufügen, die über den ausgewählten Zugriffstyp verfügen. Wenn Sie das Hinzufügen von Benutzern für den ausgewählten Zugriffstyp abgeschlossen haben, wählen Sie die Schaltfläche **OK** aus.

6.  Wiederholen Sie die Schritte 4 und 5, um Benutzer hinzuzufügen, die über einen anderen Zugriffstyp verfügen. Wählen Sie andernfalls **OK** aus, um die Änderungen zu übernehmen.

## <a name="setting-system-wide-impersonation-level"></a>Festlegen System-Wide Identitätswechselebene

Die vom Client festgelegte Identitätswechselebene bestimmt den Umfang der Autorität, die dem Server erteilt wird, um im Auftrag des Clients zu agieren. Wenn der Client beispielsweise seine Identitätswechselebene auf "Delegate" festgelegt hat, kann der Server auf lokale und Remoteressourcen als Client zugreifen, und der Server kann mehrere Computergrenzen übergehen, wenn die Verleumdungsfunktion festgelegt ist. Informationen dazu, welche Identitätswechselebene Sie auswählen sollten, finden Sie unter [Identitätswechselebenen](impersonation-levels.md) und [Verleumden von](cloaking.md).

Durch Festlegen der Standardidentitätswechselebene für den gesamten Computer wird COM mitgeteilt, welche Identitätswechselebene verwendet werden soll, wenn ein bestimmter Client auf dem Computer mit [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) oder [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)programmgesteuert keine Identitätswechselebene angibt.

**So legen Sie die Identitätswechselebene für einen Computer fest**

1.  Wenn Dcomcnfg.exe ausgeführt wird, wählen Sie die Registerkarte **Standardeigenschaften** aus.

2.  Wählen Sie im Listenfeld **Standardidentitätswechselebene** die gewünschte Identitätswechselebene aus.

3.  Wenn Sie weitere Eigenschaften für den Computer festlegen, wählen Sie die Schaltfläche **Übernehmen** aus, um die neue Identitätswechselebene anzuwenden. Wählen Sie andernfalls **OK** aus, um die Änderungen anzuwenden und Dcomcnfg.exe zu beenden.

## <a name="setting-system-wide-reference-tracking"></a>Festlegen System-Wide Verweisnachverfolgung

Wenn Sie die Verweisnachverfolgung aktivieren, fordern Sie COM auf, zusätzliche Sicherheitsüberprüfungen durchzuführen und Informationen nachzuverfolgen, die dazu führen, dass Objekte nicht zu früh freigegeben werden. Beachten Sie, dass diese zusätzlichen Überprüfungen teuer sind. Weitere Informationen zur Verweisnachverfolgung finden Sie unter [Verweisnachverfolgung.](reference-tracking.md) Verwenden Sie die folgenden Schritte, um die Verweisnachverfolgung zu aktivieren oder zu deaktivieren.

**So legen Sie die Verweisnachverfolgung für einen Computer fest**

1.  Wenn Dcomcnfg.exe ausgeführt wird, wählen Sie die Registerkarte **Standardeigenschaften** aus.

2.  Um die Verweisnachverfolgung zu aktivieren (oder zu deaktivieren), aktivieren (oder deaktivieren) Sie das Kontrollkästchen **Zusätzliche Sicherheit für verweisnachverfolgung** bereitstellen am unteren Rand der Seite.

3.  Wenn Sie weitere Eigenschaften für den Computer festlegen, wählen Sie die Schaltfläche **Übernehmen** aus, um die neue Einstellung anzuwenden. Wählen Sie andernfalls **OK** aus, um die Änderungen anzuwenden und Dcomcnfg.exe zu beenden.

## <a name="enabling-and-disabling-dcom"></a>Aktivieren und Deaktivieren von DCOM

Wenn ein Computer Teil eines Netzwerks ist, ermöglicht das DCOM-Wire Protocol COM-Objekten auf diesem Computer die Kommunikation mit COM-Objekten auf anderen Computern. Sie können DCOM für einen bestimmten Computer deaktivieren. Dadurch wird jedoch die gesamte Kommunikation zwischen Objekten auf diesem Computer und Objekten auf anderen Computern deaktiviert.

Das Deaktivieren von DCOM auf einem Computer hat keine Auswirkungen auf lokale COM-Objekte. COM sucht weiterhin nach den von Ihnen angegebenen Startberechtigungen. Wenn keine Startberechtigungen angegeben wurden, werden Standardstartberechtigungen verwendet. Selbst wenn Sie DCOM deaktivieren und ein Benutzer physischen Zugriff auf den Computer hat, kann er einen Server auf dem Computer starten, es sei denn, Sie legen Startberechtigungen fest, um ihn nicht zuzulassen.

> [!Note]  
> Wenn Sie DCOM auf einem Remotecomputer deaktivieren, können Sie anschließend nicht mehr remote auf diesen Computer zugreifen, um DCOM erneut zu aktivieren. Um DCOM erneut zu aktivieren, benötigen Sie physischen Zugriff auf diesen Computer.

 

**So aktivieren (oder deaktivieren Sie) DCOM manuell für einen Computer**

1.  Führen Sie "Dcomcnfg.exe" aus.

2.  Wählen Sie **die Registerkarte DefaultÂ Properties (Standardeigenschaften)** aus.

3.  Aktivieren (oder löschen Sie) das **Kontrollkästchen Verteiltes COM auf diesem Computer** aktivieren.

4.  Wenn Sie weitere Eigenschaften für den Computer  festlegen möchten, klicken Sie auf die Schaltfläche Anwenden, um DCOM zu aktivieren (oder zu deaktivieren). Klicken Sie **andernfalls auf OK,** um die Änderungen zu übernehmen und Dcomcnfg.exe.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen der prozessweiten Sicherheit](setting-processwide-security.md)
</dt> </dl>

 

 




