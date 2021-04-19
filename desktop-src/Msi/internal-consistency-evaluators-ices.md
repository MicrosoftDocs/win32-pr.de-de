---
description: Interne Konsistenz Auswertungen, auch als "ICES" bezeichnet, sind benutzerdefinierte Aktionen, die in VBScript, JScript oder als DLL oder exe geschrieben sind.
ms.assetid: 0789103d-ae34-46be-a9fb-093e066d6d4b
title: Interne Konsistenz Auswertung-ICES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77be6e2bf33bbe348acab45191782a211ea4663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373326"
---
# <a name="internal-consistency-evaluators---ices"></a>Interne Konsistenz Auswertung-ICES

Interne Konsistenz Auswertungen, auch als "ICES" bezeichnet, sind benutzerdefinierte Aktionen, die in VBScript, JScript oder als DLL oder exe geschrieben sind. Wenn diese benutzerdefinierten Aktionen ausgeführt werden, wird die Datenbank auf Einträge in Datenbankdaten Sätzen überprüft, die gültig sind, wenn Sie einzeln überprüft werden, dies kann jedoch zu fehlerhaftem Verhalten im Kontext der gesamten Datenbank führen. Beachten Sie, dass sich dies von der Validierung der einzelnen Datensätze mithilfe von " [**msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify)" unterscheidet.

Beispielsweise können in der [Component-Tabelle](component-table.md) mehrere Komponenten aufgeführt werden, die alle gültig sind, wenn Sie einzeln mit [**msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify)getestet werden. **Msiviewmodify** würde den Fehler jedoch nicht abfangen, wenn zwei Komponenten dieselbe [GUID](guid.md) wie der Komponenten Code verwenden. Die benutzerdefinierte Aktion [ICE08](ice08.md) ist darauf ausgelegt, zu überprüfen, ob die Komponenten Tabelle doppelte Komponenten Code-GUIDs enthält.

Benutzerdefinierte Ice-Aktionen geben vier Arten von Nachrichten zurück:

-   [**Fehler**](merge-errors.md) Fehlermeldungen melden Daten Bank Erstellung, die falsches Verhalten verursachen. Doppelte Komponenten-GUIDs bewirken beispielsweise, dass das Installationsprogramm fälschlicherweise Komponenten registriert.
-   **Warnungen** Warnmeldungen melden Daten Bank Erstellung, die in bestimmten Fällen falsches Verhalten verursachen. Warnungen können auch unerwartete Nebeneffekte der Daten Bank Erstellung melden. Wenn Sie z. b. denselben Eigenschaften Namen in zwei Bedingungen eingeben, die sich nur durch die Groß-/Kleinschreibung von Buchstaben im Namen unterscheiden. Da beim Installer die Groß-/Kleinschreibung beachtet wird, werden diese vom Installationsprogramm als verschiedene Eigenschaften behandelt.
-   **Fehler** Fehlermeldungen melden den Fehler bei der benutzerdefinierten Ice-Aktion. Der Fehler wird häufig durch eine Datenbank mit schwerwiegenden Problemen verursacht, die das Eis nicht selbst ausführen kann.
-   **Information** Informationsmeldungen liefern Informationen aus dem Eis und weisen nicht auf ein Problem mit der Datenbank hin. Häufig sind Sie Informationen zum Eis selbst, z. b. eine kurze Beschreibung. Sie können auch Statusinformationen bereitstellen, wenn die eisläufe ausgeführt werden.

Weitere Informationen finden Sie unter [using Internal Konsistenz Evaluators](using-internal-consistency-evaluators.md).

 

 



