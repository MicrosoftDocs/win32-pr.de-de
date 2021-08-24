---
description: Der Webauthentifizierungsbroker baut auf den gleichen Technologien auf, die Internet Explorer in Windows.
ms.assetid: 4BBAE30F-63AB-4AB0-9C99-016EF05220E8
title: Überlegungen für die Webseitenentwicklung
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22932f40d5268059fc30e97817de0b3671cee7447974b038ea4be12eedd76ed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883279"
---
# <a name="considerations-for-the-web-page-development"></a>Überlegungen für die Webseitenentwicklung

Der Webauthentifizierungsbroker baut auf den gleichen Technologien auf, die Internet Explorer in Windows. Aufgrund eines sehr speziellen Zwecks dieser Komponente wurden jedoch einige Features der Internet Explorer deaktiviert oder für eine bestimmte Konfiguration gesperrt. Darüber hinaus bietet der Webauthentifizierungsbroker einen dedizierten Ereignisprotokollierungskanal zur Behandlung von Problemen mit seiten, die er verarbeitet.

## <a name="internet-explorer-10-standard-document-mode"></a>Internet Explorer 10 Standarddokumentmodus

Der Webauthentifizierungsbroker zeigt alle Seiten im "IE10-Standardmodus" an. Sie können die Entwicklertools in Internet Explorer, um zu sehen, wie Ihre Seite unter verschiedenen Dokumentmodi funktioniert. Weitere Informationen zur Kompatibilität Internet Explorer 10 finden Sie in den MSDN-Themen für [Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/hh673527(v=vs.85)).

## <a name="disabled-and-locked-down-features"></a>Deaktivierte und gesperrte Features

Mehrere Features von Internet Explorer sind entweder vollständig deaktiviert oder auf bestimmte Werte gesperrt, die in den Internetoptionen des Betriebssystems nicht geändert werden können.



| Funktion                            | Status                                                                                                                                                                                                          |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anwendungscache-API ("AppCache") | Disabled                                                                                                                                                                                                        |
| Linkverlauf                       | Disabled                                                                                                                                                                                                        |
| Temporäre Dateien                    | Aktiviert                                                                                                                                                                                                         |
| Cookies                            | Sitzungscookies sind aktiviert. Persistente Cookies sind zulässig, unterliegen jedoch der automatischen Bereinigung, es sei denn, der Webauthentifizierungsbroker befindet sich im SSO-Modus. Weitere Informationen finden Sie im Abschnitt Einmaliges Anmelden. |
| Index-DATENBANK                           | Disabled                                                                                                                                                                                                        |
| DOM-Speicher                        | Disabled                                                                                                                                                                                                        |
| ActiveX                            | Disabled                                                                                                                                                                                                        |
| Dateidownloads                     | Disabled                                                                                                                                                                                                        |



 

## <a name="https-requirement"></a>HTTPS-Anforderung

Die erste URL, die eine Anwendung für die Kommunikation mit dem Onlineanbieter verwendet, muss HTTPS sein.

## <a name="dimension-for-different-window-sizes"></a>Dimension für verschiedene Fenstergrößen

Eine Windows 8-App kann in verschiedenen Größen angezeigt werden, z. B. vollbild, in einem Fenster mit geänderter Größe oder innerhalb eines Charms wie Share Charm. Je nachdem, in welchem Fensterlayout der Webauthentifizierungsbroker angezeigt wird, kann die Größe, mit der die Webseiten funktionieren müssen, unterschiedlich sein. Weitere Informationen finden Sie im Thema Richtlinien zum Ändern der Größe in schmale [Layouts](/previous-versions/windows/hh465371(v=win.10)) und im [Thema Richtlinien für die Freigabe von](/previous-versions/windows/hh465251(v=win.10)) Inhalten.

Die Webseite sollte CSS-Medienabfragen verwenden, um die Größe zu überprüfen, mit der sie arbeiten muss, und sich entsprechend zu gestalten. Die Seite sollte jedoch nicht auf der Grundlage der hier dokumentierten Pixel entworfen werden und in der Lage sein, auf unterschiedliche Größen zu skalieren. Die in diesem Dokument angegebenen Größen können sich in zukünftigen Betriebssystemversionen ändern.

Wenn eine Seite nicht alle Informationen in den zugewiesenen Bereich einpassen kann (z. B. eine lange Liste von Berechtigungen, die eine Anwendung anfing), stellt der Webauthentifizierungsbroker Bildlaufleisten zur Verfügung, damit der Benutzer bei Bedarf auf der Seite scrollen kann. Zoomen wird auch durch den Zoom für touchbasierte Geräte und STRG+Mausrad für Desktop- und Laptop-PCs bereitgestellt.

Um verschiedene Skalierungsfaktoren zu testen, verwenden Sie die in Microsoft Visual Studio Professional 2012 geladene [Webauthentifizierungsbroker-SDK-Beispiel-App,](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) die das Simulieren des Vollbild- und Größenvergrößerungszuständes ermöglicht.

Stellen Sie zusätzlich zu den oben dokumentierten Layouts sicher, dass Sie Ihre Seite in unterschiedlicher Bildschirmausrichtung (z. B. Hochformat und Querformat) sowie mit verschiedenen Lokal- und Sprachen sowie mit Barrierefreiheitsfeatures wie der Option "Alles vergrößern" testen.

Die verfügbaren Layouts sind:

-   [Vollbild](#full-screen)
-   [Fenster mit geänderter Größe](#resized)
-   [Charmansicht](#charm-view)
-   [Dateiauswahlansicht](#file-picker-view)

### <a name="full-screen"></a>Vollbildmodus

Für das Vollbildlayout sind die Webseitendimensionen:

-   Breite: 566 Pixel
-   Höhe: Bildschirmhöhe (abhängig von der Bildschirmauflösung)

Das folgende Beispiel zeigt die Webauthentifizierungsbroker-Benutzeroberfläche im Vollbildlayout.

![Beispiel für die Webauthentifizierungsbroker-Benutzeroberfläche im Vollbildlayout](images/wab-figure2.png)

### <a name="resized"></a>Geändert

Für ein Fenster mit geänderter Größe können die Webseitendimensionen wie die folgenden sein:

-   Breite: 260 Pixel
-   Höhe: Bildschirmhöhe (abhängig von der Bildschirmauflösung)

Das folgende Beispiel zeigt die Webauthentifizierungsbroker-Benutzeroberfläche in einem Fenster mit geänderter Größe auf der XBox-Webseite. Beachten Sie, dass sich die Webauthentifizierungsbroker-Benutzeroberfläche nur auf der rechten Seite der Bildschirmaufnahme befindet.

![Beispiel für die Benutzeroberfläche des Webauthentifizierungsbrokers in einem Fenster mit geänderter Größe](images/wab-figure3.png)

### <a name="charm-view"></a>Charmansicht

Für die Charm-Ansicht sind die Webseitendimensionen:

-   Breite: 566 Pixel
-   Höhe: Bildschirmhöhe (abhängig von der Bildschirmauflösung)

Das folgende Beispiel zeigt die Webauthentifizierungsbroker-Benutzeroberfläche in der Charm-Ansicht.

![Ein Beispiel zeigt die Webauthentifizierungsbroker-Benutzeroberfläche in der Charmansicht](images/wab-figure4.png)

### <a name="file-picker-view"></a>Dateiauswahlansicht

Für die Dateiauswahlansicht sind die Webseitendimensionen:

-   Breite: 566 Pixel
-   Höhe: Bildschirmhöhe (abhängig von der Bildschirmauflösung)

Das folgende Beispiel zeigt die Webauthentifizierungsbroker-Benutzeroberfläche in der Dateiauswahlansicht.

![Ein Beispiel zeigt die Webauthentifizierungsbroker-Benutzeroberfläche in der Dateiauswahlansicht.](images/wab-figure5.png)

## <a name="no-new-windows-by-default"></a>Standardmäßig keine neuen Fenster

Standardmäßig führen keine URLs dazu, dass ein neues Fenster geöffnet wird, sondern stattdessen im Fenster Webauthentifizierungsbroker angezeigt wird. Dies schließt die window.open-JavaScript-Methode, das Attribut "target" der Links oder ein, wenn der Benutzer den Strg+Klick-Mechanismus verwendet, um das Öffnen eines neuen Fensters zu erzwingen. Eine Ausnahme von dieser Regel ist, wenn eine Webseite einen Link als sicher deklariert, in einem Browser zu navigieren, wie unter Anpassen des Ziels der Links beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiel-App für das Webauthentifizierungsbroker-SDK](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
