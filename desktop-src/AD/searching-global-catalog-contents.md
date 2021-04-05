---
title: Durchsuchen des globalen Katalogs
description: Active Directory Domain Services auch über einen globalen Katalog (GC) verfügen, der ein partielles Replikat aller Objekte im Verzeichnis enthält.
ms.assetid: 83970563-1a56-4671-b264-56e29939e369
ms.tgt_platform: multiple
keywords:
- Durchsuchen des globalen Katalog Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a057330309c12df6d18a209fc3d2adaf42b03005
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707559"
---
# <a name="searching-the-global-catalog"></a>Durchsuchen des globalen Katalogs

Active Directory Domain Services auch über einen globalen Katalog (GC) verfügen, der ein partielles Replikat aller Objekte im Verzeichnis enthält. Sie enthält außerdem partielle Replikate des Schemas und der Konfigurations Container. Mindestens ein Domänen Controller in einer Domäne kann eine Kopie des globalen Katalogs enthalten. Weitere Informationen zum Binden an einen globalen Katalog finden Sie unter [binden an den globalen Katalog](binding-to-the-global-catalog.md).

Der globale Katalog enthält ein Replikat aller Objekte in Active Directory Domain Services, aber nur mit einer kleinen Anzahl von Attributen. Bei Such Vorgängen werden die Attribute im globalen Katalog häufig verwendet, z. b. die vor-und Nachnamen eines Benutzers, Anmelde Namen usw. Die Attribute des globalen Katalogs enthalten außerdem diejenigen, die zum Auffinden eines vollständigen Replikats des Objekts erforderlich sind. Der globale Katalog ermöglicht Benutzern das schnelle Auffinden von interessanten Objekten, ohne zu wissen, welche Domäne Sie enthält und ohne dass ein zusammenhängender erweiterter Namespace im Unternehmen erforderlich ist. Das heißt, Sie können die gesamte Gesamtstruktur durchsuchen.

Wenn Sie also eine Bindung zu einem Objekt im globalen Katalog herstellen, Durchsuchen Sie dieses Objekt und die gesamte Hierarchie darunter –, ohne zu einem anderen Server wechseln zu müssen. Allerdings kann bei der Suche nur ein Abfrage Filter mit Eigenschaften im globalen Katalog verwendet werden, und es können nur Eigenschaften im globalen Katalog abgerufen werden.

Das Durchsuchen des globalen Katalogs bietet die folgenden Vorteile:

-   Der globale Katalog ermöglicht es Ihnen, die gesamte Gesamtstruktur oder einen beliebigen Teil der Gesamtstruktur sowie das Schema und die Konfigurations Container zu durchsuchen.
-   Der globale Katalog ermöglicht es Ihnen, eine vollständige Suche auf einem einzelnen Server auszuführen. Es sind keine Verweise oder eine Verweis Verfolgung erforderlich.

Das Durchsuchen des globalen Katalogs hat folgende Nachteile:

-   Der globale Katalog enthält eine kleine Teilmenge der Eigenschaften für jedes Objekt. Wenn der Abfrage Filtereigenschaften enthält, die nicht im globalen Katalog enthalten sind, wertet die Abfrage die Ausdrücke, die diese Eigenschaften enthalten, als false aus. Wenn Sie in der Liste der Eigenschaften, die Sie zurückgeben möchten, nicht globale Katalog Eigenschaften angeben, werden diese Eigenschaften nicht abgerufen.
-   Ein Domänen Controller, der einen globalen Katalog enthält, muss verfügbar sein, um den globalen Katalog zu durchsuchen. Wenn eine solche nicht verfügbar ist, können Sie keine globale Katalog Suche durchführen.
-   Der globale Katalog ist schreibgeschützt. Dies bedeutet, dass Sie keine Bindung an ein Objekt im globalen Katalog vornehmen können, um-Objekte zu erstellen, zu ändern oder zu löschen.

 

 




