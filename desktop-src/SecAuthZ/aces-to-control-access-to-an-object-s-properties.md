---
description: ACEs zum Steuern des Zugriffs auf Objekteigenschaften
ms.assetid: 79dd4a45-c42c-4775-93ce-6e3206894d63
title: ACEs zum Steuern des Zugriffs auf Objekteigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1068ceb994e72deedcb795586ddf712fe9c1893
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215692"
---
# <a name="aces-to-control-access-to-an-objects-properties"></a>ACEs zum Steuern des Zugriffs auf die Eigenschaften eines Objekts

Die freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) eines Verzeichnis Dienstanbieter (DS) kann wie folgt eine Hierarchie von [*Zugriffs Steuerungs Einträgen*](/windows/desktop/SecGloss/a-gly) (ACEs) enthalten:

1.  ACEs, die das Objekt selbst schützen
2.  [Objektspezifische ACEs](object-specific-aces.md) , die eine angegebene Eigenschaft für das Objekt schützen
3.  Objektspezifische ACEs, die eine angegebene Eigenschaft für das Objekt schützen

In dieser Hierarchie gelten die auf einer höheren Ebene gewährten oder verweigerten Rechte auch für die niedrigeren Ebenen. Wenn z. b. ein Objekt spezifischer ACE für einen Eigenschaften Satz einem Vertrauens nehmer ermöglicht, dass der Vertrauens nehmer für den Vertrauens nehmer über den \_ richtigen \_ \_ \_ Lesezugriff auf alle Eigenschaften dieses Eigenschaften Satzes verfügt, hat der Vertrauens nehmer impliziten Lesezugriff auf alle Eigenschaften dieser Eigenschaft. Analog dazu gewährt ein ACE für das Objekt selbst, das ADS den \_ rechten \_ DS \_ -Lesezugriff ermöglicht, den Vertrauens nehmer \_ Lesezugriff auf alle Eigenschaften des Objekts.

Die folgende Abbildung zeigt die Struktur eines hypothetischen DS-Objekts und seine Eigenschaften Sätze und Eigenschaften.

![Verzeichnisdienst-Objekthierarchie](images/accctrl2.png)

Angenommen, Sie möchten den folgenden Zugriff auf die Eigenschaften dieses DS-Objekts zulassen:

-   Berechtigung zum Lesen/Schreiben von Gruppen für alle Eigenschaften des Objekts zulassen
-   Lese-/Schreibberechtigung für alle anderen Eigenschaften mit Ausnahme von Eigenschaft D gestatten

Legen Sie hierzu die ACEs in der DACL des Objekts fest, wie in der folgenden Tabelle gezeigt.



| Stiftungs  | Objekt-GUID    | ACE-Typ                  | Zugriffsrechte                                             |
|----------|----------------|---------------------------|-----------------------------------------------------------|
| Gruppe A  | Keine           | Zugriffs zulässiger ACE        | ADS \_ right \_ DS \_ Read \_ Prop \| ADS \_ right \_ DS \_ Write \_ Prop |
| Jeder | Eigenschaften Satz 1 | Zugriffs zulässiger Objekt-ACE | ADS \_ right \_ DS \_ Read \_ Prop \| ADS \_ right \_ DS \_ Write \_ Prop |
| Jeder | Eigenschaft C     | Zugriffs zulässiger Objekt-ACE | ADS \_ right \_ DS \_ Read \_ Prop \| ADS \_ right \_ DS \_ Write \_ Prop |



 

Der ACE für Gruppe A weist keine Objekt-GUID auf, was bedeutet, dass er den Zugriff auf alle Eigenschaften des Objekts zulässt. Der objektspezifische ACE für den Eigenschaften Satz 1 ermöglicht allen Benutzern den Zugriff auf die Eigenschaften A und B. Der andere objektspezifische ACE ermöglicht allen Benutzern den Zugriff auf die Eigenschaft C. Beachten Sie, dass diese DACL zwar keine Zugriffs verweigerten ACEs hat, aber den Zugriff auf die Eigenschaft D für alle außer Gruppe A implizit verweigert.

Wenn ein Benutzer versucht, auf die-Eigenschaft eines Objekts zuzugreifen, überprüft das System die ACEs in der angegebenen Reihenfolge, bis der angeforderte Zugriff explizit gewährt, verweigert wird oder keine weiteren ACEs vorhanden sind. in diesem Fall wird der Zugriff implizit verweigert.

Das System wertet Folgendes aus:

-   ACEs, die auf das Objekt selbst angewendet werden
-   Objektspezifische ACEs, die auf den Eigenschaften Satz angewendet werden, der die Eigenschaft enthält, auf die zugegriffen wird.
-   Objektspezifische ACEs, die auf die Eigenschaft angewendet werden, auf die zugegriffen wird.

Das System ignoriert objektspezifische ACEs, die auf andere Eigenschaften Sätze oder Eigenschaften angewendet werden.

 

 
