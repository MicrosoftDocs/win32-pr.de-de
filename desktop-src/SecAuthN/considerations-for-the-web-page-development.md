---
description: Der Webauthentifizierungs Broker basiert auf den gleichen Technologien wie Internet Explorer in Windows.
ms.assetid: 4BBAE30F-63AB-4AB0-9C99-016EF05220E8
title: Überlegungen für die Webseitenentwicklung
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbe7e738616589afc4f7ba4f03d92a12207d189c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346008"
---
# <a name="considerations-for-the-web-page-development"></a>Überlegungen für die Webseitenentwicklung

Der Webauthentifizierungs Broker basiert auf den gleichen Technologien wie Internet Explorer in Windows. Aufgrund eines besonderen zwecks dieser Komponente wurden einige Features von Internet Explorer jedoch deaktiviert oder für eine bestimmte Konfiguration gesperrt. Außerdem bietet der Webauthentifizierungs Broker einen dedizierten Ereignis Protokollierungs Kanal, um Probleme mit den von ihm verarbeiteten Seiten zu beheben.

## <a name="internet-explorer-10-standard-document-mode"></a>Internet Explorer 10-Standarddokument Modus

Der Webauthentifizierungs Broker zeigt alle Seiten im "IE10-Standards-Modus" an. Sie können die Entwicklertools in Internet Explorer verwenden, um zu sehen, wie Ihre Seite unter verschiedenen Dokument Modi funktioniert. Weitere Informationen zur Kompatibilität mit Internet Explorer 10 finden Sie in den MSDN-Themen für [Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/hh673527(v=vs.85)).

## <a name="disabled-and-locked-down-features"></a>Deaktivierte und gesperrte Features

Einige Features von Internet Explorer sind entweder vollständig deaktiviert oder für bestimmte Werte gesperrt, die in den Internet Optionen des Betriebssystems nicht geändert werden können.



| Funktion                            | Status                                                                                                                                                                                                          |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anwendungscache-API ("AppCache") | Disabled                                                                                                                                                                                                        |
| Link Verlauf                       | Disabled                                                                                                                                                                                                        |
| Temporäre Dateien                    | Aktiviert                                                                                                                                                                                                         |
| Cookies                            | Sitzungs Cookies sind aktiviert. Persistente Cookies sind zulässig, unterliegen jedoch dem automatischen Bereinigung, es sei denn, der Webauthentifizierungs Broker befindet sich im SSO-Modus. Weitere Informationen finden Sie im Abschnitt einmaliges Anmelden. |
| Index-DB                           | Disabled                                                                                                                                                                                                        |
| Dom-Speicher                        | Disabled                                                                                                                                                                                                        |
| ActiveX                            | Disabled                                                                                                                                                                                                        |
| Dateidownloads                     | Disabled                                                                                                                                                                                                        |



 

## <a name="https-requirement"></a>HTTPS-Anforderung

Die erste URL, die eine Anwendung für die Kommunikation mit dem Online Anbieter verwendet, muss https sein.

## <a name="dimension-for-different-window-sizes"></a>Dimension für verschiedene Fenstergrößen

Eine Windows 8-App kann in verschiedenen Größen wie z. b. dem Vollbildmodus, einem Fenster mit Größenänderung oder in einem Charm wie dem Teilen-Charm angezeigt werden. Abhängig davon, in welchem Fenster Layout der Webauthentifizierungs Broker angezeigt wird, kann die Größe, mit der die Webseiten funktionieren, unterschiedlich sein. Weitere Informationen finden Sie im Thema [Richtlinien für die Größe der Größe in schmale Layouts](/previous-versions/windows/hh465371(v=win.10)) und in den [Richtlinien für die Freigabe von Inhalten](/previous-versions/windows/hh465251(v=win.10)) .

Auf der Webseite sollten CSS-Medien Abfragen verwendet werden, um die zu verwendende Größe zu überprüfen und sich entsprechend auszulagern. Die Seite sollte jedoch nicht basierend auf den genauen Pixeln entworfen werden, die hier dokumentiert sind, und Sie sollten in der Lage sein, auf unterschiedliche Größen zu skalieren. Die in diesem Dokument angegebenen Größen können in zukünftigen Betriebssystemversionen geändert werden.

Wenn eine Seite nicht alle Informationen im zugewiesenen Speicherplatz enthalten kann (z. b. eine lange Liste von Berechtigungen, die eine Anwendung anfordert), stellt der Webauthentifizierungs Broker Bild Lauf leisten bereit, damit der Benutzer bei Bedarf einen Bildlauf durchführen kann. Zoom wird auch durch Verkleinern von Zoom für Berührungs basierte Geräte und Strg + Mausrad für Desktop-und Laptop-PCs bereitgestellt.

Um verschiedene Skalierungsfaktoren zu testen, verwenden Sie die in Microsoft Visual Studio Professional 2012 geladene [Web Authentication Broker SDK-Beispiel-App](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) , die das Simulieren des voll Bild Status und der Größenänderung ermöglicht.

Stellen Sie zusätzlich zu den oben beschriebenen unterschiedlichen Layouts sicher, dass Sie Ihre Seite in unterschiedlicher Bildschirm Ausrichtung (z. b. Hochformat und Querformat) und unterschiedlichen Gebiets Schemata und Sprachen sowie mit Barrierefreiheits Features wie der Option "alles größere machen" aktivieren.

Die verfügbaren Layouts lauten:

-   [Vollbild](#full-screen)
-   [Fenstergröße geändert](#resized)
-   [Charm Ansicht](#charm-view)
-   [Dateiauswahl Ansicht](#file-picker-view)

### <a name="full-screen"></a>Vollbildmodus

Für das voll Bild Layout sind die Webseiten Dimensionen:

-   Breite: 566 Pixel
-   Height: Bildschirmhöhe (abhängig von der Bildschirmauflösung)

Das folgende Beispiel zeigt die Benutzeroberfläche des Webauthentifizierungs Brokers im voll Bild Layout.

![ein Beispiel für die Benutzeroberfläche des Webauthentifizierungs Brokers im voll Bild Layout](images/wab-figure2.png)

### <a name="resized"></a>Geändert

Bei einem Fenster, das in der Größe geändert wird, können die Webseiten Dimensionen wie folgt lauten:

-   Breite: 260 Pixel
-   Height: Bildschirmhöhe (abhängig von der Bildschirmauflösung)

Das folgende Beispiel zeigt die Webauthentifizierungs Broker-Benutzeroberfläche in einem Fenster, das in der Größe geändert wurde, auf der Xbox-Webseite. Beachten Sie, dass sich die Benutzeroberfläche des Webauthentifizierungs Brokers nur auf der rechten Seite der Bildschirmaufnahme befindet.

![ein Beispiel für die Webauthentifizierungs Broker-Benutzeroberfläche in einem Fenster, dessen Größe geändert wurde](images/wab-figure3.png)

### <a name="charm-view"></a>Charm Ansicht

In der Charm Ansicht sind die Webseiten Dimensionen:

-   Breite: 566 Pixel
-   Height: Bildschirmhöhe (abhängig von der Bildschirmauflösung)

Das folgende Beispiel zeigt die Webauthentifizierungs Broker-Benutzeroberfläche in der Charm Ansicht.

![ein Beispiel zeigt die Benutzeroberfläche des Webauthentifizierungs Brokers in der Charm Ansicht](images/wab-figure4.png)

### <a name="file-picker-view"></a>Dateiauswahl Ansicht

Für die Dateiauswahl Ansicht sind die Webseiten Dimensionen:

-   Breite: 566 Pixel
-   Height: Bildschirmhöhe (abhängig von der Bildschirmauflösung)

Das folgende Beispiel zeigt die Benutzeroberfläche des Webauthentifizierungs Brokers in der Dateiauswahl Ansicht.

![ein Beispiel zeigt die Benutzeroberfläche des Webauthentifizierungs Brokers in der Dateiauswahl Ansicht](images/wab-figure5.png)

## <a name="no-new-windows-by-default"></a>Standardmäßig keine neuen Fenster

Standardmäßig wird keine URL zum Öffnen eines neuen Fensters, sondern im Fenster "Webauthentifizierungs Broker" angezeigt. Dies umfasst die Windows. Open JavaScript-Methode, das "target"-Attribut der Hyperlinks oder, wenn der Benutzer den Strg + Klick-Mechanismus verwendet, um das Öffnen eines neuen Fensters zu erzwingen. Eine Ausnahme von dieser Regel ist, wenn eine Webseite einen Link als sicher für die Navigation in einem Browser deklariert, wie im Anpassungs Ziel der Hyperlinks beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiel-App für das Web Authentication Broker SDK](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
