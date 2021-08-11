---
title: Zugreifen auf und Bearbeiten von Daten mit ADSI
description: Alle Objekte verfügen über Eigenschaften.
ms.assetid: 366a1fbc-3089-406a-9819-cf2ba7636c5f
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, Zugreifen auf und Bearbeiten von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ed09c1717f4f9a9c1c75372e7efdc23d2cce1adb39242197346061ae4df00f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181630"
---
# <a name="accessing-and-manipulating-data-with-adsi"></a>Zugreifen auf und Bearbeiten von Daten mit ADSI

Alle Objekte verfügen über Eigenschaften. Alle COM-Objekte (Active Directory Service Interface, ADSI) verfügen über eine oder mehrere Schnittstellen mit Methoden, die die Eigenschaften des Verzeichnisobjekts abrufen, das das COM-Objekt darstellt. Es gibt eine Reihe von Möglichkeiten zum Lesen von Eigenschaften aus einem Objekt:

-   Bestimmte Eigenschaft nach Namen erhalten: Die [**IADs-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iads) verfügt über zwei [**Methoden: IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) und [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) zum Lesen einer bestimmten Eigenschaft. Jedes ADSI COM-Objekt verfügt über eine **IADs-Schnittstelle.**
-   Rufen Sie eine angegebene Liste von Eigenschaften ab: Die [**IDirectoryObject-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) verfügt über die [**IDirectoryObject::GetObjectAttributes-Methode,**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) mit der Sie eine Liste angeben können, die die Namen der zu lesenden Eigenschaften enthält, und gibt ein Array von Strukturen zurück, die die angeforderten Eigenschaftswerte enthalten.
-   Auflisten aller Eigenschaften des Objekts: Mit der [**IADsPropertyList-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) können Sie alle Eigenschaften eines Objekts auflisten.
-   Spezielle Eigenschaften erhalten: Die Automatisierungsschnittstellen [**(IADs)**](/windows/desktop/api/Iads/nn-iads-iads)verfügen über Eigenschaftenmethoden, mit denen Sie spezielle Eigenschaften erhalten können, die \* nicht in einem -Objekt gespeichert sind. Oder mit den Eigenschaftenmethoden können Sie eine Objekteigenschaft in einem Datenformat erhalten, das sich vom tatsächlich gespeicherten Datentyp unterscheidet. Die **IADs-Schnittstelle** verfügt beispielsweise über Eigenschaftenmethoden wie [**IADs::get \_ Name,**](iads-property-methods.md)die den relativen Distinguished Name (RDN) eines Objekts abrufen. **IADs::get \_ Klasse**, die die Klasse eines Objekts abruft, und **IADs::get \_ Parent**, die den ADsPath zum übergeordneten Element des Objekts abruft.

MIT ADSI können Sie Eigenschaften lokal zwischenspeichern, nachdem sie vom Verzeichnisserver gelesen wurden. Auf diese Weise können Sie die Eigenschaften aus dem lokalen Eigenschaftencache lesen oder die Eigenschaften direkt vom Verzeichnisserver abrufen. ADSI verfügt auch über Methoden zum Aktualisieren des Caches und gibt an, ob alle Eigenschaften für ein Objekt zwischengespeichert werden oder nur die von Ihnen angegebenen Eigenschaften.

Nachdem Sie eine Eigenschaft abgerufen haben, lesen Sie ihren Wert. Der Datentyp einer Eigenschaft hängt von der Definition der Eigenschaft (auch als Attribut bezeichnet) im Active Directory-Schema ab. Für jeden Eigenschaftstyp, der in Active Directory vorhanden sein kann, gibt es ein **attributeSchema-Objekt** im Active Directory-Schema. Ein **attributeSchema-Objekt** definiert die Merkmale des Attributs. Eines dieser Merkmale ist die Syntax des Attributs, die den Datentyp der Werte des Attributs bestimmt. Weitere Informationen finden Sie unter [Merkmale von Attributen](/windows/desktop/AD/characteristics-of-attributes) und [Syntaxes für Active Directory-Attribute.](/windows/desktop/AD/syntaxes-for-attributes-in-active-directory-domain-services)

Die Automatisierungsschnittstellen [**(IADs)**](/windows/desktop/api/Iads/nn-iads-iads)geben einen Eigenschaftswert als VARIANT oder einen Zeiger auf eine Automation-Schnittstelle in einem COM-Objekt zurück, das \* die Eigenschaft darstellt. [](/windows/win32/api/oaidl/ns-oaidl-variant) Die [**Schnittstellen IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) und [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) geben eine Eigenschaft als Zeiger auf eine Struktur zurück, die einen typierten Eigenschaftswert oder einen Zeiger auf eine Zeichenfolge von Bytes enthält. Darüber hinaus rufen **IDirectoryObject** und **IDirectorySearch** Eigenschaften direkt vom Verzeichnisserver ab, anstatt einen lokalen Eigenschaftencache zu verwenden.

In diesem Abschnitt werden die folgenden Themen beschrieben:

-   [Die IADs und IDirectoryObject-Schnittstellen](the-iads-and-idirectoryobject-interfaces.md)
-   [Zugreifen auf Attribute mit ADSI](accessing-attributes-with-adsi.md)
-   [Ändern von Attributen mit ADSI](modifying-attributes-with-adsi.md)
-   [Direkter Zugriff auf den Eigenschaftencache mit den IADsProperty-Schnittstellen](accessing-the-property-cache-directly-with-the-iadsproperty-interfaces.md)
-   [ADSI-Attributsyntax](adsi-attribute-syntax.md)

 

 