---
description: Die CRM-Infrastruktur stellt eine Reihe von Schnittstellen bereit, die zum Überwachen der CRMs innerhalb einer bestimmten Serveranwendung verwendet werden können.
ms.assetid: b8f40c91-001b-4003-b377-57a918988100
title: Com+ CRM-Überwachungsschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c893040c46810c980c647cbacdc808200e8d5f5e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214093"
---
# <a name="com-crm-monitoring-interfaces"></a>Com+ CRM-Überwachungsschnittstellen

Die CRM-Infrastruktur stellt eine Reihe von Schnittstellen bereit, die zum Überwachen der CRMs innerhalb einer bestimmten Serveranwendung verwendet werden können. Um auf die Überwachungsschnittstellen zuzugreifen, muss eine Komponente, die in der Serveranwendung ausgeführt wird, zunächst einen spezialisierten CRM-Clerk erstellen, der als CRM-Wiederherstellungs Clerk bezeichnet

Bei der normalen Verwendung von CRMs wird erwartet, dass Transaktionen kurzlebig sind, sodass CRM-Worker und CRM-Kompensatoren für einen kurzen Zeitraum (in der Regel nur wenige Sekunden) vorhanden sind. Die Überwachungsschnittstellen dienen daher zum Erstellen einer Momentaufnahme des Status der ausgeführten CRMs zu einem bestimmten Zeitpunkt. Wenn bei einem der CRMs Probleme auftreten, können die Überwachungsschnittstellen auf dem problematischen CRM verwendet werden, um die Protokolldaten Sätze zu überprüfen und ggf. die Transaktion abzubrechen.

Im folgenden finden Sie die drei CRM-Überwachungsschnittstellen und Beschreibungen ihrer Funktionsweise.



| Schnittstelle                                                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Icrmmonitor**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitor)<br/>                     | Mithilfe von [**icrmmonitor:: getclerert**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmmonitor-getclerks)kann eine Momentaufnahme der aktuellen Gruppe aktiver CRM-clerker innerhalb der Serveranwendung abgerufen werden. Hierdurch kann ein bestimmtes CRM Clerk-Sammlungsobjekt, das von Interesse ist, gefunden und abgefragt werden, einschließlich des aktuellen Zustands der Transaktion und der Protokolldaten Sätze, die vom CRM geschrieben wurden.<br/> Wenn das Überwachungs Tool festgestellt hat, welches Clerk von Interesse ist, ruft es [**icrmmonitor:: holdclerk**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmmonitor-holdclerk) auf, um eine [**icrmmonitorlogrecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords) -Schnittstelle für diesen bestimmten Clerk zu erhalten. An diesem Punkt hält das Überwachungs Tool einen Verweis auf diesen Clerk, und wenn die Transaktion abgeschlossen ist, wird der Clerk im Arbeitsspeicher gehalten und erst freigegeben, wenn das Überwachungs Tool fertiggestellt ist.<br/>                                                                                                                                                                                                    |
| [**Icrmmonitorclerchs**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorclerks)<br/>         | Mithilfe dieser Schnittstelle kann das clerkauflistungsobjekt nach Informationen über den Zustand der clerkauflistung zu dem Zeitpunkt durchsucht werden, an dem Sie abgerufen wurde. Zu diesen Informationen zählen die Anzahl der Clerks, die ProgID des CRM-Kompensierungs Elements, die vom Clerk verwendet wurde, die Beschreibung, die zum Zeitpunkt der Registrierung des CRM-Compensators (mit [**icrmlogcontrol:: RegisterCompensator**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-registercompensator)), die Transaktions-ID der Arbeitseinheit und die Aktivitäts-ID bereitgestellt wurde. Einzelne Clerks werden auch durch eine "Clerk instance CLSID" eindeutig identifiziert, bei der es sich nicht um eine COM-CLSID handelt, die in der üblichen Bedeutung des Begriffs ist, aber einfach eine eindeutige GUID ist, die diesen bestimmten Clerk für seine Lebensdauer identifiziert.<br/>                                                                                                                                                                                                                                                                                                |
| [**Icrmmonitorlogrecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords)<br/> | Diese Schnittstelle kann verwendet werden, um den aktuellen Status der Transaktion abzufragen, um herauszufinden, wie viele Protokolldaten Sätze dieser CRM-Clerk geschrieben hat, und um die eigentlichen Protokolldaten Satz Daten zu erhalten. Die Protokolldaten Sätze werden von der [**icrmmonitorlogrecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords) -Schnittstelle im gleichen Format bereitgestellt, das Sie ursprünglich geschrieben haben (mithilfe von [**icrmlogcontrol**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)). Außerdem kann **icrmmonitorlogrecords** optional implementiert werden, um die Protokolldaten Sätze in das sichtbare Format zu konvertieren, sodass Sie mit einem generischen Überwachungs Tool angezeigt werden können.<br/> Da [**icrmmonitorlogrecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords) direkt auf dem CRM-Clerk implementiert ist, können Sie [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für [**icrmlogcontrol**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) (auch auf dem CRM-Clerk implementiert) implementieren. Dies kann dann verwendet werden, um die Transaktion bei Bedarf direkt abzubrechen ([**icrmlogcontrol:: forcetransaktiontoabort**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-forcetransactiontoabort)).<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompensierende com+-Ressourcen-Manager Konzepte](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

