---
description: ACEs zum Steuern des Zugriffs auf Objekteigenschaften
ms.assetid: 79dd4a45-c42c-4775-93ce-6e3206894d63
title: ACEs zum Steuern des Zugriffs auf Objekteigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fddd5d78ff5b02bbbe4b9b7a7ce0b77d7be263f9fd3926f44411469af2bb3c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785251"
---
# <a name="aces-to-control-access-to-an-objects-properties"></a>ACEs zum Steuern des Zugriffs auf die Eigenschaften eines Objekts

Die [*DACL (Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) eines Verzeichnisdienstobjekts (Directory Service, DS) kann wie folgt eine Hierarchie von [*Zugriffssteuerungseinträgen (ACEs)*](/windows/desktop/SecGloss/a-gly) enthalten:

1.  ACEs, die das Objekt selbst schützen
2.  [Objektspezifische ACEs,](object-specific-aces.md) die einen angegebenen Eigenschaftensatz für das Objekt schützen
3.  Objektspezifische ACEs, die eine angegebene Eigenschaft für das Objekt schützen

Innerhalb dieser Hierarchie gelten die Rechte, die auf einer höheren Ebene gewährt oder verweigert werden, auch für die unteren Ebenen. Wenn beispielsweise ein objektspezifischer ACE für einen Eigenschaftensatz einem Vertrauensnehmer das ADS \_ RIGHT \_ DS \_ READ \_ PROP-Recht zulässt, hat der Vertrauensnehmer impliziten Lesezugriff auf alle Eigenschaften dieses Eigenschaftensatzes. Analog dazu gewährt ein ACE für das Objekt selbst, das ADS RIGHT DS READ PROP-Zugriff zulässt, \_ \_ dem \_ \_ Vertrauensnehmer Lesezugriff auf alle Eigenschaften des Objekts.

Die folgende Abbildung zeigt die Struktur eines hypothetischen DS-Objekts und dessen Eigenschaftensätze und -eigenschaften.

![Verzeichnisdienstobjekthierarchie](images/accctrl2.png)

Angenommen, Sie möchten den folgenden Zugriff auf die Eigenschaften dieses DS-Objekts zulassen:

-   Gruppen-A-Lese-/Schreibberechtigung für alle Eigenschaften des Objekts zulassen
-   Allen anderen Personen lese-/schreibberechtigungen für alle Eigenschaften außer Eigenschaft D gestatten

Legen Sie hierzu die ACEs in der DACL des Objekts fest, wie in der folgenden Tabelle gezeigt.



| Treuhänder  | Objekt-GUID    | ACE-Typ                  | Zugriffsrechte                                             |
|----------|----------------|---------------------------|-----------------------------------------------------------|
| Gruppe A  | Keine           | Zugriffsberechtigung für ACE        | ADS \_ RIGHT \_ DS \_ READ \_ PROP \| ADS \_ RIGHT \_ DS \_ WRITE \_ PROP |
| allen Beteiligten | Eigenschaftensatz 1 | Zugriffsberechtigungsobjekt ACE | ADS \_ RIGHT \_ DS \_ READ \_ PROP \| ADS \_ RIGHT \_ DS \_ WRITE \_ PROP |
| allen Beteiligten | Eigenschaft C     | Zugriffsberechtigungsobjekt ACE | ADS \_ RIGHT \_ DS \_ READ \_ PROP \| ADS \_ RIGHT \_ DS \_ WRITE \_ PROP |



 

Der ACE für Gruppe A verfügt nicht über eine Objekt-GUID, was bedeutet, dass er den Zugriff auf alle Eigenschaften des Objekts zulässt. Der objektspezifische ACE für Eigenschaftensatz 1 ermöglicht jedem Zugriff auf die Eigenschaften A und B. Der andere objektspezifische ACE ermöglicht jedem Zugriff auf Eigenschaft C. Beachten Sie, dass diese DACL zwar keine ACEs mit Zugriffsverweigerung besitzt, aber implizit allen Zugriff auf Eigenschaft D mit Ausnahme von Gruppe A verweigert.

Wenn ein Benutzer versucht, auf die -Eigenschaft eines Objekts zuzugreifen, überprüft das System die ACEs in der richtigen Reihenfolge, bis der angeforderte Zugriff explizit gewährt, verweigert oder keine acEs mehr vorhanden sind. In diesem Fall wird der Zugriff implizit verweigert.

Das System wertet Folgendes aus:

-   ACEs, die für das Objekt selbst gelten
-   Objektspezifische ACEs, die für den Eigenschaftensatz gelten, der die Eigenschaft enthält, auf die zugegriffen wird
-   Objektspezifische ACEs, die für die Eigenschaft gelten, auf die zugegriffen wird

Das System ignoriert objektspezifische ACEs, die für andere Eigenschaftensätze oder Eigenschaften gelten.

 

 
