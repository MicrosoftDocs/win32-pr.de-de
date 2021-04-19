---
title: Zugreifen auf und Bearbeiten von Daten mit ADSI
description: Alle Objekte verfügen über Eigenschaften.
ms.assetid: 366a1fbc-3089-406a-9819-cf2ba7636c5f
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, zugreifen auf und Bearbeiten von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3291db7490c79aae6363f619582ed24339fb83d
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106341963"
---
# <a name="accessing-and-manipulating-data-with-adsi"></a>Zugreifen auf und Bearbeiten von Daten mit ADSI

Alle Objekte verfügen über Eigenschaften. Alle Active Directory Service Interface (ADSI) com-Objekte verfügen über eine oder mehrere Schnittstellen mit Methoden, die die Eigenschaften des Verzeichnis Objekts abrufen, das das COM-Objekt darstellt. Es gibt verschiedene Möglichkeiten, Eigenschaften aus einem Objekt zu lesen:

-   Eine bestimmte Eigenschaft nach Namen erhalten: die [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle verfügt über zwei Methoden [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) und [**IADs:: Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex) , um eine bestimmte Eigenschaft zu lesen. Jedes ADSI COM-Objekt verfügt über eine **IADs** -Schnittstelle.
-   Hiermit wird eine angegebene Liste von Eigenschaften angezeigt: die [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) -Schnittstelle verfügt über die [**IDirectoryObject:: getobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) -Methode, die es Ihnen ermöglicht, eine Liste mit den Namen der zu lesenden Eigenschaften anzugeben, und gibt ein Array von Strukturen zurück, das die angeforderten Eigenschaftswerte enthält.
-   Listet alle Eigenschaften für das Objekt auf: mit der [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) -Schnittstelle können Sie alle Eigenschaften eines Objekts aufzählen.
-   Spezielle Eigenschaften erhalten: die Automatisierungs Schnittstellen ([**IADs**](/windows/desktop/api/Iads/nn-iads-iads) \* ) verfügen über Eigenschaften Methoden, mit denen Sie spezielle Eigenschaften erhalten können, die nicht in einem Objekt gespeichert sind. Oder die-Eigenschaften Methoden ermöglichen es Ihnen, eine Objekt Eigenschaft in einem Datenformat zu erhalten, das vom tatsächlich gespeicherten Datentyp abweicht. Beispielsweise verfügt die **IADs** -Schnittstelle über Eigenschaften Methoden wie [**IADs:: get \_ Name**](iads-property-methods.md), die den relativen Distinguished Name (RDN) eines Objekts abruft. **IADs:: get \_ -Klasse**, die die Klasse eines Objekts abruft, und **IADs:: get \_ Parent**, wodurch der ADsPath zum übergeordneten Element des Objekts abgerufen wird.

ADSI ermöglicht es Ihnen, Eigenschaften lokal zwischenzuspeichern, nachdem Sie vom Verzeichnisserver gelesen wurden. Dies ermöglicht es Ihnen, die Eigenschaften aus dem lokalen Eigenschaften Cache zu lesen oder die Eigenschaften direkt vom Verzeichnisserver abzurufen. ADSI verfügt auch über Methoden zum Aktualisieren des Caches sowie für die Angabe, ob alle Eigenschaften für ein Objekt zwischengespeichert werden oder nur die von Ihnen angegebenen Eigenschaften.

Nachdem Sie eine Eigenschaft abgerufen haben, lesen Sie Ihren Wert. Der Datentyp einer Eigenschaft hängt von der Definition der Eigenschaft (auch als Attribut bezeichnet) im Active Directory Schema ab. Für jeden Eigenschaftentyp, der in Active Directory vorhanden sein kann, gibt es ein **attributeSchema** -Objekt im Active Directory Schema. Ein **attributeSchema** -Objekt definiert die Merkmale des Attributs. Eines dieser Merkmale ist die Syntax des Attributs, das den Datentyp der Werte des Attributs bestimmt. Weitere Informationen finden Sie unter [Merkmale von Attributen](/windows/desktop/AD/characteristics-of-attributes) und [Syntaxen für Active Directory Attribute](/windows/desktop/AD/syntaxes-for-attributes-in-active-directory-domain-services).

Die Automatisierungs Schnittstellen ([**IADs**](/windows/desktop/api/Iads/nn-iads-iads) \* ) geben einen Eigenschafts Wert als [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) oder einen Zeiger auf eine Automatisierungsschnittstelle für ein COM-Objekt zurück, das die Eigenschaft darstellt. Die [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) -Schnittstelle und die [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle geben eine Eigenschaft als Zeiger auf eine Struktur zurück, die einen typisierten Eigenschafts Wert oder einen Zeiger auf eine Zeichenfolge von Bytes enthält. Außerdem rufen **IDirectoryObject** und **IDirectorySearch** Eigenschaften direkt vom Verzeichnisserver ab, anstatt einen lokalen Eigenschafts Cache zu verwenden.

In diesem Abschnitt werden die folgenden Themen beschrieben:

-   [IADs und IDirectoryObject-Schnittstellen](the-iads-and-idirectoryobject-interfaces.md)
-   [Zugreifen auf Attribute mit ADSI](accessing-attributes-with-adsi.md)
-   [Ändern von Attributen mit ADSI](modifying-attributes-with-adsi.md)
-   [Direktes Zugreifen auf den Eigenschaften Cache mit den iadsproperty-Schnittstellen](accessing-the-property-cache-directly-with-the-iadsproperty-interfaces.md)
-   [ADSI-Attribut Syntax](adsi-attribute-syntax.md)

 

 