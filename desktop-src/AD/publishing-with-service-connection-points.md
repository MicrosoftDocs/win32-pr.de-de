---
title: Veröffentlichen mit Dienst Verbindungs Punkten
description: Das Active Directory Schema definiert eine serviceConnectionPoint-Objektklasse (SCP), um es einem Dienst zu erleichtern, Dienst spezifische Daten im Verzeichnis zu veröffentlichen.
ms.assetid: 3544aa64-ecb0-48a1-ae49-05247a983842
ms.tgt_platform: multiple
keywords:
- Veröffentlichen mit Dienst Verbindungs Punkten AD
- Dienst Verbindungspunkte AD
- Dienst Verbindungspunkte AD, Veröffentlichung mit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a458822f6c5e4d764b2e330c7ba084021b586548
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707577"
---
# <a name="publishing-with-service-connection-points"></a>Veröffentlichen mit Dienst Verbindungs Punkten

Das Active Directory Schema definiert eine **serviceConnectionPoint** -Objektklasse (SCP), um es einem Dienst zu erleichtern, Dienst spezifische Daten im Verzeichnis zu veröffentlichen. Clients des Dienstanbieter verwenden die Daten in einem Dienst Verbindungspunkt, um eine Instanz des Dienstanbieter zu suchen, zu verbinden und zu authentifizieren.

Dieser Abschnitt enthält eine Übersicht über Dienst Verbindungspunkte und Codebeispiele, die zeigen, wie eine Client-/Dienstanwendung SCPs verwendet.

Im Codebeispiel werden die folgenden Schritte ausgeführt, um eine Dienst Veröffentlichung mit SCPs zu implementieren.

Weitere Informationen und ein Codebeispiel, in dem diese Schritte ausgeführt werden, finden Sie unter [Erstellen eines Dienst Verbindungs Punkts](creating-a-service-connection-point.md).

**So erstellen Sie SCPs im Verzeichnis bei der Dienst Installation**

1.  Binden Sie an das Computer Objekt für den Host Computer, auf dem die Dienst Instanz installiert ist.
2.  Erstellen Sie ein SCP-Objekt als untergeordnetes Element des Computer Objekts, und geben Sie die Anfangswerte für die Attribute des Dienst Verbindungs Punkts an.
3.  Legen Sie Zugriffs Steuerungs Einträge (Access Control Entries, ACEs) in der Sicherheits Beschreibung des SCP-Objekts fest, damit der Dienst SCP-Eigenschaften zur Laufzeit ändern kann.
4.  Speichern Sie die **objectGUID** des Dienst Verbindungs Diensts in der Registrierung auf dem Host Computer des Diensts.

Weitere Informationen und ein Codebeispiel, das diese Schritte ausführt, finden Sie unter [Aktualisieren eines Dienst Verbindungs Punkts](updating-a-service-connection-point.md).

**So aktualisieren Sie die SCP-Attribute beim Dienst Start**

1.  Rufen Sie die **objectGUID** aus der Registrierung ab, und verwenden Sie Sie zum Binden an den SCP.
2.  Abrufen von Attributen (z. b. **servicednsname** und **serviceBindingInformation**) vom SCP. Vergleichen Sie diese Werte mit den aktuellen Werten, und aktualisieren Sie ggf. den Dienst Verbindungspunkt.

Weitere Informationen und ein Codebeispiel, in dem diese Schritte ausgeführt werden, finden Sie unter [wie Clients einen Dienst Verbindungspunkt suchen und verwenden](how-clients-find-and-use-a-service-connection-point.md).

**So suchen und verwenden Sie einen SCP durch eine Client Anwendung**

1.  Binden Sie an den globalen Katalog, und suchen Sie nach Objekten mit einem **Schlüssel** Wort Attribut, das der Produkt-GUID des dienstanzdienstan Jedes gefundene Objekt ist eine Instanz des Dienstanbieter. Wählen Sie eine Instanz aus, und rufen Sie den Distinguished Name des Dienst Verbindungs Punkts ab.
2.  Verwenden Sie den definierten Namen, um eine Bindung mit dem Dienstverbindungspunkt herzustellen.
3.  Rufen Sie die Werte verschiedener Attribute aus dem SCP ab, z. b. **servicednsname** und **serviceBindingInformation**. Verwenden Sie diese Werte, um sich mit der Dienstinstanz zu verbinden und sich bei dieser zu authentifizieren.

Weitere Informationen zu den Rollen, die ein SCP erstellen und aktualisieren können, finden Sie unter [Sicherheitsprobleme bei der Dienst Veröffentlichung](security-issues-for-service-publication.md).

Weitere Informationen zum Erstellen eines Dienst Verbindungs Punkts finden Sie unter [Erstellen eines Dienst Verbindungs Punkts](where-to-create-a-service-connection-point.md).

Weitere Informationen zur Art der Daten, die in einem SCP gespeichert werden sollen, finden Sie unter [Eigenschaften von Dienst Verbindungs Punkten](service-connection-point-properties.md).

Weitere Informationen darüber, wie ein Dienst Installationsprogramm und der Dienst zusammenarbeiten, um aktuelle Daten in einem Dienst Verbindungspunkt beizubehalten, finden Sie unter [Erstellen und Verwalten eines Dienst Verbindungs Punkts](creating-and-maintaining-a-service-connection-point.md).

 

 




