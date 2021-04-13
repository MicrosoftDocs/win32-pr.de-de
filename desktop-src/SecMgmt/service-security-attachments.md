---
description: Das Microsoft Security Configuration Tool ist ein Satz von Microsoft Management Console (MMC)-Tools, die die Konfiguration und Analyse der Systemsicherheit vereinfachen.
ms.assetid: c6558789-84eb-4998-a2c1-725d8a64d255
title: Dienst Sicherheitsanlagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47cdd0ca3799615125900a3ae6b0b78c26f4abc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343089"
---
# <a name="service-security-attachments"></a>Dienst Sicherheitsanlagen

Das Microsoft Security Configuration Tool ist ein Satz von Microsoft Management Console (MMC)-Tools, die die Konfiguration und Analyse der Systemsicherheit vereinfachen. Einige Dienste verfügen jedoch über spezielle Konfigurations Anforderungen, die über die vom Standard Toolset bereitgestellten Sicherheitseinstellungen hinausgehen. Um diese Anforderungen zu erfüllen, können Sie die Funktionalität des Toolsets erweitern, indem Sie eine Anlage schreiben, die die Dienst spezifischen Sicherheitsaufgaben behandelt.

Spooler ist beispielsweise ein Windows NT-Dienst, der private Objekte definiert, die gesichert werden müssen, z. b. Drucker. Diese Funktion wird nicht von der Standard Toolreihe behandelt und erfordert daher eine Anlage zur Handhabung der Konfiguration und Analyse von Drucker Objekten. Die Konfiguration allgemeiner Sicherheitsparameter, wie z. b. der Dienst Aufruf Richtlinie, wird weiterhin vom Sicherheitskonfigurations-Toolset behandelt.

Sicherheitsdienst Anlagen erweitern die Funktionalität des Sicherheitskonfigurations Tools, die für die Unterstützung Dienst spezifischer Konfigurationen festgelegt ist.

Eine Anlage verfügt über zwei Komponenten:

-   Eine MMC-Snap-in-Erweiterung, die die Benutzeroberfläche der Anlage implementiert.
-   Eine Anlage-Engine, die Dienst spezifische Sicherheitskonfigurations-und Analyse Tasks verarbeitet.

Die Erweiterungs-Snap-in-Erweiterung wird von den Snap-Ins "Sicherheitskonfiguration" gehostet. Hierbei handelt es sich um MMC-Snap-Ins, die dem Benutzer Schnittstellen zum Konfigurieren und Analysieren der allgemeinen Sicherheitseinstellungen für einen Dienst bereitstellen. Dienst spezifische Einstellungen werden mithilfe der Erweiterungs-Snap-in-Erweiterung konfiguriert.

Wenn der Benutzer eine Konfigurationseinstellung ändert, werden die neuen Informationen in den Snap-Ins "Sicherheitskonfigurations-Snap-Ins" gespeichert, und die Anforderung wird an die Sicherheitskonfigurations-Engine übergeben. Die Engine verarbeitet die Anforderung und legt den Dienst auf die neue Konfiguration fest. Wenn die Anforderung eine Standard Sicherheitseinstellung betrifft, wird Sie von der-Engine behandelt. Wenn die Anforderung Dienst spezifisch ist, ruft die Engine die entsprechende Anlage-Engine auf, um die Anforderung zu verarbeiten.

In der folgenden Abbildung wird gezeigt, wie die Anlagen-Engine und die Snap-in-Erweiterung innerhalb des Frameworks des Sicherheitskonfigurations-Toolsets funktionieren.

![Anlagen-Engine und Snap-Ins](images/model1a.png)

Weitere Informationen zur Verwendung des Microsoft Security Configuration Tool Sets finden Sie unter Sicherheitskonfiguration mithilfe Ihrer bevorzugten Suchmaschine.

 

 



