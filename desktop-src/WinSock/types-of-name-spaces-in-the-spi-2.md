---
description: Die drei Typen von Namespaces in der Windows Sockets (Winsock) SPI umfassen dynamische, statische und persistente Namespaces.
ms.assetid: 2968ac98-bd40-4d37-9dd7-7870c4decd40
title: Typen von Namespaces in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ec933650825e891a723cbbc041ad4f631c6f54b7b2b4f6a255359b640509ef3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733190"
---
# <a name="types-of-namespaces-in-the-spi"></a>Typen von Namespaces in der SPI

Es gibt drei verschiedene Arten von Namespaces, in denen ein Dienst registriert werden kann:

-   Dynamisch
-   statischen
-   Beständig

Dynamische Namespaces ermöglichen es Diensten, sich dynamisch beim Namespace zu registrieren und clients die verfügbaren Dienste zur Laufzeit zu entdecken. Dynamische Namespaces basieren häufig auf Broadcasts, um die weitere Verfügbarkeit eines Netzwerkdiensts anzugeben. Beispiele für dynamische Namespaces sind der SAP-Namespace, der in einer NetWare-Umgebung verwendet wird, und der nbp-Namespace, der von AppleTalk verwendet wird.

Statische Namespaces erfordern, dass alle Dienste im Voraus registriert werden, d.&a; wenn der Namespace erstellt wird. Das DNS ist ein Beispiel für einen statischen Namespace. Obwohl es eine programmgesteuerte Möglichkeit gibt, Namen aufzulösen, gibt es keine programmgesteuerte Möglichkeit, Namen zu registrieren.

Persistente Namespaces ermöglichen es Diensten, sich während der Zeit beim Namespace zu registrieren. Im Gegensatz zu dynamischen Namespaces behalten persistente Namespaces die Registrierungsinformationen jedoch in einem nicht permanenten Speicher bei, in dem sie so lange beibehalten werden, bis der Dienst anfing, sie zu entfernen. Persistente Namespaces werden von Verzeichnisdiensten wie X.500 und dem NDS (NetWare Directory Service) typisiert. Diese Umgebungen ermöglichen das Hinzufügen, Löschen und Ändern von Diensteigenschaften. Darüber hinaus kann das Dienstobjekt, das den Dienst innerhalb des Verzeichnisdiensts darstellt, über eine Vielzahl von Attributen verfügen, die dem Dienst zugeordnet sind. Das wichtigste Attribut für Clientanwendungen sind die Adressierungsinformationen des Diensts.

 

 



