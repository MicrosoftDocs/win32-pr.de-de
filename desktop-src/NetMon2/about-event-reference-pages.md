---
description: Eine Ereignis Referenzseite (ERP) ist ein HTML-Dokument, das Netzwerkmonitor Informationen zu Ereignissen bereitstellt, die während des Experten-oder Monitor Vorgangs erkannt werden.
ms.assetid: 097bae90-5dab-4f79-a829-648033b38016
title: Informationen zu Ereignis Verweis Seiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e989e3e1d4ab0c41dc78c567c662e8a3090906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865468"
---
# <a name="about-event-reference-pages"></a>Informationen zu Ereignis Verweis Seiten

Eine Ereignis Referenzseite (ERP) ist ein HTML-Dokument, das Netzwerkmonitor Informationen zu Ereignissen bereitstellt, die während des Experten-oder Monitor Vorgangs erkannt werden.

Sie können Erps in der Ereignisanzeige Netzwerkmonitor, im Überwachungs Steuerungs Tool oder in einem beliebigen Browser anzeigen, der die HTML-Features von Microsoft Internet Explorer Version 4,01 oder höher unterstützt. Das heißt, Sie können Ihrer ERP unterstützte Steuerelemente oder Skriptsprachen hinzufügen.

Erps werden jedoch nur angezeigt, wenn der Experte das HTML-Dokument anhand des Namens bestimmt. Bei ordnungsgemäßer Festschreibung wird das ERP im unteren Bereich angezeigt, wenn das Ereignis im Ereignisanzeige ausgewählt ist. Die folgende Abbildung zeigt eine ERP, die dem IP-Bereichs Monitor (Internet Protocol) zugeordnet ist.

![ein ERP, das mit dem IP-Bereichs Monitor verknüpft ist](images/exview2.png)

## <a name="expert-events"></a>Expertenereignisse

Expertenereignisse werden vom **eventident** -Member einer [**nmeventdata**](nmeventdata.md) -Struktur identifiziert. Wenn Sie einen Experten schreiben, bestimmen Sie die **eventident** -Werte, die in der Regel 1, 2, 3 usw. lauten. Nehmen wir beispielsweise an, dass ein Experte zwei Ereignisse generiert (**EventIdent1** und **EventIdent2**). Wenn das Ereignisanzeige die Ereignisse separat anzeigen soll, müssen Sie zwei separate ERP-Dokumente erstellen.

 

 



