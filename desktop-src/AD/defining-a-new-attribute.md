---
title: Definieren eines neuen Attributs
description: In diesem Thema wird gezeigt, wie Sie ein neues Attribut definieren, wenn Sie das Active Directory Schema erweitern.
ms.assetid: b8ac69ba-3b75-4e55-bf80-dabf2e80288a
ms.tgt_platform: multiple
keywords:
- Definieren eines neuen Attribut AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9da1a0a003d92fe09f27043098cb1abc4387b81e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101459"
---
# <a name="defining-a-new-attribute"></a>Definieren eines neuen Attributs

In diesem Thema wird gezeigt, wie Sie ein neues Attribut definieren, wenn Sie das Active Directory Schema erweitern.

Beachten Sie beim Definieren eines neuen Attributs Folgendes:

-   Verwenden Sie nach Möglichkeit vorhandene Attribute.
-   Verwenden Sie immer die **CN** ("Common Name")-Eigenschaft als Benennungs Attribut (Relative Distinguished Name). Dies ist die Standardeinstellung für die meisten Klassen, einschließlich derjenigen, die direkt von oben abgeleitet werden. Die **CN** -Eigenschaft ist eine indizierte Eigenschaft und macht das Suchen nach Objekten nach Namen effizienter.
-   Das Speichern und Abrufen großer Attribute mit mehreren Werten ist aufwendig und sollte vermieden werden. Active Directory Domain Services eine LDAP-Erweiterung implementieren, um das inkrementelle Lesen von großen Eigenschaften mit mehreren Werten zu ermöglichen, aber nicht alle LDAP-Clients erkennen diese Erweiterung.
-   Beachten Sie, dass Attribute flach sind, d. h., es gibt keine implizite Unterstruktur zu einem Attribut. Alle Attribute in einer bestimmten Klasse sollten direkt mit Instanzen dieser Klasse in Beziehung stehen.

## <a name="creating-a-new-attribute"></a>Erstellen eines neuen Attributs

So erstellen Sie ein neues Attribut:

-   Wählen Sie einen Namen für das Attribut aus. Der Name wird in den Attributen **CN** und **ldapDisplayName** enthalten sein. Weitere Informationen zum Erstellen eines Namens für ein neues Attribut finden Sie unter [Benennen von Attributen und Klassen](naming-attributes-and-classes.md).
-   Abrufen eines Objekt Bezeichners (OID) für das Attribut. Weitere Informationen finden Sie unter Abrufen [eines Stamm Objekt Bezeichners](obtaining-an-object-identifier.md).
-   Wählen Sie eine Syntax für das Attribut aus. Die Syntax wird durch die Kombination der Attribute **oMSyntax** und **oMObjectClass** bestimmt. Weitere Informationen finden Sie unter [Auswählen einer Syntax](choosing-a-syntax.md).
-   Entscheiden Sie, ob das Attribut ein-oder mehr wertig ist. Das **issinglewert** -Attribut bestimmt, ob das Attribut ein-oder mehr wertig ist.
-   Entscheiden Sie, ob das Attribut standardmäßig indiziert werden soll. Weitere Informationen finden Sie unter [indizierte Attribute](indexed-attributes.md).
-   Entscheiden Sie, ob das Attribut standardmäßig im globalen Katalog vorliegen soll. Weitere Informationen finden Sie unter [Attribute, die im globalen Katalog enthalten](attributes-included-in-the-global-catalog.md)sind.
-   Wenn das Attribut eine ganze Zahl oder eine Zeichenfolge ist, entscheiden Sie, ob ein Bereichs Limit erforderlich ist. Das **rangeLower** -Attribut und das **rangeUpper** -Attribut werden verwendet, um das Bereichs Limit anzugeben.
-   Wenn das Attribut DN-wertig ist, entscheiden Sie, ob das Attribut mit einem anderen Attribut verknüpft werden soll. Wenn dies der Fall ist, muss das [**linkid**](/windows/desktop/ADSchema/a-linkid) -Attribut für jedes Attribut entsprechend festgelegt werden. bei einem Attribut muss es sich um einen vorwärts Link handeln, der andere einen Backlink. Weitere Informationen zu verknüpften Attributen finden Sie unter [verknüpfte Attribute](linked-attributes.md).
-   Erstellen Sie ein neues **attributeSchema** -Objekt im Schema Container, und legen Sie die entsprechenden Attribute für das Objekt fest. Es gibt eine große Anzahl von Attributen, die für ein **attributeSchema** -Objekt festgelegt werden können, aber die in der folgenden Tabelle aufgeführten Attribute sind wichtig für die Definition eines neuen Attributs. Die Werte dieser Attribute werden durch die vorherigen Schritte bestimmt. Weitere Informationen zu diesen Attributen finden Sie unter [Attribute von Attributen](characteristics-of-attributes.md).

    | Attribut                                    | Kommentar                                              |
    |----------------------------------------------|------------------------------------------------------|
    | **2.300**<br/>                            | Erforderlich.<br/>                                 |
    | **lDAPDisplayName**<br/>               | Erforderlich.<br/>                                 |
    | **adminDisplayName**<br/>              | Erforderlich.<br/>                                 |
    | **attributeSyntax**<br/>               | Erforderlich.<br/>                                 |
    | **oMSyntax**<br/>                      | Erforderlich.<br/>                                 |
    | **oMObjectClass**<br/>                 | Erforderlich.<br/>                                 |
    | **schemaIDGUID**<br/>                  | Erforderlich.<br/>                                 |
    | **AttributeID**<br/>                   | Erforderlich.<br/>                                 |
    | **isSingleValued**<br/>                | Erforderlich.<br/>                                 |
    | **searchFlags**<br/>                   | Erforderlich.<br/>                                 |
    | **isMemberOfPartialAttributeSet**<br/> | Erforderlich.<br/>                                 |
    | **rangeLower**<br/>                    | Dies ist optional.<br/>                                 |
    | **rangeUpper**<br/>                    | Dies ist optional.<br/>                                 |
    | **LinkId**<br/>                        | Dies ist optional. Für verknüpfte Attribute erforderlich.<br/> |
    | **Beschreibung**<br/>                   | Dies ist optional.<br/>                                 |

    

     

-   Commit für das neue **attributeSchema** -Objekt an den Schema Container übergeben.
-   Aktualisieren Sie ggf. den Schema Cache. Weitere Informationen finden Sie unter [Aktualisieren des Schema Caches](updating-the-schema-cache.md).

 

