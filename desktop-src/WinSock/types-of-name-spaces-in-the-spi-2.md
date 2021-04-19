---
description: Die drei Typen von Namespaces im Windows Sockets (Winsock) SPI enthalten dynamische, statische und persistente Namespaces.
ms.assetid: 2968ac98-bd40-4d37-9dd7-7870c4decd40
title: Typen von Namespaces in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e40356987c67604755696f1a8b7224de15851ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368933"
---
# <a name="types-of-namespaces-in-the-spi"></a>Typen von Namespaces in der SPI

Es gibt drei verschiedene Typen von Namespaces, in denen ein Dienst registriert werden kann:

-   Dynamisch
-   statischen
-   Beständig

Mithilfe dynamischer Namespaces können Dienste bei Bedarf beim Namespace registriert werden, und Clients können die verfügbaren Dienste zur Laufzeit ermitteln. Dynamische Namespaces basieren häufig auf Übertragungen, um die fortgesetzte Verfügbarkeit eines Netzwerk Dienstanbieter anzugeben. Beispiele für dynamische Namespaces sind der SAP-Namespace, der in einer NetWare-Umgebung verwendet wird, und der NBP-Namespace, der von AppleTalk verwendet wird.

Statische Namespaces erfordern, dass alle Dienste vorab registriert werden, d. h. wenn der Namespace erstellt wird. Der DNS ist ein Beispiel für einen statischen Namespace. Obwohl es eine programmgesteuerte Methode zum Auflösen von Namen gibt, gibt es keine programmgesteuerte Methode zum Registrieren von Namen.

Persistente Namespaces ermöglichen es Diensten, sich dynamisch bei dem Namespace zu registrieren. Im Gegensatz zu dynamischen Namespaces behalten persistente Namespaces jedoch die Registrierungsinformationen im nicht flüchtigen Speicher bei, wo Sie bis zu dem Zeitpunkt verbleibt, an dem der Dienst die Entfernung anfordert. Persistente Namespaces werden durch Verzeichnisdienste wie z. b. X. 500 und den NDS (NetWare-Verzeichnisdienst) typisierten. Diese Umgebungen ermöglichen das Hinzufügen, löschen und Ändern von Dienst Eigenschaften. Außerdem kann das Dienst Objekt, das den Dienst im Verzeichnisdienst darstellt, über eine Vielzahl von Attributen verfügen, die mit dem Dienst verknüpft sind. Das wichtigste Attribut für Client Anwendungen sind die Adressierungs Informationen des dienstanders.

 

 



