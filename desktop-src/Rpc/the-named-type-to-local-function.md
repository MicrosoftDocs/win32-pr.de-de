---
title: Die named_type_to_local-Funktion
description: Die Stubs rufen den benannten Typ in die lokale Funktion auf, um Daten von einem übertragenen Typ in den Typ zu konvertieren, den \_ \_ sie der Anwendung \_ präsentieren.
ms.assetid: c272cc1f-e47b-4d5a-a4e2-cefeaeb8c175
keywords:
- named_type_to_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59fc1d45545c920ef19eb4c230045e62322833d3ef38e765357c29b20a48589c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924060"
---
# <a name="the-named_type_to_local-function"></a>Der benannte \_ Typ für die lokale \_ \_ Funktion

Die Stubs rufen den benannten Typ in die lokale **\_ \_ \_ Funktion** auf, um Daten von einem übertragenen Typ in den Typ zu konvertieren, den sie der Anwendung präsentieren. Die Funktion ist wie die folgenden definiert:

``` syntax
void __RPC_USER <named_type>_to_local( 
    <named_type> __RPC_FAR * _RPC_FAR * , 
    <local_type> __RPC_FAR * );
```

Der erste Parameter verweist auf die übertragenen Daten. Die Funktion legt den zweiten Parameter so fest, dass er auf die dargestellten Daten zeigen soll.

Der **benannte Typ der lokalen \_ \_ \_ Funktion** muss den Arbeitsspeicher für den dargestellten Typ verwalten. Die Funktion muss Arbeitsspeicher für die gesamte Datenstruktur zuordnen, die an der durch den zweiten Parameter angegebenen Adresse beginnt, mit Ausnahme des Parameters selbst (der Stub weist Arbeitsspeicher für den Stammknoten zu und übergibt ihn an die Funktion). Der Wert des zweiten Parameters kann sich während des Aufrufs nicht ändern. Die Funktion kann den Inhalt an dieser Adresse ändern.

 

 




