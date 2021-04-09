---
title: Delegierung
description: Die Delegierung ist eines der wichtigsten Sicherheitsfunktionen von Active Directory Domain Services.
ms.assetid: ab8740c9-f5a2-40cc-abce-0ef80c3fca7a
ms.tgt_platform: multiple
keywords:
- Delegierungs-AD
- Security AD, Delegierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26be1f9350c664d289832874994e2b3ba2e696c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947401"
---
# <a name="delegation"></a>Delegierung

Die *Delegierung* ist eines der wichtigsten Sicherheitsfunktionen von Active Directory Domain Services. Durch die Delegierung können Administratoren und Gruppen bestimmte Administratorrechte für Container und Unterstrukturen erteilen. Domänen Administratoren, die weitreichende Berechtigungen für große Benutzer Segmente haben, sind nicht mehr erforderlich.

Ein ACE kann einem Benutzer oder einer Gruppe bestimmte Administratorrechte für die Objekte in einem Container erteilen. Rechte werden für bestimmte Vorgänge für bestimmte Objektklassen mithilfe von ACEs in der ACL des Containers erteilt. Um z. b. einen Benutzer mit dem Namen "Benutzer 1" als Administrator der Organisationseinheit "Unternehmens Buchhaltungs" zu aktivieren, fügen Sie ACEs der ACL in "Unternehmens Buchhaltungs" wie folgt hinzu:

"Benutzer 1"; Schusses Erstellen, ändern, löschen; objektklassenbenutzer "Benutzer 1"; Schusses Erstellen, ändern, löschen; Objektklassen Gruppe "Benutzer 1"; Schusses Schreiben; objektklassenbenutzer; Attribut Kennwort "

Jetzt kann Benutzer 1 neue Benutzer und Gruppen in der Unternehmens Rechnung erstellen und die Kenn Wörter für vorhandene Benutzer festlegen. Benutzer 1 kann jedoch keine anderen Objektklassen erstellen und kann sich nicht auf Benutzer in anderen Containern auswirken, es sei denn, Benutzer 1 erhält Zugriff durch ACEs in den anderen Containern.

 

 




