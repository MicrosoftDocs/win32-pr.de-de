---
description: Der Volumeschattenkopie-Dienst (VSS) ist ein Satz von COM- und C++-APIs, mit denen Volumesicherungen ausgeführt werden können, während Anwendungen im System (als Writer bezeichnet) weiterhin auf die Volumes schreiben.
ms.assetid: 94d9504b-2838-4516-8031-daa7bd9d2fec
title: Referenz zur Volumeschattenkopie-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fbc2d0bec6d68572a67a1dc80327fb80028d7f8d98487f24fec24e2c2e65f95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751527"
---
# <a name="volume-shadow-copy-api-reference"></a>Referenz zur Volumeschattenkopie-API

Der Volumeschattenkopie-Dienst (VSS) ist ein Satz von COM- und C++-APIs, mit denen Volumesicherungen ausgeführt werden können, während Anwendungen im System (als Writer bezeichnet) weiterhin auf die Volumes schreiben.

VSS unterstützt diese Sicherungen durch die Erstellung von Schattenkopien, einem Duplikat des ursprünglichen Volumes zu einem bestimmten Zeitpunkt.

Drittanbieterentwickler können die VSS-API verwenden, um Anfordernde (z. B. eine Sicherungsanwendung) zum Erstellen und Verwalten von Schattenkopien zu erstellen und zu verwalten.

Die eigentliche Arbeit zum Erstellen und Darstellen von Schattenkopien wird von Anwendungen auf Systemebene durchgeführt, die als Anbieter bezeichnet werden.

Entwickler können die API auch verwenden, um Writer zu erstellen: VSS-orientierte Anwendungen, die E/A-Vorgänge mit der Erstellung und Bearbeitung von Schattenkopien koordinieren können.

-   [Volumeschattenkopie-API-Klassen](volume-shadow-copy-api-classes.md)
-   [Volumeschattenkopie-API-Datentypen](volume-shadow-copy-api-data-types.md)
-   [Enumerationen der Volumeschattenkopie-API](volume-shadow-copy-api-enumeration-types.md)
-   [Funktionen der Volumeschattenkopie-API](volume-shadow-copy-api-functions.md)
-   [Volumeschattenkopie-API-Schnittstellen](volume-shadow-copy-api-interfaces.md)
-   [Volumeschattenkopie-API-Strukturen](volume-shadow-copy-api-structures.md)
-   [Glossar für Volumeschattenkopien](volume-shadow-copy-glossary.md)

Weitere Informationen zum Schreiben von Anfordernden und Writern finden Sie unter [Verwenden der Volumeschattenkopie-Dienst](using-the-volume-shadow-copy-service.md).

 

 



