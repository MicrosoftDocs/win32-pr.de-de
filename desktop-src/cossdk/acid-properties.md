---
description: Das von den kernelverarbeitungs-pionikern geprägt ist, die Akronym ACID steht für atomarisch, konsistent, isoliert und dauerhaft.
ms.assetid: 857d145c-710d-4097-8ed6-df11e8d52228
title: ACID-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2e725cae75b4aa80d25f2959d474e8baa05f70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126601"
---
# <a name="acid-properties"></a>ACID-Eigenschaften

Das von den kernelverarbeitungs-pionikern geprägt ist, die Akronym ACID steht für atomarisch, konsistent, isoliert und dauerhaft. Um ein vorhersagbares Verhalten zu gewährleisten, müssen alle Transaktionen diese grundlegenden Eigenschaften besitzen, um die Rolle Unternehmens kritischer Transaktionen als all-oder-None-Vorschläge zu verstärken.

Die folgende Liste enthält eine Definition und eine Beschreibung der einzelnen ACID-Eigenschaften:

<dl> <dt>

<span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Atomic
</dt> <dd>

Eine Transaktion muss genau einmal ausgeführt werden und muss atomarisch sein – entweder ist entweder die gesamte Arbeit abgeschlossen, oder es ist kein Vorgang erforderlich. Vorgänge innerhalb einer Transaktion teilen sich in der Regel eine allgemeine Absicht und sind unabhängig. Wenn nur eine Teilmenge dieser Vorgänge durchgeführt wird, könnte das System die allgemeine Absicht der Transaktion kompromittieren. Atomicity eliminiert nicht nur die Möglichkeit, nur eine Teilmenge der Vorgänge zu verarbeiten.

</dd> <dt>

<span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Sten
</dt> <dd>

Eine Transaktion muss die Konsistenz der Daten beibehalten und einen konsistenten Zustand von Daten in einen anderen konsistenten Zustand von Daten umwandeln. Ein Großteil der Verantwortung für die Aufrechterhaltung der Konsistenz fällt dem Anwendungsentwickler.

</dd> <dt>

<span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>Isolation
</dt> <dd>

Eine Transaktion muss eine Isolationseinheit sein, was bedeutet, dass sich gleichzeitige Transaktionen so verhalten sollten, als ob es sich um die einzige Transaktion handelt, die im System ausgeführt wird. Da die Anzahl gleichzeitiger Transaktionen durch einen hohen Grad an Isolation eingeschränkt werden kann, verringern einige Anwendungen die Isolationsstufe in Exchange, um einen besseren Durchsatz zu erzielen. Weitere Informationen finden Sie unter [Konfigurieren von Transaktions Isolations Stufen](configuring-transaction-isolation-levels.md) .

</dd> <dt>

<span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Bar
</dt> <dd>

Eine Transaktion muss wiederherstellbar sein und muss daher über Dauerhaftigkeit verfügen. Wenn für eine Transaktion ein Commit ausgeführt wird, gewährleistet das System, dass die Updates dauerhaft bleiben können, auch wenn der Computer unmittelbar nach dem Commit abstürzt. Die spezialisierte Protokollierung ermöglicht es dem Neustart des Systems, nicht abgeschlossene Vorgänge abzuschließen, die für die Transaktion erforderlich sind, sodass die Transaktion dauerhaft ist.

</dd> </dl>

 

 



