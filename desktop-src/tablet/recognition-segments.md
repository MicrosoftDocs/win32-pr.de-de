---
description: Ein Erkennungs Segment ist die grundlegende frei Hand Einheit, die eine Erkennung intern verwendet, um ein Erkennungs Ergebnis für ein bestimmtes Ink-Objekt zu erhalten.
ms.assetid: 5215a0bd-6dff-4cda-b2e5-c54f64680e02
title: Erkennungs Segmente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7037849378477950b906b85efe6980c4246421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350112"
---
# <a name="recognition-segments"></a>Erkennungs Segmente

Ein Erkennungs Segment ist die grundlegende frei Hand Einheit, die eine Erkennung intern verwendet, um ein Erkennungs Ergebnis für ein bestimmtes Ink-Objekt zu erhalten. Ein Erkennungs Segment ist eine Auflistung von Hand Strichen. Beispielsweise kann ein Erkennungs Modul, das eine englische, kursive Handschrift erkennen kann, ein Wort als grundlegendes Erkennungs Segment verwenden.

Andere Erkennungs Tools können Teile von zusammengesetzten Wörtern als einfache Segmente verwenden. In Spanisch werden z. b. kurze Wörter häufig kombiniert, um längere zusammengesetzte Wörter bereitzustellen. "Damelo" ist ein spanisches Wort, das aus drei Wörtern besteht ("da bin Lo"), aber als einzelnes Wort geschrieben wird. Ein spanischer Erkennungs Modul könnte jedes Teilwort als Segment erkennen.

Eine Erkennung kann verschiedene Möglichkeiten finden, ein Ink-Beispiel in Erkennungs Segmente zu unterteilen. Da Mehrdeutigkeit an der Erkennung der beabsichtigten Eingabe des Benutzers beteiligt ist, kann die Erkennung viele alternative Übereinstimmungen zurückgeben.

Weitere Informationen zu Alternativen finden Sie unter [Alternativen](alternates.md).

 

 



