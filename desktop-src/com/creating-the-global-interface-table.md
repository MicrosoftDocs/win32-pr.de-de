---
title: Erstellen der globalen Schnittstellentabelle
description: Erstellen der globalen Schnittstellentabelle
ms.assetid: e8e46642-ef41-4322-97d0-8dd5b7c72992
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 836cc5507ac9b8e7cccd6e9dc8fd8c2d71e1a23419945ecc01d35b3978940124
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793770"
---
# <a name="creating-the-global-interface-table"></a>Erstellen der globalen Schnittstellentabelle

Verwenden Sie den folgenden Aufruf, um das globale Schnittstellentabellenobjekt zu erstellen und einen Zeiger auf [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable)abzurufen:

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
> Beim Erstellen des globalen Schnittstellentabellenobjekts mithilfe des vorherigen Aufrufs muss eine Verknüpfung mit der Bibliothek "uuid.lib" hergestellt werden. Dadurch werden die externen Symbole CLSID \_ StdGlobalInterfaceTable und IID \_ IGlobalInterfaceTable aufgelöst.

 

Es gibt eine einzelne Instanz der globalen Schnittstellentabelle pro Prozess, sodass alle Aufrufe dieser Funktion in einem Prozess dieselbe Instanz zurückgeben.

Registrieren Sie nach dem Aufruf der [**CoCreateInstance-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) die -Schnittstelle aus dem Apartment, in dem sie sich befindet, mit einem Aufruf der [**RegisterInterfaceInGlobal-Methode.**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) Diese Methode stellt ein Cookie zur Verfügung, das die Schnittstelle und deren Position identifiziert. Ein Apartment, das einen Zeiger auf diese Schnittstelle sucht, ruft dann die [**GetInterfaceFromGlobal-Methode**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal) mit diesem Cookie auf, und die Implementierung stellt dann einen Schnittstellenzeiger auf das aufrufende Apartment bereit. Um die globale Registrierung der Schnittstelle zu widerrufen, kann jedes Apartment die [**RevokeInterfaceFromGlobal-Methode**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) aufrufen.

Ein einfaches Beispiel für die Verwendung von [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) wäre, wenn Sie einen Schnittstellenzeiger für ein Objekt in einem Singlethread-Apartment (STA) an einen Arbeitsthread in einem anderen Apartment übergeben möchten. Anstatt ihn in einen Stream zu marshallen und den Stream als Threadparameter an den Arbeitsthread zu übergeben, ermöglicht **IGlobalInterfaceTable** ihnen einfach das Übergeben eines Cookies.

Wenn Sie die Schnittstelle in der globalen Schnittstellentabelle registrieren, erhalten Sie ein Cookie, das Sie verwenden können, anstatt den tatsächlichen Zeiger zu übergeben (wenn Sie den Zeiger übergeben müssen), entweder an einen Nichtmethodparameter, der in ein anderes Apartment (als Parameter für [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) über [**CreateThread)**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)oder an den Prozessspeicher außerhalb Ihres Apartments geht.

Vorsicht ist erforderlich, da die Verwendung von globalen Schnittstellen dem Programmierer die zusätzliche Belastung für die Verwaltung von Problemen wie Racebedingungen und gegenseitigem Ausschluss mit sich bringt, die mit dem gleichzeitigen Zugriff auf den globalen Zustand von mehreren Threads verbunden sind.

COM stellt eine Standardimplementierungen der [**IGlobalInterfaceTable-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) bereit. Es wird dringend empfohlen, diese Standardimplementierungen zu verwenden, da sie vollständige threadsichere Funktionen bietet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwendung der globalen Schnittstellentabelle](when-to-use-the-global-interface-table.md)
</dt> </dl>

 

 