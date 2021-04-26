---
description: Gibt einen Vorgang an, für den Code generiert werden soll.
ms.assetid: d198197e-d146-4f1b-99df-944822e83357
title: operation-Element
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c0e4562241f5f437554d0af28dc8bca482512ea
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994316"
---
# <a name="operation-element"></a>operation-Element

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
| [**subscriptionFunctionDeclarations**](subscriptionfunctiondeclarations.md)<br/>                 | Generiert Implementierungsdeklarationen für Subscribe/Unsubscribe-Proxyfunktionen für Porttypbenachrichtigungsvorgänge.<br/> <br/> |
| [**subscriptionIdlFunctionDeclarations**](subscriptionidlfunctiondeclarations.md)<br/>           | Generiert IDL-Deklarationen für Subscribe/Unsubscribe-Proxyfunktionen für Porttypbenachrichtigungsvorgänge.<br/> <br/>            |
| [**subscriptionProxyFunctionImplementations**](subscriptionproxyfunctionimplementations.md)<br/> | Generiert Implementierungen für Subscribe/Unsubscribe-Proxyfunktionen für Porttypbenachrichtigungsvorgänge.<br/> <br/>             |



## <a name="remarks"></a>Hinweise

Eine beliebige Anzahl von Vorgängen kann angegeben werden. Wenn keine Vorgänge angegeben werden, wird Code für alle Vorgänge in allen relevanten Porttypen generiert. Durch  die Verwendung des Vorgangselements werden die generierten Methoden auf die im Vorgang enthaltenen Methoden beschränkt.

Beispielsweise unterstützt ein Drucker diese Vorgänge unter anderem:

-   **PrintJobByPost**
-   **PrintJobByReference**
-   **CancelJob**
-   **GetJobElements**
-   **GetActiveJobs**
-   **GetJobHistory**
-   **SubscribeToPrinterConfigChange**
-   **UnsubscribeToPrinterConfigChange**

Das Codegenerierungsskript verwendet die [**idlFunctionDeclarations-Elemente**](idlfunctiondeclarations.md) wie folgt, um nur die Methoden im Zusammenhang mit den **Vorgängen PrintJobByPost** und **GetJobElements** zu enthalten:

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



 

 




