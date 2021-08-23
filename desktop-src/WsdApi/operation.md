---
description: Gibt einen Vorgang an, für den Code generiert werden soll.
ms.assetid: d198197e-d146-4f1b-99df-944822e83357
title: operation-Element
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab38721d1eb0d32c2ed7209dde872a83b29a523942ac7b91ca76f479ce5d51d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502190"
---
# <a name="operation-element"></a>operation-Element

Gibt einen Vorgang an, für den Code generiert werden soll.

## <a name="usage"></a>Verwendung

``` syntax
<operation/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                                                 | Beschreibung                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**functionDeclarations**](functiondeclarations.md)<br/>                                         | Generiert Implementierungsdeklarationen für Proxyfunktionen für Porttypvorgänge.<br/> <br/>                                    |
| [**idlFunctionDeclarations**](idlfunctiondeclarations.md)<br/>                                   | Generiert IDL-Deklarationen für Proxyfunktionen für Porttypvorgänge.<br/> <br/>                                               |
| [**messageStructureDefinitions**](messagestructuredefinitions.md)<br/>                           | Generiert C-Strukturdefinitionen für Nachrichtentypen.<br/> <br/>                                                                   |
| [**messageTypeDeclarations**](messagetypedeclarations.md)<br/>                                   | Generiert C-Konstantendeklarationen für XML-Schematabellen für Nachrichtentypen.<br/> <br/>                                             |
| [**messageTypeDefinitions**](messagetypedefinitions.md)<br/>                                     | Generiert C-Konstanten für XML-Schematabellen für Nachrichtentypen.<br/> <br/>                                                         |
| [**portTypeDeclarations**](porttypedeclarations.md)<br/>                                         | Generiert C-Konstantendeklarationen für Porttypen.<br/> <br/>                                                                      |
| [**portTypeDefinitions**](porttypedefinitions.md)<br/>                                           | Generiert C-Konstanten für Porttypen.<br/> <br/>                                                                                  |
| [**proxyFunctionImplementations**](proxyfunctionimplementations.md)<br/>                         | Generiert Implementierungen für Proxyfunktionen für Porttypvorgänge.<br/> <br/>                                                |
| [**stubDeclarations**](stubdeclarations.md)<br/>                                                 | Generiert Deklarationen für Stubfunktionen für Porttypvorgänge.<br/> <br/>                                                    |
| [**stubDefinitions**](stubdefinitions.md)<br/>                                                   | Generiert Implementierungen für Stubfunktionen für Porttypvorgänge.<br/> <br/>                                                 |
| [**subscriptionFunctionDeclarations**](subscriptionfunctiondeclarations.md)<br/>                 | Generiert Implementierungsdeklarationen für Abonnieren/Kündigen von Proxyfunktionen für Porttypbenachrichtigungsvorgänge.<br/> <br/> |
| [**subscriptionIdlFunctionDeclarations**](subscriptionidlfunctiondeclarations.md)<br/>           | Generiert IDL-Deklarationen für Abonnement-/Abonnementproxyfunktionen für Porttypbenachrichtigungsvorgänge.<br/> <br/>            |
| [**subscriptionProxyFunctionImplementations**](subscriptionproxyfunctionimplementations.md)<br/> | Generiert Implementierungen für Abonnieren/Kündigen von Proxyfunktionen für Benachrichtigungsvorgänge für Porttypen.<br/> <br/>             |



## <a name="remarks"></a>Hinweise

Es kann eine beliebige Anzahl von Vorgängen angegeben werden. Wenn keine Vorgänge angegeben werden, wird Code für alle Vorgänge in allen relevanten Porttypen generiert. Die Verwendung **des Vorgangselements** schränkt die generierten Methoden auf die im Vorgang enthaltenen Methoden ein.

Beispielsweise unterstützt ein Drucker diese Vorgänge unter anderem:

-   **PrintJobByPost**
-   **PrintJobByReference**
-   **CancelJob**
-   **GetJobElements**
-   **GetActiveJobs**
-   **GetJobHistory**
-   **SubscribeToPrinterConfigChange**
-   **UnsubscribeToPrinterConfigChange**

Um jedoch nur die Methoden zu verwenden, die sich auf die **Vorgänge PrintJobByPost** und **GetJobElements** bezieht, verwendet das Codegenerierungsskript die [**idlFunctionDeclarations-Elemente**](idlfunctiondeclarations.md) wie folgt:

``` syntax
<idlFunctionDeclarations>
    <operation>PrintJobByPost</operation>
    <operation>GetJobElements></operation>
</idlFunctionDeclarations>
```

Dadurch werden idl-Funktionsdeklarationen für alle Methoden generiert, die den beiden Vorgängen zugeordnet sind (z. B. **BeginPrintJobByPost,** **EndPrintJobByPost,** **BeginGetJobElements** und **EndGetJobElements).**

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




