---
description: Aktivierungskontexte sind während des gesamten Prozesses sichtbar.
ms.assetid: 6eda00d5-9dac-4267-bf61-b481814201f8
title: Threads, asynchrone Prozeduren und Fenstermeldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 529be75a3bc72679f44dfb69196f9487aa4f1de4f3cdbeada4ec89e26f05d646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141703"
---
# <a name="using-threads-asynchronous-procedures-and-window-messages"></a>Verwenden von Threads, asynchronen Prozeduren und Fenstermeldungen

Aktivierungskontexte sind während des gesamten Prozesses sichtbar. Die Aktivierungskontextstapel sind jedoch threadübergreifend, und zwei Threads im selben Prozess können unterschiedliche Aktivierungsstapel aufweisen. [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread) legt den aktuellen Aktivierungskontext automatisch oben im Aktivierungsstapel des neuen Threads ab. Dies kann das Upgrade von vorhandenem Code zur Verwendung paralleler Komponenten vereinfachen, da der neue Thread sofort im aktuellen Aktivierungskontext ausgeführt werden kann.

Asynchrone Prozeduraufrufe, Abschlussportrückrufe und alle anderen Rückrufe in anderen Threads erhalten automatisch den Aktivierungskontext der Quelle. Wenn der Rückruf aufgerufen wird, wird der Aktivierungsstapel bereinigt. Dies bedeutet, dass Ihre Anwendung asynchrone Prozeduraufrufe und Rückrufe verwenden kann, ohne explizit Kontexte zu aktivieren, da die Kontextverwaltung von der zugrunde liegenden nebeneinander liegenden Infrastruktur durchgeführt wird. Um andere Kontexte während eines Rückrufs oder neuen Threads aktiv zu machen, kann Ihre Anwendung eine eigene Kontextverwaltung durchführen. In diesem Fall muss Ihr Programm die richtige Sequenz von Aktivierungskontextfunktionen zum Aktivieren und Deaktivieren von Funktionen verwenden.

Aktivierungskontexte sind threadneutral. Durch das Aktivieren eines Kontexts wird nur der Stapel des aktuellen Threads geändert, und Sie können keinen Kontext threadübergreifend aktivieren. Thread A kann keinen Kontext auf Thread B erzwingen. Die Funktionen der Aktivierungskontext-API sind ebenfalls threadfähige Funktionen.

Wenn Sie [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) oder [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) verwenden, um eine Fenstermeldung an eine andere Fensterprozedur in Ihrem Prozess zu senden, wird der aktuelle Aktivierungskontext aktiviert, bevor die Nachricht an die Zielprozedur übergeben wird. Der aktuelle Aktivierungskontext wird zusammen mit der Nachricht angezeigt. Dadurch wird sichergestellt, dass Nachrichten, die auf COM-Objekte, DLL-Namen oder andere ressourcenseitige Ressourcen verweisen, die richtigen Kontextinformationen beibehalten.

 

 
