---
description: .
ms.assetid: 25d07e42-b5eb-4f72-b4b1-0ebb881644ba
title: Zusätzliche Windows-Ressourcenschutz von Registrierungs Schlüsseln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb048a45324e52c9b9319f52f95b64361b95bbfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360870"
---
# <a name="additional-windows-resource-protection-on-registry-keys"></a>Zusätzliche Windows-Ressourcenschutz von Registrierungs Schlüsseln

## <a name="platform"></a>Plattform

**Clients** -Windows 7  
**Server** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkungen von Features

**Schweregrad** -Mittel  
**Häufigkeit** -niedrig  


## <a name="description"></a>BESCHREIBUNG

Zusätzliche Systemressourcen haben in Windows 7 Windows-Ressourcenschutz Einstellungen (WRP) hinzugefügt, sodass Sie schreibgeschützte Einstellungen haben. Die meisten Ressourcen, die zusätzlichen Schutz erhalten haben, sind System-com-Server Schlüssel, obwohl einige Features den Ziel Ressourcenschutz hinzugefügt haben. Microsoft hat diese Ressourcen geändert, um zu verhindern, dass das System und andere Anwendungen voneinander unterbrechen und eine konsistente, stabile Plattform bereitstellen, auf der die Anwendungen zuverlässig ausgeführt werden können. In der Vergangenheit konnten Anwendungen benutzerdefinierte Dateien bereitstellen und die ungeschützte com-Registrierung verwenden, um das System zu ändern. Bei älteren Anwendungen können dadurch System Laufzeiten herabgestuft oder die Schnittstelle geändert werden, auf der andere Anwendungen ordnungsgemäß funktionieren. Im schlimmsten Fall können solche Installationen zu Systemfehlern oder zu einer Verschlechterung der Zeit führen. Um eine bessere und stabilere Anwendungsplattform bereitzustellen, haben wir diese Registrierungen gesperrt, damit nur Microsoft-Updates Systemkomponenten ändern können.

Da die meisten geänderten Ressourcen vom System verwendet werden, wirkt sich diese Änderung nicht auf die Mehrzahl der Anwendungen aus. Obwohl wir davon ausgehen, dass die meisten Anwendungen aufgrund dieser Änderungen eine bessere Leistung für Windows 7 aufweisen, kann eine kleine Teilmenge der Anwendungen negativ beeinträchtigt werden. Die Anwendungs kompatibilitätsschichten des Systems lösen automatisch Setup Probleme aus, indem Sie der Anwendung immer mitteilen, dass es erfolgreich war, eine Einstellung zu ändern. Dies ist auch dann der Fall, wenn es sich um eine geschützte Ressource handelt. Dadurch wird verhindert, dass Anwendungs Setups unterbrochen werden, aber möglicherweise Probleme verursachen, wenn die Einstellung geändert werden muss, damit die Anwendung ordnungsgemäß funktioniert.

## <a name="manifestation"></a>Ausstrahlung

Anwendungen haben diese Einstellungen möglicherweise vor Windows 7 geändert. Bei der Installation von unter Windows 7 finden Anwendungen möglicherweise bestimmte Features nicht mehr, da die Einstellungen nicht widerspiegeln, was die Anwendung erwartet hat.

Es gibt zwei Szenarien, in denen Anwendungen möglicherweise Probleme im Zusammenhang mit diesem zusätzlichen Schutz haben:

-   Anwendungen, die möglicherweise die nun geschützten Einstellungen als Datenspeicher oder als seltenen oder unbeabsichtigten Erweiterungs Punkt verwendet haben
-   In seltenen Fällen erkennt der Erkennungsmechanismus, der zur Identifizierung von Anwendungs Setups verwendet wird, ein bestimmtes Setup nicht, sodass die Kompatibilitäts Ebene der Anwendungs Kompatibilität möglicherweise nicht angewendet wird.

## <a name="mitigation"></a>Minderung

Das primäre Mittel der Entschärfung ist die Anwendungs Kompatibilitäts Ebene des Systems, die automatisch auf Anwendungs Setups angewendet wird, wenn Sie erkannt wird. Sie können es auch manuell auf eine beliebige Anwendung anwenden, indem Sie die Registerkarte Kompatibilität in den Eigenschaften der Anwendung verwenden.

Diese Ebene löst das Problem, indem Registrierungs Vorgänge abgefangen werden. In dem Fall, in dem die Anwendung versucht hat, eine schreibgeschützte Einstellung (WRP) zu ändern, gibt die Ebene immer Erfolg zurück, auch wenn die Einstellung nicht wirklich geändert wurde. Bei den meisten Anwendungen werden dadurch keine Probleme verursacht. Es besteht jedoch die Möglichkeit, dass die Anwendung diese Einstellung geändert hat, damit Sie ordnungsgemäß funktioniert. Dies ist das erste Szenario, das oben beschrieben wird.

## <a name="solution"></a>Lösung

Für die beiden oben genannten Szenarien:

-   Wenn die Anwendung erfordert, dass der Schlüssel beschreibbar ist, um den Datenspeicher zu verwenden oder zu verwenden, gibt es keine andere Lösung als das Ändern der Anwendung, sodass Sie nicht mehr in diesen Speicherort schreibt.
-   Wenn die Kompatibilitäts Ebene nicht auf ein Setup angewendet wurde, sollte der Setup Fehler erkannt und bereitgestellt und erneut ausgeführt werden. Anwendungen können auch im Kompatibilitätsmodus ausgeführt werden. in diesem Fall wird immer die Entschärfungs Ebene angewendet.

## <a name="compatibility-tests"></a>Kompatibilitäts Tests

Erkennen, ob eine Anwendung eine WRP-Entschärfung angewendet hat:

-   Windows Installer ist von WRP abhängig. Versuche, eine geschützte Ressource zu schreiben oder zu ändern, werden automatisch und ignoriert. Wenn die Anwendung mit Windows Installer installiert wurde und die Protokollierung aktiviert wurde, wird eine Warnung für jeden Schreibvorgang des Registrierungsschlüssels protokolliert, der aufgrund einer durch WRP geschützten Ressource ignoriert wurde.
-   Die WRP-API umfasst sfciskeyprotected, das Abfragen kann, ob ein Registrierungsschlüssel auf dem aktuellen System durch WRP geschützt ist. Weitere Informationen zur Verwendung dieser API finden Sie in der WRP-Eintrag in MSDN unter den folgenden Links.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

<dl>

[Windows-Ressourcenschutz](/windows/desktop/Wfp/windows-resource-protection-portal)  
</dl>

 

 
