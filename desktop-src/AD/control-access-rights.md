---
title: Steuern von Zugriffsrechten (AD DS)
description: Alle Objekte in Active Directory Domain Services unterstützen einen Standardsatz von Zugriffsrechten, der in der AD \_ Rights \_ enum-Enumeration definiert ist.
ms.assetid: 27ad74bd-ad87-422e-a4a2-02c0d51c4dd4
ms.tgt_platform: multiple
keywords:
- Zugriffsrechte Steuern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 048c4aa685e0c569ef2ac762dcf17366a2394826
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472644"
---
# <a name="control-access-rights-ad-ds"></a>Steuern von Zugriffsrechten (AD DS)

Alle Objekte in Active Directory Domain Services unterstützen einen Standardsatz von Zugriffsrechten, der in der [**AD \_ Rights \_ enum**](/windows/win32/api/iads/ne-iads-ads_rights_enum) -Enumeration definiert ist. Diese Zugriffsrechte können in den Access Control Einträgen (ACEs) der Sicherheits Beschreibung eines Objekts verwendet werden, um den Zugriff auf das Objekt zu steuern. Das heißt, um zu steuern, wer Standard Vorgänge ausführen kann, z. b. das Erstellen und Löschen von untergeordneten Objekten oder das Lesen und Schreiben der Objekt Attribute. Bei manchen Objektklassen kann es jedoch wünschenswert sein, den Zugriff auf eine Art und Weise zu steuern, die von den Standard Zugriffsrechten nicht unterstützt wird. Um dies zu vereinfachen, Active Directory Domain Services zulassen, dass der standardmäßige Zugriffs Steuerungsmechanismus durch das **controlAccessRight** -Objekt erweitert wird.

Zugriffsrechte für das Steuerelement werden auf drei Arten verwendet:

-   Für erweiterte Rechte, bei denen es sich um spezielle Vorgänge handelt, die nicht vom Standardsatz von Zugriffsrechten abgedeckt werden. Der Benutzerklasse kann z. b. ein "Send as"-Recht erteilt werden, das von Exchange, Outlook oder einer beliebigen anderen e-Mail-Anwendung verwendet werden kann, um zu bestimmen, ob ein bestimmter Benutzer in seinem Namen eine e-Mail senden kann. Erweiterte Rechte werden für **controlAccessRight** -Objekte erstellt, indem das **validzugriffsattribut** auf die gleiche Anzeige des Zugriffsrechts **\_ \_ DS \_ Control \_ Access** (256) festgelegt wird.
-   Zum Definieren von Eigenschaften Sätzen, um das Steuern des Zugriffs auf eine Teilmenge der Attribute eines Objekts anstelle der einzelnen Attribute zu aktivieren. Mithilfe der standardmäßigen Zugriffsrechte kann ein einzelner Ace den Zugriff auf alle Attribute eines Objekts oder auf ein einzelnes Attribut gewähren oder verweigern. Steuerungs Zugriffsrechte bieten eine Möglichkeit für einen einzelnen ACE, den Zugriff auf einen Satz von Attributen zu steuern. Beispielsweise unterstützt die User-Klasse die Eigenschaft " **Personal-Information** ", die Attribute wie z. b. die Adresse der Straße und die Telefonnummer enthält. Eigenschaften Satz Rechte werden für **controlAccessRight** -Objekte erstellt, indem das **validaccess** -Attribut so festgelegt wird, dass es die **actr \_ DS \_ Read \_ Prop** (16) und die **actrl \_ DS- \_ Schreib \_ Prop** -Zugriffsrechte (32) enthält.
-   Für validierte Schreibvorgänge, die erfordern, dass das System eine Wert Überprüfung durchführt, oder Überprüfung, die über die für das Schema erforderliche Validierung hinausgeht, bevor ein Wert in ein Attribut für ein DS-Objekt geschrieben wird. Dadurch wird sichergestellt, dass der für das Attribut eingegebene Wert der erforderlichen Semantik entspricht, sich innerhalb eines gültigen Bereichs von Werten befindet oder eine andere besondere Prüfung durchführt, die für einen einfachen Schreibvorgang auf niedriger Ebene in das Attribut nicht durchgeführt würde. Ein validierter Schreibvorgang ist einer speziellen Berechtigung zugeordnet, die sich von der Berechtigung "Write" unterscheidet <attribute> , die es ermöglicht, dass ein beliebiger Wert in das Attribut geschrieben wird, ohne dass eine Wert Überprüfung durchgeführt wird Der validierte Schreibvorgang ist das einzige der drei Steuerungs Zugriffsrechte, das nicht als neues Zugriffsrecht für eine Anwendung erstellt werden kann. Dies liegt daran, dass das vorhandene System nicht Programm gesteuert geändert werden kann, um die Überprüfung zu erzwingen. Wenn ein Zugriffsrecht für das Steuerelement im System als validierter Schreibvorgang eingerichtet wurde, enthält das **validzugriffsattribut** für die **controlAccessRight** -Objekte das Zugriffsrecht " **AD \_ right \_ DS \_ Self** (8)".

    Im Windows 2000-Active Directory Schema sind nur drei validierte Schreibvorgänge definiert:

    -   Self-Membership Berechtigung für ein Gruppen Objekt, mit dem das Konto des Aufrufers, aber kein anderes Konto, der Mitgliedschaft einer Gruppe hinzugefügt oder daraus entfernt werden kann.
    -   Validieren der DNS-Host-Name-Berechtigung für ein Computer Objekt, das ein DNS-Hostname-Attribut zulässt, das mit dem festzulegenden Computer Namen und Domänen Namen kompatibel ist.
    -   Validierte SPN-Berechtigung für ein Computer Objekt, das ein SPN-Attribut zulässt, das mit dem DNS-Hostnamen des festzulegenden Computers kompatibel ist.

Aus praktischer Gründen wird jedes Steuerelement Zugriffsrecht durch ein **controlAccessRight** -Objekt im Extended-Rights Container der Konfigurations Partition dargestellt, auch wenn Eigenschaften Sätze und validierte Schreibvorgänge nicht als erweiterte Rechte betrachtet werden. Da der Konfigurations Container über die gesamte Gesamtstruktur repliziert wird, werden die Steuerungs Rechte über alle Domänen in einer Gesamtstruktur hinweg weitergegeben. Es gibt eine Reihe von vordefinierten Steuerungs Zugriffsrechten, und natürlich können auch benutzerdefinierte Zugriffsrechte definiert werden.

Alle Steuerungs Zugriffsrechte können im ACL-Editor als Berechtigungen angezeigt werden.

Weitere Informationen und ein C++-und Visual Basic Codebeispiel, in dem ein ACE zum Steuern des Lese-/Schreibzugriffs auf einen Eigenschaften Satz festgelegt wird, finden Sie unter [Beispielcode für das Festlegen eines ACE für ein Verzeichnis Objekt](example-code-for-setting-an-ace-on-a-directory-object.md).

Weitere Informationen zum Steuern des Zugriffs auf besondere Vorgänge mithilfe von Zugriffsrechten finden Sie unter:

-   [Erstellen eines Zugriffsrechts für das Steuerelement](creating-a-control-access-right.md)
-   [Festlegen eines Steuerungs Zugriffsrechts-ACE in der ACL eines Objekts](setting-a-control-access-right-ace-in-an-objectampaposs-acl.md)
-   [Überprüfen des Zugriffs auf das Steuerungs Recht in der ACL eines Objekts](checking-a-control-access-right-in-an-objectampaposs-acl.md)
-   [Lesen eines Steuerelement Zugriffsrechts, das in der ACL eines Objekts festgelegt ist](reading-a-control-access-right-set-in-an-objectampaposs-acl.md)

 

 