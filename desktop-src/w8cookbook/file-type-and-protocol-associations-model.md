---
title: Dateityp und URI-Zuordnungs Modell
description: Dateityp und URI-Zuordnungs Modell
ms.assetid: 4DE7DD08-088A-4E09-B1C7-AE9033EA533D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c78540a072405aade01a9f94503999ad105d2078
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104039744"
---
# <a name="file-type-and-uri-associations-model"></a>Dateityp und URI-Zuordnungs Modell

## <a name="platforms"></a>Plattformen

 **Clients** -Windows 8  
**Server** -Windows Server 2012  



## <a name="description"></a>BESCHREIBUNG

Der Dateityp und das URI-Zuordnungs Modell wurden in Windows 8 geändert. Apps können nicht mehr Programm gesteuert als Standard Handler für einen Dateityp oder URI festgelegt werden. Stattdessen steuert der Benutzer nun immer, was der Standard Handler für einen Dateityp oder ein URI-Schema ist.

## <a name="manifestation"></a>Ausstrahlung

Welche Auswirkungen diese Änderung auf den Benutzer hat, hängt davon ab, wie die APP entworfen wurde, z. b.:

-   Viele apps überprüfen, ob Sie bei jedem Ausführen der Standardeinstellung sind. wenn dies nicht der Fall ist, wird der Benutzer aufgefordert, Sie als Standard festzulegen. Da apps jedoch nicht mehr genau Abfragen können, um zu bestimmen, welche App der Standard Handler für einen Dateityp oder ein URI-Schema ist, funktioniert keiner dieser Vorgänge.
-   Viele apps verfügen über ein Dialogfeld oder ein Menü, das bzw. das in das Installationsprogramm integriert ist, das die Dateitypen angibt, für die die APP als Standard fungieren soll. Da apps jedoch nicht mehr Programm gesteuert als Standard Handler für einen Dateityp oder ein URI-Schema festgelegt werden können, funktioniert das nicht mehr.

## <a name="mitigation"></a>Minderung

Es gibt mehrere Möglichkeiten, wie Benutzer diese Änderungen durchführen können:

-   Benutzer werden dazu aufgefordert, eine Standard-App zum Verarbeiten von Dateitypen, URI-Schemas oder beides auszuwählen, wenn keine Angabe erfolgt ist.
-   Benutzern wird die Option angeboten, Ihren Standard Handler nach der Installation neuer apps zu ändern, die einen Dateityp oder ein URI-Schema verarbeiten können.
-   Mithilfe der Systemsteuerung "Standardprogramme" können Benutzer Standardwerte für eine APP festlegen, oder für einen Dateityp, ein URI-Schema oder beides. Apps können mit der Systemsteuerung verknüpft werden.
-   Standardwerte können im Windows-Explorer geändert werden.

## <a name="solution"></a>Lösung

Aufgrund dieser Änderungen wird diese API-Anleitung bereitgestellt:

-   Die Funktionalität einiger Methodenaufrufe innerhalb der [iapplicationassociationregistration](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) -API wurde geändert und sollte nicht mehr verwendet werden.

    -   Rufen **Sie nicht** [queryappisdefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) / [queryappisdefaultall](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall) auf, um zu bestimmen, ob eine APP die Standardeinstellung ist.
    -   " [Querycurrentdefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault) " **nicht** aufzurufen, um zu bestimmen, welche app (sofern vorhanden) der aktuelle Standardwert ist
    -    [Setappisdefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefault) / [setappisdefaultall](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall) nicht zum Festlegen der Standard-App anrufen

-   Die Anleitung lautet wie folgt:

    -   **Nicht** Abfragen, um zu sehen, welche App der Standard Handler für Dateitypen oder URI-Schemas ist

    -   Versuchen **Sie nicht** , Änderungen im Standard Handler für Dateitypen oder URI-Schemas zu überwachen.

    -   Versuchen **Sie nicht** , eine App als Standard Handler für Dateitypen oder URI-Schemas festzulegen.

    -   Versuchen **Sie nicht** , Standardwerte für Dateitypen oder URI-Schemas innerhalb einer APP zu verwalten.

    -   **Verwenden** Sie die Systemsteuerung " [Standardprogramme festlegen](../shell/default-programs.md) ", wenn Sie Benutzern Ihrer APP den Zugriff auf die standardmäßige Verwaltungs Benutzeroberfläche gestatten möchten (die Verwaltungs Benutzeroberfläche innerhalb der APP wird nicht mehr unterstützt).

        -   Durch Aufrufen von [iapplicationassociationregistrationui:: launchadvancedassociationui](/windows/win32/api/shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) kann der Benutzer auf die System Steuerungs Seite "[Standardprogramme festlegen](../shell/default-programs.md)" für die angegebene App zugreifen.

## <a name="tests"></a>Tests

-   Testen Sie, ob apps ordnungsgemäß in der Systemsteuerung "Standardprogramme festlegen" registriert sind.
-   Testen Sie, ob apps ordnungsgemäß registriert werden, damit Sie in der openWith-Liste für die Dateitypen, URI-Schemas oder beides angezeigt werden, die Sie für die Behandlung von
-   Testen Sie, ob nach der Installation der APP neue APP-Benachrichtigungen angezeigt werden und der Benutzer einen Dateityp, ein URI-Schema oder beides aufruft, das Ihre APP für die Verarbeitung registriert hat.

## <a name="resources"></a>Ressourcen

-   [Bewährte Methoden für Dateityp-und URI-Zuordnungen in Windows 8-Desktop-Apps](/previous-versions/windows/desktop/legacy/cc144156(v=vs.85))
-   [Dateityp Zuordnungen und Präsentation der buildkonferenz](https://channel9.msdn.com/events/BUILD/BUILD2011/PLAT-282T)

 

 