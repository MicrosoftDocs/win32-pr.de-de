---
title: Verzeichnis Definition
description: Die Beispiel Anbieter Komponente verwendet einen relativ einfachen Verzeichnis Entwurf, um die Beziehung zwischen den Komponenten zu verdeutlichen und die Mindestanforderungen anzuzeigen, die für einen ADSI-Anbieter erforderlich sind.
ms.assetid: d8dcd255-4a17-4c80-a749-61c1af605dba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6156f2e1ab89b34f009f1a86e5de011c20cf9503
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855324"
---
# <a name="directory-definition"></a>Verzeichnis Definition

Die Beispiel Anbieter Komponente verwendet einen relativ einfachen Verzeichnis Entwurf, um die Beziehung zwischen den Komponenten zu verdeutlichen und die Mindestanforderungen anzuzeigen, die für einen ADSI-Anbieter erforderlich sind.

Das "Verzeichnis" für die Beispiel Anbieter Komponente besteht aus zwei Stamm Knoten: "Seattle" und "Toronto". Seattle enthält zwei weitere Unterebenen: "Bellevue" und "Redmond". Jeder dieser Einträge enthält mehrere Benutzerkonten. Der Eintrag "Toronto" hat keine weiteren Unterebenen, sondern enthält direkt mehrere Benutzerkonten. In der folgenden Abbildung werden diese beiden Stamm Knoten angezeigt, die mit einem Netzwerk verbunden sind.

![Verzeichnis Definition](images/dssmdo.png)

Im hierarchischen Begriffen enthält der Namespace-Knoten "Seattle" und "Toronto". "Seattle" enthält "Bellevue" und "Redmond". "Bellevue" und "Redmond" enthalten jeweils eine Gruppe von Benutzerkonten. "Toronto" enthält direkt die Benutzerkonten ohne zwischengeschaltete Organisations Knoten.

Die Beispiel Anbieter Komponente stellt diese Struktur mit nur zwei Active Directory Objekttypen dar: ein Container Objekt und ein Blatt Objekt. "Seattle", "Toronto", "Bellevue" und "Redmond" sind Containerobjekte, und jedes Benutzerkonto ist ein Blatt Objekt.

Die Beispiel Anbieter Komponente erstellt eine Schema Klasse mit dem Namen "Organisationseinheit" für einen Container Objekttyp und eine Schema Klasse mit dem Namen "User" für ein Benutzerkonto.

Die Eigenschaften für jede Schema Klasse, ihre Methoden und die Regeln, die die Einschluss Beziehungen für diese Objekte steuern, sind alle in der [Schema Verwaltung](schema-management.md)definiert.

 

 




