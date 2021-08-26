---
description: Bevor Sie Code implementieren, der Kennwörter schützt, ist es am besten, Ihre spezielle Umgebung auf Möglichkeiten zu analysieren, wie ein Angreifer versuchen könnte, Softwareschutz zu durchdringen.
ms.assetid: 4ebf7185-0179-4754-80da-63b0002c883f
title: Bewertung von Kennwortbedrohungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9042efa524b0503a648a195e77669b19231fec0445c4b0c8347b802b323076
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977150"
---
# <a name="password-threat-assessment"></a>Bewertung von Kennwortbedrohungen

Bevor Sie Code implementieren, der Kennwörter schützt, ist es am besten, Ihre spezielle Umgebung auf Möglichkeiten zu analysieren, wie ein Angreifer versuchen könnte, Softwareschutz zu durchdringen.

Beginnen Sie mit der Analyse Ihrer Netzwerk- oder Systemarchitektur. Hier sind einige Beispiele:

-   Die Anzahl der Kennwörter, die geschützt werden müssen. Ist ein Kennwort erforderlich, um sich am lokalen Computer anmelden zu können? Wird das gleiche Kennwort für die Anmeldung beim Netzwerk verwendet? Werden Kennwörter an mehrere Server im Netzwerk übermittelt? Wie viele Kennwörter müssen berücksichtigt werden?
-   Die Art des Netzwerks (falls möglich), das verwendet wird. Wird das Netzwerk mithilfe eines Unternehmensverzeichnissystems (z. B. LDAP) implementiert, und wird die Kennwortarchitektur verwendet? Speichern Objekte unverschlüsselte Kennwörter?
-   Offenes und geschlossenes Netzwerk. Ist das Netzwerk in sich geschlossen, oder ist es nach außen geöffnet? Wenn ja, wird es durch eine Firewall geschützt?
-   Ras. Müssen Benutzer von einem Remotestandort aus auf das Netzwerk zugreifen?

Nachdem Sie Ihr System oder Ihre Netzwerkarchitektur analysiert haben, können Sie damit beginnen zu analysieren, wie ein Angreifer versuchen könnte, es angreifen zu können. Einige mögliche Ursachen:

-   Liest ein unverschlüsselte Kennwort aus der Registrierung eines Computers.
-   Liest ein unverschlüsselte Kennwort, das in der Software hart codiert ist.
-   Liest ein unverschlüsselte Kennwort von der ausgetauschten Codepage eines Computers.
-   Liest ein Kennwort aus dem Ereignisprotokoll eines Programms.
-   Liest ein Kennwort aus einem erweiterten Microsoft Active Directory-Verzeichnisdienstschema mit Objekten, die ein Klartextkennwort enthalten.
-   Führen Sie einen Debugger für ein Programm aus, das ein Kennwort erfordert.
-   Erraten Sie ein Kennwort. Es kann eine der verschiedenen Techniken verwendet werden. Beispielsweise kann der Angreifer einige persönliche Informationen zu einem Benutzer kennen und versuchen, ein Kennwort aus diesen Informationen zu erraten (z. B. den Namen eines Bzw. eines Partners oder eines Untergeordneten). Oder es kann eine Brute-Force-Methode versucht werden, bei der alle Kombinationen aus Buchstaben, Zahlen und Interpunktion ausprobiert werden (nur bei Verwendung kurzer Kennwörter möglich).

Der Vergleich der möglichen Angriffsmethoden mit der System- oder Netzwerkarchitektur wird wahrscheinlich Sicherheitsrisiken aufschluss geben. An diesem Punkt kann ein Risikofaktor für jedes Risiko festgelegt werden, und die Risikofaktoren können verwendet werden, um Korrekturen zu seligen.

 

 



