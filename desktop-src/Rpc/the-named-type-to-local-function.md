---
title: Die named_type_to_local-Funktion
description: Die Stubdateien nennen den benannten \_ Typ \_ an die \_ lokale Funktion, um Daten von einem übertragenen Typ in den Typ zu konvertieren, den Sie für die Anwendung enthalten.
ms.assetid: c272cc1f-e47b-4d5a-a4e2-cefeaeb8c175
keywords:
- named_type_to_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746cbdd01ea657408b1bf355f41b3b9dfba673a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036961"
---
# <a name="the-named_type_to_local-function"></a>Der benannte \_ Typ \_ der \_ lokalen Funktion.

Die Stubdateien nennen den **benannten \_ Typ an die \_ \_ lokale** Funktion, um Daten von einem übertragenen Typ in den Typ zu konvertieren, den Sie für die Anwendung enthalten. Die-Funktion ist wie folgt definiert:

``` syntax
void __RPC_USER <named_type>_to_local( 
    <named_type> __RPC_FAR * _RPC_FAR * , 
    <local_type> __RPC_FAR * );
```

Der erste Parameter verweist auf die übertragenen Daten. Die-Funktion legt den zweiten Parameter fest, um auf die dargestellten Daten zu verweisen.

Der **benannte \_ Typ \_ der \_ lokalen** Funktion muss den Arbeitsspeicher für den dargestellten Typ verwalten. Die-Funktion muss für die gesamte Datenstruktur, die bei der durch den zweiten Parameter angegebenen Adresse beginnt, Arbeitsspeicher zuweisen, mit Ausnahme des-Parameters selbst (der Stub weist Speicher für den Stamm Knoten zu und übergibt ihn an die-Funktion). Der Wert des zweiten Parameters kann während des Aufrufes nicht geändert werden. Die Funktion kann den Inhalt an dieser Adresse ändern.

 

 




