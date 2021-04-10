---
title: Suchen nach einer Liste der abzufragende Attribute
description: Bei der Suche nach Objekten einer bestimmten Klasse sollten Vergleiche in Ihrem Suchfilter Attribute angeben, die tatsächlich für die Objekte dieser Klasse vorhanden sind.
ms.assetid: 19d52933-e4b0-414f-9785-871e624da07b
ms.tgt_platform: multiple
keywords:
- Suchen nach einer Liste von Attributen zum Abfragen von AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b6fb6b4d948a7cbc4d76caba9b78e189324eaa
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724513"
---
# <a name="finding-a-list-of-attributes-to-query"></a>Suchen nach einer Liste der abzufragende Attribute

Bei der Suche nach Objekten einer bestimmten Klasse sollten Vergleiche in Ihrem Suchfilter Attribute angeben, die tatsächlich für die Objekte dieser Klasse vorhanden sind. Um die Listen Attribute für ein Objekt einer bestimmten Klasse abzurufen, binden Sie diese Klasse im abstrakten Schema an, und rufen Sie die Eigenschaften [**iadsclass. MandatoryProperties**](/windows/desktop/ADSI/iadsclass-property-methods) und **iadsclass. OptionalProperties** ab. Weitere Informationen finden Sie unter [Lesen des abstrakten Schemas](reading-the-abstract-schema.md).

Außerdem erben alle Objekte von der obersten abstrakten Klasse. Daher kann jedes Attribut in **Top** vorhanden sein, auch wenn es für ein beliebiges Objekt nicht festgelegt werden kann.

Wenn Sie den globalen Katalog durchsuchen, stellen Sie sicher, dass Sie im globalen Katalog Attribute angeben. Bei Attributen, die im globalen Katalog enthalten sind, ist **ismembership ofpartialattributeset** für Ihre **attributeSchema** -Objekte auf **true** festgelegt. Beachten Sie, dass diese Daten im abstrakten Schema nicht verfügbar sind. Lesen Sie es aus dem **attributeSchema** -Objekt im Schema Container.

Im globalen Katalog kann ein Attribut für die Rück Verknüpfung nur abgefragt werden, wenn die beiden folgenden Bedingungen erfüllt sind: zuerst wird das Attribut für die Einbindung in den globalen Katalog markiert. Zweitens wird der entsprechende Forward-Link auch für die Einbindung in den globalen Katalog markiert. Dies gilt für Abfrage Filter und Abfrageergebnisse. Weitere Informationen finden Sie unter [verknüpfte Attribute](linked-attributes.md).

Außerdem werden einige Attribute, hauptsächlich für das Benutzerobjekt, erstellt. Abfrage Filter können keine konstruierten Attribute enthalten. Konstruierte Attribute können nicht in Abfrage filtern ausgewertet werden. Sie können jedoch in den Abfrage Ergebnissen zurückgegeben werden. Dies gilt für alle Namenskontexte und den globalen Katalog. Bei Attributen, die erstellt werden, **\_ wird ADS Systemflag \_ attr \_ \_** in der **systemFlags** -Eigenschaft für Ihre **attributeSchema** -Objekte erstellt (0x00000004).

> [!Note]  
> Weitere Informationen über vordefinierte Klassen und Attribute, die im System enthalten sind, finden Sie unter [Active Directory Domain Services Referenz](active-directory-domain-services-reference.md). Auf diesen Seiten sind obligatorische und optionale Attribute der einzelnen Objektklassen aufgeführt. Bei Attributen gibt die Verweisseite an, ob das Attribut indiziert, erstellt, verknüpft oder im globalen Katalog erstellt wird.

 

 

 