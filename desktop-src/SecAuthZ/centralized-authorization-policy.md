---
description: Das Dynamic Access Control (DAC)-Szenario ermöglicht die zentralisierte Zugriffs Steuerungs Verwaltung für Dateiserver Szenarien in Unternehmen.
ms.assetid: 5A06B8D8-F14B-4D9E-9ED6-4246A26BF945
title: Zentralisierte Autorisierungs Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1e5798c477a69e80f325a35fd443df101a148c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103961000"
---
# <a name="centralized-authorization-policy"></a>Zentralisierte Autorisierungs Richtlinie

Das [Dynamic Access Control (DAC)-Szenario](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap) ermöglicht die zentralisierte Zugriffs Steuerungs Verwaltung für Dateiserver Szenarien in Unternehmen. Die meisten Organisationen verfügen über mehrere Bereiche, in denen Sie den Zugriff steuern möchten.

Beispiele:

-   Steuern des Zugriffs auf vertrauliche Informationen, in denen Dateien, die als vertraulich gekennzeichnet sind, über bestimmte Berechtigungen verfügen
-   Steuern des Zugriffs auf Dateien mit personenbezogenen Informationen (PII)
-   Einschränken des Zugriffs auf Dokumente basierend auf den Beibehaltungs Richtlinien für Unternehmen.

Einige neue Autorisierungs Richtlinien Abstraktionen werden bereitgestellt, damit Administratoren diese Richtlinien zentral definieren und den Definitions Prozess vereinfachen können, indem Sie zulassen, dass jeder dieser Zugriffs Anforderungen separat definiert und verwaltet wird, aber als eine Richtlinie angewendet wird.

Zwei neue Active Directory Richtlinien Objekte, eine [zentrale Autorisierungs Richtlinie](central-authorization-policies.md) (Cap) und eine [zentrale Autorisierungs Richtlinien Regel](central-authorization-policy-rule.md) (Capr), werden in Windows 8 eingeführt, um zentralisierte Autorisierungs Richtlinien basierend auf Ausdrücken von Ansprüchen und Ressourcen Attributen zu definieren und anzuwenden. bei der Verwendung dieser Objekte definiert ein Administrator eine Capr als spezifische Autorisierungs Richtlinie, die auf Ressourcen angewendet werden kann, die über ein bestimmtes Attribut verfügen oder eine bestimmte anwendbarkeits Bedingung erfüllen. beispielsweise Dokumente mit der Bezeichnung "High Business Impact". Capes können für jede gewünschte Zugriffs Steuerungs Richtlinie in einer Organisation definiert werden, die ausgedrückt werden kann, und die Ressourcen, auf die Sie angewendet werden sollen, können in Bezug auf Windows 8-DAC-Ausdrücke identifiziert werden. eine Obergrenze ist eine Sammlung von caprs, die auf Ressourcen angewendet werden können. Im folgenden Diagramm werden die Beziehungen zwischen Cap und Kap sowie die konzeptionellen Schritte zum Definieren und Anwenden dieser Objekte auf Datei Ressourcen dargestellt. ![Beziehung zwischen Capes und Caps](images/cap.png)

 

 
