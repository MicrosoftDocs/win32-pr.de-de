---
title: Welche Anwendungs-und Dienst Entwickler müssen über Gruppen Bescheid wissen?
description: Wenn Sie eine Anwendung oder einen Dienst entwickeln, können Sie Gruppen verwenden, um die Verwaltung zu delegieren oder den Zugriff auf die Anwendung oder den Dienst als Ganzes oder teilweise zu steuern.
ms.assetid: 19e189a5-2880-4b45-84c8-e7b542c4fbb6
ms.tgt_platform: multiple
keywords:
- Welche Anwendungs-und Dienst Entwickler müssen über Gruppen Bescheid wissen?
- Gruppen Werbung, Informationen für Anwendungs-und Dienst Entwickler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd23f598925c959502e1013ff43ad18bbb42ed7b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724384"
---
# <a name="what-application-and-service-developers-need-to-know-about-groups"></a>Welche Anwendungs-und Dienst Entwickler müssen über Gruppen Bescheid wissen?

Wenn Sie eine Anwendung oder einen Dienst entwickeln, können Sie Gruppen verwenden, um die Verwaltung zu delegieren oder den Zugriff auf die Anwendung oder den Dienst als Ganzes oder teilweise zu steuern. Beispielsweise kann eine Anwendung steuern, wer verschiedene administrative Vorgänge ausführen kann. Erstellen Sie hierzu ACEs, die den entsprechenden Gruppen die angegebenen Zugriffsrechte erteilen. Es empfiehlt sich, einen ACE zu haben, der Zugriff auf eine Gruppe gewährt, als mehrere ACEs haben, die Zugriff auf einzelne Benutzer oder Computer gewähren.

Es wird empfohlen, dass Anwendungen bei der Verwendung von Gruppen die folgenden Richtlinien verwenden:

-   Erstellen Sie keine Abhängigkeiten von hart codierten Gruppen, die Komplikationen verursachen können, wenn die Gruppe gelöscht oder verschoben wird.
-   Vermeiden Sie die Verwendung integrierter Gruppen, es sei denn, die Funktion der Gruppe stellt die spezifischen Anforderungen für die Anwendung bereit. Nehmen Sie z. b. nicht an, dass ein Benutzer Mitglied der Gruppe "Administratoren" sein muss, um dem Benutzer die Berechtigung zum Erstellen eines Computer Kontos zu erteilen. Dadurch erhält der Benutzerberechtigungen und Berechtigungen, die Sie möglicherweise nicht benötigen, was zu Sicherheitsrisiken führen kann. Stattdessen sollten Sie eine neue Sicherheitsgruppe erstellen, die über die erforderlichen Berechtigungen verfügt, und den Benutzer dieser neuen Gruppe hinzufügen.
-   Wenn Sie neue Gruppen erstellen, beachten Sie die folgenden Empfehlungen:
    -   Schützen Sie die Gruppe durch Festlegen von ACEs, die Steuern, wer Mitglieder hinzufügen oder entfernen darf.
    -   Verwenden Sie globale Gruppen, wenn Sie für die Zugriffs Steuerung für Objekte in Active Directory Domain Services verwendet werden.
    -   Verwenden Sie universelle Gruppen nur bei Bedarf (Elementdaten werden global mithilfe des globalen Katalogs benötigt; die Gruppe kann beliebige Benutzer/Gruppen enthalten). Wenn Sie universelle Gruppen verwenden, platzieren Sie globale Gruppen in der universellen Gruppe, und fügen Sie Benutzer aus der globalen Gruppe hinzu bzw. entfernen Sie Sie. Vermeiden Sie übermäßige Änderungen an universellen Gruppen für die Replikations Effizienz.
-   Verwenden Sie die Gruppenmitgliedschaft nicht für die Zugriffs Steuerung. Verwenden Sie stattdessen einen ACE, und Steuern Sie den Zugriff, indem Sie eine Zugriffs Überprüfung durch das System durchführen lassen.

Verwenden Sie zum Steuern des Zugriffs auf Vorgänge, die nicht in die vordefinierten Zugriffsrechte für Objekte in Active Directory-Domäne Services passen, das Feature Zugriffsrechte für die Steuerung der Zugriffs Steuerung in Windows 2000. Weitere Informationen finden Sie unter [**ADS \_ - \_ Rechte**](/windows/win32/api/iads/ne-iads-ads_rights_enum)Aufzählung.

**So verwenden Sie ein Zugriffsrecht zum Steuern der Rechte zum Ausführen eines Vorgangs**

1.  Erstellen Sie ein Zugriffsrecht für das Steuerelement, das den Typ des Zugriffs auf die Anwendung oder den Dienst definiert. Weitere Informationen finden Sie unter [Steuern von Zugriffsrechten](control-access-rights.md).
2.  Erstellen Sie ein Objekt in Active Directory Domain Services, das die Anwendung, den Dienst oder die Ressource darstellt.
3.  Fügen Sie der DACL in der Sicherheits Beschreibung des Objekts Objekt-ACEs hinzu, um Benutzern oder Gruppen das Zugriffsrecht für dieses Objekt zu gewähren oder zu verweigern. Weitere Informationen finden Sie unter [Festlegen von Zugriffsrechten für ein Objekt](setting-access-rights-on-an-object.md).
4.  Wenn ein Benutzer versucht, den geschützten Vorgang auszuführen, verwendet die Anwendung oder der Dienst die [**accesscheckbytyperesultlist**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) -Funktion, um zu bestimmen, ob dem Benutzer das Zugriffsrecht für das Steuerelement erteilt wird. Weitere Informationen finden Sie unter über [Prüfen eines Steuerungs Zugriffsrechts in der ACL eines Objekts](checking-a-control-access-right-in-an-objectampaposs-acl.md).
5.  Basierend auf dem Ergebnis der Zugriffs Überprüfung für das-Objekt kann die Anwendung oder der Dienst dem Benutzer den Zugriff auf die Anwendung oder den Dienst gewähren oder verweigern.

Eine-Dienst Anwendung könnte auch eine Gruppe erstellen, deren Mitglieder die verschiedenen Dienst Instanzen sind. Beispielsweise kann ein Dienst, der auf mehreren Computern in einem Unternehmen installiert ist, über eine gemeinsame Protokolldatei verfügen, in die alle Dienst Instanzen schreiben. Das Dienst Installationsprogramm erstellt die Protokolldatei und verwendet eine DACL, um nur Mitgliedern einer Gruppe Zugriff zu gewähren. Bei den Gruppenmitgliedern handelt es sich um die Benutzerkonten, unter denen die verschiedenen Dienst Instanzen ausgeführt werden. wenn die Dienste unter dem Konto "LocalSystem" ausgeführt werden, sind die Mitglieder die Computer Konten der Host Server.

 

 