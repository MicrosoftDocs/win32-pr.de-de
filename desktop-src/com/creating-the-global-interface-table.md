---
title: Erstellen der globalen Schnittstellen Tabelle
description: Erstellen der globalen Schnittstellen Tabelle
ms.assetid: e8e46642-ef41-4322-97d0-8dd5b7c72992
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f792f9664da554f6522086796f94a00ccdf0dc07
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391088"
---
# <a name="creating-the-global-interface-table"></a>Erstellen der globalen Schnittstellen Tabelle

Verwenden Sie den folgenden Aufruf, um das globale Schnittstellen Tabellenobjekt zu erstellen, und rufen Sie einen Zeiger auf [**iglobalinterfaketable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable)ab:

``` syntax
HRESULT hr;
hr = CoCreateInstance(CLSID_StdGlobalInterfaceTable,
                 NULL,
                 CLSCTX_INPROC_SERVER,
                 IID_IGlobalInterfaceTable,
                 (void **)&gpGIT);
if (hr != S_OK) {
  exit(0); // Handle errors here.
}
```

> [!Note]  
> Beim Erstellen des globalen Schnittstellen Tabellenobjekts mit dem vorhergehenden-Befehl ist es erforderlich, eine Verknüpfung mit der Bibliothek UUID. lib herzustellen. Hierdurch werden die externen Symbole CLSID \_ stdglobalinterfaketable und IID \_ iglobalinterfaketable aufgelöst.

 

Es gibt eine einzelne Instanz der globalen Schnittstellen Tabelle pro Prozess, sodass alle Aufrufe dieser Funktion in einem Prozess dieselbe Instanz zurückgeben.

Nachdem Sie die [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion aufgerufen haben, registrieren Sie die-Schnittstelle aus dem Apartment, in dem Sie sich befindet, mit einem Aufrufen der [**registerinterfaceinglobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) -Methode. Diese Methode stellt ein Cookie bereit, das die-Schnittstelle und deren Position identifiziert. Ein Apartment, das einen Zeiger auf diese Schnittstelle sucht, ruft dann die [**getinterfacefromglobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal) -Methode mit diesem Cookie auf, und die Implementierung stellt dann einen Schnittstellen Zeiger auf das aufrufende Apartment bereit. Um die globale Registrierung der Schnittstelle aufzuheben, kann jedes Apartment die [**revokeinterfacefromglobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) -Methode aufzurufen.

Ein einfaches Beispiel für die Verwendung von [**iglobalinterfaketable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) wäre, wenn Sie einen Schnittstellen Zeiger für ein Objekt in einem Single Thread-Apartment (STA) an einen Arbeits Thread in einem anderen Apartment übergeben möchten. Anstatt Sie in einen Datenstrom zu Mars Hallen und den Datenstrom als Thread Parameter an den Arbeits Thread zu übergeben, ermöglicht **iglobalinterfaketable** lediglich das Übergeben eines Cookies.

Wenn Sie die Schnittstelle in der globalen Schnittstellen Tabelle registrieren, wird ein Cookie angezeigt, das Sie verwenden können, anstatt den tatsächlichen Zeiger zu übergeben (wenn Sie den Zeiger übergeben müssen), entweder an einen nicht-Methoden Parameter, der zu einem anderen Apartment (als Parameter für [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) durch " [**kreatethread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)") oder zu einem Prozess internen Speicher außerhalb des Apartment.

Vorsicht ist erforderlich, da durch die Verwendung von globalen Schnittstellen der Programmierer für das Verwalten von Problemen wie Racebedingungen und gegenseitiger Ausschluss, die mit dem gleichzeitigen Zugriff auf den globalen Zustand mehrerer Threads verknüpft sind, zusätzliche Belastung entstehen kann.

COM stellt eine Standard Implementierung der [**iglobalinterfaketable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) -Schnittstelle bereit. Es wird dringend empfohlen, diese Standard Implementierung zu verwenden, da Sie eine komplette Thread sichere Funktionalität bereitstellt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwendungszwecke der globalen Schnittstellen Tabelle](when-to-use-the-global-interface-table.md)
</dt> </dl>

 

 