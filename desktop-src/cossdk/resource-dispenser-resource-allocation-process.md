---
description: Ressourcen Zuordnungs Prozess Ressourcen Verteiler
ms.assetid: 695d08f4-ba5c-4a5f-a2ad-481a8ede49ab
title: Ressourcen Zuordnungs Prozess Ressourcen Verteiler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a12cb22abd6d4d825f1ca048495b032a77fe216
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214140"
---
# <a name="resource-dispenser-resource-allocation-process"></a>Ressourcen Zuordnungs Prozess Ressourcen Verteiler

Jedes Mal, wenn ein Ressourcen Verteiler eine Ressource von seinem Inhaber zugeordnet hat, geschieht Folgendes:

1.  Der Ressourcen Verteiler deklariert einen Ressourcentyp Bezeichner (**restypid**), der den Typ der erforderlichen Ressource beschreibt.

2.  Der Ressourcen Verteiler ruft die [**ihälter:: Zuweisung**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) -Methode des Inhabers auf und übergibt diese **restypid**.

3.  Der Inhaber generiert eine Kandidatenliste aus den verfügbaren Ressourcen. Kandidaten sind Ressourcen, die entweder nicht in einer Transaktion eingetragen sind oder bereits in der Transaktion des aufrufenden Objekts eingetragen wurden.

4.  Diese Kandidaten werden einzeln an die [**idispenser Server Driver:: rateresource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-rateresource) -Methode übergeben, wo Sie (auf einer Skala von 0 bis 100) bewertet werden, um wie gut die Candidate-Ressource mit der gewünschten **restypid** übereinstimmt.

5.  Der Inhaber wählt die Ressource aus, die der Ressourcen Spender als höchsten Wert bewertet.

6.  Der Ressourcen Verteiler kann die Bewertungs Schleife frühzeitig beenden, indem er den Kandidaten eine Ressourcenbewertung von 100 (eine perfekte Anpassung) zuweist. Die Bewertung 100 ist normalerweise für Kandidaten Ressourcen reserviert, die bereits ordnungsgemäß eingetragen sind, es sei denn, der Ressourcen Verteiler schließt aus, dass die Eintragung ein kostengünstiger Vorgang ist. Wenn alle möglichen Ressourcen (sofern vorhanden) als 0 (unbrauchbar) eingestuft werden, wird eine neue Ressource durch Aufrufen von [**idispenser Server:: CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource)erstellt.

7.  Wenn die zuvor ausgewählte Ressource noch nicht in der Transaktion des aufrufenden Objekts eingetragen ist, wird die [**idispenser Server Driver:: enlistresource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) -Methode des Ressourcen Verteilers aufgerufen.

8.  Der Methoden Aufrufder [**Zuweisung**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) wird an den Ressourcen Verteiler mit der eingetragenen Ressource zurückgegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte des com+-Ressourcen Verteilers](com--resource-dispenser-concepts.md)
</dt> <dt>

[Eintragen einer Ressource in eine Transaktion](enlisting-a-resource-in-a-transaction.md)
</dt> <dt>

[Nachverfolgen nicht zugewiesener Ressourcen](tracking-non-allocated-resources.md)
</dt> </dl>

 

 



