---
title: Informationen zum Active Directory Schema
description: Jedes Objekt in Active Directory Domain Services ist eine Instanz einer Objektklasse, die im Active Directory Schema definiert ist.
ms.assetid: 8fc9cd2d-8fed-4fda-918c-79b01f9a19bb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f55513b359a7ef293b005d93a20ac43f470d515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855207"
---
# <a name="about-the-active-directory-schema"></a>Informationen zum Active Directory Schema

Jedes Objekt in Active Directory Domain Services ist eine Instanz einer Objektklasse, die im Active Directory Schema definiert ist. Eine Objektklasse stellt eine Kategorie von Objekten dar, wie z. B. Benutzer, Drucker oder Anwendungsprogramme, die gemeinsame Merkmale aufweisen. Die Definition für jede Objektklasse enthält eine Liste der Attribute, mit denen Instanzen der Klasse beschrieben werden können. Beispielsweise weist die Klasse Benutzer Attribute wie **givenName**, **surname** und **streetAddress** auf. Die Liste der Attribute für eine Klasse wird in diejenigen unterteilt, die ein Objekt dieser Klasse enthalten muss, sowie zusätzliche Attribute, die ein Objekt enthalten kann. Das Verzeichnis ist in einer Hierarchie angeordnet. die Definition jeder Klasse listet auch die Klassen auf, deren Objekte übergeordnete Elemente von Objekten einer bestimmten Klasse sein können – dies steuert die Form der Verzeichnishierarchie.

Das Schema definiert auch formal jedes Attribut. Die Definition für jedes Attribut umfasst eindeutige Bezeichner für das Attribut, die Syntax für das Attribut (d. h. den Datentyp für die Werte des Attributs), optionale Bereichs Begrenzungen für die Attributwerte, ob das Attribut nur einen Wert oder mehrere Werte aufweisen kann und ob das Attribut indiziert ist. Das Verzeichnisschema definiert jedes Attribut genau einmal, – Objektklassen Definitionen enthalten Verweise auf die Attribute, die im Schema definiert sind. Das Attribut "Description" wird beispielsweise nur einmal definiert, und es wird von vielen Objektklassen darauf verwiesen. Dies unterscheidet sich von einem relationalen Datenbankschema, bei dem die "Attribute" (Spalten) für jede Tabelle separat definiert werden.

 

 




