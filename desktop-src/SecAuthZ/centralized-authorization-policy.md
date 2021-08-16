---
description: Das Szenario mit dynamischem Access Control (Dynamic Access Control, DAC) ermöglicht eine zentralisierte Zugriffssteuerungsverwaltung für Dateiserverszenarien in Unternehmen.
ms.assetid: 5A06B8D8-F14B-4D9E-9ED6-4246A26BF945
title: Zentralisierte Autorisierungsrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a07730bff997b545285b0d2845547a4d5deaffe78324e354e7eecbf879b763f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783188"
---
# <a name="centralized-authorization-policy"></a>Zentralisierte Autorisierungsrichtlinie

Das [DAC-Szenario (Dynamic Access Control)](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap) ermöglicht die zentrale Verwaltung der Zugriffssteuerung für Dateiserverszenarien in Unternehmen. Die meisten Organisationen verfügen über mehrere Bereiche, in denen sie den Zugriff steuern möchten.

Beispiele:

-   Steuern des Zugriffs auf vertrauliche Informationen, bei denen Dateien, die als sensibel markiert sind, über bestimmte Berechtigungen verfügen
-   Steuern des Zugriffs auf Dateien mit personenbezogenen Informationen (PII.)
-   Beschränken des Zugriffs auf Dokumente basierend auf den Aufbewahrungsrichtlinien der Organisation.

Es werden mehrere neue Autorisierungsrichtlinienabstraktionen bereitgestellt, damit ein Administrator diese Richtlinien zentral definieren und den Definitionsvorgang vereinfachen kann, indem jede dieser Zugriffsanforderungen separat definiert und verwaltet, aber als eine Richtlinie angewendet werden kann.

In Windows 8 werden zwei neue Active Directory-Richtlinienobjekte eingeführt: eine [zentrale Autorisierungsrichtlinie](central-authorization-policies.md) (Cap) und eine [zentrale Autorisierungsrichtlinienregel](central-authorization-policy-rule.md) (Capr), um zentralisierte Autorisierungsrichtlinien basierend auf Ausdrücken von Ansprüchen und Ressourcenattributen zu definieren und anzuwenden. bei der Verwendung dieser Objekte definiert ein Administrator eine Obergrenze als eine bestimmte Autorisierungsrichtlinie, die auf Ressourcen angewendet werden kann, die über ein bestimmtes Attribut verfügen oder eine bestimmte Anwendbarkeitsbedingung erfüllen. z. B. Dokumente, die als "hohe geschäftliche Auswirkungen" bezeichnet werden. -Ausdrücke können für jede gewünschte Zugriffssteuerungsrichtlinie in einer Organisation definiert werden, die ausgedrückt werden kann, und die Ressourcen, auf die sie angewendet werden soll, können in Form von Windows 8-DAC-Ausdrücken identifiziert werden. Eine Obergrenze ist eine Sammlung von Caprs, die zusammen auf Ressourcen angewendet werden können. Das folgende Diagramm zeigt die Beziehungen von Cap und Cap sowie die konzeptionellen Schritte zum Definieren und Anwenden dieser Objekte auf Dateiressourcen. ![Beziehung von Kapern und Caps](images/cap.png)

 

 
