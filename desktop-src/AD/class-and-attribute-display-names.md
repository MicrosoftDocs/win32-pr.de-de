---
title: Anzeigenamen für Klassen und Attribute
description: Dieses Thema enthält Informationen zu und Richtlinien für Klassen- und Attributanzeigenamen.
ms.assetid: c85905b2-ed8b-4032-8c54-fd4de8b34ecf
ms.tgt_platform: multiple
keywords:
- Anzeigespezifizierer AD, Klassen- und Attributanzeigenamen
- Anzeigenamen der Klasse AD
- Attributanzeigenamen AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213132acfa6463b1c1e8a7615f5d7f488e53edfcdf9b75f8df5759fcd0e4d398
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022591"
---
# <a name="class-and-attribute-display-names"></a>Anzeigenamen für Klassen und Attribute

Der Anzeigespezifizierer für eine Objektklasse enthält die folgenden Attribute, die verwendet werden können, um die lokalisierten Anzeigenamen anzugeben, die in der Benutzeroberfläche für Objekte dieser Klasse verwendet werden:

-   Das **classDisplayName-Attribut** ist eine Unicode-Zeichenfolge mit einem Wert, die den Anzeigenamen der Klasse angibt.
-   Das **attributeDisplayNames-Attribut** ist eine Mehrwerteigenschaft, die die Namen angibt, die in der Benutzeroberfläche für Attribute der Objektklasse verwendet werden sollen.

Die **attributeDisplayNames-Werte** sind Unicode-Zeichenfolgen. jedes Element besteht aus einem durch Trennzeichen getrennten Namenspaar:


```C++
<attribute name>,<display text>
```



In diesem Beispiel ist " &lt; Attributname &gt; " der **lDAPDisplayName** des Attributs, und " &lt; anzeigetext " ist der &gt; Text, der als Name dieses Attributs auf der Benutzeroberfläche angezeigt werden soll.

## <a name="guidelines-for-class-and-attribute-display-names"></a>Richtlinien für Klassen- und Attributanzeigenamen

Da viele Anbieter Klassen mit neuen Attributen erweitern oder völlig neue Klassen erstellen können, ist es wichtig, dass die Anzeigenamen der Klassen und Attribute eindeutig sind und keine Konflikte verursachen.

Jeder Anbieter sollte dem Klassenanzeigenamen einen eindeutigen Anzeigebezeichner basierend auf dem Herstellernamen voranstellen. Wenn beispielsweise das fiktive Unternehmen Fabrikam Inc. eine neue Klasse erstellt, die von der Klasse "contact" abgeleitet ist, kann es einen eindeutigen Klassenanzeigenamen "Fabrikam Contact" haben.

Wenn ein Anbieter eine vorhandene Klasse um neue Attribute erweitert, sollte er den Anzeigenamen des Attributs erneut eindeutig identifizieren, sodass keine Konflikte mit anderen Attributanzeigenamen auftreten. Auch hier ist es eine bewährte Methode, dem Anzeigenamen des Attributs einen eindeutigen Anzeigebezeichner basierend auf dem Herstellernamen voranstellen. Wenn beispielsweise das Fabrikam-Unternehmen die Benutzerklasse um ein neues HR-Attribut erweitert, kann das Attribut eindeutig als "Fabrikam HR Information" angezeigt werden.

Darüber hinaus sollte jeder Anbieter aus Lokalisierungssicht die Anzeigenamen der Klassen und Attribute in jede Sprache lokalisieren, die von Windows 2000 unterstützt wird.

## <a name="adding-a-value-to-the-attributedisplaynames-attribute"></a>Hinzufügen eines Werts zum AttributDisplayNames-Attribut

**So fügen Sie dem **attributDisplayNames-Attribut** einen Wert für die Namenszuordnung hinzu**

1.  Bestimmen Sie, ob der Wert für die Namenszuordnung für das Attribut vorhanden ist. Wenn ein Wert für die Namenszuordnung ersetzt werden soll, löschen Sie zuerst den vorhandenen Wert mithilfe der [**IADs::P utEx-Methode,**](/windows/desktop/api/iads/nf-iads-iads-putex) wobei der *lnControlCode-Parameter* auf **ADS PROPERTY \_ \_ DELETE** und der *vProp-Parameter* auf den zu entfernenden Wert festgelegt ist. Verwenden Sie ADS **\_ PROPERTY \_ CLEAR** oder **ADS PROPERTY \_ \_ UPDATE** nicht für *lnControlCode*.
2.  Erstellen Sie die Zeichenfolge, die den Anzeigenamen des Attributs darstellt. Ein Beispiel finden Sie im obigen Format.
3.  Verwenden Sie die [**IADs::P utEx-Methode,**](/windows/desktop/api/iads/nf-iads-iads-putex) wobei der *lnControlCode-Parameter* auf **ADS PROPERTY \_ \_ APPEND** festgelegt ist, um den neuen Wert hinzuzufügen.
4.  Rufen Sie [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) auf, um die Änderungen an das Verzeichnis zu committen.

Weitere Informationen zum Benennen neuer Klassen und Attribute finden Sie unter [Benennen von Attributen und Klassen.](naming-attributes-and-classes.md)

 

 