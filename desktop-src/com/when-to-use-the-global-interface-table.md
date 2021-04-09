---
title: Verwendungszwecke der globalen Schnittstellen Tabelle
description: Verwendungszwecke der globalen Schnittstellen Tabelle
ms.assetid: def8f7f8-9d0d-49a4-9d5c-40233903eea5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f89bbd7437b65c85abe89e8d647cbd73555c2d6a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039651"
---
# <a name="when-to-use-the-global-interface-table"></a>Verwendungszwecke der globalen Schnittstellen Tabelle

Wenn Sie einen Schnittstellen Zeiger mehrmals zwischen den Apartments in einem Prozess wieder verwenden, können Sie die [**iglobalinterfaketable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) -Schnittstelle verwenden. Bei anderen Techniken müssten Sie jedes Mal einen erneuten Mars Hall durchsetzen.

> [!Note]  
> Wenn der Schnittstellen Zeiger nur einmal gemarshallt wird, können Sie die [**comarshalinterthreadinterfakeinstream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) -Funktion verwenden. Sie kann auch verwendet werden, um einen Schnittstellen Zeiger von einem Thread an einen anderen Thread im gleichen Prozess zu übergeben.

 

Die [**iglobalinterfaketable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) -Schnittstelle macht auch ein anderes, bisher schwieriges Problem für den Programmierer einfacher. Dieses Problem tritt auf, wenn die folgenden Bedingungen zutreffen:

-   Ein in-Process-Agile-Objekt aggregiert den frei Thread-Mars Haller.
-   Das gleiche Agile-Objekt enthält auch (als Element Variablen) Schnittstellen Zeiger auf andere Objekte, die nicht agil sind und den Freethread-Mars Haller nicht aggregieren.

Wenn das äußere Objekt in diesem Fall an ein anderes Apartment gemarshallt wird und die Anwendung darauf aufruft, und das Objekt versucht, für einen seiner Member-Variablen Schnittstellen Zeiger aufzurufen, die nicht frei Thread sind oder für Objekte in anderen Apartments Proxys sind, erhalten Sie möglicherweise falsche Ergebnisse oder den falschen RPC-Fehler \_ \_ \_ Thread. Dieser Fehler tritt auf, weil die innere Schnittstelle nur von dem Apartment aus aufgerufen werden kann, in dem Sie zuerst in der Element Variablen gespeichert wurde.

Um dieses Problem zu beheben, sollte das äußere Objekt, das den Freethread-Mars Haller aggregiert, [**iglobalinterfaketable:: registerinterfakeinglobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) auf der inneren Schnittstelle aufrufen und das resultierende Cookie in seiner Member-Variablen speichern, anstatt den eigentlichen Schnittstellen Zeiger zu speichern. Wenn das äußere Objekt für den Schnittstellen Zeiger eines inneren Objekts aufrufen möchte, sollte es [**iglobalinterfaketable:: getinterfakefromglobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal)aufrufen, den zurückgegebenen Schnittstellen Zeiger verwenden und es dann freigeben. Wenn das äußere Objekt entfernt wird, sollte es [**iglobalinterfaketable:: revokeinterfakefromglobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) aufgerufen werden, um die Schnittstelle aus der globalen Schnittstellen Tabelle zu entfernen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen der globalen Schnittstellen Tabelle](creating-the-global-interface-table.md)
</dt> </dl>

 

 