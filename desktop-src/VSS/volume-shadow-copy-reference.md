---
description: Der Volumeschattenkopie-Dienst (VSS) ist ein Satz von com-und C++-APIs, mit denen Volumesicherungen ausgeführt werden können, während Anwendungen auf dem System (als Writer bezeichnet) weiterhin auf den Volumes schreiben.
ms.assetid: 94d9504b-2838-4516-8031-daa7bd9d2fec
title: Volumen Schatten Kopie-API-Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea8651c987c01ce67f1383f2ab1a24ca3fea8bbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526294"
---
# <a name="volume-shadow-copy-api-reference"></a>Volumen Schatten Kopie-API-Referenz

Der Volumeschattenkopie-Dienst (VSS) ist ein Satz von com-und C++-APIs, mit denen Volumesicherungen ausgeführt werden können, während Anwendungen auf dem System (als Writer bezeichnet) weiterhin auf den Volumes schreiben.

VSS unterstützt diese Sicherungen durch die Erstellung von Schatten Kopien, ein Duplikat des ursprünglichen Volumes zu einem bestimmten Zeitpunkt.

Entwickler von Drittanbietern können mit der VSS-API Anforderer (z. b. eine Sicherungs Anwendung) zum Erstellen und Verwalten von Schatten Kopien erstellen.

Die tatsächliche Erstellung und Darstellung von Schatten Kopien erfolgt durch Anwendungen auf Systemebene, die als Anbieter bezeichnet werden.

Entwickler können die API auch zum Erstellen von Writern verwenden: VSS-fähige Anwendungen, die e/a-Vorgänge mit der Erstellung und Bearbeitung von Schatten Kopien koordinieren können.

-   [Volumen Schatten Kopie-API-Klassen](volume-shadow-copy-api-classes.md)
-   [Datentypen der Volumeschattenkopie-API](volume-shadow-copy-api-data-types.md)
-   [Volumeschattenkopie-API-Enumerationen](volume-shadow-copy-api-enumeration-types.md)
-   [Volumen Schatten Kopie-API-Funktionen](volume-shadow-copy-api-functions.md)
-   [Volumeschattenkopie-API](volume-shadow-copy-api-interfaces.md)
-   [Volumen Schatten Kopie-API-Strukturen](volume-shadow-copy-api-structures.md)
-   [Glossar der Volumeschattenkopie](volume-shadow-copy-glossary.md)

Weitere Informationen zum Schreiben von Anforderern und Writern finden [Sie unter Verwenden der Volumeschattenkopie-Dienst](using-the-volume-shadow-copy-service.md).

 

 



