---
title: Einfache Elemente
description: Ein einfaches Element ist ein Benutzeroberflächenelement, das ein IAccessible-Objekt mit anderen Elementen teilt und dieses IAccessible-Objekt (in der Regel sein übergeordnetes Objekt) verwendet, um seine Eigenschaften verfügbar zu machen.
ms.assetid: 3f6bd992-4e0a-4dba-b6e9-e70dca77c880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9676b8bf4198f8be753b3788fcc6defdec2d6a1d8ad3ff3fed2f41da4f256554
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133643"
---
# <a name="simple-elements"></a>Einfache Elemente

Ein *einfaches Element* ist ein Benutzeroberflächenelement, das ein [**IAccessible-Objekt**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) mit anderen Elementen teilt und dieses **IAccessible-Objekt** (in der Regel sein übergeordnetes Objekt) verwendet, um seine Eigenschaften verfügbar zu machen. Um zwischen den Elementen zu unterscheiden, die ein **IAccessible-Objekt** gemeinsam nutzen, weist der Server jedem einfachen Element einen eindeutigen, positiven untergeordneten Bezeichner zu. Diese Zuweisung erfolgt pro Instanz der Schnittstelle, sodass die IDs innerhalb dieses Kontexts eindeutig sein müssen. Viele Implementierungen weisen diese IDs sequenziell zu, beginnend mit 1. Dieses Schema lässt nicht zu, dass einfache Elemente eigene elemente besitzen. Einfache Elemente werden auch als children *bezeichnet.*

Um eindeutig identifiziert und verfügbar gemacht zu werden, erfordert ein einfaches Element ein [**IAccessible-Objekt**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) und eine untergeordnete ID. Daher müssen die Clients bei der Kommunikation mit einem **IAccessible-Objekt** die entsprechende untergeordnete ID liefern. Ein spezieller Bezeichner, **CHILDID \_ SELF,** kann verwendet werden, um auf das barrierefreie Objekt selbst statt auf eines seiner untergeordneten Objekte zu verweisen.

Das [**IAccessible-Objekt,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) das von einfachen Elementen gemeinsam genutzt wird, entspricht häufig einem gemeinsamen übergeordneten Objekt in der Benutzeroberfläche. Beispielsweise machen Systemlistenfelder ein barrierefreies Objekt für das gesamte Listenfeld und einfache Elemente für jedes Listenfeldelement verfügbar. In diesem Fall ist das **IAccessible-Objekt** für das Listenfeld auch das übergeordnete Element oder der Container der Listenelemente.

Weitere Informationen zu barrierefreien Objekten finden Sie unter [Barrierefreie Objekte.](accessible-objects.md)

 

 




