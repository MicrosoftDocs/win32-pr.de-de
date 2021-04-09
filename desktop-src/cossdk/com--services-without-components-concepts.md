---
description: Mit com+ 1,5 wird die Möglichkeit eingeführt, com+-Dienste ohne Komponenten zu verwenden.
ms.assetid: da93d164-234a-4d1e-b82c-f3f904bb8cb6
title: Konzepte der com+-Dienste ohne Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d692657d33143b9437a9c8134260a8c32431cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861555"
---
# <a name="com-services-without-components-concepts"></a>Konzepte der com+-Dienste ohne Komponenten

Mit com+ 1,5 wird die Möglichkeit eingeführt, com+-Dienste ohne Komponenten zu verwenden. Dadurch werden die Leistungskosten erheblich reduziert, wenn com+-Dienste aus einer Umgebung verwendet werden, in der keine Komponenten verwendet werden, und die Komplexität der Verwendung dieser Dienste entfällt. Ab IIS 6,0 nutzen IIS und ASP die Verwendung von COM+-Diensten ohne Komponenten.

Com+-Dienste wurden ursprünglich für die Verwendung mit COM+-Komponenten entwickelt. Einige Programmierumgebungen sind jedoch nicht Komponenten basiert und erfordern daher einen beträchtlichen Verwaltungsaufwand für die Verwendung von COM+-Diensten. Vor der Veröffentlichung von com+ 1,5 musste IIS beispielsweise ausschließlich Shim-Objekte erstellen, um com+-Transaktionsdienste in ASP-Seiten verwenden zu können. Zu den Leistungseinbußen bei der Erstellung dieser Objekte gehören das Speichern der Konfigurationsdaten in der IIS-Metabasis und der COM+-Registrierungsdatenbank (RegDB) sowie die zusätzliche Kommunikation zwischen der IIS-Metabase und der com+-RegDB, die zur effektiven Verwaltung der Konfigurationsdaten benötigt wird.

Wenn IIS einen zweiten com+-Dienst verwenden muss, z. b. die Synchronisierung, musste hierfür ein vollständig anderes Shim-Objekt erstellt werden. Um com+-Transaktionen und die Synchronisierung zu verwenden, wäre ein drittes shimobjekttyp erforderlich. Die Komplexität dieses Ansatzes wird als O (N2) skaliert, sodass die Implementierung neuer Dienste sehr schwierig ist.

Durch die Einführung von COM+-Diensten ohne Komponenten werden die benötigten Dienste über ein Objekt konfiguriert, das von der-Klasse instanziiert wird. Die [**cserviceconfig**](cserviceconfig.md) -Klasse implementiert die zum Konfigurieren der verschiedenen Dienste erforderlichen Schnittstellen und bietet gleichzeitig die Flexibilität, mehrere Dienste gleichzeitig zu unterstützen, sowie die Möglichkeit, neue Dienste in Zukunft zu unterstützen.

Die konfigurierten Dienste können dann über zwei verschiedene Mechanismen verwendet werden: Sie können mithilfe der [**cokreateactivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) -Funktion verwendet werden, die die Dienste auf alle über die von der-Funktion erstellten-Aktivitäten übermittelt, und Sie können auch verwendet werden, indem Sie die Arbeit einbetten, die die Dienste zwischen Aufrufen der [**coenterservicedomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) -und [**coleaveservicedomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) -Funktionen verwendet. Keine dieser Funktionen erfordert die Erstellung neuer Komponenten, damit die com+-Dienste verwendet werden können. nur das [**cserviceconfig**](cserviceconfig.md) -Objekt ist erforderlich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Com+-Dienste ohne Komponenten Aufgaben](com--services-without-components-tasks.md)
</dt> </dl>

 

 



