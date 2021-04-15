---
description: Die folgenden Fehlercodes sind spezifisch für die Setup-API.
ms.assetid: C4EB130F-2A83-4A14-BBA8-DB10225D0C0A
title: Fehler Codes (Setup-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ce77fd224abb16c519f4b77fa93f775fe203d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485534"
---
# <a name="error-codes-setup-api"></a>Fehler Codes (Setup-API)

Die folgenden Fehlercodes sind spezifisch für die Setup-API.



| INF-Parsing-Fehler              | BESCHREIBUNG                                                                                                         |
|---------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Fehler beim \_ erwarteten \_ Abschnitts \_ Name.  | Ein Abschnitts Name wurde erwartet und wurde nicht gefunden.                                                                          |
| Fehler \_ hafte \_ Abschnitts \_ namens \_ Zeile | Der Abschnitts Name hatte nicht das richtige Format. (Ein Name wird z. b. nicht durch eine rechte eckige Klammer ( \] ) beendet. |
| der Fehler \_ Abschnitts \_ Name ist \_ zu \_ lang. | Der Abschnitts Name hat die maximale Länge von Max \_ . Sect- \_ Name len überschritten \_ .                                               |
| \_Allgemeine Fehler \_ Syntax          | Die allgemeine Syntax ist falsch.                                                                                    |



 



| INF-Laufzeitfehler         | BESCHREIBUNG                                                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fehler \_ beim \_ INF- \_ Stil.   | Die INF-Datei ist nicht vom Typ, der im Funktions aufrufsbefehl angegeben ist. Dieser Fehler kann z. b. von der [**setupopenappendinffile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) -Funktion zurückgegeben werden, wenn die INF-Datei für eine frühe Version von Windows vorgesehen war. |
| der Fehler \_ Abschnitt wurde \_ nicht \_ gefunden. | Der Abschnitt wurde in der INF-Datei nicht gefunden.                                                                                                                                                                                                     |
| Fehler \_ Zeile \_ nicht \_ gefunden.    | Die Zeile wurde im INF-Abschnitt nicht gefunden.                                                                                                                                                                                                     |



 

 

 



