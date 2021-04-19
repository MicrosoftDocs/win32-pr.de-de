---
title: Einfache Elemente
description: Ein einfaches Element ist ein Benutzeroberflächen Element, das ein IAccessible-Objekt mit anderen Elementen gemeinsam nutzt und darauf basiert, dass dieses Objekt (in der Regel sein übergeordnetes Objekt) seine Eigenschaften verfügbar macht.
ms.assetid: 3f6bd992-4e0a-4dba-b6e9-e70dca77c880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f8cb00b19719a4a8779a61f37b079633ada40c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342084"
---
# <a name="simple-elements"></a>Einfache Elemente

Ein *einfaches Element* ist ein Benutzeroberflächen Element, das ein [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt mit anderen Elementen gemeinsam nutzt und darauf basiert, dass dieses Objekt (in der Regel sein übergeordnetes Objekt) seine **Eigenschaften verfügbar macht** . Um die Elemente zu unterscheiden, die ein **IAccessible** -Objekt gemeinsam nutzen, weist der Server jedem einfachen Element einen eindeutigen, positiven untergeordneten Bezeichner zu. Diese Zuweisung erfolgt auf der Basis einer Schnittstelle pro Instanz, sodass die IDs innerhalb dieses Kontexts eindeutig sein müssen. Viele Implementierungen weisen diese IDs sequenziell zu, beginnend mit 1. Mit diesem Schema können einfache Elemente keine eigenen Elemente besitzen. Einfache Elemente werden *auch als unter* geordnete Elemente bezeichnet.

Für ein einfaches Element, das eindeutig identifiziert und verfügbar gemacht werden muss, [**ist ein einfaches**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Element erforderlich Daher müssen die Clients bei der Kommunikation mit einem Objekt, das nicht **zugänglich** ist, die entsprechende untergeordnete ID angeben. Ein spezieller Bezeichner, " **childID \_ Self**", kann verwendet werden, um auf das barrierefreie Objekt selbst zu verweisen, statt eines seiner untergeordneten Elemente.

Das [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt, das von einfachen Elementen gemeinsam genutzt wird, entspricht häufig einem gemeinsamen übergeordneten Objekt in der Benutzeroberfläche. So machen z. b. System Listenfelder ein Barrierefreies Objekt für das allgemeine Listenfeld und einfache Elemente für jedes Listenfeld Element verfügbar. In diesem Fall ist das **IAccessible** -Objekt für das Listenfeld auch das übergeordnete Element oder der Container der Listenelemente.

Weitere Informationen zu zugänglichen Objekten finden Sie unter [barrierefreie Objekte](accessible-objects.md).

 

 




