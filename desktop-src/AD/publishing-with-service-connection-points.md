---
title: Veröffentlichen mit Dienstverbindungspunkten
description: Das Active Directory-Schema definiert eine serviceConnectionPoint (SCP)-Objektklasse, um es einem Dienst zu erleichtern, dienstspezifische Daten im Verzeichnis zu veröffentlichen.
ms.assetid: 3544aa64-ecb0-48a1-ae49-05247a983842
ms.tgt_platform: multiple
keywords:
- Veröffentlichen mit Dienstverbindungspunkten AD
- Dienstverbindungspunkte AD
- Dienstverbindungspunkte AD , Veröffentlichung mit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058c0a0e1f488ecdb50c14eb04788470b6bc25a0a3442457f1c57ced4b13efd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184944"
---
# <a name="publishing-with-service-connection-points"></a>Veröffentlichen mit Dienstverbindungspunkten

Das Active Directory-Schema definiert eine **serviceConnectionPoint** (SCP)-Objektklasse, um es einem Dienst zu erleichtern, dienstspezifische Daten im Verzeichnis zu veröffentlichen. Clients des Diensts verwenden die Daten in einem SCP, um eine Instanz Ihres Diensts zu suchen, eine Verbindung mit ihr herzustellen und diese zu authentifizieren.

Dieser Abschnitt enthält eine Übersicht über Dienstverbindungspunkte und Codebeispiele, die zeigen, wie eine Client-/Dienstanwendung SCPs verwendet.

Im Codebeispiel werden diese Schritte zum Implementieren der Dienstveröffentlichung mit SCPs ausgeführt.

Weitere Informationen und ein Codebeispiel, in dem diese Schritte ausgeführt werden, finden Sie unter [Erstellen eines Dienstverbindungspunkts.](creating-a-service-connection-point.md)

**So erstellen Sie SCPs im Verzeichnis bei der Dienstinstallation**

1.  Binden Sie an das Computerobjekt für den Hostcomputer, auf dem die Dienstinstanz installiert ist.
2.  Erstellen Sie ein SCP-Objekt als untergeordnetes Element des Computerobjekts, und geben Sie dabei die Anfangswerte für die Attribute des SCP an.
3.  Legen Sie Zugriffssteuerungseinträge (ACEs) in der Sicherheitsbeschreibung des SCP-Objekts fest, damit der Dienst die SCP-Eigenschaften zur Laufzeit ändern kann.
4.  Zwischenspeichern sie die **objectGUID** des SCP in der Registrierung auf dem Hostcomputer des Diensts.

Weitere Informationen und ein Codebeispiel, in dem diese Schritte ausgeführt werden, finden Sie unter [Aktualisieren eines Dienstverbindungspunkts.](updating-a-service-connection-point.md)

**So aktualisieren Sie die SCP-Attribute beim Dienststart**

1.  Rufen Sie **objectGUID** aus der Registrierung ab, und verwenden Sie sie zum Binden an den SCP.
2.  Rufen Sie Attribute wie **serviceDNSName** und **serviceBindingInformation** vom SCP ab. Vergleichen Sie diese Werte mit den aktuellen Werten, und aktualisieren Sie ggf. den SCP.

Weitere Informationen und ein Codebeispiel, in dem diese Schritte ausgeführt werden, finden Sie unter [Suchen und Verwenden eines Dienstverbindungspunkts](how-clients-find-and-use-a-service-connection-point.md)durch Clients.

**So suchen und verwenden Sie einen SCP von einer Clientanwendung**

1.  Binden Sie an den globalen Katalog, und suchen Sie nach Objekten mit einem Schlüsselwortattribut, das der Produkt-GUID des Diensts entspricht.  Jedes gefundene Objekt ist eine Instanz des Diensts. Wählen Sie eine Instanz aus, und rufen Sie den Distinguished Name des SCP ab.
2.  Verwenden Sie den definierten Namen, um eine Bindung mit dem Dienstverbindungspunkt herzustellen.
3.  Rufen Sie die Werte verschiedener Attribute vom SCP ab, z. B. **serviceDNSName** und **serviceBindingInformation.** Verwenden Sie diese Werte, um sich mit der Dienstinstanz zu verbinden und sich bei dieser zu authentifizieren.

Weitere Informationen dazu, welche Rollen einen SCP erstellen und aktualisieren können, finden Sie unter [Sicherheitsprobleme bei der Dienstveröffentlichung.](security-issues-for-service-publication.md)

Weitere Informationen zum Erstellen eines SCP finden Sie unter [Erstellen eines Dienstverbindungspunkts.](where-to-create-a-service-connection-point.md)

Weitere Informationen zur Art der Daten, die in einem SCP gespeichert werden sollen, finden Sie unter Eigenschaften des [Dienstverbindungspunkts.](service-connection-point-properties.md)

Weitere Informationen dazu, wie ein Dienstinstallationsprogramm und der Dienst zusammenarbeiten, um aktuelle Daten in einem SCP zu verwalten, finden Sie unter [Erstellen und Verwalten eines Dienstverbindungspunkts.](creating-and-maintaining-a-service-connection-point.md)

 

 




