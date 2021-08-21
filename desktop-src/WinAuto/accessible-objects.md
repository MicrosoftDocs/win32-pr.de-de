---
title: Barrierefreie Objekte
description: Mit Microsoft Active Accessibility werden Benutzeroberflächenelemente für Clients als Component Object Model (COM)-Objekte verfügbar gemacht.
ms.assetid: ab5669c3-33ce-4d56-a028-e36db25c0b28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9591c4884826ba9d85192e5702d0528f25087797faf83d83314d5c00f172459b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994380"
---
# <a name="accessible-objects"></a>Barrierefreie Objekte

Mit Microsoft Active Accessibility werden Benutzeroberflächenelemente für Clients als Component Object Model (COM)-Objekte verfügbar gemacht. Diese *barrierefreien Objekte* behalten Informationen, die als Eigenschaften bezeichnet werden, bei, die den Namen, die Bildschirmposition des Objekts und andere Informationen beschreiben, die von Barrierefreiheitshilfen benötigt werden. Barrierefreie Objekte stellen auch *Methoden zur Verfügung,* die Clients aufrufen, damit das Objekt eine Aktion ausführen kann. Barrierefreie Objekte, denen einfache Elemente zugeordnet sind, werden auch als *über- oder*-Container *bezeichnet.*

Barrierefreie Objekte werden mithilfe Microsoft Active Accessibility COM-basierten [**IAccessible-Schnittstelle implementiert.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Mit **den IAccessible-Methoden** und -Eigenschaften können Clientanwendungen Informationen zu Benutzeroberflächenelementen erhalten, die von Benutzern benötigt werden. Beispielsweise gibt [**IAccessible::get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) einen Schnittstellenzeiger auf das übergeordnete Element eines barrierefreien Objekts zurück, und [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) bietet Clients eine Möglichkeit, Informationen zu anderen Objekten in einem Container zu erhalten.

Weitere Informationen dazu, wie barrierefreie Objekte und einfache Elemente verknüpft sind, finden Sie unter [Simple Elements](simple-elements.md).

 

 




