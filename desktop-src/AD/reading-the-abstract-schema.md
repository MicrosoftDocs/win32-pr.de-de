---
title: Lesen des abstrakten Schemas
description: Dieses Thema enthält ein Codebeispiel und Richtlinien zum Lesen aus dem abstrakten Schema, das eine Teilmenge der Daten bereitstellt, die in den AttributeSchema- und classSchema-Objekten im Schemacontainer gespeichert sind.
ms.assetid: f31fc0ae-048f-413c-9370-96367dc68df8
ms.tgt_platform: multiple
keywords:
- 'Active Directory-Schema: Lesen des abstrakten Schemas'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7095dc4fb5ffe5f11f64781ecd423a60b3d434d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881302"
---
# <a name="reading-the-abstract-schema"></a>Lesen des abstrakten Schemas

Dieses Thema enthält ein Codebeispiel und Richtlinien zum Lesen aus dem abstrakten Schema, das eine Teilmenge der Daten bereitstellt, die in den **AttributeSchema-** und **classSchema-Objekten** im Schemacontainer gespeichert sind. Um Daten abzurufen, die im abstrakten Schema nicht verfügbar sind, lesen Sie die Daten direkt aus dem Schemacontainer, wie unter [Lesen von attributeSchema und classSchema Objects](reading-attributeschema-and-classschema-objects.md)beschrieben.

Verwenden Sie die Bindungszeichenfolge "LDAP://schema", um eine Bindung an einen [**IADsContainer-Zeiger**](/windows/desktop/api/iads/nn-iads-iadscontainer) im abstrakten Schema zu erstellen. Verwenden Sie diesen Zeiger, um die Klassen-, Attribut- und Syntaxeinträge im abstrakten Schema aufzuzählen. Sie können auch die [**IADsContainer.GetObject-Methode**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) verwenden, um einzelne Einträge abzurufen.


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



Verwenden Sie eine ähnliche Bindungszeichenfolge , "LDAP://schema/ &lt; &gt; Objekt", um eine direkte Bindung an eine Klasse oder einen Attributeintrag im abstrakten Schema zu erstellen. In dieser Zeichenfolge &lt; &gt; ist "object" der **lDAPDisplayName** einer Klasse oder eines Attributs. Für Klassen, die an die [**IADsClass-Schnittstelle**](/windows/desktop/api/iads/nn-iads-iadsclass) gebunden sind; binden Sie für Attribute an die [**IADsProperty-Schnittstelle.**](/windows/desktop/api/iads/nn-iads-iadsproperty)


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



Darüber hinaus stellt die [**IADs-Schnittstelle**](/windows/desktop/api/iads/nn-iads-iads) die [**IADs.Schema-Eigenschaft**](/windows/desktop/ADSI/iads-property-methods) bereit. Diese Eigenschaft gibt den ADsPath für die Objektklasse im Format der abstrakten Schemabindungszeichenfolge zurück. Wenn Sie über einen **IADs-Zeiger** auf ein Objekt verfügen, können Sie eine Bindung an seine Klasse im abstrakten Schema mithilfe des von **IADs.Schema** zurückgegebenen ADsPath-Objekts erstellen.

Für Klassen werden in der folgenden Tabelle die schlüsseleigenschaften aufgelistet, die vom abstrakten Schema bereitgestellt werden.



| Eigenschaft                                                             | Bedeutung                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IADsClass.Abstract**](/windows/desktop/ADSI/iadsclass-property-methods)            | Gibt an, ob dies eine abstrakte Klasse ist.                                                                                                                                                                                                                                            |
| [**IADsClass.Auxiliary**](/windows/desktop/ADSI/iadsclass-property-methods)           | Gibt an, ob dies eine Hilfsklasse ist.                                                                                                                                                                                                                                           |
| [**IADsClass.AuxDerivedFrom**](/windows/desktop/ADSI/iadsclass-property-methods)      | Array von Hilfsklassen, von der diese Klasse abgeleitet wird.                                                                                                                                                                                                                                     |
| [**IADsClass.Container**](/windows/desktop/ADSI/iadsclass-property-methods)           | Gibt an, ob Objekte dieser Klasse andere Objekte enthalten können. Dies ist true, wenn eine Klasse diese Klasse in ihre Liste der **möglichenSuperiors** einschließt.                                                                                                                                 |
| [**IADsClass.DerivedFrom**](/windows/desktop/ADSI/iadsclass-property-methods)         | Array von Klassen, von denen diese Klasse abgeleitet ist.                                                                                                                                                                                                                                       |
| [**IADsClass.MandatoryProperties**](/windows/desktop/ADSI/iadsclass-property-methods) | Ruft ein Array der obligatorischen Eigenschaften ab, die für eine Instanz der -Klasse festgelegt werden müssen. Die zurückgegebene Liste enthält alle **mustContain-** und **systemMustContain-Werte** für die Klasse und die Klassen, von denen sie abgeleitet wird, einschließlich Superklassen und Hilfsklassen. |
| [**IADsClass.OID**](/windows/desktop/ADSI/iadsclass-property-methods)                 | Ruft die governsID der -Klasse ab.                                                                                                                                                                                                                                                   |
| [**IADsClass.OptionalProperties**](/windows/desktop/ADSI/iadsclass-property-methods)  | Ruft ein Array der optionalen Eigenschaften ab, die für eine Instanz der -Klasse festgelegt werden können. Die zurückgegebene Liste enthält alle **mayContain-** und **systemMayContain-Werte** für die Klasse und die Klassen, von denen sie abgeleitet wird, einschließlich Superklassen und Hilfsklassen.   |
| [**IADsClass.PossibleSuperiors**](/windows/desktop/ADSI/iadsclass-property-methods)   | Ruft ein Array der **possibleSuperiors-Werte** für die -Klasse ab, das die Objektklassen angibt, die Objekte dieser Klasse enthalten können.                                                                                                                                        |



 

Das abstrakte Schema wird im **subSchema-Objekt** im Schemacontainer gespeichert. Um den Distinguished Name des **subSchema-Objekts** abzurufen, binden Sie an rootDSE, und lesen Sie das **subSchemaSubEntry-Attribut,** wie unter [Serverlose Bindung und RootDSE](serverless-binding-and-rootdse.md)beschrieben. Beachten Sie, dass es effizienter ist, das abstrakte Schema durch Binden an "LDAP://schema" zu lesen, als durch direktes Binden an das **subSchema-Objekt.**

 

 
