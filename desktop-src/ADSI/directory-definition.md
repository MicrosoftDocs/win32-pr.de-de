---
title: Verzeichnisdefinition
description: Die Beispielanbieterkomponente verwendet einen relativ einfachen Verzeichnisentwurf, um die Beziehung zwischen Komponenten zu verdeutlichen und die Mindestanforderungen anzuzeigen, die erforderlich sind, um ein ADSI-Anbieter zu sein.
ms.assetid: d8dcd255-4a17-4c80-a749-61c1af605dba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8a46ee47bfa280fb9cffce32480fdad3164a648eee59a0c0b2740834b1f21cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691948"
---
# <a name="directory-definition"></a>Verzeichnisdefinition

Die Beispielanbieterkomponente verwendet einen relativ einfachen Verzeichnisentwurf, um die Beziehung zwischen Komponenten zu verdeutlichen und die Mindestanforderungen anzuzeigen, die erforderlich sind, um ein ADSI-Anbieter zu sein.

Das "Verzeichnis" für die Beispielanbieterkomponente besteht aus zwei Stammknoten: "Seattle" und "Toronto". Seattle enthält zwei weitere Unterebenen: "Bellevue" und "Redmond". Jeder dieser Einträge enthält mehrere Benutzerkonten. Der Eintrag "Toronto" hat keine weiteren Unterebenen, enthält jedoch direkt mehrere Benutzerkonten. Die folgende Abbildung zeigt diese beiden Stammknoten, die mit einem Netzwerk verbunden sind.

![Verzeichnisdefinition](images/dssmdo.png)

In hierarchischer Hinsicht enthält der Namespaceknoten "Seattle" und "Toronto". "Seattle" enthält "Bellevue" und "Redmond". "Bellevue" und "Redmond" enthalten jeweils eine Reihe von Benutzerkonten. "Toronto" enthält direkt die Benutzerkonten ohne zwischengeschaltete Organisationsknoten.

Die Beispielanbieterkomponente stellt diese Struktur mit nur zwei Active Directory-Objekttypen dar: einem Containerobjekt und einem Blattobjekt. "Seattle", "Toronto", "Bellevue" und "Redmond" sind Containerobjekte, und jedes Benutzerkonto ist ein Blattobjekt.

Die Beispielanbieterkomponente erstellt eine Schemaklasse namens "Organisationseinheit" für einen Containerobjekttyp und eine Schemaklasse namens "User" für ein Benutzerkonto.

Die Eigenschaften für die einzelnen Schemaklassen, ihre Methoden und die Regeln, die die Containmentbeziehungen für diese Objekte steuern, werden alle in [schemaverwaltung definiert.](schema-management.md)

 

 




