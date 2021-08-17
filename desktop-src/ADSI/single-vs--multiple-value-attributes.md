---
title: Einzelne und mehrere Wertattribute
description: Die Attribute, die in einem Verzeichnis vorhanden sein können, werden in der Regel im Schema für das Verzeichnis definiert.
ms.assetid: ea06ca66-6407-448f-8238-c8de5353663b
ms.tgt_platform: multiple
keywords:
- Adsi mit einzelnen und mehreren Wertattributen
- Adsi-Attribute, Attribute mit einem oder mehreren Werten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd9442a5365efbe343c2a9af74aa8576928e7a6a383cc131a3384152c2b1c0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119262030"
---
# <a name="single-vs-multiple-value-attributes"></a>Einzelne und mehrere Wertattribute

Die Attribute, die in einem Verzeichnis vorhanden sein können, werden in der Regel im Schema für das Verzeichnis definiert. Die Schemadefinition eines Attributs gibt eine Reihe von Merkmalen des Attributs an, z. B. den Datentyp und ob eine Instanz des Attributs mehrere Werte aufweisen kann.

Eine Instanz eines einwertigen Attributs kann einen einzelnen Wert enthalten. Eine Instanz eines mehrwertigen Attributs kann entweder einen einzelnen Wert oder mehrere Werte enthalten. Active Directory erstellt keine Attribute mit leeren Werten. Entweder enthält das Attribut einen gültigen Wert oder ist für das Objekt nicht vorhanden.

> [!Note]  
> In Active Directory und den meisten anderen LDAP-Servern ist die Reihenfolge der Werte in einem mehrwertigen Attribut nicht definiert. Außerdem muss jeder Wert eines mehrwertigen Attributs eindeutig sein.

 

ADSI lädt normalerweise Schemadaten, wenn Ihr Verzeichnis wie Active Directory ein Schema unterstützt. Da ADSI die Syntax von Attributen im Schema kennt, müssen Sie beim Zugriff darauf nicht den Attributtyp angeben. ADSI marshallt Attributwerte an den entsprechenden Datentyp, wie im Schema definiert.

Wenn Ihr Verzeichnis über kein Schema verfügt, geben Sie beim Zugriff auf ein Attribut den Datentyp an.

> [!Note]  
> Active Directory, Exchange, Windows NT 4.0 und Standortserver verfügen alle über ein Schema. Darüber hinaus verfügt Active Directory über ein erweiterbares Schema.

 

 

 




