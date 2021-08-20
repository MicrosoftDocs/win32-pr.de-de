---
title: Modell für Dateityp- und URI-Zuordnungen
description: Modell für Dateityp- und URI-Zuordnungen
ms.assetid: 4DE7DD08-088A-4E09-B1C7-AE9033EA533D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aabcdb40bd38aeee24ee0e5d86f11651633a7eead1748810e8c1c6a846827690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028858"
---
# <a name="file-type-and-uri-associations-model"></a>Modell für Dateityp- und URI-Zuordnungen

## <a name="platforms"></a>Plattformen

 **Clients** – Windows 8  
**Server** – Windows Server 2012  



## <a name="description"></a>Beschreibung

Der Dateityp und das URI-Zuordnungsmodell wurden in Windows 8 geändert. Apps können sich nicht mehr programmgesteuert als Standardhandler für einen Dateityp oder URI festlegen. Stattdessen steuert der Benutzer jetzt immer, was der Standardhandler für einen Dateityp oder ein URI-Schema ist.

## <a name="manifestation"></a>Manifestation

Wie diese Änderung dem Benutzer präsentiert wird, hängt davon ab, wie die App entworfen wird, z. B.:

-   Viele Apps überprüfen bei jeder Ausführung, ob sie die Standardeinstellung sind. Andernfalls werden sie vom Benutzer aufgefordert, sie als Standard festzulegen. Da Apps jedoch nicht mehr genau abfragen können, um zu bestimmen, welche App der Standardhandler für einen Dateityp oder ein URI-Schema ist, funktioniert keiner dieser Vorgänge.
-   In vielen Apps ist ein Dialogfeld oder Menü integriert oder in ihrem Installationsprogramm enthalten, das die Dateitypen angibt, für die die App als Standard fungieren soll. Da Apps sich jedoch nicht mehr programmgesteuert als Standardhandler für einen Dateityp oder ein URI-Schema festlegen können, funktioniert dies nicht mehr.

## <a name="mitigation"></a>Minderung

Es gibt mehrere Möglichkeiten für Benutzer, diese Änderungen zu berücksichtigen:

-   Benutzer werden kontextabhängig aufgefordert, eine Standard-App für die Verarbeitung von Dateitypen, URI-Schemas oder beidem auszuwählen, wenn keines angegeben wurde.
-   Benutzern wird die Option angeboten, ihren Standardhandler nach der Installation neuer Apps zu ändern, die einen Dateityp oder ein URI-Schema verarbeiten können.
-   Mit der Systemsteuerung für Standardprogramme können Benutzer Standardwerte für eine App oder für einen Dateityp, ein URI-Schema oder beides festlegen. apps can link to the control panel (Apps können mit der Systemsteuerung verknüpft werden)
-   Standardwerte können über Windows Explorer geändert werden.

## <a name="solution"></a>Lösung

Aufgrund dieser Änderungen wird dieser API-Leitfaden bereitgestellt:

-   Die Funktionalität einiger Methodenaufrufe innerhalb der [IApplicationAssociationRegistration-API](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) hat sich geändert und sollte nicht mehr verwendet werden.

    -   **Rufen Sie** [queryAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) / [QueryAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall) nicht auf, um zu ermitteln, ob eine App die Standardeinstellung ist.
    -   Rufen Sie [queryCurrentDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault) **nicht** auf, um zu bestimmen, welche App (falls vorhanden) die aktuelle Standardeinstellung ist.
    -   **Rufen Sie** [SetAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefault) / [SetAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall) nicht auf, um die Standard-App festzulegen.

-   In Zukunft wird Folgendes als Leitfaden dienen:

    -   **Fragen Sie nicht** ab, welche App der Standardhandler für Dateitypen oder URI-Schemas ist.

    -   **Versuchen Sie nicht,** Änderungen im Standardhandler für Dateitypen oder URI-Schemas zu überwachen.

    -   **Versuchen Sie nicht,** eine App als Standardhandler für Dateitypen oder URI-Schemas festzulegen.

    -   **Versuchen Sie nicht,** Standardwerte für Dateitypen oder URI-Schemas innerhalb einer App zu verwalten.

    -   **Integrieren** Sie in die Systemsteuerung [Standardprogramme festlegen,](../shell/default-programs.md) wenn Sie Benutzern Ihrer App den Zugriff auf die Standardverwaltungsoberfläche gestatten möchten (die Verwaltungsoberfläche innerhalb der App wird nicht mehr unterstützt).

        -   Durch Aufrufen [von IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI](/windows/win32/api/shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) kann der Benutzer auf die Systemsteuerungsseite["Standardprogramme festlegen"](../shell/default-programs.md)für die angegebene App zugreifen.

## <a name="tests"></a>Tests

-   Testen, um zu überprüfen, ob Apps ordnungsgemäß in der Systemsteuerung "Standardprogramme festlegen" registriert sind
-   Testen Sie, ob Apps ordnungsgemäß registriert werden, damit sie in der OpenWith-Liste für die Dateitypen, URI-Schemas oder beides angezeigt werden, die sie für die Verarbeitung registrieren.
-   Testen Sie, ob neue App-Benachrichtigungen angezeigt werden, nachdem Ihre App installiert wurde und der Benutzer einen Dateityp, ein URI-Schema oder beides aufruft, für die Ihre App registriert ist.

## <a name="resources"></a>Ressourcen

-   [Bewährte Methoden für Dateityp- und URI-Zuordnungen in Windows 8 Desktop-Apps](/previous-versions/windows/desktop/legacy/cc144156(v=vs.85))
-   [Präsentation zu Dateitypzuordnungen und AutoPlay Build Conference](https://channel9.msdn.com/events/BUILD/BUILD2011/PLAT-282T)

 

 