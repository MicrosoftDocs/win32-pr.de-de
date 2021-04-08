---
description: 'Bei einer Transaktion handelt es sich um eine Gruppe von Vorgängen, die über die folgenden Eigenschaften verfügen: atomarisch, konsistent, isoliert und dauerhaft (ACID).'
ms.assetid: b3da52a3-1c52-4577-a997-7e72ebc03fa8
title: Was ist eine Transaktion?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c459462d3aee3d7eef556ce0951ede537e8109
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864564"
---
# <a name="what-is-a-transaction"></a>Was ist eine Transaktion?

Bei einer Transaktion handelt es sich um eine Gruppe von Vorgängen, die über die folgenden Eigenschaften verfügen: atomarisch, konsistent, isoliert und dauerhaft (ACID). Durch die Unterstützung von Transaktionen können neue Arten von Anwendungen entwickelt werden, die den Entwicklungsprozess vereinfachen und die Anwendung stabiler werden. Der Rest dieses Themas enthält Szenarios, in denen die Notwendigkeit dieser Eigenschaften veranschaulicht wird, und dann eine Tabelle, in der jede Eigenschaft definiert wird.

In einer *atomaren* Gruppe von Vorgängen muss entweder jeder Vorgang in der Gruppe erfolgreich ausgeführt werden, oder die Auswirkungen all dieser Vorgänge müssen rückgängig gemacht werden (auch als *Rollback* bezeichnet). Eine Bank Übertragung muss beispielsweise ein atomarischer Satz von zwei Vorgängen sein: ein Abgleich von einem Konto und eine Gutschrift für ein anderes Konto. Der Debit und das Guthaben müssen als atomarische Gruppe implementiert werden. Wenn diese beiden Vorgänge nicht beides erfolgreich sind, wird die Übertragung entweder von der Bank oder dem Kontoinhaber nicht durchgeführt.

Die *Konsistenz* Anforderung bedeutet, dass die Daten nach der Transaktion konsistent sind (vorausgesetzt, dass wir mit einem konsistenten System vor der Transaktion gestartet haben). Für das Beispiel "Bank Übertragung" kann die Konsistenz so definiert werden, dass der kombinierte Konto Saldo der beiden Konten eine Konstante ist. Um die Konsistenz im Beispiel der Bank Übertragung zu implementieren, müssen die Vorgänge "Debit" und "Credit" lediglich für die gleiche Menge an Geld erfolgen.

Ein weiteres Beispiel für eine Transaktion ist ein Update für eine Website. Für eine Electronic Commerce-Website ist es erforderlich, dass eine neue Navigationsseite der Produktkategorie genau zur gleichen Zeit wie die Produktdetailseiten angezeigt wird, die die neuen Produkte beschreiben. In diesem Fall müssen Sie unter Kontrolle einer Transaktion mehrere Verzeichniseinträge aktualisieren und hinzufügen. Es ist nicht nur erforderlich, dass die Updates atomarisch sind, aber es ist auch erforderlich, dass ein Kunde, der derzeit Einkäufe durchläuft, die laufenden Updates nicht sehen kann. Dies ist ein Beispiel für die *Isolations* Eigenschaft der Transaktionen.

Die Eigenschaft der *Dauerhaftigkeit* erfordert, dass nach Abschluss eines Updates die Auswirkungen weiterhin bestehen, auch wenn das System nicht mehr reagiert. Im vorherigen Beispiel kann die Dauerhaftigkeit einfach durch sicherstellen einer ausreichenden Datenwiederherstellung gewährleistet werden, sodass alle neuen Dateisystem Einträge, die das Hinzufügen eines neuen Produkts zum Standort darstellen, angezeigt werden, nachdem ein System nicht mehr reagiert. Hierfür ist ein System mit Daten Sicherungs-, Wiederherstellungs-und hoch Verfügbarkeits Mechanismen erforderlich.

Die Gewährleistung der Atomizität einer Transaktion sowie der anderen Eigenschaften ist bei einer beliebigen Anzahl von Fehlern vorhanden, einschließlich Fehlern, die während der Wiederherstellungs Phase eines vorherigen Fehlers auftreten. Letztendlich erreicht das System entweder einen von zwei Zuständen: alle Vorgänge wurden angewendet, oder es wurden keine Vorgänge angewendet.

Die Eigenschaften einer Transaktion werden in der folgenden Tabelle zusammengefasst.



| Begriff                                                                                                         | BESCHREIBUNG                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Atomic<br/>                 | Entweder werden alle Vorgänge in der Transaktion erfolgreich ausgeführt, oder keiner der Vorgänge bleibt bestehen.<br/>                             |
| <span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Sten<br/> | Wenn die Daten vor Beginn der Transaktion konsistent sind, sind Sie nach Abschluss der Transaktion konsistent.<br/> |
| <span id="Isolated_"></span><span id="isolated_"></span><span id="ISOLATED_"></span>Isolation <br/>     | Die Auswirkungen einer aktuell ausgeführten Transaktion werden in allen anderen Transaktionen ausgeblendet.<br/>                               |
| <span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Bar<br/>             | Wenn eine Transaktion abgeschlossen wird, sind die Ergebnisse persistent und bleiben bei einem Systemabsturz bestehen.<br/>                               |



 

Mit diesen Eigenschaften wird sichergestellt, dass die Software unerwartete Fehler verarbeiten kann, da Sie eine Transaktion einfach abbrechen kann, wenn eine unerwartete Situation einen erfolgreichen Abschluss verhindert. Die Transaktions Infrastruktur stellt sicher, dass für alle Auswirkungen der abgebrochenen Transaktion ein Rollback ausgeführt wird und die Daten in einen konsistenten Zustand zurückversetzt werden. Daher ermöglicht ein Transaktionssystem eine ordnungsgemäße Wiederherstellung von Systemfehlern.

Um die ACID-Eigenschaften zu gewährleisten, muss ein System, das Transaktionen unterstützt, über eine robuste Protokollierungsfunktion verfügen, die bei Bedarf für das Ausführen eines Commits oder eines Rollbacks von Transaktionen Weitere Informationen finden Sie unter [gemeinsames Protokolldateisystem](/previous-versions/windows/desktop/clfs/common-log-file-system-portal).

 

