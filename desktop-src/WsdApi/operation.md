---
description: Gibt einen Vorgang an, für den Code generiert werden soll.
ms.assetid: d198197e-d146-4f1b-99df-944822e83357
title: Operation-Element
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdd8324553e046000f467c103afd6ac0464cbc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042050"
---
# <a name="operation-element"></a>Operation-Element

Gibt einen Vorgang an, für den Code generiert werden soll.

## <a name="usage"></a>Verbrauch

``` syntax
<operation/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                                                 | BESCHREIBUNG                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**functiondeklarationen**](functiondeclarations.md)<br/>                                         | Generiert Implementierungs Deklarationen für Proxy Funktionen für Porttyp Vorgänge.<br/> <br/>                                    |
| [**idlfunctiondeklarationen**](idlfunctiondeclarations.md)<br/>                                   | Generiert IDL-Deklarationen für Proxy Funktionen für Porttyp Vorgänge.<br/> <br/>                                               |
| [**messagestructuredefinitions**](messagestructuredefinitions.md)<br/>                           | Generiert C-Strukturdefinitionen für Nachrichten Typen.<br/> <br/>                                                                   |
| [**messagetypedeklarationen**](messagetypedeclarations.md)<br/>                                   | Generiert C-Konstante Deklarationen für XML-Schema Tabellen für Nachrichten Typen.<br/> <br/>                                             |
| [**messagetypedefinitions**](messagetypedefinitions.md)<br/>                                     | Generiert C-Konstanten für XML-Schema Tabellen für Nachrichten Typen.<br/> <br/>                                                         |
| [**porttypeer-Deklarationen**](porttypedeclarations.md)<br/>                                         | Generiert C-Konstante Deklarationen für Porttypen.<br/> <br/>                                                                      |
| [**porttypeer Definitionen**](porttypedefinitions.md)<br/>                                           | Generiert C-Konstanten für Porttypen.<br/> <br/>                                                                                  |
| [**proxyfunctionimplementierungen**](proxyfunctionimplementations.md)<br/>                         | Generiert Implementierungen für Proxy Funktionen für Porttyp Vorgänge.<br/> <br/>                                                |
| [**stubdeklarationen**](stubdeclarations.md)<br/>                                                 | Generiert Deklarationen für Stub-Funktionen für Porttyp Vorgänge.<br/> <br/>                                                    |
| [**stubdefinitionen**](stubdefinitions.md)<br/>                                                   | Generiert Implementierungen für Stub-Funktionen für Porttyp Vorgänge.<br/> <br/>                                                 |
| [**"abonnemenfunctiondeklarationen"**](subscriptionfunctiondeclarations.md)<br/>                 | Generiert Implementierungs Deklarationen für Abonnement-/abonnementproxyfunktionen für Porttyp-Benachrichtigungs Vorgänge.<br/> <br/> |
| [**"abonnemenidlfunctiondeklarationen"**](subscriptionidlfunctiondeclarations.md)<br/>           | Generiert IDL-Deklarationen für Abonnement-/abonnementproxyfunktionen für Port-Benachrichtigungs Vorgänge.<br/> <br/>            |
| [**abonnemenproxyfunctionimplementierungen**](subscriptionproxyfunctionimplementations.md)<br/> | Generiert Implementierungen für Abonnement-/Abonnement-Proxyfunktionen für Porttyp-Benachrichtigungs Vorgänge.<br/> <br/>             |



## <a name="remarks"></a>Bemerkungen

Es kann eine beliebige Anzahl von Vorgängen angegeben werden. Wenn keine Vorgänge angegeben werden, wird der Code für alle Vorgänge in allen relevanten Porttypen generiert. Wenn Sie das **Operation** -Element verwenden, werden die generierten Methoden auf die im-Vorgang enthaltenen Methoden beschränkt.

Ein Drucker unterstützt z. b. die folgenden Vorgänge:

-   **Printjobbypost**
-   **Printjobbyreference**
-   **CancelJob**
-   **Getjobelements**
-   **Getactivejobs**
-   **Getjobhistory**
-   **Abonniert.**
-   **Unabonniert betoprinterconfigchange**

Wenn Sie jedoch nur die Methoden im Zusammenhang mit den **printjobbypost** -und **getjobelements** -Vorgängen einschließen möchten, verwendet das Code Generierungs Skript die [**idlfunctionscripts**](idlfunctiondeclarations.md) -Elemente wie folgt:

``` syntax
<idlFunctionDeclarations>
    <operation>PrintJobByPost</operation>
    <operation>GetJobElements></operation>
</idlFunctionDeclarations>
```

Dadurch werden IDL-Funktions Deklarationen für alle Methoden generiert, die den beiden Vorgängen zugeordnet sind (z. b. **beginprintjobbypost**, **endprintjobbypost**, **begingetjobelements** und **endgetjobelements**).

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




