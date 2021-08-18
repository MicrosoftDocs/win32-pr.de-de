---
description: Zusätzliche Windows Resource Protection für Registrierungsschlüssel
ms.assetid: 25d07e42-b5eb-4f72-b4b1-0ebb881644ba
title: Zusätzliche Windows Resource Protection für Registrierungsschlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3ea823b2075905b8f22cbc02539f058c9ad8f2ed33ed51d712cd8cb43f59d18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995020"
---
# <a name="additional-windows-resource-protection-on-registry-keys"></a>Zusätzliche Windows Resource Protection für Registrierungsschlüssel

## <a name="platform"></a>Plattform

**Clients** – Windows 7  
**Server** – Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkungen auf Features

**Schweregrad –** Mittel  
**Häufigkeit** : Niedrig  


## <a name="description"></a>BESCHREIBUNG

Zusätzliche Systemressourcen haben Windows Resource Protection-Einstellungen (WRP) in Windows 7 hinzugefügt, sodass sie schreibgeschützt sind. Die überwiegende Mehrheit der Ressourcen, die zusätzlichen Schutz erhalten haben, sind COM-Serverschlüssel des Systems, obwohl einige Features einen gezielten Ressourcenschutz hinzugefügt haben. Microsoft hat diese Ressourcen geändert, um das System und andere Anwendungen vor dem Gegenseitigbruch zu schützen und eine konsistente, stabile Plattform bereitzustellen, auf der Anwendungen zuverlässig ausgeführt werden können. In der Vergangenheit konnten Anwendungen benutzerdefinierte Dateien bereitstellen und die ungeschützte COM-Registrierung verwenden, um das System zu ändern. Bei älteren Anwendungen kann dies ein Downgrade der Systemlaufzeiten oder eine Änderung der Schnittstelle bewirken, auf der andere Anwendungen ordnungsgemäß funktionieren mussten. Im schlimmsten Fall können solche Installationen im Laufe der Zeit zu Systemfehlern oder -beeinträchtigungen führen. Um eine bessere Benutzererfahrung und eine stabilere Anwendungsplattform zu bieten, haben wir diese Registrierungen gesperrt, sodass nur Microsoft-Updates Systemkomponenten ändern können.

Da die meisten geänderten Ressourcen COM-Schlüssel sind, die vom System verwendet werden, wirkt sich diese Änderung nicht auf die meisten Anwendungen aus. Obwohl wir erwarten, dass die meisten Anwendungen aufgrund dieser Änderungen eine bessere Erfahrung mit Windows 7 haben, kann eine kleine Teilmenge der Anwendungen negativ beeinflusst werden. Die Anwendungskompatibilitätsebenen des Systems lösen Setupprobleme automatisch, indem sie der Anwendung immer mitteilen, dass es erfolgreich war, eine Einstellung zu ändern, auch wenn sie aufgrund einer geschützten Ressource fehlgeschlagen ist. Dadurch wird verhindert, dass Anwendungssetups fehlerhaft sind, kann aber zu Problemen führen, wenn die Einstellung geändert werden musste, damit die Anwendung ordnungsgemäß funktioniert.

## <a name="manifestation"></a>Manifestation

Anwendungen haben diese Einstellungen möglicherweise vor Windows 7 geändert. Nach der Installation auf Windows 7 können Anwendungen feststellen, dass bestimmte Features nicht mehr funktionieren, da die Einstellungen nicht den Erwartungen der Anwendung entsprechen.

Es gibt zwei Szenarien, in denen Anwendungen probleme im Zusammenhang mit diesem hinzugefügten Schutz auftreten können:

-   Anwendungen, die die jetzt geschützten Einstellungen möglicherweise als Datenspeicher oder als seltenen oder unbeabsichtigten Erweiterbarkeitspunkt verwendet haben
-   In seltenen Fällen erkennt der Erkennungsmechanismus, der zum Identifizieren von Anwendungssetups verwendet wird, möglicherweise kein bestimmtes Setup, sodass die Entschärfungsebene für die Anwendungskompatibilität möglicherweise nicht angewendet wird.

## <a name="mitigation"></a>Minderung

Die primäre Möglichkeit zur Risikominderung ist die Anwendungskompatibilitätsebene des Systems, die bei Erkennung automatisch auf Anwendungssetups angewendet wird. Sie können sie auch manuell auf jede Anwendung anwenden, indem Sie die Registerkarte Kompatibilität in den Eigenschaften der Anwendung verwenden.

Diese Ebene löst das Problem, indem Registrierungsvorgänge abgefangen werden. Für den Fall, dass die Anwendung versucht hat, eine schreibgeschützte Einstellung (WRP) zu ändern, gibt die Ebene immer erfolglos zurück, obwohl die Einstellung nicht wirklich geändert wurde. Für die meisten Anwendungen führt dies zu keinen Problemen. Es besteht jedoch die Möglichkeit, dass die Anwendung diese Einstellung benötigt, um ordnungsgemäß zu funktionieren. Dies ist das erste oben beschriebene Szenario.

## <a name="solution"></a>Lösung

Für die beiden oben genannten Szenarien:

-   Wenn die Anwendung erfordert, dass der Schlüssel beschreibbar ist, um den Datenspeicher zu verwenden oder zu verwenden, gibt es keine andere Lösung als das Ändern der Anwendung, sodass sie nicht mehr an diesen Speicherort schreibt.
-   Wenn die Kompatibilitätsschicht nicht auf ein Setup angewendet wurde, sollte der Setupfehler erkannt und angeboten werden, angewendet und erneut ausgeführt zu werden. Anwendungen können auch im Kompatibilitätsmodus ausgeführt werden. In diesem Fall wird immer die Entschärfungsebene angewendet.

## <a name="compatibility-tests"></a>Kompatibilitätstests

Ermitteln, ob auf eine Anwendung wrp-Entschärfung angewendet wurde:

-   Windows Das Installationsprogramm kennt WRP. sie ignoriert automatisch und im Hintergrund Versuche, eine geschützte Ressource zu schreiben oder zu ändern. Wenn die Anwendung mit Windows Installer installiert wurde und die Protokollierung aktiviert wurde, wird für jeden Schreibvorgang des Registrierungsschlüssels eine Warnung protokolliert, die ignoriert wurde, da es sich um eine WRP-geschützte Ressource handelt.
-   Die WRP-API enthält SfCIsKeyProtected, das abfragen kann, ob ein Registrierungsschlüssel im aktuellen System WRP-geschützt ist. Weitere Informationen zur Verwendung dieser API finden Sie im WRP-Eintrag in MSDN unter den folgenden Links.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

<dl>

[Windows Ressourcenschutz](/windows/desktop/Wfp/windows-resource-protection-portal)  
</dl>

 

 
