---
title: Zugreifen auf Schnittstellen über mehrere Apartments
description: Zugreifen auf Schnittstellen über mehrere Apartments
ms.assetid: 4e0467b9-bbf1-410c-8aab-40450a7f963a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626707daf721aee3b440bb79ba2d1e084d154a98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709258"
---
# <a name="accessing-interfaces-across-apartments"></a>Zugreifen auf Schnittstellen über mehrere Apartments

COM bietet eine Möglichkeit für jedes Apartment in einem Prozess, Zugriff auf eine Schnittstelle zu erhalten, die für ein Objekt in einem beliebigen anderen Apartment im Prozess implementiert ist. Dies erfolgt über die [**iglobalinterfaketable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) -Schnittstelle. Diese Schnittstelle verfügt über drei Methoden, mit denen Sie die folgenden Aktionen ausführen können:

-   Registrieren Sie eine Schnittstelle als *globale* (Processwide) Schnittstelle.
-   Einen Zeiger auf diese Schnittstelle von einem beliebigen anderen Apartment über ein Cookie erhalten.
-   Widerrufen Sie die globale Registrierung einer Schnittstelle.

Die [**iglobalinterfaketable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) -Schnittstelle ist ein effizientes Verfahren zum Speichern eines Schnittstellen Zeigers an einem Speicherort, auf den von mehreren Apartments innerhalb des Prozesses zugegriffen werden kann, z. b. Prozess weite Variablen und *Agile* -Objekte (frei Thread-, gemarshallte Objekte), die Schnittstellen Zeiger auf andere Objekte enthalten.

Ein Agile-Objekt kennt die zugrunde liegende COM-Infrastruktur, in der es ausgeführt wird, nicht. Anders ausgedrückt: Das Apartment, der Kontext und der Thread, auf dem es ausgeführt wird. Das Objekt ist möglicherweise für Schnittstellen, die für ein Apartment oder einen kontextspezifisch sind. Aus diesem Grund funktioniert das Aufrufen dieser Schnittstellen von überall aus, wo die Agile-Komponente ausgeführt wird, möglicherweise nicht immer ordnungsgemäß. Die globale Schnittstellen Tabelle vermeidet dieses Problem, indem Sie sicherstellt, dass ein gültiger Proxy (oder direkter Zeiger) für das-Objekt verwendet wird, je nachdem, wo das Agile-Objekt ausgeführt wird.

> [!Note]  
> Die globale Schnittstellen Tabelle ist nicht über Prozess-oder Computer Grenzen hinweg portabel und kann daher nicht anstelle des normalen Parameters-Passing-Mechanismus verwendet werden.

 

Weitere Informationen zum Erstellen und Verwenden einer globalen Schnittstellen Tabelle finden Sie in den folgenden Themen:

-   [Erstellen der globalen Schnittstellen Tabelle](creating-the-global-interface-table.md)
-   [Verwendungszwecke der globalen Schnittstellen Tabelle](when-to-use-the-global-interface-table.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Auswählen des Threading Modells](choosing-the-threading-model.md)
</dt> <dt>

[Multithread-Apartments](multithreaded-apartments.md)
</dt> <dt>

[Threading Probleme im Prozess internen Server](in-process-server-threading-issues.md)
</dt> <dt>

[Prozesse, Threads und Apartments](processes--threads--and-apartments.md)
</dt> <dt>

[Single Thread-und Multithread-Kommunikation](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Single Thread-Apartments](single-threaded-apartments.md)
</dt> </dl>

 

 




