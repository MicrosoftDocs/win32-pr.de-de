---
description: Verwenden von CryptoAPI-Funktionen zum Verwalten von Zertifikat speichern und Zertifikaten, Zertifikat Sperr Listen und Zertifikat Vertrauens Listen innerhalb dieser Speicher.
ms.assetid: 6a56c355-8f24-41cc-88d9-2a02d9863ccf
title: Verwalten von Zertifikaten mit Zertifikat speichern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98abb2b612f77db3f1c59e53fb9c7bf0f34cefb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568309"
---
# <a name="managing-certificates-with-certificate-stores"></a>Verwalten von Zertifikaten mit Zertifikat speichern

Über einen bestimmten Zeitraum häufen sich die [*Zertifikate*](../secgloss/c-gly.md) auf dem Computer eines Benutzers an. Zum Verwalten dieser Zertifikate sind Tools erforderlich. [*CryptoAPI*](../secgloss/c-gly.md) stellt diese Tools als Funktionen zum Speichern, abrufen, löschen, auflisten (auflisten) und Überprüfen von Zertifikaten bereit. CryptoAPI bietet auch die Möglichkeit, Zertifikate an Nachrichten anzufügen.

CryptoAPI bietet zwei Hauptkategorien von Funktionen für die Verwaltung von Zertifikaten: Funktionen zum Verwalten von [*Zertifikat speichern*](../secgloss/c-gly.md)und Funktionen, die mit den Zertifikaten, [*Zertifikat Sperr Listen*](../secgloss/c-gly.md) (CRLs) und [*Zertifikat Vertrauens Listen*](../secgloss/c-gly.md) (CTLs) in diesen speichern funktionieren.

Zu den Funktionen, die [*Zertifikat Speicher*](../secgloss/c-gly.md) verwalten, gehören Funktionen zum Arbeiten mit logischen oder [*virtuellen speichern*](../secgloss/v-gly.md), [*Remote speichern*](../secgloss/r-gly.md), [*externen speichern*](../secgloss/e-gly.md)und speichern, die verschoben werden können.

Zertifikate, [*CRLs*](../secgloss/c-gly.md)und [*CTLs*](../secgloss/c-gly.md) können in [*Zertifikat speichern*](../secgloss/c-gly.md)aufbewahrt und verwaltet werden. Sie können aus einem Speicher abgerufen werden, in dem Sie für die Verwendung in Authentifizierungs Prozessen persistent gespeichert wurden.

Der [*Zertifikat Speicher*](../secgloss/c-gly.md) ist für alle Zertifikat Funktionen von zentraler Bedeutung. Die Zertifikate werden im Speicher mithilfe von Funktionen mit einem Präfix "CERT" verwaltet. Ein typischer Zertifikat Speicher ist eine verknüpfte Liste mit [*Zertifikaten*](../secgloss/c-gly.md) , wie in der folgenden Abbildung dargestellt.

![Zertifikatspeicher](images/certstore1.png)

Die vorherige Abbildung zeigt Folgendes:

-   Jeder [*Zertifikat Speicher*](../secgloss/c-gly.md) verfügt über einen Zeiger auf den ersten Zertifikat Block in diesem Speicher.
-   Ein Zertifikat Block enthält einen Zeiger auf die Daten dieses Zertifikats und einen "Next"-Zeiger auf den nächsten Zertifikat Block im Speicher.
-   Der "Next"-Zeiger im letzten Zertifikat Block wird auf **null** festgelegt.
-   Der Datenblock eines Zertifikats enthält den schreibgeschützten Zertifikat Kontext und alle erweiterten Eigenschaften des Zertifikats.
-   Der Datenblock jedes Zertifikats enthält einen [*Verweis Zähler*](../secgloss/r-gly.md) , der die Anzahl der Zeiger auf das Zertifikat nachverfolgt, das vorhanden ist.

Zertifikate in einem [*Zertifikat Speicher*](../secgloss/c-gly.md) werden normalerweise in einem permanenten Speicher gespeichert, z. b. einer Datenträger Datei oder der Systemregistrierung. Zertifikat Speicher können auch ausschließlich im Arbeitsspeicher erstellt und geöffnet werden. Ein Speicher Speicher bietet temporären Zertifikat Speicher für das Arbeiten mit Zertifikaten, die nicht aufbewahrt werden müssen.

Zusätzliche Speicherorte ermöglichen das aufbewahren und Durchsuchen von Speichern in den verschiedenen Teilen der Registrierung eines lokalen Computers oder, wobei die entsprechenden Berechtigungen in der Registrierung auf einem Remote Computer festgelegt sind.

Jeder Benutzer verfügt über einen persönlichen Speicher, in dem die Zertifikate des Benutzers gespeichert sind. Der My-Speicher kann sich an einem der vielen physischen Standorte befinden, einschließlich der Registrierung auf einem lokalen Computer oder Remote Computer, einer Datenträger Datei, einer Datenbank, eines Verzeichnis Diensts, einer [*Smartcard*](../secgloss/s-gly.md)oder einem anderen Speicherort. Obwohl alle Zertifikate im My-Speicher gespeichert werden können, sollte dieser Speicher für die persönlichen Zertifikate eines Benutzers reserviert werden: die Zertifikate, die zum Signieren und Entschlüsseln der Nachrichten dieses Benutzers verwendet werden.

Die Verwendung von Zertifikaten für die Authentifizierung hängt davon ab, welche Zertifikate von einem vertrauenswürdigen Zertifikat Aussteller ausgestellt wurden. Zertifikate für vertrauenswürdige Zertifikat Aussteller werden in der Regel im Stamm Speicher gespeichert, der derzeit in einem Registrierungs Unterschlüssel persistent gespeichert wird. Im kryptoapi-Kontext wird der Stamm Speicher geschützt, und die Dialogfelder in der Benutzeroberfläche erinnern den Benutzer daran, nur vertrauenswürdige Zertifikate in diesem Speicher zu platzieren. In Unternehmensnetzwerk Situationen können Zertifikate von einem Systemadministrator per pushübertragung (kopiert) vom Domänen Controller Computer in die Stamm Speicher auf Client Computern übermittelt werden. Bei diesem Vorgang werden alle Mitglieder einer Domäne mit ähnlichen Vertrauens Listen bereitstellt.

Andere Zertifikate können im Systemspeicher der [*Zertifizierungsstelle (Certification Authority*](../secgloss/c-gly.md) , ca) oder in Benutzer erstellten, dateibasierten speichern gespeichert werden.

Eine Liste der Funktionen zum verwenden und Verwalten von Zertifikat speichern finden Sie unter [Zertifikat Speicherfunktionen](cryptography-functions.md).

Ein Beispiel, in dem einige dieser Funktionen verwendet werden, finden Sie unter [Beispiel C-Programm: Zertifikat Speichervorgänge](example-c-program-certificate-store-operations.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwalten eines Zertifikat Speicher Zustands](managing-a-certificate-store-state.md)
</dt> <dt>

[Arbeiten mit Zertifikaten in Zertifikat speichern](working-with-certificates-in-certificate-stores.md)
</dt> <dt>

[Zertifikat Verknüpfungen](certificate-links.md)
</dt> <dt>

[Sammlungs Speicher](collection-stores.md)
</dt> <dt>

[Logische und physische Speicher](logical-and-physical-stores.md)
</dt> <dt>

[System Speicherorte](system-store-locations.md)
</dt> <dt>

[Zertifikat Speicher Migration](certificate-store-migration.md)
</dt> </dl>

 

 
