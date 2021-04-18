---
description: Vor der Implementierung von Code, mit dem Kenn Wörter geschützt werden, empfiehlt es sich, ihre jeweilige Umgebung so zu analysieren, dass ein Angreifer versucht, die Software Abwehr zu durchdringen.
ms.assetid: 4ebf7185-0179-4754-80da-63b0002c883f
title: Kenn Wort Bedrohungsbewertung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48a79d44bda9714083c5dd1085e9d09497e7341
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350952"
---
# <a name="password-threat-assessment"></a>Kenn Wort Bedrohungsbewertung

Vor der Implementierung von Code, mit dem Kenn Wörter geschützt werden, empfiehlt es sich, ihre jeweilige Umgebung so zu analysieren, dass ein Angreifer versucht, die Software Abwehr zu durchdringen.

Beginnen Sie mit der Analyse der Netzwerk-oder Systemarchitektur. Im Folgenden finden Sie einige Beispiele:

-   Die Anzahl der Kenn Wörter, die geschützt werden müssen. Ist ein Kennwort erforderlich, das für die Anmeldung beim lokalen Computer erforderlich ist? Ist dasselbe Kennwort für die Anmeldung beim Netzwerk verwendet? Werden Kenn Wörter an mehr als einen Server im Netzwerk weitergegeben? Wie viele Kenn Wörter müssen untergebracht werden?
-   Die Art des zu verwendenden Netzwerks (sofern vorhanden). Wird das Netzwerk mithilfe eines Unternehmensverzeichnis Systems (z. b. LDAP) implementiert, und wird die Kenn Wort Architektur verwendet? Werden von Objekten unverschlüsselte Kenn Wörter gespeichert?
-   Geöffnet im Vergleich zum geschlossenen Netzwerk. Ist das Netzwerk in sich selbst enthalten oder ist es für das Außendienst offen? Wenn dies der Fall ist, wird er durch eine Firewall geschützt?
-   Remote Zugriff. Müssen Benutzer von einem Remote Standort aus auf das Netzwerk zugreifen?

Nachdem Sie die System-oder Netzwerkarchitektur analysiert haben, können Sie mit der Analyse der Angriffs Weise eines Angreifers beginnen. Einige mögliche Ursachen:

-   Lesen Sie ein unverschlüsseltes Kennwort aus der Registrierung eines Computers.
-   Lesen Sie ein unverschlüsseltes Kennwort, das in der Software hart codiert ist.
-   Lesen Sie ein unverschlüsseltes Kennwort von einer ausgetauschten Codepage eines Computers.
-   Lesen eines Kennworts aus dem Ereignisprotokoll eines Programms
-   Lesen eines Kennworts aus einem erweiterten Verzeichnisdienst Schema von Microsoft Active Directory Verzeichnis, das über Objekte verfügt, die ein Klartext-Kennwort enthalten.
-   Führen Sie einen Debugger für ein Programm aus, das ein Kennwort erfordert.
-   Erraten Sie ein Kennwort. Es können mehrere Techniken verwendet werden. Der Angreifer könnte z. b. einige persönliche Informationen zu einem Benutzer kennen und versuchen, ein Kennwort aus diesen Informationen zu erraten (z. b. den Namen eines Ehepartners/Partners oder eines untergeordneten Elements). Oder es kann versucht werden, eine Brute-Force-Methode auszuprobieren, bei der alle Kombinationen aus Buchstaben, Ziffern und Interpunktions Zeichen ausprobiert werden (nur möglich, wenn kurze Kenn Wörter verwendet werden).

Wenn Sie die möglichen Angriffsmethoden mit der System-oder Netzwerkarchitektur vergleichen, werden wahrscheinlich Sicherheitsrisiken offengelegt. Zu diesem Zeitpunkt kann für jedes Risiko ein Risikofaktor festgelegt werden, und die Risikofaktoren können verwendet werden, um Korrekturen zu selektiert.

 

 



