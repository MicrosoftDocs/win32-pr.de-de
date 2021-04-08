---
title: Lesen des abstrakten Schemas
description: Dieses Thema enthält ein Codebeispiel und Richtlinien zum Lesen aus dem abstrakten Schema, das eine Teilmenge der Daten bereitstellt, die in den attributeSchema-und classSchema-Objekten im Schema Container gespeichert sind.
ms.assetid: f31fc0ae-048f-413c-9370-96367dc68df8
ms.tgt_platform: multiple
keywords:
- Schema Active Directory, Lesen des abstrakten Schemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d7fadba33bcc5e93bf2b9e89934e8b440d559b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858123"
---
# <a name="reading-the-abstract-schema"></a>Lesen des abstrakten Schemas

Dieses Thema enthält ein Codebeispiel und Richtlinien zum Lesen aus dem abstrakten Schema, das eine Teilmenge der Daten bereitstellt, die in den **attributeSchema** -und **classSchema** -Objekten im Schema Container gespeichert sind. Zum Abrufen von Daten, die im abstrakten Schema nicht verfügbar sind, lesen Sie die Daten direkt aus dem Schema Container, wie unter [Lesen von attributeSchema-und classSchema-Objekten](reading-attributeschema-and-classschema-objects.md)beschrieben.

Verwenden Sie die Bindungs Zeichenfolge "LDAP://Schema", um eine Bindung an einen [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Zeiger auf das abstrakte Schema herzustellen. Verwenden Sie diesen Zeiger, um die Klassen-, Attribut-und Syntax Einträge im abstrakten Schema aufzuzählen. Sie können auch die [**IADsContainer. GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) -Methode verwenden, um einzelne Einträge abzurufen.


```C++
// Bind to the abstract schema.
IADsContainer *pAbsSchema = NULL;
hr = ADsGetObject(L"LDAP://schema",
                  IID_IADsContainer,
                  (void**)&pAbsSchema);
```




```VB
' Bind to the abstract schema.
Dim adschema As IADsContainer
Set adschema = GetObject("LDAP://schema")
```



Verwenden Sie eine ähnliche Bindungs Zeichenfolge ("LDAP://Schema/ <object> "), um direkt an einen Klassen-oder Attribut Eintrag im abstrakten Schema zu binden. In dieser Zeichenfolge &lt; ist "Object &gt; " der **ldapDisplayName** einer Klasse oder eines Attributs. Für Klassen, die an die [**iadsclass**](/windows/desktop/api/iads/nn-iads-iadsclass) -Schnittstelle gebunden sind; Binden Sie für Attribute an die [**iadsproperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) -Schnittstelle.


```C++
// Bind to the user class entry in the abstract schema.
IADsClass *pClass;
hr = ADsGetObject(L"LDAP://schema/user",
                  IID_IADsClass,
                  (void**)&pClass);
```




```VB
Bind to the user class entry in the abstract schema.
Dim userclass As IADsClass
Set userclass = GetObject("LDAP://schema/user")
```



Außerdem stellt die [**IADs**](/windows/desktop/api/iads/nn-iads-iads) -Schnittstelle die [**IADs. Schema**](/windows/desktop/ADSI/iads-property-methods) -Eigenschaft bereit. Diese Eigenschaft gibt den ADsPath für die Objektklasse im Format der abstrakten Schema Bindungs Zeichenfolge zurück. Wenn Sie einen **IADs** -Zeiger auf ein Objekt haben, können Sie mithilfe des von **IADs. Schema** zurückgegebenen ADsPath eine Bindung an die zugehörige Klasse im abstrakten Schema herstellen.

In der folgenden Tabelle sind die Schlüsseleigenschaften aufgeführt, die vom abstrakten Schema bereitgestellt werden.



| Eigenschaft                                                             | Bedeutung                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iadsclass. Abstract**](/windows/desktop/ADSI/iadsclass-property-methods)            | Gibt an, ob dies eine abstrakte Klasse ist.                                                                                                                                                                                                                                            |
| [**Iadsclass. hilfskit**](/windows/desktop/ADSI/iadsclass-property-methods)           | Gibt an, ob es sich um eine Hilfsklasse handelt.                                                                                                                                                                                                                                           |
| [**Iadsclass. auxderivedfrom**](/windows/desktop/ADSI/iadsclass-property-methods)      | Array von Hilfsklassen, von denen diese Klasse abgeleitet ist.                                                                                                                                                                                                                                     |
| [**Iadsclass. Container**](/windows/desktop/ADSI/iadsclass-property-methods)           | Gibt an, ob Objekte dieser Klasse andere-Objekte enthalten können, was true ist, wenn eine Klasse diese Klasse in der Liste der **possiblevorgesetzten** enthält.                                                                                                                                 |
| [**Iadsclass. derivedfrom**](/windows/desktop/ADSI/iadsclass-property-methods)         | Array von Klassen, von denen diese Klasse abgeleitet ist.                                                                                                                                                                                                                                       |
| [**Iadsclass. MandatoryProperties**](/windows/desktop/ADSI/iadsclass-property-methods) | Ruft ein Array der obligatorischen Eigenschaften ab, die für eine Instanz der-Klasse festgelegt werden müssen. Die zurückgegebene Liste enthält alle Werte von **mustare** und **systemmustare** für die Klasse und die Klassen, von denen Sie abgeleitet wird, einschließlich übergeordneten Klassen und Hilfsklassen. |
| [**Iadsclass. Oid**](/windows/desktop/ADSI/iadsclass-property-methods)                 | Ruft die governsID der-Klasse ab.                                                                                                                                                                                                                                                   |
| [**Iadsclass. OptionalProperties**](/windows/desktop/ADSI/iadsclass-property-methods)  | Ruft ein Array der optionalen Eigenschaften ab, die möglicherweise für eine Instanz der-Klasse festgelegt werden. Die zurückgegebene Liste enthält alle Werte für " **mayincludes** " und " **systemmayare** " für die Klasse und die Klassen, von denen Sie abgeleitet wird, einschließlich übergeordneten Klassen und Hilfsklassen.   |
| [**Iadsclass. possiblevorgesetzten**](/windows/desktop/ADSI/iadsclass-property-methods)   | Ruft ein Array der **possibledie** -Werte für die-Klasse ab, die die Objektklassen angibt, die Objekte dieser Klasse enthalten können.                                                                                                                                        |



 

Das abstrakte Schema ist im Schema Container im **unter Schema** Objekt gespeichert. Um den Distinguished Name des **unter Schema** Objekts zu erhalten, binden Sie an RootDSE, und lesen Sie das **subschemasubentry** -Attribut, wie unter [Server lose Bindung und RootDSE](serverless-binding-and-rootdse.md)beschrieben. Beachten Sie, dass es effizienter ist, das abstrakte Schema durch Binden an "LDAP://Schema" zu lesen, als indem es direkt an das **unter Schema** Objekt gebunden wird.

 

 