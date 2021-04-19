---
title: Name-Eigenschaft
description: Die Name-Eigenschaft ist eine Zeichenfolge, die von Clients verwendet wird, um ein Objekt für den Benutzer zu identifizieren, zu suchen oder zu ankündigen. Alle-Objekte unterstützen die Name-Eigenschaft.
ms.assetid: 7533955a-9538-4ead-a6ca-f61dd1b4d5c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e93d8b90190f81179d681600f4b1bfacf4665e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339205"
---
# <a name="name-property"></a>Name-Eigenschaft

Die **Name** -Eigenschaft ist eine Zeichenfolge, die von Clients verwendet wird, um ein Objekt für den Benutzer zu identifizieren, zu suchen oder zu ankündigen. Alle-Objekte unterstützen die **Name** -Eigenschaft.

Der Text auf einem Schaltflächen-Steuerelement ist beispielsweise der Name, während der Name für ein Listenfeld oder Bearbeitungs Steuerelement der statische Text ist, der unmittelbar vor dem Steuerelement in der Tabstopp Reihenfolge steht. Auch Grafik Objekte, die keinen Namen anzeigen, stellen Text bereit, wenn die **Name** -Eigenschaft abgefragt wird.

Die **Name** -Eigenschaft wird durch Aufrufen von " [**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)" abgerufen.

## <a name="selecting-names"></a>Auswählen von Namen

Der Name eines Objekts sollte intuitiv sein, damit die Benutzer die Bedeutung oder den Zweck des Objekts verstehen. Außerdem sollte die **Name** -Eigenschaft in Bezug auf alle gleich geordneten Objekte im übergeordneten Element eindeutig sein.

Die Navigation innerhalb von Tabellen stellt für einige Benutzer besonders schwierige Probleme dar. Daher sollten Server Entwickler Tabellen Zell Namen so beschreibend wie möglich machen. Beispielsweise können Sie einen Zellnamen erstellen, indem Sie die Namen der Zeile und der Spalte, die Sie einnimmt, kombinieren, z. b. "a1". Es ist jedoch in der Regel besser, aussagekräftigeren Namen zu verwenden, wie z. b. "Nancy, Februar", wobei "Nancy" die aktuelle Zeile und "Februar" die aktuelle Spalte ist.

## <a name="delegating-requests"></a>Delegieren von Anforderungen

Wenn ein Objekt keinen Zugriff auf die **Name** -Eigenschaft hat, delegiert es Anforderungen an das übergeordnete Objekt und identifiziert sich selbst durch seine untergeordnete ID. Wenn ein Client z. b. die **Name** -Eigenschaft eines Bearbeitungs Steuer Elements aufruft, delegiert das Bearbeitungs Steuerelement die Abfrage an das übergeordnete Element, das den Wert des statischen Text Steuer Elements zurückgibt, das das Bearbeitungs Steuerelement bezeichnet.

 

 




