---
title: Was Anwendungs- und Dienstentwickler über Gruppen wissen müssen
description: Beim Entwickeln einer Anwendung oder eines Diensts können Sie Gruppen verwenden, um die Verwaltung zu delegieren oder den Zugriff auf die Anwendung oder den Dienst als Ganzes oder als Teil zu steuern.
ms.assetid: 19e189a5-2880-4b45-84c8-e7b542c4fbb6
ms.tgt_platform: multiple
keywords:
- Was Anwendungs- und Dienstentwickler über Gruppen wissen müssen
- gruppen AD , Informationen für Anwendungs- und Dienstentwickler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b59a8a1ce369d9b5fa1093297f219bf6a206178a950b9d0762fde3069846551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024392"
---
# <a name="what-application-and-service-developers-need-to-know-about-groups"></a>Was Anwendungs- und Dienstentwickler über Gruppen wissen müssen

Beim Entwickeln einer Anwendung oder eines Diensts können Sie Gruppen verwenden, um die Verwaltung zu delegieren oder den Zugriff auf die Anwendung oder den Dienst als Ganzes oder als Teil zu steuern. Beispielsweise kann eine Anwendung steuern, wer verschiedene Verwaltungsvorgänge ausführen kann. Erstellen Sie zu diesem Zweck ACEs, die den entsprechenden Gruppen angegebene Zugriffsrechte gewähren. Es empfiehlt sich, über einen ACE zu verfügen, der Zugriff auf eine Gruppe gewährt, anstatt über mehrere ACEs zu verfügen, die einzelnen Benutzern oder Computern Zugriff gewähren.

Es wird empfohlen, dass Anwendungen bei der Verwendung von Gruppen die folgenden Richtlinien befolgen:

-   Erstellen Sie keine Abhängigkeiten von hart codierten Gruppen, was zu Schwierigkeiten führen kann, wenn die Gruppe gelöscht oder verschoben wird.
-   Vermeiden Sie die Verwendung integrierter Gruppen, es sei denn, die Funktion der Gruppe stellt die spezifischen Anforderungen für die Anwendung bereit. Fordern Sie z. B. nicht an, dass ein Benutzer Mitglied der Gruppe Administratoren ist, nur um dem Benutzer die Berechtigung zum Erstellen eines Computerkontos zu erteilen. Auf diese Weise erhalten Benutzer Berechtigungen und Berechtigungen, die sie möglicherweise nicht benötigen, was zu Sicherheitsrisiken führen kann. Stattdessen sollten Sie eine neue Sicherheitsgruppe erstellen, die über die spezifischen erforderlichen Berechtigungen verfügt, und den Benutzer dieser neuen Gruppe hinzufügen.
-   Beachten Sie beim Erstellen neuer Gruppen die folgenden Empfehlungen:
    -   Schützen Sie die Gruppe, indem Sie ACEs festlegen, die steuern, wer Mitglieder hinzufügen oder entfernen kann.
    -   Verwenden Sie globale Gruppen, wenn sie für die Zugriffssteuerung für Objekte in Active Directory Domain Services verwendet werden.
    -   Verwenden Sie universelle Gruppen nur, wenn dies erforderlich ist (Mitgliedsdaten sind global mithilfe des globalen Katalogs erforderlich. Die Gruppe kann beliebige Benutzer/Gruppen enthalten). Wenn Sie universelle Gruppen verwenden, platzieren Sie globale Gruppen in der universellen Gruppe, und fügen Sie Der globalen Gruppe Benutzer hinzu/entfernen Sie sie. Vermeiden Sie übermäßige Änderungen an universellen Gruppen, um die Replikationseffizienz zu steigern.
-   Verwenden Sie keine Gruppenmitgliedschaft für die Zugriffssteuerung. Verwenden Sie stattdessen einen ACE, und steuern Sie den Zugriff, indem Sie das System eine Zugriffsüberprüfung durchführen lassen.

Um den Zugriff auf Vorgänge zu steuern, die nicht in die vordefinierten Zugriffsrechte für Objekte in Active Directory-Domäne Diensten passen, verwenden Sie die Zugriffssteuerungsfunktion der Zugriffssteuerung in Windows 2000. Weitere Informationen finden Sie unter [**ADS \_ RIGHTS \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_rights_enum).

**So verwenden Sie ein Steuerelementzugriffsrecht, um das Recht zum Ausführen eines Vorgangs zu steuern**

1.  Erstellen Sie ein Zugriffssteuerungsrecht, das den Typ des Zugriffs auf die Anwendung oder den Dienst definiert. Weitere Informationen finden Sie unter [Steuern von Zugriffsrechten.](control-access-rights.md)
2.  Erstellen Sie ein Objekt in Active Directory Domain Services, das die Anwendung, den Dienst oder die Ressource darstellt.
3.  Fügen Sie der DACL im Objektsicherheitsdeskriptor Objekt-ACEs hinzu, um Benutzern oder Gruppen das Steuerelementzugriffsrecht für dieses Objekt zu gewähren oder zu verweigern. Weitere Informationen finden Sie unter [Festlegen von Zugriffsrechten für ein Objekt.](setting-access-rights-on-an-object.md)
4.  Wenn ein Benutzer versucht, den geschützten Vorgang auszuführen, verwendet Ihre Anwendung oder Ihr Dienst die [**AccessCheckByTypeResultList-Funktion,**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) um zu bestimmen, ob dem Benutzer das Zugriffssteuerungsrecht gewährt wird. Weitere Informationen finden Sie unter [Checking a Control Access Right in an Object es ACL](checking-a-control-access-right-in-an-objectampaposs-acl.md).
5.  Basierend auf dem Ergebnis der Zugriffsüberprüfung für das Objekt kann Ihre Anwendung oder Ihr Dienst dem Benutzer den Zugriff auf die Anwendung oder den Dienst gewähren oder verweigern.

Eine Dienstanwendung kann auch eine Gruppe erstellen, deren Mitglieder die verschiedenen Dienstinstanzen sind. Beispielsweise kann ein Dienst mit Instanzen, die auf mehreren Computern in einem Unternehmen installiert sind, über eine gemeinsame Protokolldatei verfügen, in die alle Dienstinstanzen schreiben. Das Dienstinstallationsprogramm erstellt die Protokolldatei und verwendet eine DACL, um nur Mitgliedern einer Gruppe Zugriff zu gewähren. Die Gruppenmitglieder sind die Benutzerkonten, unter denen die verschiedenen Dienstinstanzen ausgeführt werden, oder wenn die Dienste unter dem LocalSystem-Konto ausgeführt werden, sind die Mitglieder die Computerkonten der Hostserver.

 

 