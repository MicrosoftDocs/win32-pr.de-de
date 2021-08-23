---
title: Verwendung der globalen Schnittstellentabelle
description: Verwendung der globalen Schnittstellentabelle
ms.assetid: def8f7f8-9d0d-49a4-9d5c-40233903eea5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37457e0e1b35c0c1acb2c8f84750f3d0f08c1344eaf27e0361c442aea3be23ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639230"
---
# <a name="when-to-use-the-global-interface-table"></a>Verwendung der globalen Schnittstellentabelle

Wenn Sie einen Schnittstellenzeiger mehrmals zwischen den Apartments in einem Prozess entmarten, können Sie die [**IGlobalInterfaceTable-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) verwenden. Mit anderen Techniken müssten Sie jedes Mal erneut einatmen.

> [!Note]  
> Wenn der Schnittstellenzeiger nur einmal nichtmarshaliert ist, können Sie die [**CoMarshalInterThreadInterfaceInStream-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) verwenden. Sie kann auch verwendet werden, um einen Schnittstellenzeiger von einem Thread an einen anderen Thread im gleichen Prozess zu übergeben.

 

Die [**IGlobalInterfaceTable-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) vereinfacht auch ein weiteres zuvor schwieriges Problem für den Programmierer. Dieses Problem tritt auf, wenn die folgenden Bedingungen erfüllt sind:

-   Ein prozessübergreifendes agiles Objekt aggregiert den Marshaller mit freiem Thread.
-   Dieses agile Objekt enthält auch (als Membervariablen) Schnittstellenzeiger auf andere Objekte, die nicht agil sind und den Marshaller mit freiem Thread nicht aggregieren.

Wenn in diesem Fall das äußere Objekt in ein anderes Apartment gemarshallt wird und die Anwendung darauf aufruft und das Objekt versucht, für einen seiner Schnittstellenzeigenzeigen von Membervariablen aufzurufen, die nicht über Einenthread verfügen oder Proxys für Objekte in anderen Apartments sind, kann dies zu falschen Ergebnissen oder dem Fehler RPC \_ E \_ WRONG THREAD \_ führen. Dieser Fehler tritt auf, da die innere Schnittstelle so konzipiert ist, dass sie nur aus dem Apartment aufrufbar ist, in dem sie zuerst in der Membervariablen gespeichert wurde.

Um dieses Problem zu lösen, sollte das äußere Objekt, das den Marshaller mit Freiem Thread aggregiert, [**IGlobalInterfaceTable::RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) auf der inneren Schnittstelle aufrufen und das resultierende Cookie in seiner Membervariablen speichern, anstatt den tatsächlichen Schnittstellenzeiger zu speichern. Wenn das äußere Objekt für den Schnittstellenzeiger eines inneren Objekts aufrufen möchte, sollte es [**IGlobalInterfaceTable::GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal)aufrufen, den zurückgegebenen Schnittstellenzeiger verwenden und ihn dann los lassen. Wenn das äußere Objekt entfernt wird, sollte es [**IGlobalInterfaceTable::RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) aufrufen, um die Schnittstelle aus der globalen Schnittstellentabelle zu entfernen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen der globalen Schnittstellentabelle](creating-the-global-interface-table.md)
</dt> </dl>

 

 