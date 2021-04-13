---
title: Barrierefreie Objekte
description: Mit Microsoft Active Accessibility werden Benutzeroberflächen Elemente für Clients als Component Object Model (com)-Objekte verfügbar gemacht.
ms.assetid: ab5669c3-33ce-4d56-a028-e36db25c0b28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba496e011d42fac9a3c4b047a7d8c3b9e0ecf84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388725"
---
# <a name="accessible-objects"></a>Barrierefreie Objekte

Mit Microsoft Active Accessibility werden Benutzeroberflächen Elemente für Clients als Component Object Model (com)-Objekte verfügbar gemacht. Diese *barrierefreien Objekte* behalten Informationen, die als *Eigenschaften* bezeichnet werden, die den Namen des Objekts, den Bildschirm Speicherort und andere von hilfshilfen benötigte Informationen beschreiben. Barrierefreie Objekte stellen auch *Methoden* bereit, die von Clients aufgerufen werden, damit das Objekt Aktionen ausführt. Barrierefreie Objekte, denen einfache Elemente zugeordnet sind, werden *auch als über* geordnete Elemente oder *Container* bezeichnet.

Barrierefreie Objekte werden mithilfe der com-basierten [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle von Microsoft Active Accessibility implementiert. Die **IAccessible** -Methoden und-Eigenschaften ermöglichen es Client Anwendungen, Informationen zu Benutzeroberflächen Elementen zu erhalten, die von Benutzern benötigt werden. [**IAccessible:: get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) gibt z. b. einen Schnittstellen Zeiger auf das übergeordnete Element eines barrierefreien Objekts zurück, und [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) bietet Clients die Möglichkeit, Informationen zu anderen Objekten in einem Container zu erhalten.

Weitere Informationen dazu, wie barrierefreie Objekte und einfache Elemente verknüpft sind, finden Sie unter [einfache Elemente](simple-elements.md).

 

 




