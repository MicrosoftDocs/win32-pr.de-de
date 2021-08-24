---
description: Verwenden von CryptoAPI-Funktionen zum Verwalten von Zertifikatspeichern und der Zertifikate, Zertifikatsperrlisten und Zertifikatvertrauenslisten in diesen Speichern.
ms.assetid: 6a56c355-8f24-41cc-88d9-2a02d9863ccf
title: Verwalten von Zertifikaten mit Zertifikatspeichern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0bfab57522ea8b400ee8d042b5b2cb1ad37fe7c234a291000eb516b11a6be0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425654"
---
# <a name="managing-certificates-with-certificate-stores"></a>Verwalten von Zertifikaten mit Zertifikatspeichern

Über einen bestimmten Zeitraum [*sammeln sich Zertifikate*](../secgloss/c-gly.md) auf dem Computer eines Benutzers an. Tools sind erforderlich, um diese Zertifikate zu verwalten. [*CryptoAPI*](../secgloss/c-gly.md) stellt diese Tools als Funktionen zum Speichern, Abrufen, Löschen, Auflisten (Auflisten) und Überprüfen von Zertifikaten zur Verfügung. CryptoAPI bietet auch die Möglichkeit zum Anfügen von Zertifikaten an Nachrichten.

CryptoAPI bietet zwei Hauptkategorien von Funktionen zum [](../secgloss/c-gly.md)Verwalten von Zertifikaten: Funktionen zum Verwalten von Zertifikatspeichern und Funktionen, die mit den Zertifikaten arbeiten, Zertifikatsperrlisten (Certificate [*Revocation Lists,*](../secgloss/c-gly.md) CRLs) und Zertifikatvertrauenslisten (Certificate [*Trust Lists,*](../secgloss/c-gly.md) CTLs) in diesen Speichern.

Die Funktionen zum Verwalten von [*Zertifikatspeichern*](../secgloss/c-gly.md) umfassen Funktionen zum Arbeiten mit logischen oder virtuellen [*Speichern,*](../secgloss/v-gly.md)Remotespeichern, [](../secgloss/r-gly.md)externen Speichern und [*Speichern,*](../secgloss/e-gly.md)die verschoben werden können.

Zertifikate, [*CRLs*](../secgloss/c-gly.md)und [*CTLs*](../secgloss/c-gly.md) können in Zertifikatspeichern beibehalten [*und verwaltet werden.*](../secgloss/c-gly.md) Sie können aus einem Speicher abgerufen werden, in dem sie für die Verwendung in Authentifizierungsprozessen beibehalten wurden.

Der [*Zertifikatspeicher*](../secgloss/c-gly.md) ist für alle Zertifikatfunktionen von zentraler Bedeutung. Die Zertifikate werden im Speicher mithilfe von Funktionen mit dem Präfix "Cert" verwaltet. Ein typischer Zertifikatspeicher ist eine verknüpfte Liste von [*Zertifikaten,*](../secgloss/c-gly.md) wie in der folgenden Abbildung dargestellt.

![Zertifikatspeicher](images/certstore1.png)

Die obige Abbildung zeigt Folgendes:

-   Jeder [*Zertifikatspeicher*](../secgloss/c-gly.md) verfügt über einen Zeiger auf den ersten Zertifikatblock in diesem Speicher.
-   Ein Zertifikatblock enthält einen Zeiger auf die Daten dieses Zertifikats und einen "next"-Zeiger auf den nächsten Zertifikatblock im Speicher.
-   Der Zeiger "next" im letzten Zertifikatblock ist auf **NULL festgelegt.**
-   Der Datenblock eines Zertifikats enthält den schreibgeschützten Zertifikatkontext und alle erweiterten Eigenschaften des Zertifikats.
-   Der Datenblock jedes Zertifikats enthält eine [*Verweisanzahl,*](../secgloss/r-gly.md) die die Anzahl der Verweise auf das zertifikat nachverfolgung, die vorhanden sind.

Zertifikate in einem [*Zertifikatspeicher*](../secgloss/c-gly.md) werden normalerweise in einer Art permanenten Speicher wie einer Datenträgerdatei oder der Systemregistrierung gespeichert. Zertifikatspeicher können auch ausschließlich im Arbeitsspeicher erstellt und geöffnet werden. Ein Speicher bietet temporären Zertifikatspeicher für die Arbeit mit Zertifikaten, die nicht aufbewahrt werden müssen.

Zusätzliche Speicherorte ermöglichen das Beibehalten und Durchsuchen von Speichern in verschiedenen Teilen der Registrierung eines lokalen Computers oder in der Registrierung auf einem Remotecomputer, wenn die richtigen Berechtigungen festgelegt sind.

Jeder Benutzer verfügt über einen persönlichen My-Speicher, in dem die Zertifikate dieses Benutzers gespeichert werden. Der Speicher My kann sich an einem beliebigen physischen Speicherort befinden, einschließlich der Registrierung auf einem [](../secgloss/s-gly.md)lokalen Computer oder Remotecomputer, einer Datenträgerdatei, einer Datenbank, eines Verzeichnisdiensts, einer Smartcard oder eines anderen Speicherorts. Während jedes Zertifikat im Speicher My gespeichert werden kann, sollte dieser Speicher für die persönlichen Zertifikate eines Benutzers reserviert sein: die Zertifikate, die zum Signieren und Entschlüsseln der Nachrichten dieses Benutzers verwendet werden.

Die Verwendung von Zertifikaten für die Authentifizierung hängt davon ab, ob Zertifikate von einem vertrauenswürdigen Zertifikataussteller ausgestellt wurden. Zertifikate für vertrauenswürdige Zertifikataussteller werden in der Regel im Stammspeicher gespeichert, der derzeit in einem Registrierungsunterschlüssel beibehalten wird. Im CryptoAPI-Kontext ist der Stammspeicher geschützt, und die Dialogfelder der Benutzeroberfläche erinnern den Benutzer daran, nur vertrauenswürdige Zertifikate in diesem Speicher zu platzieren. In Unternehmensnetzwerksituationen können Zertifikate von einem Systemadministrator per Push vom Domänencontrollercomputer in die Stammspeicher auf Clientcomputern kopiert werden. Dieser Prozess stellt allen Mitgliedern einer Domäne ähnliche Vertrauenslisten zur Seite.

Andere Zertifikate können im Systemspeicher der Zertifizierungsstelle [*oder*](../secgloss/c-gly.md) in vom Benutzer erstellten dateibasierten Speichern gespeichert werden.

Listen mit Funktionen zum Verwenden und Verwalten von Zertifikatspeichern finden Sie unter [Certificate Store Functions](cryptography-functions.md).

Ein Beispiel, in dem einige dieser Funktionen verwendet werden, finden Sie unter [Beispiel C-Programm: Store Vorgänge.](example-c-program-certificate-store-operations.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwalten eines Zertifikats Store Status](managing-a-certificate-store-state.md)
</dt> <dt>

[Arbeiten mit Zertifikaten in Zertifikatspeichern](working-with-certificates-in-certificate-stores.md)
</dt> <dt>

[Zertifikatlinks](certificate-links.md)
</dt> <dt>

[Sammlungsspeicher](collection-stores.md)
</dt> <dt>

[Logische und physische Speicher](logical-and-physical-stores.md)
</dt> <dt>

[System Store Speicherorte](system-store-locations.md)
</dt> <dt>

[Migration Store Zertifikaten](certificate-store-migration.md)
</dt> </dl>

 

 
