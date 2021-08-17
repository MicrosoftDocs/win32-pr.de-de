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

Der COM+-Katalog ist der zugrunde liegende Datenspeicher, der alle COM+-Konfigurationsdaten enthält. Wenn Sie eine COM+-Verwaltung durchführen, lesen und schreiben Sie daten, die im Katalog gespeichert sind. Sie können nur über das Verwaltungstool Komponentendienste oder über die COMAdmin-Bibliothek auf den Katalog zugreifen.

Der COM+-Katalog bietet eine Abstraktionsebene über die tatsächlichen Details dazu, wo und wie COM+-Konfigurationsdaten gespeichert werden. Ein Großteil der Daten wird in der COM+-Registrierungsdatenbank (oder RegDB) gespeichert, die Daten für alle konfigurierten Komponenten enthält, die in COM+-Anwendungen installiert sind. Diese Datenbank wird zur Laufzeit der Anwendung verwendet, um Konfigurationsdaten für COM+ bereitzustellen, um Objekte in einem geeigneten Kontext ordnungsgemäß zu aktivieren, sodass Dienste für Objekte gemäß ihrer Konfiguration bereitgestellt werden können. Die RegDB selbst ist ein transaktiver Ressourcen-Manager, der DTC-Transaktionen über den [kompensierenden Ressourcen-Manager](com--compensating-resource-manager.md)verwendet. Wenn Sie persistente Konfigurationsänderungen vornehmen, wird für sie ein Transaktions commit ausgeführt. Sie können nur über den COM+-Katalog mithilfe der COMAdmin-Objekte oder des Component Services-Verwaltungstools auf die RegDB zugreifen.

Auf jedem Computer befindet sich ein COM+-Katalogserver, der als Komponente in der Systemanwendung ausgeführt wird. Der Katalogserver steuert den Zugriff auf die auf seinem Computer gespeicherten Katalogdaten. Tatsächlich ist der Katalogserver eine Abfrage-Engine, mit der Sie Daten im Katalog auf diesem Computer lesen und schreiben können. Wenn Sie die programmgesteuerte Verwaltung durch Instanziieren eines [**COMAdminCatalog-Objekts**](comadmincatalog.md) initiieren, öffnet dieses Objekt eine Sitzung mit dem lokalen Katalogserver. Anforderungen für Sammlungen oder Sammlungselemente im lokalen Katalog werden vom lokalen Katalogserver verarbeitet. Wenn Sie eine Verbindung mit einem Remotecomputer herstellen, kommunizieren Sie mit dem Katalogserver auf diesem Computer.

## <a name="security-considerations-in-administration"></a>Sicherheitsüberlegungen in der Verwaltung

Um Daten im COM+-Katalog zu ändern, benötigen Sie die Autorität als Administrator. Um konfigurationsdaten mithilfe des Component Services-Verwaltungstools zu ändern, müssen Sie Mitglied der Administratorrolle sein, die der Systemanwendung auf dem Computer zugewiesen ist, den Sie verwalten möchten. Ebenso muss Ihr Code mit administratorautorität ausgeführt werden, um alle Daten mithilfe der COMAdmin-Objekte zu ändern. Das heißt, eine Anwendung oder ein Skript, die die COMAdmin-Objekte verwendet, muss unter einem Benutzerkonto ausgeführt werden, das der Administratorrolle der Systemanwendung auf dem Computer zugewiesen ist, den sie verwalten möchte. Die Anwendung kann nur auf Informationen im Katalog zugreifen und diese ändern, sofern das Konto, unter dem sie ausgeführt wird, über diese Autorität verfügt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die COMAdmin-Objekte](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Zusammenfassungsbeschreibung der COMAdmin-Klassen](summary-description-of-the-comadmin-classes.md)
</dt> </dl>

 

 



