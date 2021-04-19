---
description: Eine Anlage-Snap-in-Erweiterung ist die Komponente einer Anlage, in der die Dienst spezifische Benutzeroberfläche angezeigt wird.
ms.assetid: 1cafa02f-f240-476c-8ce2-ba088afaf889
title: Erweiterungs-Snap-in-Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55267edcd30f32ad371a4aa276587b4eca06c57
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106357169"
---
# <a name="attachment-snap-in-extensions"></a>Erweiterungs-Snap-in-Erweiterungen

Eine Anlage-Snap-in-Erweiterung ist die Komponente einer Anlage, in der die Dienst spezifische Benutzeroberfläche angezeigt wird. Die Snap-in-Erweiterung wird von den Snap-Ins "Sicherheitskonfigurations-Snap-Ins" gehostet. Die Kommunikation zwischen der Anlagen Erweiterung und dem zugehörigen Snap-in-Host erfolgt durch die standardmäßigen MMC-Mechanismen, die in der Dokumentation zu [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) beschrieben werden.

Zusätzlich zu den Schnittstellen, die von der Snap-in-Erweiterung unterstützt werden müssen, um eine MMC-Snap-in-Erweiterung zu sein, muss auch die COM-Schnittstelle [**iscesvplattachmentpersistinfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo)von der Erweiterung des Erweiterungs-Snap-Ins unterstützt werden. Diese Schnittstelle implementiert Methoden, die angeben, ob Dienst spezifische Daten vorhanden sind, die in der Sicherheitsdatenbank gespeichert werden sollen. wenn dies der Fall ist, können Sie diese neuen Daten abrufen und speichern. Die Sicherheitskonfigurations-Snap-Ins rufe regelmäßig Methoden dieser Schnittstelle auf, um die Sicherheitsdatenbank zu aktualisieren.

Die Sicherheitskonfigurations-Snap-Ins implementieren eine Schnittstelle, [**iscesvasetachmentdata**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), die Methoden zum Abrufen Dienst spezifischer Daten aus der Sicherheitsdatenbank bereitstellt. Anlagen-Snap-in-Erweiterungen können Methoden dieser Schnittstelle aufrufen, um Daten aus der Sicherheitsdatenbank abzurufen.

Diese Architektur wird im folgenden Diagramm veranschaulicht.

![Erweiterungs-Snap-in-Erweiterungen](images/model2.png)

Wenn Sie eine Erweiterungs-Snap-in-Erweiterung erstellen, müssen Sie Sie installieren und mit den Sicherheitskonfigurations-Snap-Ins registrieren. Hierzu fügen Sie der Registrierung Schlüssel hinzu, wie unter [Registrieren einer Anlage-Snap-in-Erweiterung](registering-an-attachment-snap-in-extension.md)erläutert. Wenn ein Snap-in für die Sicherheitskonfiguration gestartet wird, wird die Registrierung überprüft, und alle registrierten Snap-in-Erweiterungen werden geladen. Die Erweiterungen werden als Knoten im Sicherheitsbereich für jeden Dienst im Snap-in "Sicherheitskonfiguration" angezeigt.

> [!Note]
> Die Erweiterungs-Snap-in-Erweiterung kann nur Dienst Knoten erweitern. Der Knoten Dienste ist das MMC-Snap-in, das Tools zum Verwalten der auf dem System installierten Dienste enthält. Die Erweiterungs-Snap-in-Erweiterung deklariert sich als untergeordnete Knoten eines bestimmten Dienst Knoten Typs. dann fügt die MMC-Konsole automatisch die zugehörigen Snap-in-Erweiterungen hinzu.
> 
> Jede Anlage-Snap-in-Erweiterung besitzt einen Bereichs Knoten Knoten und den zugehörigen Ergebnisbereich in MMC.

 

 

 
