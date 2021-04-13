---
title: Festlegen der System-Wide Sicherheit mithilfe von DCOMCNFG
description: Wenn Sie möchten, dass alle Anwendungen auf einem Computer, die nicht über Ihre eigene Sicherheit verfügen, dieselben Standard Sicherheitseinstellungen verwenden, legen Sie die Sicherheit auf systemweite Basis fest.
ms.assetid: 23d1e222-c00b-497c-adc8-4ae14c5bdd98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7feaaf356263a48c2c93eb9b3b3764b7352cd39
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388523"
---
# <a name="setting-system-wide-security-using-dcomcnfg"></a>Festlegen der System-Wide Sicherheit mithilfe von DCOMCNFG

Das Ändern der systemweiten Sicherheitseinstellungen wirkt sich auf alle com-Server Anwendungen aus, die keine eigene Prozess weite Sicherheit festlegen. Dadurch wird möglicherweise verhindert, dass solche Anwendungen ordnungsgemäß funktionieren. Wenn Sie die systemweiten Sicherheitseinstellungen ändern, um die Sicherheitseinstellungen für eine bestimmte COM-Anwendung zu beeinflussen, sollten Sie stattdessen die Prozess weiten Sicherheitseinstellungen für die jeweilige COM-Anwendung ändern. Weitere Informationen zum Festlegen der Prozess weiten Sicherheit finden Sie unter [Festlegen der Prozess weiten Sicherheit](setting-processwide-security.md).

Wenn Sie möchten, dass alle Anwendungen auf einem Computer, die nicht über Ihre eigene Sicherheit verfügen, dieselben Standard Sicherheitseinstellungen verwenden, legen Sie die Sicherheit auf systemweite Basis fest. Wenn Sie Dcomcnfg.exe verwenden, ist es einfach, Standardwerte in der Registrierung festzulegen, die für alle Anwendungen auf einem Computer gelten.

Es ist wichtig zu wissen, dass, wenn der Client oder Server explizit [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) aufruft, um die Prozess weite Sicherheit festzulegen, die Standardeinstellungen in der Registrierung ignoriert werden und stattdessen die Parameter für **CoInitializeSecurity** für die Sicherheitseinstellungen für den Prozess verwendet werden. Wenn Sie Dcomcnfg.exe verwenden, um Sicherheitseinstellungen für einen bestimmten Prozess anzugeben, werden die Standardeinstellungen des Computers von den Einstellungen für den Prozess überschrieben.

Wenn Sie die systemweite Sicherheit aktivieren, müssen Sie die Authentifizierungs Ebene auf einen anderen Wert als "None" festlegen, und Sie müssen Start-und Zugriffsberechtigungen festlegen. Sie haben die Möglichkeit, die standardmäßige Identitätswechsel Ebene festzulegen, und Sie können auch die Verweis Nachverfolgung aktivieren. Die folgenden Themen enthalten Schritt-für-Schritt-Anleitungen:

-   [Festlegen System-Wide Standard Authentifizierungs Ebene](#setting-system-wide-default-authentication-level)
-   [Festlegen System-Wide Start Berechtigungen](#setting-system-wide-launch-permissions)
-   [Festlegen System-Wide Zugriffsberechtigungen](#setting-system-wide-access-permissions)
-   [Festlegen System-Wide Identitätswechsel Ebene](#setting-system-wide-impersonation-level)
-   [Festlegen System-Wide Verweis Nachverfolgung](#setting-system-wide-reference-tracking)
-   [Aktivieren und Deaktivieren von DCOM](#enabling-and-disabling-dcom)
-   [Zugehörige Themen](#related-topics)

## <a name="setting-system-wide-default-authentication-level"></a>Festlegen System-Wide Standard Authentifizierungs Ebene

Die Authentifizierungs Ebene wird verwendet, um com mitzuteilen, auf welcher Ebene der Client authentifiziert werden soll. Diese Ebenen bieten verschiedene Schutzstufen, von keinem Schutz bis zur vollständigen Verschlüsselung. Um die Sicherheit für einen Computer zu aktivieren, müssen Sie eine andere Authentifizierungs Ebene als None auswählen. Mithilfe der folgenden Schritte können Sie eine solche Einstellung auswählen, indem Sie Dcomcnfg.exe verwenden.

**So legen Sie die Authentifizierungs Ebene auf systemweite Basis fest**

1.  Führen Sie "Dcomcnfg.exe" aus.

2.  Wählen Sie die Registerkarte **Standardeigenschaften** aus.

3.  Wählen Sie im Listenfeld **default\authenticationlevel** einen anderen Wert als **(keine)** aus.

4.  Wenn Sie weitere Eigenschaften für den Computer festlegen, klicken Sie auf die Schaltfläche **anwenden** , um die neue Authentifizierungs Ebene anzuwenden. Andernfalls klicken Sie auf **OK** , um die Änderungen zu übernehmen und Dcomcnfg.exe zu beenden.

## <a name="setting-system-wide-launch-permissions"></a>Festlegen System-Wide Start Berechtigungen

Die Start Berechtigungen, die Sie mit Dcomcnfg.exe festlegen, bestimmen eine Liste von Benutzern, denen jeweils explizit die Berechtigung zum Starten eines Servers, der keine eigenen Start Berechtigungseinstellungen bereitstellt, erteilt oder verweigert wird. Beim Festlegen von Start Berechtigungen können Sie einen oder mehrere Benutzer oder Gruppen aus dieser Liste hinzufügen oder entfernen. Sie müssen für jeden Benutzer, den Sie hinzufügen, angeben, ob dem Benutzer die Berechtigung zum Starten erteilt oder verweigert wird.

**So legen Sie Start Berechtigungen für einen Computer fest**

1.  Wählen Sie auf der Eigenschaften Seite **Standard Sicherheit** in Dcomcnfg.exe die Schaltfläche **Standard bearbeiten** im Bereich **Standard Start Berechtigungen** aus.

2.  Um Benutzer oder Gruppen zu entfernen, wählen Sie den Benutzer oder die Gruppe aus, den Sie entfernen möchten, und wählen Sie die Schaltfläche **Entfernen** . Der ausgewählte Benutzer oder die ausgewählte Gruppe wird nicht mehr im Listenfeld angezeigt. Wenn Sie das Entfernen von Benutzern und Gruppen abgeschlossen haben, klicken Sie auf **OK**.

3.  Wenn Sie einen Benutzer oder eine Gruppe hinzufügen möchten, klicken Sie auf die Schaltfläche **Hinzufügen** .

4.  Wenn Sie den voll qualifizierten Benutzernamen kennen, den Sie hinzufügen möchten, geben Sie ihn in das Textfeld **Namen hinzufügen** ein. Wenn Sie den Benutzernamen nicht kennen, finden Sie weitere Informationen unter **Festlegen von Processwide Security mithilfe von DCOMCNFG** . Wenn Sie den Benutzernamen gefunden haben, wählen Sie im Listenfeld **Namen** den Benutzer oder die Gruppe aus, und klicken Sie auf die Schaltfläche **Hinzufügen** .

5.  Wählen Sie im Listenfeld **Zugriffstyp** den Zugriffstyp aus ( **starten** oder **verweigern starten**). Um weitere Benutzer hinzuzufügen, die ebenfalls den ausgewählten Zugriffstyp haben, wiederholen Sie Schritt 4. Wenn Sie das Hinzufügen von Benutzern für den ausgewählten Zugriffstyp abgeschlossen haben, klicken Sie auf die Schaltfläche **OK** .

6.  Wiederholen Sie die Schritte 4 und 5, um Benutzer hinzuzufügen, die einen anderen Zugriffstyp haben werden. Wählen Sie andernfalls **OK** aus, um die Änderungen zu übernehmen.

## <a name="setting-system-wide-access-permissions"></a>Festlegen System-Wide Zugriffsberechtigungen

Mit Dcomcnfg.exe können Sie Zugriffsberechtigungen festlegen, um die Liste der Benutzer zu steuern, denen der Zugriff auf die Methoden der Server erteilt oder verweigert wird, die nicht über eigene Zugriffsberechtigungen verfügen. Sie können der Liste Benutzer oder Gruppen hinzufügen und dabei angeben, ob die Zugriffsberechtigung gewährt oder verweigert wird. Sie können Benutzer auch aus der Liste entfernen.

Beim Festlegen von Zugriffsberechtigungen müssen Sie sicherstellen, dass das System in der Liste der Benutzer enthalten ist, denen der Zugriff gewährt wird. Wenn Sie allen Benutzern Zugriffsberechtigungen erteilt haben, wird das System implizit eingeschlossen.

Der Vorgang zum Festlegen von Zugriffsberechtigungen für einen Computer ähnelt dem Festlegen von Start Berechtigungen. Die folgenden Schritte müssen ausgeführt werden.

**So legen Sie die Zugriffsberechtigungen für einen Computer fest**

1.  Wählen Sie auf der Eigenschaften Seite **Standard Sicherheit** in Dcomcnfg.exe die Schaltfläche **Standard bearbeiten** im Bereich **Standard Zugriffsberechtigungen** aus.

2.  Um Benutzer oder Gruppen zu entfernen, wählen Sie den Benutzer oder die Gruppe aus, den Sie entfernen möchten, und wählen Sie die Schaltfläche **Entfernen** . Der ausgewählte Benutzer oder die ausgewählte Gruppe wird nicht mehr im Listenfeld angezeigt. Wenn Sie das Entfernen von Benutzer und Gruppen abgeschlossen haben, klicken Sie auf **OK**.

3.  Wenn Sie einen Benutzer oder eine Gruppe hinzufügen möchten, klicken Sie auf die Schaltfläche **Hinzufügen** .

4.  Wenn Sie den voll qualifizierten Benutzernamen kennen, den Sie hinzufügen möchten, geben Sie ihn in das Textfeld **Namen hinzufügen** ein. Wenn Sie den Benutzernamen nicht kennen, finden Sie weitere Informationen unter [Festlegen der Prozess weiten Sicherheit mithilfe von DCOMCNFG](setting-processwide-security-using-dcomcnfg.md) . Wenn Sie den Benutzernamen gefunden haben, wählen Sie im Listenfeld **Namen** den Benutzer oder die Gruppe aus, und klicken Sie auf die Schaltfläche **Hinzufügen** .

5.  Wählen Sie im Listenfeld **Zugriffstyp** den Zugriffstyp aus (entweder **Zugriff zulassen** oder **Zugriff verweigern**). Wiederholen Sie Schritt 4, um weitere Benutzer hinzuzufügen, die den ausgewählten Zugriffstyp haben werden. Wenn Sie das Hinzufügen von Benutzern für den ausgewählten Zugriffstyp abgeschlossen haben, klicken Sie auf die Schaltfläche **OK** .

6.  Wiederholen Sie die Schritte 4 und 5, um Benutzer hinzuzufügen, die einen anderen Zugriffstyp haben werden. Wählen Sie andernfalls **OK** aus, um die Änderungen zu übernehmen.

## <a name="setting-system-wide-impersonation-level"></a>Festlegen System-Wide Identitätswechsel Ebene

Die vom Client festgelegte Identitätswechsel Ebene bestimmt die Menge an Autorität, die dem Server für den Auftrag des Clients erteilt wird. Wenn der Client die Identitätswechsel Ebene beispielsweise auf "Delegat" festgelegt hat, kann der Server auf lokale und Remote Ressourcen als Client zugreifen, und der Server kann über mehrere Computer Grenzen umgrenzen, wenn die Möglichkeit zum Verbergen festgelegt ist. Informationen dazu, welche Identitätswechsel Ebene Sie auswählen sollten, finden Sie unter Identitätswechsel [Ebenen](impersonation-levels.md) und [Cloaking](cloaking.md).

Durch Festlegen der Standard Identitätswechsel Ebene für den gesamten Computer wird com mitgeteilt, welche Identitätswechsel Ebene verwendet werden soll, wenn ein bestimmter Client auf dem Computer eine Identitätswechsel Ebene nicht Programm gesteuert mithilfe von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) oder [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)angibt.

**So legen Sie die Identitätswechsel Ebene für einen Computer fest**

1.  Wenn Dcomcnfg.exe ausgeführt wird, wählen Sie die Registerkarte **Standardeigenschaften** aus.

2.  Wählen Sie im Listenfeld Standard-Identitätswechsel **Ebene** die gewünschte Identitätswechsel Ebene aus.

3.  Wenn Sie weitere Eigenschaften für den Computer festlegen, klicken Sie auf die Schaltfläche **anwenden** , um die neue Identitätswechsel Ebene anzuwenden. Wählen Sie andernfalls **OK** aus, um die Änderungen zu übernehmen und Dcomcnfg.exe zu beenden.

## <a name="setting-system-wide-reference-tracking"></a>Festlegen System-Wide Verweis Nachverfolgung

Wenn Sie die Verweis Nachverfolgung aktivieren, werden Sie von com aufgefordert, zusätzliche Sicherheitsüberprüfungen durchzuführen und Informationen nachzuverfolgen, die die Freigabe von Objekten zu früh halten. Beachten Sie, dass diese zusätzlichen Überprüfungen kostspielig sind. Weitere Informationen zur Verweis Nachverfolgung finden Sie unter [Verweis Verfolgung](reference-tracking.md). Verwenden Sie die folgenden Schritte zum Aktivieren oder Deaktivieren der Verweis Verfolgung.

**So legen Sie die Verweis Nachverfolgung für einen Computer fest**

1.  Wenn Dcomcnfg.exe ausgeführt wird, wählen Sie die Registerkarte **Standardeigenschaften** aus.

2.  Zum Aktivieren (oder deaktivieren) der Verweis Nachverfolgung aktivieren oder deaktivieren Sie das Kontrollkästchen **zusätzliche Sicherheit für die Verweis Verfolgung bereitstellen** am unteren Rand der Seite.

3.  Wenn Sie weitere Eigenschaften für den Computer festlegen, klicken Sie auf die Schaltfläche übernehmen, um die neue **Einstellung anzuwenden.** Wählen Sie andernfalls **OK** aus, um die Änderungen zu übernehmen und Dcomcnfg.exe zu beenden.

## <a name="enabling-and-disabling-dcom"></a>Aktivieren und Deaktivieren von DCOM

Wenn ein Computer Teil eines Netzwerks ist, ermöglicht das DCOM-Wire-Protokoll es COM-Objekten auf diesem Computer, mit COM-Objekten auf anderen Computern zu kommunizieren. Sie können DCOM für einen bestimmten Computer deaktivieren, dabei wird jedoch die gesamte Kommunikation zwischen Objekten auf diesem Computer und Objekten auf anderen Computern deaktiviert.

Die Deaktivierung von DCOM auf einem Computer hat keine Auswirkung auf lokale COM-Objekte. COM sucht weiterhin nach Start Berechtigungen, die Sie angegeben haben. Wenn keine Start Berechtigungen angegeben wurden, werden die standardmäßigen Start Berechtigungen verwendet. Auch wenn Sie DCOM deaktivieren, kann ein Benutzer, der überphysischen Zugriff auf den Computer verfügt, einen Server auf dem Computer starten, es sei denn, Sie legen die Start Berechtigungen nicht fest, um ihn zuzulassen.

> [!Note]  
> Wenn Sie DCOM auf einem Remote Computer deaktivieren, können Sie später nicht mehr Remote auf diesen Computer zugreifen, um DCOM erneut zu aktivieren. Zum erneuten Aktivieren von DCOM benötigen Sie physischen Zugriff auf diesen Computer.

 

**So aktivieren oder deaktivieren Sie DCOM für einen Computer manuell**

1.  Führen Sie "Dcomcnfg.exe" aus.

2.  Wählen Sie die Registerkarte **Eigenschaften von default.**

3.  Aktivieren (oder deaktivieren) Sie das Kontrollkästchen **"verteiltes anmelden auf diesem Computer aktivieren"** .

4.  Wenn Sie weitere Eigenschaften für den Computer festlegen, klicken Sie auf die Schaltfläche **anwenden** , um DCOM zu aktivieren (oder zu deaktivieren). Andernfalls klicken Sie auf **OK** , um die Änderungen zu übernehmen und Dcomcnfg.exe zu beenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen der Prozess weiten Sicherheit](setting-processwide-security.md)
</dt> </dl>

 

 




