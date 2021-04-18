---
description: Zugreifen auf den com+-Katalog
ms.assetid: 1322a3fe-faee-4971-949f-5e0d2dfe469b
title: Zugreifen auf den com+-Katalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2de7c87da1744e23b384199dce68628fd77d5d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344837"
---
# <a name="accessing-the-com-catalog"></a>Zugreifen auf den com+-Katalog

Der com+-Katalog ist der zugrunde liegende Datenspeicher, der alle com+-Konfigurationsdaten enthält. Jedes Mal, wenn Sie eine com+-Verwaltung durchführen, lesen und schreiben Sie Daten, die im Katalog gespeichert sind. Die einzige Möglichkeit, auf den Katalog zuzugreifen, ist das Verwaltungs Programmkomponenten Dienste oder die COMAdmin-Bibliothek.

Der com+-Katalog bietet eine Abstraktions Ebene über die tatsächlichen Details, wo und wie com+-Konfigurationsdaten gespeichert werden. Ein Großteil der Daten wird in der COM+-Registrierungsdatenbank (oder RegDB) gespeichert, die Daten für alle in com+-Anwendungen installierten, konfigurierten Komponenten enthält. Diese Datenbank wird zur Laufzeit der Anwendung verwendet, um Konfigurationsdaten für com+ bereitzustellen, um Objekte ordnungsgemäß in einem geeigneten Kontext zu aktivieren, sodass Dienste für Objekte gemäß ihrer Konfiguration bereitgestellt werden können. Die RegDB selbst ist ein transaktiver Ressourcen-Manager, der DTC-Transaktionen über den [kompensierenden Ressourcen-Manager](com--compensating-resource-manager.md)verwendet. Wenn Sie beibehaltene Konfigurationsänderungen vornehmen, wird für die Transaktion ein Commit ausgeführt. Die einzige Möglichkeit, auf die RegDB zuzugreifen, ist der com+-Katalog mit den COMAdmin-Objekten oder dem Verwaltungs Programmkomponenten Dienste.

Auf jedem Computer wird ein com+-Katalogserver als Komponente in der Systemanwendung ausgeführt. Der Katalogserver steuert den Zugriff auf die auf seinem Computer gespeicherten Katalogdaten. der Katalogserver ist in der Tat eine Abfrage-Engine, mit der Sie Daten im Katalog auf diesem Computer lesen und schreiben können. Wenn Sie die programmgesteuerte Verwaltung durch Instanziieren eines [**comadmincatalog**](comadmincatalog.md) -Objekts initiieren, öffnet dieses Objekt eine Sitzung mit dem lokalen Katalogserver. Anforderungen für Sammlungen oder Sammel Elemente im lokalen Katalog werden vom lokalen Katalogserver verarbeitet. Wenn Sie eine Verbindung mit einem Remote Computer herstellen, kommunizieren Sie mit dem Katalogserver auf diesem Computer.

## <a name="security-considerations-in-administration"></a>Sicherheitsüberlegungen für die Verwaltung

Um Daten im com+-Katalog zu ändern, müssen Sie über eine Autorität als Administrator verfügen. Wenn Sie Konfigurationsdaten mithilfe des Verwaltungs Programms Komponenten Dienste ändern möchten, müssen Sie Mitglied der Rolle "-Administratoren" sein, die der Systemanwendung auf dem Computer zugewiesen ist, den Sie verwalten möchten. Ebenso muss der Code mit Administrator Berechtigungen ausgeführt werden, um Daten mithilfe der COMAdmin-Objekte zu ändern. Das heißt, eine Anwendung oder ein Skript, das die COMAdmin-Objekte verwendet, muss unter einem Benutzerkonto ausgeführt werden, das der Rolle "Administratoren" in der Systemanwendung auf dem Computer zugewiesen ist, den Sie zu verwalten versucht. Die Anwendung kann nur dann auf Informationen im Katalog zugreifen und diese ändern, wenn das Konto, unter dem Sie ausgeführt wird, über diese Berechtigung verfügt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die COMAdmin-Objekte](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Zusammenfassungs Beschreibung der COMAdmin-Klassen](summary-description-of-the-comadmin-classes.md)
</dt> </dl>

 

 



