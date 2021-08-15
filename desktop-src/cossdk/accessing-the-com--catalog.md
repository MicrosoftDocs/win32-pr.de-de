---
description: Zugreifen auf den COM+-Katalog
ms.assetid: 1322a3fe-faee-4971-949f-5e0d2dfe469b
title: Zugreifen auf den COM+-Katalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f05d85526cb6d82916aa48a49c7f97e581c01b7410530878a7f6e0fc69dac20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129411"
---
# <a name="accessing-the-com-catalog"></a>Zugreifen auf den COM+-Katalog

Der COM+-Katalog ist der zugrunde liegende Datenspeicher, der alle COM+-Konfigurationsdaten enthält. Bei jeder Art von COM+-Verwaltung lesen und schreiben Sie im Katalog gespeicherte Daten. Die einzige Möglichkeit, auf den Katalog zu zugreifen, ist das Verwaltungstool Komponentendienste oder die COMAdmin-Bibliothek.

Der COM+-Katalog bietet eine Abstraktionsebene über die tatsächlichen Details dazu, wo und wie COM+-Konfigurationsdaten gespeichert werden. Ein Teil der Daten wird in der COM+-Registrierungsdatenbank (oder RegDB) gespeichert, die Daten für alle konfigurierten Komponenten enthält, die in COM+-Anwendungen installiert sind. Diese Datenbank wird zur Laufzeit der Anwendung verwendet, um Konfigurationsdaten für COM+ zur ordnungsgemäßen Aktivierung von Objekten in einem geeigneten Kontext zur Verfügung zu stellen, sodass Dienste für Objekte entsprechend ihrer Konfiguration bereitgestellt werden können. Die RegDB selbst ist ein transaktiver Ressourcen-Manager, der DTC-Transaktionen über den [kompensierenden Ressourcen-Manager verwendet.](com--compensating-resource-manager.md) Wenn Sie persistente Konfigurationsänderungen vornehmen, wird für diese transaktional ein Committed ausgeführt. Sie können nur über den COM+-Katalog auf regDB zugreifen, indem Sie die COMAdmin-Objekte oder das Verwaltungstool Komponentendienste verwenden.

Auf jedem Computer wird ein COM+-Katalogserver als Komponente in der Systemanwendung ausgeführt. Der Katalogserver steuert den Zugriff auf die Katalogdaten, die auf seinem Computer gespeichert sind. Tatsächlich ist der Katalogserver eine Abfrage-Engine, mit der Sie Daten im Katalog auf diesem Computer lesen und schreiben können. Wenn Sie die programmgesteuerte Verwaltung durch Instanziieren eines [**COMAdminCatalog-Objekts**](comadmincatalog.md) initiieren, öffnet dieses Objekt eine Sitzung mit dem lokalen Katalogserver. Anforderungen für Sammlungen oder Sammlungselemente im lokalen Katalog werden vom lokalen Katalogserver verarbeitet. Wenn Sie eine Verbindung mit einem Remotecomputer herstellen, kommunizieren Sie mit dem Katalogserver auf diesem Computer.

## <a name="security-considerations-in-administration"></a>Sicherheitsüberlegungen in der Verwaltung

Um Daten im COM+-Katalog zu ändern, müssen Sie über eine Autorität als Administrator verfügen. Um das Verwaltungstool komponentendienste zum Ändern von Konfigurationsdaten zu verwenden, müssen Sie Mitglied der Administratorrolle sein, die der Systemanwendung auf dem Computer zugewiesen ist, den Sie verwalten möchten. Um Daten mithilfe der COMAdmin-Objekte zu ändern, muss Ihr Code mit Administratorberechtigung ausgeführt werden. Das heißt, eine Anwendung oder ein Skript, die die COMAdmin-Objekte verwendet, muss unter einem Benutzerkonto ausgeführt werden, das der Administratorrolle auf der Systemanwendung auf dem Computer zugewiesen ist, den sie verwalten soll. Die Anwendung kann nur dann auf Informationen im Katalog zugreifen und diese ändern, wenn das Konto, unter dem sie ausgeführt wird, über diese Autorität verfügt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die COMAdmin-Objekte](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Zusammenfassungsbeschreibung der COMAdmin-Klassen](summary-description-of-the-comadmin-classes.md)
</dt> </dl>

 

 



