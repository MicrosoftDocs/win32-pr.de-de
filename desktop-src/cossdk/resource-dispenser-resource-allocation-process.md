---
description: Ressourcenzuordnungsprozess des Ressourcensenders
ms.assetid: 695d08f4-ba5c-4a5f-a2ad-481a8ede49ab
title: Ressourcenzuordnungsprozess des Ressourcensenders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e91802b001bdb8a1af3a933d458c4e9b86b6e3bcd2eb40646e9b64a2e2e14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953820"
---
# <a name="resource-dispenser-resource-allocation-process"></a>Ressourcenzuordnungsprozess des Ressourcensenders

Jedes Mal, wenn ein Ressourcensender eine Ressource vom Besitzer zuteilen, geschieht Folgendes:

1.  Der Ressourcensender deklariert einen Ressourcentypbezeichner (**RESTYPID**), der den typ der erforderlichen Ressource beschreibt.

2.  Der Ressourcenspender ruft die [**IHolder::AllocResource-Methode**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) des Besitzers auf und übergibt **diese RESTYPID.**

3.  Der Besitzer generiert eine Kandidatenliste aus den verfügbaren Ressourcen. Kandidaten sind Ressourcen, die entweder nicht in einer Transaktion eingetragen oder bereits in der Transaktion des aufrufenden Objekts eingetragen sind.

4.  Diese Kandidaten werden einzeln an die [**IDispenserDriver::RateResource-Methode**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-rateresource) übergeben, wo sie bewertet werden (auf einer Skala von 0 bis 100), wie gut die Kandidatenressource der gewünschten **RESTYPID** entspricht.

5.  Der Besitzer wählt die Ressource aus, für die der Ressourcenspender die höchste Raten hat.

6.  Der Ressourcensender kann die Bewertungsschleife frühzeitig beenden, indem er dem Kandidaten eine Ressourcenbewertung von 100 (perfekte Anpassung) zupasst. Eine Bewertung von 100 wäre normalerweise für Kandidatenressourcen reserviert, die bereits ordnungsgemäß eingetragen sind, es sei denn, der Ressourcensender schließt daraus, dass die Eintragung ein kostengünstiger Vorgang ist. Wenn alle Kandidatenressourcen (sofern verfügbar) mit 0 (unbrauchbar) bewertet werden, wird eine neue Ressource durch Aufrufen von [**IDispenserDriver::CreateResource erstellt.**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource)

7.  Wenn die zuvor ausgewählte Ressource nicht bereits in der Transaktion des aufrufenden Objekts eingetragen ist, wird die [**IDispenserDriver::EnlistResource-Methode**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) des Ressourcensenders aufgerufen.

8.  Der [**AllocResource-Methodenaufruf**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) kehrt an den Ressourcenverzehrer mit der eingetragenen Ressource zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[KONZEPTE DES COM+-Ressourcensenders](com--resource-dispenser-concepts.md)
</dt> <dt>

[Eintragung einer Ressource in eine Transaktion](enlisting-a-resource-in-a-transaction.md)
</dt> <dt>

[Nachverfolgen nicht zugeordneter Ressourcen](tracking-non-allocated-resources.md)
</dt> </dl>

 

 



