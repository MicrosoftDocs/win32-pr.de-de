---
description: Die CRM-Schnittstellen sind erforderlich, um die Unterstützung für CRM-Worker und CRM-kompenatoren zu bieten, die mit Visual Basic und Visual C++
ms.assetid: 68a75da7-1f35-41a4-8872-e3f4ad1fc30d
title: Com+ CRM-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ba3235b1cd2a82fc913dd676bbb78324f340cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749008"
---
# <a name="com-crm-interfaces"></a>Com+ CRM-Schnittstellen

Die CRM-Schnittstellen sind erforderlich, um die Unterstützung für CRM-Worker und CRM-kompenatoren zu bieten, die mit Visual Basic und Visual C++

Sie können das com+-kompensierende Ressourcen-Manager (CRM) verwenden, um Anwendungs Ressourcen schnell und einfach in Microsoft Distributed Transaction Coordinator (DTC)-Transaktionen zu integrieren.

Bei Komponenten, die mit Visual Basic geschrieben wurden, ist es einfacher, einen Protokolldaten Satz als eine Sammlung von Varianten zu erstellen. Außerdem sind Visual Basic Komponenten Apartment Thread, was bedeutet, dass es möglich sein muss, die Schnittstellen aus dem Multithread-Apartment in ein Single Thread-Apartment zu Mars Hallen. Bei CRM-Komponenten, die mit Visual C++ entwickelt wurden, könnte auch das Apartment Threading Modell verwendet werden. es wird jedoch empfohlen, stattdessen das beide Threading Modell zu verwenden.

Die in der folgenden Tabelle beschriebenen Schnittstellen enthalten ausführliche Referenzinformationen für Entwickler von com+-CRMs.



| CRM-Schnittstellen                                             | BESCHREIBUNG                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Icrmcompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator)                 | Diese Schnittstelle stellt unstrukturierte Protokolldaten Sätze in Visual C++ bereit.                                                           |
| [**Icrmcompensatorvarianten**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) | Diese Schnittstelle stellt beim Verwenden von Visual Basic strukturierte Protokolldaten Sätze an den CRM-kompenerer bereit.                            |
| [**Icrmformatlogrecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmformatlogrecords)       | Diese Schnittstelle konvertiert die Protokolldaten Sätze in das Anzeige Format, sodass Sie mit einem generischen Überwachungs Tool angezeigt werden können. |
| [**Icrmlogcontrol**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)                   | Diese Schnittstelle wird vom CRM-Worker und CRM-kompenator verwendet, um Datensätze in das Protokoll zu schreiben und Sie dauerhaft zu machen.           |
| [**Icrmmonitor**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitor)                         | Diese Schnittstelle erfasst eine Momentaufnahme des aktuellen Status eines CRM und enthält einen bestimmten CRM-Clerk.                          |
| [**Icrmmonitorclerchs**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorclerks)             | Diese Schnittstelle erhält Informationen über den Zustand von clerchs.                                                             |
| [**Icrmmonitorlogrecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords)     | Diese Schnittstelle überwacht die einzelnen Protokolldaten Sätze, die von einem bestimmten CRM-Clerk für eine bestimmte Transaktion verwaltet werden.            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompensierende com+-Ressourcen-Manager Konzepte](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



