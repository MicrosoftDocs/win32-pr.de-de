---
title: Suchen einer Liste der abfragenden Attribute
description: Bei der Suche nach Objekten einer bestimmten Klasse sollten Vergleiche in Ihrem Suchfilter Attribute angeben, die tatsächlich für die Objekte dieser Klasse vorhanden sind.
ms.assetid: 19d52933-e4b0-414f-9785-871e624da07b
ms.tgt_platform: multiple
keywords:
- Suchen einer Liste von Attributen zum Abfragen von AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0edfee59c42a8cf07be05ab31e58c0298f7285c8a02de659257e3b3cd14bfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189190"
---
# <a name="finding-a-list-of-attributes-to-query"></a>Suchen einer Liste der abfragenden Attribute

Bei der Suche nach Objekten einer bestimmten Klasse sollten Vergleiche in Ihrem Suchfilter Attribute angeben, die tatsächlich für die Objekte dieser Klasse vorhanden sind. Um die Listenattribute für ein Objekt einer bestimmten Klasse abzurufen, binden Sie eine Bindung an diese Klasse im abstrakten Schema, und rufen Sie die [**Eigenschaften IADsClass.MandatoryProperties**](/windows/desktop/ADSI/iadsclass-property-methods) und **IADsClass.OptionalProperties** ab. Weitere Informationen finden Sie unter [Lesen des abstrakten Schemas.](reading-the-abstract-schema.md)

Darüber hinaus erben alle Objekte von der obersten abstrakten Klasse. Daher kann jedes **Attribut** oben für ein Beliebiges Objekt vorhanden sein, obwohl es nicht festgelegt werden kann.

Stellen Sie beim Durchsuchen des globalen Katalogs sicher, dass Sie Attribute im globalen Katalog angeben. Für Attribute, die im globalen Katalog enthalten sind, ist **isMemberOfPartialAttributeSet** für ihre **attributeSchema-Objekte** auf **TRUE** festgelegt. Beachten Sie, dass diese Daten im abstrakten Schema nicht verfügbar sind. liest es aus dem **attributeSchema-Objekt** im Schemacontainer.

Im globalen Katalog kann ein Backlinkattribut nur abgefragt werden, wenn beide der folgenden Bedingungen erfüllt sind: Erstens wird das Attribut für die Aufnahme in den globalen Katalog markiert. Zweitens wird der entsprechende Vorwärtslink auch für die Aufnahme in den globalen Katalog markiert. Dies gilt sowohl für Abfragefilter als auch für Abfrageergebnisse. Weitere Informationen finden Sie unter [Verknüpfte Attribute.](linked-attributes.md)

Darüber hinaus werden einige Attribute, die größtenteils auf dem Benutzerobjekt liegen, erstellt. Abfragefilter dürfen keine konstruierten Attribute enthalten. Konstruierte Attribute können in Abfragefiltern nicht ausgewertet werden. sie können jedoch in Abfrageergebnissen zurückgegeben werden. Dies gilt für alle Benennungskontexte und den globalen Katalog. Attribute, die erstellt werden, verfügen über **ADS \_ SYSTEMFLAG \_ ATTR \_ IS \_ CONSTRUCTED** (0x00000004) in der **systemFlags-Eigenschaft** für **ihre attributeSchema-Objekte.**

> [!Note]  
> Weitere Informationen zu vordefinierten Klassen und Attributen, die im System enthalten sind, finden Sie unter [Active Directory Domain Services Referenz.](active-directory-domain-services-reference.md) Auf diesen Seiten sind obligatorische und optionale Attribute der einzelnen Objektklassen aufgeführt. Bei Attributen gibt die Referenzseite an, ob das Attribut indiziert, konstruiert, verknüpft oder im globalen Katalog ist.

 

 

 