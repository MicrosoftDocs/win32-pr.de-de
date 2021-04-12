---
description: Com+-Transaktionen
ms.assetid: 40eccce1-a362-4adc-8060-f6923b9162c9
title: Com+-Transaktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef51f4c8ed5e37101f64d36af385c93ac7e69ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393133"
---
# <a name="com-transactions"></a>Com+-Transaktionen

Wenn Sie ein Buch von einem Online Buchhandel kaufen, verwenden Sie eine Kreditkarte, um Geld für ein Buch zu kaufen. Nachdem Sie Ihre Bestellung eingereicht haben, wird durch eine Reihe verwandter Vorgänge (Überprüfung der Kreditkarte, Überprüfung der Bestands Verfügbarkeit usw.) sichergestellt, dass Sie das Buch erhalten und dass der Buchhandel Ihr Geld erhält. Wenn ein einzelner Vorgang in der Reihe während des Austauschs fehlschlägt, schlägt der gesamte Austausch fehl. Sie erhalten das Buch nicht, und der Buchhandel erhält nicht Ihr Geld.

Die Technologie, die für die ausgeglichene und vorhersagbare Online Verarbeitung zuständig ist, wird als *Transaktionsverarbeitung* bezeichnet. Eine *Transaktion* ist Programm gesteuert eine Arbeitseinheit, in der eine Reihe von Vorgängen stattfinden. Com+ verwendet programmgesteuerte Transaktionen, um sicherzustellen, dass Ressourcen nicht dauerhaft aktualisiert werden, es sei denn, alle Vorgänge innerhalb der Transaktion werden erfolgreich abgeschlossen Durch das Binden eines Satzes verwandter Vorgänge in einer com+-Transaktion, die entweder vollständig erfolgreich oder vollständig fehlschlägt, können Sie die Fehlerwiederherstellung erheblich vereinfachen.

In den folgenden Themen wird die allgemeine Transaktions Verarbeitungs Theorie vorgestellt, eine genauere Betrachtung der Transaktionen in com+ und praktische Tipps zum Schreiben von Transaktions Komponenten bereitgestellt.



| Thema                                                                   | BESCHREIBUNG                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Konzepte der com+-Transaktionen](com--transactions-concepts.md)<br/> | Stellt grundlegende Begriffe und Konzepte dar.<br/>                                  |
| [Aufgaben für COM+-Transaktionen](com--transactions-tasks.md)<br/>       | Bietet praktische Informationen zum Schreiben von transaktionalen Komponenten.<br/> |



 

 

 




