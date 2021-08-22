---
description: Die folgenden Fehlercodes gelten speziell für die Setup-API.
ms.assetid: C4EB130F-2A83-4A14-BBA8-DB10225D0C0A
title: Fehlercodes (Setup-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c3955bd64f38946a59589259fc750892cfa9e84b3ef6e32ba2d9a5f6ca2244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887339"
---
# <a name="error-codes-setup-api"></a>Fehlercodes (Setup-API)

Die folgenden Fehlercodes gelten speziell für die Setup-API.



| INF-Analysefehler              | BESCHREIBUNG                                                                                                         |
|---------------------------------|---------------------------------------------------------------------------------------------------------------------|
| FEHLER \_ ERWARTETER \_ \_ ABSCHNITTSNAME  | Ein Abschnittsname wurde erwartet und nicht gefunden.                                                                          |
| FEHLER: \_ \_ FEHLERHAFTE \_ ABSCHNITTSNAMENSZEILE \_ | Der Abschnittsname hat nicht das richtige Format. (Beispiel: Ein Name, der nicht durch eine rechte Klammer () beendet \] wird. |
| NAME \_ DES \_ \_ FEHLERABSCHNITTS ZU \_ LANG | Der Abschnittsname hat die maximale Länge von MAX \_ SECT \_ NAME \_ LEN überschritten.                                               |
| ALLGEMEINE \_ \_ FEHLERSYNTAX          | Die allgemeine Syntax ist falsch.                                                                                    |



 



| INF-Laufzeitfehler         | BESCHREIBUNG                                                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FEHLER: \_ \_ FALSCHER INF-STIL \_   | Die INF-Datei hat nicht den im Funktionsaufruf angegebenen Typ. Dieser Fehler kann beispielsweise von der [**SetupOpenAppendInfFile-Funktion**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) zurückgegeben werden, wenn die INF-Datei für eine frühe Version von Windows. |
| FEHLERABSCHNITT \_ \_ NICHT \_ GEFUNDEN | Der Abschnitt wurde in der INF-Datei nicht gefunden.                                                                                                                                                                                                     |
| FEHLERZEILE \_ \_ NICHT \_ GEFUNDEN    | Die Zeile wurde im INF-Abschnitt nicht gefunden.                                                                                                                                                                                                     |



 

 

 



