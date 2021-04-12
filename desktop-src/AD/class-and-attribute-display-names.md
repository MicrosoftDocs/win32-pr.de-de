---
title: Klassen-und Attribut anzeigen Amen
description: Dieses Thema enthält Informationen zu und Richtlinien für Klassen-und Attribut anzeigen Amen.
ms.assetid: c85905b2-ed8b-4032-8c54-fd4de8b34ecf
ms.tgt_platform: multiple
keywords:
- Anzeige Spezifizierer anzeigen, Klassen-und Attribut anzeigen Amen
- Klassen Anzeige Namen AD
- anzeigen amen des Attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d65cd6ac6fc3077ff0d2bba15ffa9904b147654
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472669"
---
# <a name="class-and-attribute-display-names"></a>Klassen-und Attribut anzeigen Amen

Der Anzeige Bezeichner für eine Objektklasse enthält die folgenden Attribute, die verwendet werden können, um die lokalisierten anzeigen Amen anzugeben, die in der Benutzeroberfläche für Objekte dieser Klasse verwendet werden:

-   Das **classdisplayname** -Attribut ist eine Einzelwert-Unicode-Zeichenfolge, die den Klassen anzeigen Amen angibt.
-   Das **attributeDisplayNames** -Attribut ist eine mehrwertige Eigenschaft, die die Namen angibt, die in der Benutzeroberfläche für Attribute der Objektklasse verwendet werden sollen.

Die **attributeDisplayNames** -Werte sind Unicode-Zeichen folgen. jedes Element besteht aus einem durch Trennzeichen getrennten namens paar:


```C++
<attribute name>,<display text>
```



In diesem Beispiel ist " &lt; Attribut Name &gt; " der **ldapDisplayName** des Attributs, und " &lt; Anzeige Text &gt; " ist der Text, der als Name dieses Attributs in der Benutzeroberfläche angezeigt werden soll.

## <a name="guidelines-for-class-and-attribute-display-names"></a>Richtlinien für Klassen-und Attribut anzeigen Amen

Da viele Lieferanten Klassen mit neuen Attributen erweitern oder vollständig neue Klassen erstellen können, ist es wichtig, dass die anzeigen amen der Klasse und des Attributs eindeutig sind und keine Konflikte verursachen.

Jeder Anbieter sollte dem Namen der Klassen Anzeige einen eindeutigen, auf dem Herstellernamen basierenden Bezeichner als Präfix voranstellen. Wenn z. b. das fiktive Unternehmen Fabrikam Inc. eine neue Klasse erstellt, die von der "Contact"-Klasse abgeleitet ist, können Sie einen eindeutigen Klassen anzeigen Amen mit dem Namen "Fabrikam Contact" aufweisen.

Wenn ein Anbieter eine vorhandene Klasse mit neuen Attributen erweitert, sollte der Anzeige Name des Attributs erneut eindeutig identifiziert werden, sodass keine Konflikte mit anderen Attribut anzeigen Amen auftreten. Auch hier empfiehlt es sich, den Attribut anzeigen Amen mit dem eindeutigen, auf dem Herstellernamen basierenden Bezeichner als präfixvorgang festzulegen. Wenn beispielsweise das Fabrikam-Unternehmen die User-Klasse mit einem neuen HR-Attribut erweitert, könnte es das Attribut eindeutig als "Fabrikam HR-Informationen" anzeigen.

Außerdem sollte jeder Anbieter aus Lokalisierungs Sicht die Klassen-und Attribut Anzeige Namen in jeder Sprache lokalisieren, die von Windows 2000 unterstützt wird.

## <a name="adding-a-value-to-the-attributedisplaynames-attribute"></a>Hinzufügen eines Werts zum attributeDisplayNames-Attribut

**So fügen Sie dem **attributeDisplayNames** -Attribut einen Name-Zuordnungswert hinzu**

1.  Bestimmen Sie, ob der Name Zuordnungswert für das Attribut vorhanden ist. Wenn ein Name für die Namenszuordnung ersetzt werden soll, löschen Sie zuerst den vorhandenen Wert, indem Sie die [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) -Methode verwenden, wobei der *lncontrolcode* -Parameter auf **ADS \_ Property \_ Delete** und der *vprop* -Parameter auf den zu entfernenden Wert festgelegt ist. Verwenden Sie nicht die **ADS- \_ Eigenschaft \_ Clear** oder **ADS \_ Property \_ Update** für *lncontrolcode*.
2.  Erstellen Sie die Zeichenfolge, die den anzeigen amen des Attributs darstellt. Ein Beispiel finden Sie im obigen Format.
3.  Verwenden Sie die [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) -Methode, bei der der *lncontrolcode* -Parameter auf **ADS- \_ Eigenschaft \_ Append** festgelegt ist, um den neuen Wert hinzuzufügen.
4.  Ruft [**IADs:: abtinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) auf, um die Änderungen im Verzeichnis zu übertragen.

Weitere Informationen zum Benennen neuer Klassen und Attribute finden Sie unter [Benennen von Attributen und Klassen](naming-attributes-and-classes.md).

 

 