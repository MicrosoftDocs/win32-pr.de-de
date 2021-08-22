---
description: 'Eine Transaktion ist eine Gruppe von Vorgängen mit den folgenden Eigenschaften: atomisch, konsistent, isoliert und dauerhaft (ACID).'
ms.assetid: b3da52a3-1c52-4577-a997-7e72ebc03fa8
title: Was ist eine Transaktion?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f04a21eaec081a42e1cd4bcd60cb7cf48d609075eec772ed18fd41494c47d1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119289720"
---
# <a name="what-is-a-transaction"></a>Was ist eine Transaktion?

Eine Transaktion ist eine Gruppe von Vorgängen mit den folgenden Eigenschaften: atomisch, konsistent, isoliert und dauerhaft (ACID). Die Unterstützung von Transaktionen ermöglicht die Entwicklung neuer Anwendungstypen, vereinfacht den Entwicklungsprozess und macht die Anwendung stabiler. Der Rest dieses Themas enthält Szenarien, die die Notwendigkeit dieser Eigenschaften und dann eine Tabelle veranschaulichen, die jede Eigenschaft definiert.

In einer *atomaren* Gruppe von Vorgängen muss entweder jeder Vorgang in der Gruppe erfolgreich sein, oder die Auswirkungen aller Vorgänge müssen rückgängig gemacht werden (auch bekannt als Roll *back*). Bei einer Bankübertragung muss es sich z. B. um einen atomaren Satz von zwei Vorgängen (Eine Lastschrift von einem Konto und eine Gutschrift auf ein anderes Konto) richten. Debit- und Guthaben müssen als atomarer Gruppe implementiert werden. Wenn diese beiden Vorgänge nicht beide erfolgreich sind, wird die Übertragung entweder von der Bank oder dem Kontoinhaber als unlauter bezeichnet.

Die Anforderung der *Konsistenz bedeutet,* dass die Daten nach der Transaktion konsistent sind (vorausgesetzt, wir haben vor der Transaktion mit einem konsistenten System begonnen). Im Beispiel für die Bankübertragung kann Konsistenz so definiert werden, dass das kombinierte Kontoguthaben der beiden Konten konstant ist. Um Konsistenz im Bankübertragungsbeispiel zu implementieren, müssen die Debit- und Kreditvorgänge einfach für die gleiche Geldmenge verwendet werden.

Ein weiteres Beispiel für eine Transaktion ist ein Update einer Website. Eine E-Commerce-Website erfordert, dass eine neue Navigationsseite für die Produktkategorie genau zur gleichen Zeit wie die Produktdetailseiten angezeigt wird, die die neuen Produkte beschreiben. In diesem Fall ist es notwendig, mehrere Verzeichniseinträge unter der Kontrolle einer Transaktion zu aktualisieren und hinzuzufügen. Die Updates müssen nicht nur atomar sein, sondern es ist auch erforderlich, dass ein Kunde, der gerade einkauft, die Updates nicht sehen darf. Dies ist ein Beispiel für die *Isolationseigenschaft* von Transaktionen.

Die -Eigenschaft der *Dauerhaftigkeit* erfordert, dass die Auswirkungen nach Abschluss eines Updates auch dann beibehalten werden, wenn das System nicht mehr reagiert. Im vorherigen Beispiel kann die Dauerhaftigkeit einfach durch Sicherstellen einer angemessenen Datenwiederherstellung gewährleistet werden, sodass alle neuen Dateisystemeinträge, die das Hinzustellen eines neuen Produkts zum Standort darstellen, angezeigt werden, nachdem ein System nicht mehr reagiert. Dies erfordert ein System mit Datensicherungs-, Wiederherstellungs- und Hochverfügbarkeitsmechanismen.

Die Garantie der Atomarität einer Transaktion sowie der anderen Eigenschaften ist bei einer beliebigen Anzahl von Fehlern vorhanden, einschließlich Fehlern, die während der Wiederherstellungsphase eines vorherigen Fehlers auftreten. Schließlich erreicht das System einen von zwei Zuzuständen: Alle Vorgänge wurden angewendet, oder keiner der Vorgänge wurde angewendet.

Die Eigenschaften einer Transaktion sind in der folgenden Tabelle zusammengefasst.



| Begriff                                                                                                         | BESCHREIBUNG                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Atomic<br/>                 | Entweder sind alle Vorgänge in der Transaktion erfolgreich, oder keiner der Vorgänge wird beibehalten.<br/>                             |
| <span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Konsistent<br/> | Wenn die Daten vor Beginn der Transaktion konsistent sind, sind sie nach Abschluss der Transaktion konsistent.<br/> |
| <span id="Isolated_"></span><span id="isolated_"></span><span id="ISOLATED_"></span>Isoliert <br/>     | Die Auswirkungen einer Transaktion, die ausgeführt wird, werden von allen anderen Transaktionen ausgeblendet.<br/>                               |
| <span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Langlebig<br/>             | Wenn eine Transaktion abgeschlossen ist, sind die Ergebnisse persistent und bleiben nach einem Systemabsturz erhalten.<br/>                               |



 

Diese Eigenschaften stellen sicher, dass Software unerwartete Fehler behandeln kann, da sie eine Transaktion einfach abbrechen kann, wenn eine unerwartete Situation einen erfolgreichen Abschluss verhindert. Die Transaktionsinfrastruktur stellt sicher, dass für alle Auswirkungen der abgebrochenen Transaktion ein Rollback ausgeführt wird, und die Daten in einen konsistenten Zustand zurückgesetzt werden. Daher ermöglicht ein Transaktionssystem eine ordnungsgemäß wiederherstellung nach Systemfehlern.

Um die ACID-Eigenschaften zu gewährleisten, muss ein System, das Transaktionen unterstützt, über eine stabile Protokollierungsfunktion verfügen, die bei Bedarf zum Commit oder Rollback von Transaktionen verwendet werden kann. Weitere Informationen finden Sie unter [Gemeinsames Protokolldateisystem](/previous-versions/windows/desktop/clfs/common-log-file-system-portal).

 

