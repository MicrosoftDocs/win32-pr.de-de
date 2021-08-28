---
title: Zugriffssteuerungsrechte (AD DS)
description: Alle Objekte in Active Directory Domain Services unterstützen einen Standardsatz von Zugriffsrechten, die in der ADS \_ RIGHTS \_ ENUM-Enumeration definiert sind.
ms.assetid: 27ad74bd-ad87-422e-a4a2-02c0d51c4dd4
ms.tgt_platform: multiple
keywords:
- Steuern von Zugriffsrechten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c975ac20cac683e754f1b703bd272356c9b8df8f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881618"
---
# <a name="control-access-rights-ad-ds"></a>Zugriffssteuerungsrechte (AD DS)

Alle Objekte in Active Directory Domain Services unterstützen einen Standardsatz von Zugriffsrechten, die in der [**ADS \_ RIGHTS \_ ENUM-Enumeration**](/windows/win32/api/iads/ne-iads-ads_rights_enum) definiert sind. Diese Zugriffsrechte können in den Access Control Einträgen (ACEs) der Sicherheitsbeschreibung eines Objekts verwendet werden, um den Zugriff auf das Objekt zu steuern. Das heißt, um zu steuern, wer Standardvorgänge ausführen kann, z. B. das Erstellen und Löschen von untergeordneten Objekten oder das Lesen und Schreiben der Objektattribute. Für einige Objektklassen kann es jedoch wünschenswert sein, den Zugriff auf eine Weise zu steuern, die von den Standardzugriffsrechten nicht unterstützt wird. Um dies zu erleichtern, Active Directory Domain Services zulassen, dass der Standardmechanismus für die Zugriffssteuerung über das **controlAccessRight-Objekt** erweitert wird.

Zugriffssteuerungsrechte werden auf drei Arten verwendet:

-   Für erweiterte Rechte, bei denen es sich um spezielle Vorgänge handelt, die nicht durch den Standardsatz von Zugriffsrechten abgedeckt sind. Der Benutzerklasse kann z. B. das Recht "Senden als" gewährt werden, das von Exchange, Outlook oder einer anderen E-Mail-Anwendung verwendet werden kann, um zu bestimmen, ob ein bestimmter Benutzer von einem anderen Benutzer E-Mails in dessen Namen senden kann. Erweiterte Rechte werden für **controlAccessRight-Objekte** erstellt, indem das **attribut validAccesses** auf das **Zugriffsrecht ADS \_ RIGHT \_ DS CONTROL \_ \_ ACCESS** (256) festgelegt wird.
-   Zum Definieren von Eigenschaftensätzen, um die Steuerung des Zugriffs auf eine Teilmenge der Attribute eines Objekts zu ermöglichen, anstatt nur auf die einzelnen Attribute. Mithilfe der Standardzugriffsrechte kann ein einzelner ACE den Zugriff auf alle Attribute eines Objekts oder auf ein einzelnes Attribut gewähren oder verweigern. Zugriffssteuerungsrechte bieten einem einzelnen ACE die Möglichkeit, den Zugriff auf einen Satz von Attributen zu steuern. Die Benutzerklasse unterstützt z. B. den Eigenschaftensatz **Personal-Information,** der Attribute wie Adresse und Telefonnummer enthält. Eigenschaftssatzrechte werden für **controlAccessRight-Objekte** erstellt, indem das **attribut validAccesses** auf die Zugriffsberechtigungen **ACTR \_ DS \_ READ \_ PROP** (16) und **ACTRL \_ DS WRITE \_ \_ PROP** (32) festgelegt wird.
-   Für validierte Schreibvorgänge, um vor dem Schreiben eines Werts in ein Attribut für ein DS-Objekt eine Wertüberprüfung oder -validierung zu erzwingen, die über das hinausgeht, was für das Schema erforderlich ist. Dadurch wird sichergestellt, dass der für das Attribut eingegebene Wert der erforderlichen Semantik entspricht, innerhalb eines rechtlichen Wertebereichs liegt oder einer anderen speziellen Überprüfung unterzogen wird, die nicht für einen einfachen Schreibvorgang auf niedriger Ebene in das Attribut durchgeführt würde. Ein überprüfter Schreibvorgang ist einer speziellen Berechtigung zugeordnet, die sich von der Berechtigung "Write &lt; &gt; attribute" unterscheidet, die das Schreiben eines beliebigen Werts in das Attribut ohne durchgeführte Wertüberprüfung ermöglicht. Der überprüfte Schreibvorgang ist die einzige der drei Steuerelementzugriffsrechte, die nicht als neues Steuerelementzugriffsrecht für eine Anwendung erstellt werden können. Dies liegt daran, dass das vorhandene System nicht programmgesteuert geändert werden kann, um die Validierung zu erzwingen. Wenn ein Steuerelementzugriffsrecht im System als überprüfter Schreibvorgang eingerichtet wurde, enthält das **validAccesses-Attribut** für die **controlAccessRight-Objekte** das **ADS RIGHT \_ \_ DS \_ SELF** (8)-Zugriffsrecht.

    Im Active Directory-Schema Windows 2000 sind nur drei überprüfte Schreibvorgänge definiert:

    -   Self-Membership Berechtigung für ein Group-Objekt, mit dem das Konto des Aufrufers, aber kein anderes Konto, der Mitgliedschaft einer Gruppe hinzugefügt oder daraus entfernt werden kann.
    -   Überprüfte DNS-Hostname-Berechtigung für ein Computerobjekt, das das Festlegen eines DNS-Hostnamenattributs ermöglicht, das mit dem Computernamen und Domänennamen kompatibel ist.
    -   Überprüfte SPN-Berechtigung für ein Computerobjekt, das das Festlegen eines SPN-Attributs ermöglicht, das mit dem DNS-Hostnamen des Computers kompatibel ist.

Der Einfachheit halber wird jedes Steuerelementzugriffsrecht durch ein **controlAccessRight-Objekt** im Extended-Rights Container der Konfigurationspartition dargestellt, obwohl Eigenschaftssätze und überprüfte Schreibvorgänge nicht als erweiterte Rechte betrachtet werden. Da der Konfigurationscontainer in der gesamten Gesamtstruktur repliziert wird, werden Steuerungsrechte über alle Domänen in einer Gesamtstruktur verteilt. Es gibt eine Reihe vordefinierter Zugriffsberechtigungen für die Steuerung, und natürlich können auch benutzerdefinierte Zugriffsrechte definiert werden.

Alle Zugriffssteuerungsrechte können als Berechtigungen im ACL-Editor angezeigt werden.

Weitere Informationen und ein C++- und Visual Basic Codebeispiel, das einen ACE zum Steuern des Lese-/Schreibzugriffs auf einen Eigenschaftensatz festlegt, finden Sie unter [Beispielcode zum Festlegen eines ACE für ein Verzeichnisobjekt.](example-code-for-setting-an-ace-on-a-directory-object.md)

Weitere Informationen zur Verwendung von Zugriffssteuerungsrechten zum Steuern des Zugriffs auf spezielle Vorgänge finden Sie unter:

-   [Erstellen eines Steuerelementzugriffsrechts](creating-a-control-access-right.md)
-   [Festlegen eines Zugriffssteuerungs-ACE in der Zugriffssteuerungsliste eines Objekts](setting-a-control-access-right-ace-in-an-objectampaposs-acl.md)
-   [Überprüfen eines Steuerelementzugriffsrechts in der ACL eines Objekts](checking-a-control-access-right-in-an-objectampaposs-acl.md)
-   [Lesen eines Steuerelementzugriffs-Berechtigungssatzes in der ACL eines Objekts](reading-a-control-access-right-set-in-an-objectampaposs-acl.md)

 

 
