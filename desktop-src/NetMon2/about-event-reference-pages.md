---
description: Eine Ereignisreferenzseite (EVENT Reference Page, ERP) ist ein HTML-Dokument, das Netzwerkmonitor Informationen zu Ereignissen bereitstellt, die während des Experten- oder Überwachungsvorgangs erkannt wurden.
ms.assetid: 097bae90-5dab-4f79-a829-648033b38016
title: Informationen zu Ereignisverweisseiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f277e2fc31050c5702c1f3cbb3a9b188515386f0b30522fd511771c0b9f3a69e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744870"
---
# <a name="about-event-reference-pages"></a>Informationen zu Ereignisverweisseiten

Eine Ereignisreferenzseite (EVENT Reference Page, ERP) ist ein HTML-Dokument, das Netzwerkmonitor Informationen zu Ereignissen bereitstellt, die während des Experten- oder Überwachungsvorgangs erkannt wurden.

Sie können ERPs in der Ereignisanzeige von Netzwerkmonitor, Monitor Control Tool oder in einem beliebigen Browser anzeigen, der die HTML-Features von Microsoft Internet Explorer Version 4.01 oder höher unterstützt. Das heißt, Sie können Ihrem ERP unterstützte Steuerelemente oder Skriptsprachen hinzufügen.

ERPs werden jedoch nur angezeigt, wenn der Experte das HTML-Dokument anhand des Namens bestimmt. Wenn das ERP ordnungsgemäß festgelegt ist, wird es im unteren Bereich angezeigt, wenn das Ereignis im Ereignisanzeige ausgewählt ist. Die folgende Abbildung zeigt ein ERP, das dem Ip-Bereichsmonitor (Internet Protocol) zugeordnet ist.

![ein ERP, das dem IP-Adressbereichsmonitor zugeordnet ist](images/exview2.png)

## <a name="expert-events"></a>Expertenereignisse

Expertenereignisse werden durch das **EventIdent-Element** einer [**NMEVENTDATA-Struktur**](nmeventdata.md) identifiziert. Wenn Sie einen Experten schreiben, bestimmen Sie die **EventIdent-Werte,** die in der Regel mit 1, 2, 3 usw. nummeriert sind. Angenommen, ein Experte generiert zwei Ereignisse (**EventIdent1** und **EventIdent2**). Wenn die Ereignisanzeige die Ereignisse separat anzeigen soll, müssen Sie zwei separate ERP-Dokumente erstellen.

 

 



