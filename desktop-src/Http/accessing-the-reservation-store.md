---
title: Zugreifen auf den Reservierungs Speicher
description: Die HTTP-Server-API verwaltet die Liste der Namespace Reservierungen für alle Benutzer auf dem Computer.
ms.assetid: 4b1291fc-cc62-4d4f-9150-18cbb1f6e5c0
keywords:
- Zugreifen auf den Reservierungs Speicher http
- Reservierungs Speicher http, zugreifen auf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a138a0a2385e6338877e5e8623527a64a6eca796
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388321"
---
# <a name="accessing-the-reservation-store"></a>Zugreifen auf den Reservierungs Speicher

Die HTTP-Server-API verwaltet die Liste der Namespace Reservierungen für alle Benutzer auf dem Computer. Ein Reservierungs Eintrag besteht aus einem [URLPrefix](urlprefix-strings.md) und einer entsprechenden ACL. Jedes URLPrefix im Speicher verfügt über eine ACL, die alle Benutzer auflistet, die sich für den Empfang von Anforderungen für den Namespace registrieren dürfen. Benutzer mit Delegierungs Berechtigungen können Teil Strukturen des Namespace, den Sie besitzen, an andere Benutzer delegieren oder vorhandene Reservierungen mithilfe der Konfigurations-APIs löschen.

Um dem permanenten Reservierungs Speicher eine Reservierung hinzuzufügen, ruft die Anwendung die [**httpsetserviceconfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) -Funktion auf, wobei der Konfigurations-ID-Parameter auf den **httpserviceconfigurlaclinfo** -Wert festgelegt ist. Die HTTP-Server-API überprüft den Besitz des Namespace und der Benutzer-ID, bevor eine Reservierung zum Speicher hinzugefügt wird.

Die HTTP-Server-API stellt auch Funktionen zum Abfragen und Löschen der Dienst Konfigurationen für URL-Namespaces bereit. Die [**httpqueryserviceconfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) -Funktion, die mit dem Parameter "Configuration ID" aufgerufen wurde, ist auf die **httpserviceconfigurlaclinfo** -Wert Abfragen festgelegt, und die Funktion " [**httpdelta eteserviceconfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) " wird im URL-Namespace Speicher gelöscht.

 

 




