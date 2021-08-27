---
description: COM+-Transaktionen
ms.assetid: 40eccce1-a362-4adc-8060-f6923b9162c9
title: COM+-Transaktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f800f637a9faec7564d929f3fe7f638ba36d9556db138283c0e6ff3aee87a4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070800"
---
# <a name="com-transactions"></a>COM+-Transaktionen

Wenn Sie ein Buch in einer Onlinebuchhandlung erwerben, verwenden Sie eine Kreditkarte, um Geld für ein Buch zu handeln. Nachdem Sie Ihre Bestellung übermittelt haben, stellt eine Reihe verwandter Vorgänge (Überprüfung Ihrer Kreditkarte, Überprüfung der Inventurverfügbarkeit usw.) sicher, dass Sie das Buch erhalten und dass die Buchhandlung Ihr Geld erhält. Wenn ein einzelner Vorgang in der Reihe während des Austauschs fehlschlägt, schlägt der gesamte Austausch fehl. Sie erhalten das Buch nicht, und die Buchhandlung bekommt Ihr Geld nicht.

Die Technologie, die dafür verantwortlich ist, diesen Onlineaustausch ausgeglichen und vorhersagbar zu machen, wird als *Transaktionsverarbeitung bezeichnet.* Programmgesteuert ist eine *Transaktion* eine Arbeitseinheit, in der eine Reihe von Vorgängen ausgeführt wird. COM+ verwendet programmgesteuerte Transaktionen, um sicherzustellen, dass Ressourcen nicht dauerhaft aktualisiert werden, es sei denn, alle Vorgänge innerhalb der Transaktion wurden erfolgreich abgeschlossen. Durch das Binden einer Reihe verwandter Vorgänge in einer COM+-Transaktion, die entweder vollständig erfolgreich oder vollständig fehlschlägt, können Sie die Fehlerwiederherstellung deutlich vereinfachen.

Die folgenden Themen stellen eine allgemeine Transaktionsverarbeitungstheore vor, bieten einen genaueren Blick auf Transaktionen in COM+ und stellen praktische Tipps zum Schreiben von Transaktionskomponenten vor.



| Thema                                                                   | BESCHREIBUNG                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [COM+-Transaktionskonzepte](com--transactions-concepts.md)<br/> | Stellt grundlegende Begriffe und Konzepte vor.<br/>                                  |
| [COM+-Transaktionsaufgaben](com--transactions-tasks.md)<br/>       | Enthält praktische Informationen zum Schreiben von Transaktionskomponenten.<br/> |



 

 

 




