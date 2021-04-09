---
title: Einzelne Attribute und Attribute mit mehreren Werten
description: Die Attribute, die in einem Verzeichnis vorhanden sein können, werden in der Regel im Schema für das Verzeichnis definiert.
ms.assetid: ea06ca66-6407-448f-8238-c8de5353663b
ms.tgt_platform: multiple
keywords:
- Einzel-und mehrfach Wert Attribute ADSI
- Attribute ADSI, Single-und Multiple Value-Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfabd985be3446e4f104d300d75f891ef0ce60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036299"
---
# <a name="single-vs-multiple-value-attributes"></a>Einzelne Attribute und Attribute mit mehreren Werten

Die Attribute, die in einem Verzeichnis vorhanden sein können, werden in der Regel im Schema für das Verzeichnis definiert. Die Schema Definition eines Attributs gibt eine Reihe von Merkmalen des Attributs an, z. b. den Datentyp und ob eine Instanz des Attributs mehrere Werte aufweisen kann.

Eine Instanz eines einwertigen Attributs kann einen einzelnen Wert enthalten. Eine Instanz eines mehrwertigen Attributs kann entweder einen einzelnen Wert oder mehrere Werte enthalten. Active Directory erstellt keine Attribute mit leeren Werten – entweder enthält das Attribut einen gültigen Wert oder ist im Objekt nicht vorhanden.

> [!Note]  
> In Active Directory und den meisten anderen LDAP-Servern ist die Reihenfolge der Werte in einem mehrwertigen Attribut nicht definiert. Außerdem muss jeder Wert eines mehrwertigen Attributs eindeutig sein.

 

ADSI lädt in der Regel Schema Daten, wenn Ihr Verzeichnis ein Schema unterstützt, wie Active Directory. Da ADSI die Syntax von Attributen im Schema kennt, ist es nicht erforderlich, den Attributtyp anzugeben, wenn darauf zugegriffen wird. ADSI Marshalls Attributwerte in den entsprechenden Datentyp, wie im Schema definiert.

Wenn Ihr Verzeichnis kein Schema aufweist, geben Sie den Datentyp an, wenn Sie auf ein Attribut zugreifen.

> [!Note]  
> Active Directory, Exchange, Windows NT 4,0 und der Standort Server verfügen alle über ein Schema. Außerdem verfügt Active Directory über ein erweiterbares Schema.

 

 

 




