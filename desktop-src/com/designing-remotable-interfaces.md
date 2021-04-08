---
title: Entwerfen von Remote fähigen Schnittstellen
description: Mit der Einführung des Objektmodells für verteilte Komponenten ist es wichtig, dass die benutzerdefinierte Schnittstelle Remote fähig ist, auch wenn Sie Sie nur in-Process verwenden möchten.
ms.assetid: 2ee4d950-dfd5-4965-bd77-a600e878be59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3502604d62e6a5129ca3e3538761722909c0198f
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "103857952"
---
# <a name="designing-remotable-interfaces"></a>Entwerfen von Remote fähigen Schnittstellen

Mit der Einführung des Objektmodells für verteilte Komponenten ist es wichtig, dass die benutzerdefinierte Schnittstelle Remote fähig ist, auch wenn Sie Sie nur in-Process verwenden möchten.

Die Mittel l ist mehr als nur eine Möglichkeit zum Generieren von Header Dateien für ihre Schnittstellen. Es handelt sich um eine Programmiersprache für Remoting, mit der Sie Ihre Schnittstellen über die verschiedenen Computer-, Prozess-und Thread Grenzen hinweg verwenden können. Dies bedeutet, dass Sie das Verhalten ihrer Mittelwert definierten Schnittstellen unter diesen Bedingungen überprüfen müssen, bevor Sie Ihr Programm für Kunden freigeben. Wenn Sie in ihrer IDL einen Fehler gemacht haben und die Schnittstelle nicht ordnungsgemäß Remote ist, kann es schwierig sein, diesen Fehler zu beheben. Entweder müssen Sie Ihre Schnittstelle mit einer neuen IID überarbeiten und die alte in aus Gründen der Abwärtskompatibilität belassen, oder Sie müssen jeden Client und jeden Server Computer gleichzeitig konvertieren.

Auch wenn Ihre Schnittstelle nie außerhalb des Prozesses verwendet wird, kann Sie Thread übergreifend verwendet werden. Das schlimmste Problem für eine nicht überprüfte IDL-Datei kann für Prozess interne Server auftreten, die mehrere [Single Thread-Apartments](single-threaded-apartments.md)nicht unterstützen. Ein Server, der kein Threading Modell angibt, ist implizit Single Thread. Alles markierte als Single Thread wird für den Thread erzwungen, der zuerst [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) oder [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)aufgerufen hat. Wenn es sich bei einem anderen Thread um den Thread handelt, der das Objekt aktiviert hat, müssen alle Schnittstellen auf diesem Single Thread-Server auf den Aktivierungs Thread zurückgesetzt werden. Dies kann zu einer Rückgabe von RegDB \_ E \_ iidnotreg als Reaktion auf einen aufzurufenden [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))-Auflistungen führen. Es sei denn, Sie können sicherstellen, dass Ihre Schnittstelle in-Process ist und immer im gleichen Thread aufgerufen wird.

Als Schnittstellen Designer müssen Sie schließlich die Verwendung Ihrer Schnittstelle durch Client Anwendungen in Erwägung gezogen werden. Zwei Dinge bestimmen, ob eine Schnittstelle über Prozess-und Computer Grenzen hinweg effizient sein wird: die Häufigkeit von Methoden aufrufen über die Schnittstellen Grenze hinweg und die Menge an Daten, die in einem bestimmten Methodenaufruf übertragen werden. Obwohl com prozessübergreifende und Netzwerk übergreifende Aufrufe für Programme transparent macht, kann der Aufruf von hoch-und Hochbandbreite nicht über Adressräume hinweg effizient erfolgen. In einigen Fällen ist es besser, Schnittstellen zu entwerfen, die normalerweise nur als Prozess interne Server implementiert werden, während andere Schnittstellen besser für die Remote Verwendung geeignet sind.

 

 




