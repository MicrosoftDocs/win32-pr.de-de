---
description: Gibt den Porttyp an, für den Code generiert werden soll.
ms.assetid: 8a7762ae-2e39-46e1-b49f-09cae1af9b0d
title: portType-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a98f02fc5a18e330bb5617b52563adc79a039831
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996537"
---
# <a name="porttype-element"></a>portType-Element

Gibt den Porttyp an, für den Code generiert werden soll.

## <a name="usage"></a>Verbrauch

``` syntax
<portType/>
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
| [**subscriptionFunctionDeclarations**](subscriptionfunctiondeclarations.md)<br/>                 | Generiert Implementierungsdeklarationen für Abonnieren/Kündigen von Proxyfunktionen für Porttypbenachrichtigungsvorgänge.<br/> <br/> |
| [**subscriptionIdlFunctionDeclarations**](subscriptionidlfunctiondeclarations.md)<br/>           | Generiert IDL-Deklarationen für Abonnement-/Abonnementproxyfunktionen für Porttypbenachrichtigungsvorgänge.<br/> <br/>            |
| [**subscriptionProxyFunctionImplementations**](subscriptionproxyfunctionimplementations.md)<br/> | Generiert Implementierungen für Abonnieren/Kündigen von Proxyfunktionen für Benachrichtigungsvorgänge für Porttypen.<br/> <br/>             |



## <a name="remarks"></a>Hinweise

Standardmäßig wird Code für alle Porttypen in WSDL-Eingabedateien generiert.

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




