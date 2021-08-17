---
title: Name-Eigenschaft
description: Die Name-Eigenschaft ist eine Zeichenfolge, die von Clients zum Identifizieren, Suchen oder Ankündigen eines Objekts für den Benutzer verwendet wird. Alle -Objekte unterstützen die Name-Eigenschaft.
ms.assetid: 7533955a-9538-4ead-a6ca-f61dd1b4d5c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce046ef693e9e52323cdb7484bbdc291127b958d88857de6a8be4522b88e33de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133773"
---
# <a name="name-property"></a>Name-Eigenschaft

Die **Name-Eigenschaft** ist eine Zeichenfolge, die von Clients zum Identifizieren, Suchen oder Ankündigen eines Objekts für den Benutzer verwendet wird. Alle -Objekte unterstützen die **Name-Eigenschaft.**

Beispielsweise ist der Text auf einem Schaltflächen-Steuerelement sein Name, während der Name für ein Listenfeld oder Bearbeitungssteuerfeld der statische Text ist, der dem Steuerelement in der Tabulatorfolge unmittelbar voraus geht. Selbst Grafikobjekte, die keinen Namen anzeigen, stellen Text zur Verfügung, wenn sie nach der **Eigenschaft Name abgefragt** werden.

Die **Name-Eigenschaft** wird abgerufen, indem [**IAccessible::get \_ accName aufgerufen wird.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)

## <a name="selecting-names"></a>Auswählen von Namen

Der Name eines Objekts sollte intuitiv sein, damit Benutzer die Bedeutung oder den Zweck des Objekts verstehen. Außerdem sollte die **Name-Eigenschaft** relativ zu allen gleichgeordneten Objekten im übergeordneten Element eindeutig sein.

Die Navigation innerhalb von Tabellen stellt für einige Benutzer besonders schwierige Probleme vor. Daher sollten Serverentwickler Tabellenzellennamen so beschreibend wie möglich machen. Sie können z. B. einen Zellennamen erstellen, indem Sie die Namen der Zeile und Spalte kombinieren, die sie belegt, z. B. "A1". Im Allgemeinen ist es jedoch besser, aussagekräftigere Namen zu verwenden, z. B. "Nancy, February", wobei "Nancy" die aktuelle Zeile und "Februar" die aktuelle Spalte ist.

## <a name="delegating-requests"></a>Delegieren von Anforderungen

Wenn ein Objekt keinen Zugriff auf seine **Name-Eigenschaft** hat, delegiert es Anforderungen an das übergeordnete Element und identifiziert sich durch seine untergeordnete ID. Wenn ein Client z. B. die **Name-Eigenschaft** eines Bearbeitungssteuerfelds aufruft, delegiert das Bearbeitungssteuerzeichen die Abfrage an das übergeordnete Steuerelement, das den Wert des statischen Textsteuerfelds zurückgibt, das das Bearbeitungssteuerfeld bezeichnet.

 

 




