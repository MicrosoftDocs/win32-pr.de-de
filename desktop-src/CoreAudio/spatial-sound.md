---
description: Microsoft Spatial Sound ist die Plattform auf Platt Form Ebene von Microsoft für räumliche Audiounterstützung auf Xbox, Windows und hololens 2 und ermöglicht sowohl das umschließen als auch das erhöhen (oberhalb oder unterhalb der Listener) Audiohinweise.
ms.assetid: 4F962F1A-CA4A-4018-BA97-516EA3519650
title: Raumklang für Entwickler
ms.custom: contperf-fy21q1
ms.topic: article
ms.date: 09/18/2020
ms.openlocfilehash: 9db3614ea7932af874da351e7a92980d51b90011
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/04/2021
ms.locfileid: "104564018"
---
# <a name="spatial-sound-for-developers"></a>Raumklang für Entwickler
> [!Note] 
> Diese Dokumentation richtet sich an eine Entwicklergruppe. Unterstützung für Endbenutzer zum Aktivieren von räumlichem Sound auf Ihrem Gerät finden Sie unter [How to Turn on Spatial Sound in Windows 10](https://support.microsoft.com/help/4563140/how-to-turn-on-spatial-sound-in-windows-10).

Microsoft Spatial Sound ist die Plattform auf Platt Form Ebene von Microsoft für räumliche Audiounterstützung auf Xbox, Windows und hololens 2 und ermöglicht sowohl das umschließen als auch das erhöhen (oberhalb oder unterhalb der Listener) Audiohinweise. Räumlicher Sound kann von Windows-Desktop-Apps (Win32) und universelle Windows-Plattform-Apps (UWP) auf unterstützten Plattformen genutzt werden. Die räumlichen Sound-APIs ermöglichen es Entwicklern, Audioobjekte zu erstellen, die Audiodaten von Positionen im 3D-Raum ausgeben. Dynamische Audioobjekte ermöglichen es Ihnen, Audiodaten aus einer beliebigen Position im Raum auszugeben, die sich im Laufe der Zeit ändern können. Sie können auch angeben, dass Audioobjekte Sound von einem von 17 vordefinierten statischen Kanälen (8.1.4.4) ausgeben, die echte oder virtualisierte Referenten darstellen können. Das tatsächliche Ausgabeformat wird vom Benutzer ausgewählt und kann aus räumlichen Microsoft-audioimplementierungen abstrahiert werden. die Audiodaten werden vorhandenen Referenten, Kopfhörern und Heim Netz Empfängern angezeigt, ohne dass Code oder Inhalts Änderungen erforderlich sind. Die Plattform unterstützt vollständig Dolby Atmos-Codierungs Codierungen sowohl für die HDMI-als auch für die Stereo-Haupt telefonausgabe, DTS: X für Kopfhörer und Windows Sonic for Kopfhörer Encoding für Stereo-Kopfhörer. Schließlich unterstützen räumliche Microsoft Spatial-Apps die systemmischungs Richtlinie, und ihre Audiodaten werden auch mit nicht räumlich-fähigen apps gemischt. Die räumliche Unterstützung von Microsoft ist auch in Media Foundation integriert. Apps, die Media Foundation verwenden, können Dolby Atmos-Inhalte ohne zusätzliche Implementierung erfolgreich wiedergeben.

Räumlicher Sound mit Microsoft Spatial Sound unterstützt die Verwendung von Fernsehgeräten, Heim Theatern und Sound leisten, die Dolby Atmos unterstützen. Räumlicher Sound kann auch mit einem beliebigen Paar von Kopfhörern verwendet werden, die der Consumer besitzen kann. Audiodaten werden von der Plattform mithilfe von Windows Sonic für Kopfhörer, Dolby Atmos für Kopfhörer oder DTS Headphone: X gerendert.


## <a name="enabling-microsoft-spatial-sound"></a>Aktivieren von Microsoft Spatial Sound

Unabhängig davon, ob es sich um einen Entwickler oder einen Consumer handelt, muss ein Benutzer Microsoft Spatial Sound auf seinem Gerät aktivieren, um räumlichkeits Geräusche zu hören.

### <a name="windows"></a>Windows
Auf Windows-PCs erfolgt dies über die Seite "Eigenschaften" für ein bestimmtes Audioausgabegerät. Wählen Sie in der **Sound** -Systemsteuerung ein Ausgabegerät aus, und klicken Sie auf **Geräteeigenschaften**. Wenn das Gerät im Abschnitt **räumlicher Sound** der Seite räumliche Töne unterstützt, können Sie in der Dropdown Liste **räumliches Sound Format** eines der verfügbaren Formate auswählen.

![räumliches Sound in der Sound-Systemsteuerung aktivieren](images/spatialsoundsettingswindows1.png)

Sie können auch den räumlichen Ton von Microsoft aktivieren, indem Sie in der Taskleiste mit der rechten Maustaste auf das **Volume** -Symbol klicken.

![räumlichen Sound über die Taskleiste aktivieren](images/spatialsoundsettingswindows2.png)

### <a name="xbox-one"></a>Xbox One
Auf Xbox One sind die räumlichen Funktionen von Microsoft für den Consumer immer verfügbar und werden über die app "Einstellungen" unter " **Allgemein-> Volume & Audioausgabe**" aktiviert.


![Aktivieren von räumlichem Sound auf Xbox One in der App "Einstellungen" ](images/audiosettingsbitstream.png)

Nachdem Dolby Atmos für das Heimtheater als "Bitstream-Format" ausgewählt wurde, wird die Unterstützung für dieses Format mithilfe der erweiterten Anzeige Identifikationsdaten (EDID) von HDMI geprüft. Wenn das-Format für das Gerät nicht unterstützt wird, wird dem Benutzer eine Fehlermeldung angezeigt. Beachten Sie, dass der Benutzer die Dolby Access-app herunterladen muss, wenn Sie diese Option zum ersten Mal auswählen.

Wenn ein anderes Format als "Bitstream-out" für die **-HDMI-Audiodatei** ausgewählt ist, wird die Dropdown Liste **Bitstream-Format** deaktiviert.

![räumliches Sound auf Xbox One in der App "Einstellungen" deaktiviert ](images/audiosettingsplain.png)

Wählen Sie Dolby Atmos für Kopfhörer, DTS-kopftelefon: X oder Windows Sonic für Kopfhörer aus der Dropdown Liste für den **Headset-Format** unter " **Headset-Audiodatei** "

![Aktivieren von räumlichem Sound für Kopfhörer auf Xbox One in der App "Einstellungen" ](images/audiosettingsheadphone.png)

Wenn Microsoft Spatial Sound nicht verfügbar ist (beispielsweise bei der Wiedergabe von eingebetteten Laptop-Stereo-Sprechern oder wenn der Benutzer Microsoft Spatial Sound nicht explizit aktiviert hat), wird die Anzahl der verfügbaren dynamischen Objekte, die von [**ispatialaudioclient:: getmaxdynamicobjectcount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) an eine Anwendung zurückgegeben werden, auf 0 festgelegt.

### <a name="hololens-2"></a>HoloLens 2

Auf hololens 2 ist Microsoft Spatial Sound standardmäßig aktiviert und verwendet die Hardware-DSP-Auslagerung, die speziell für Windows Sonic für Kopfhörer entworfen wurde.

## <a name="microsoft-spatial-sound-and-audio-middleware"></a>Räumliche Microsoft-Audio-und audiomiddleware

Viele APP-und Spielentwickler verwenden audiorendering-Engine-Lösungen von Drittanbietern, die häufig ausgereifte Tools zum Erstellen und übermitteln enthalten. Microsoft hat sich mit mehreren dieser Lösungsanbieter zusammengearbeitet, um Microsoft Spatial Sound in Ihren vorhandenen Erstellungs Umgebungen zu implementieren. Dies bedeutet häufig, dass die hier behandelten APIs aus der Ansicht der APP abstrahiert werden. Sie sind als DSP (Digital Signal Processing)-Plug-ins umschließt, die die APP instanziieren kann. Außerdem können Sie die audioimplementierer der App verwenden, um eine Mischung mit einem räumlichen skit-Format von Microsoft zu erhalten. Wenden Sie sich an Ihren Anbieter für audiomiddleware-Lösungen, um die Unterstützung für räumliche Daten von Microsoft zu erhalten.

## <a name="microsoft-spatial-sound-for-audio-renderers"></a>Räumlicher Sound von Microsoft für audiorenderer

Viele audiorenderer Zielen auf den [**iaudioclient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) -Endpunkt der Windows-audiositzungsapi (WASAPI) ab, auf dem die Anwendung Puffer gemischter Audiodaten mit gemischtem und formatierten Format an eine WASAPI-Audiosenke übergibt. die übermittelten Puffer werden dann für die Vermischung mit anderen Clients, der abschließenden Verarbeitung auf Systemebene und dem Rendering verwendet.

Räumliche räumliche Endpunkte von Microsoft werden als [**ispatialaudioclient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)implementiert, das viele Ähnlichkeiten mit **iaudioclient** aufweist. Es unterstützt *statische* Sound Objekte, die einen channelbereich bilden, mit Unterstützung für bis zu 8.1.4.4 Kanäle (8 Kanäle um den Listener – Links, rechts, zentriert, Links, rechts, Links, Links, rückwärts und zurück Center; 1 Low Frequency Effects-Kanal; 4 Kanäle über dem Listener; 4 Kanäle unterhalb des Listener). Außerdem werden *dynamische* Sound Objekte unterstützt, die beliebig in 3D-Raum positioniert werden können.

Das allgemeine Implementierungs Codierungs Muster für **ispatialaudioclient** lautet wie folgt:

-   Erstellen Sie statische und/oder dynamische Audioobjekte.
-   Die Audiopuffer der einzelnen Objekte werden von jedem Frame Feed, damit das System Sie wieder erzeugen kann.
-   Aktualisieren Sie die 3D-Positionen von dynamischen Objekten bei Bedarf – so oft (oder nur selten), wie die APP wünscht.

Beachten Sie, dass das aktuelle Ausgabeformat (Sprecher oder Kopfhörer) vorliegt. Windows Sonic für Kopfhörer, Dolby Atmos oder DTS Headphone: X) wird aus der obigen Implementierung abstrahiert – der App-Entwickler kann sich auf den räumlichen Sound konzentrieren, ohne sich auf der Grundlage des Formats drehen zu müssen. Apps, deren Verhalten auf Grundlage des Ausgabeformats abweichen soll, können das verwendete Format Abfragen, aber die Abstraktion bedeutet, dass eine APP nicht erforderlich ist, um diese Formate zu verarbeiten.

## <a name="microsoft-spatial-sound-integration-with-audio-renderers"></a>Integration von Microsoft Spatial Sound in audiorenderer

Da es sich bei [**ispatialaudioclient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) um eine Audiosenke handelt, die Daten verbraucht, bietet ein audiorenderer mehrere Optionen für die Interaktion mit und die Bereitstellung von Audiodaten. Es gibt drei häufig verwendete Integrations Techniken (und für Titel, die audiomiddleware verwenden, sehen Sie möglicherweise äquivalente Plug-ins, die basierend auf diesen Optionen verfügbar gemacht werden):

-   **7.1.4 Panner und Mastering Voice**: Renderer, die bereits 7,1-Endpunkte unterstützen, können die Unterstützung für die vier zusätzlichen Höhen Kanäle hinzufügen, die vom statischen Channeltyp **ispatialaudioclient** unterstützt werden. Alle Kanal schwenken, die Sie zuvor durchgeführt haben (wahrscheinlich bereits x-, y-, z-Koordinaten genutzt), können aktualisiert werden, um jetzt diese Höhen Kanäle einzubeziehen. Dies bietet häufig die geringste Unterbrechung für Renderer und App-audioworkflows, Signal, Fluss und Mischungs Steuerung. Über Kopfhörer: Beachten Sie, dass die vollständige App-Mischung räumlich – wird, sodass selbst Stereo Musik als "externalized" vom Listener wahrgenommen werden kann.
-   Verwalten Sie **einen vorhandenen Endpunkt, und fügen Sie einen 7.1.4 Bus (und Panner) hinzu**: einige Titel können zwei Endpunkte verwalten: Ihren vorhandenen Stereo-WASAPI-Endpunkt (für "direkt zu Ohren"-Inhalte, die nicht für die räumenalisierung vorgesehen sind) neben einem statischen **ispatialaudioclient** -Kanal, der 7.1.4 unterstützt (oder sogar bis 8.1.4.4). Das Verwalten von Interaktionen zwischen zwei Mischungen stellt natürlich zusätzliche Herausforderungen für Inhalts Ersteller dar, obwohl die Synchronisierung beibehalten wird, da sowohl die WASAPI-als auch die Isac-Instanzen, die zu einem bestimmten Zeitpunkt aktiv sind, die gleiche Puffergröße und-Uhrzeit für die
-   **Verwenden dynamischer Sound Objekte für bestimmte Stimmen oder Unterverzeichnisse**: das Angebot ist vielleicht die ausführlichste/exakte Positionierung, aber potenziell eine Mischungs Deckkraft zu schaffen. diese Vorgehensweise umfasst die Verwendung dynamischer Sound Objekte von **ispatialaudioclient** . Beachten Sie, dass die Metadaten und der Audiopuffer an den Renderer übermittelt werden, sodass diese Sounds für den Rest der APP-Mischung nicht transparent sind. Da es nur eine begrenzte Anzahl verfügbarer dynamischer Sound Objekte gibt, muss der Renderer in Erwägung gezogen werden, priorisierungstechniken zu implementieren – Culling, Sound Co-Location, Blending in den statischen kanalB usw. Spiele haben dieses Verfahren häufig für einzelne "Hero"-Sounds eingesetzt, z. b. einen Helikopter, der über dem Listener bewegt wird.

Renderer können auch zwischen diesen Ansätzen gemischt werden.

## <a name="microsoft-spatial-sound-runtime-resource-implications"></a>Auswirkungen auf die räumliche Lauf Zeit Ressource von Microsoft

Unter Windows und Xbox variiert die Anzahl der verfügbaren Stimmen basierend auf dem verwendeten Format. Dolby Atmos-Formate unterstützen 32 aktive Objekte insgesamt (Wenn also ein 7.1.4-Kanaltyp verwendet wird, können 20 zusätzliche dynamische Sound Objekte aktiv sein). Windows Sonic for Kopfhörer unterstützt 128 aktive Objekte, bei denen der LFE-Kanal (Low Frequency Effects) tatsächlich nicht als Objekt gezählt wird. Wenn also ein 8.1.4.4-channelbett verwendet wird, können auch 112 dynamische Sound Objekte aktiv sein.

Bei universelle Windows-Plattform-apps, die auf Xbox One-Spielkonsolen ausgeführt werden, wird die Echtzeit-Codierung (für Dolby Atmos für das Heimtheater, Dolby Atmos für Kopfhörer, DTS-Kopfhörer: X und Windows Sonic für Kopfhörer) in Hardware ohne CPU-Kosten ausgeführt.

| Format                       | Maximale Anzahl statischer Objekte (kanalB) | Maximale Anzahl dynamischer Objekte <br> Xbox One | Maximale Anzahl dynamischer Objekte <br> Windows | Maximale Anzahl dynamischer Objekte <br> HoloLens 2
|------------------------------|----------------------------------|-------------------------------------------|------------------------------------------|------------------------------------------|
| Dolby Atmos (HDMI)           | 12 (7.1.4)                       | 20                                        | 20                                       | Nicht verfügbar |
| Dolby Atmos (Kopfhörer & integrierten Referenten)     | 17 (8.1.4.4)                     | 16                                        | 16                                       | Nicht verfügbar |
| DTS-kopftelefon: X (Kopfhörer) | 17 (8.1.4.4)        | 16                                        | 32                                      | Nicht verfügbar |
| Windows-Sonic für Kopfhörer | 17 (8.1.4.4)        | 15                                        | 112                                      | 31 |


Apps sollten auch die folgenden Auswirkungen auf die Ressource berücksichtigen:

-   **Storage/Disk Bandwidth**: lineare Inhalte, die vorab für 7.1.4 erstellt wurden, sind in der Regel größer als 7,1 lineare Inhalte (obwohl perzeptive Codecs bereits häufig von der Kanal Korrelation profitieren, um dies weitaus weniger als 50% mehr tatsächliche Kanäle von Audiodaten zu ermöglichen)
-   **Weitere Kosten für die Verarbeitung digitaler Signale**: einige zuvor globale Effekte können jetzt pro dynamischem Sound Objekt instanziierten werden. Außerdem möchten einige Inhalts Ersteller möglicherweise einige DSP-Effekte aktualisieren, um zusätzliche Kanäle zu unterstützen oder Sie eindeutig zu verwenden.

## <a name="microsoft-spatial-sound-and-sound-spatialization-cues"></a>Microsoft Spatial Sound und Sound spatialization-Hinweise

Der räumliche Ton von Microsoft konzentriert sich auf die Simulation der Sound Positionierung in einer idealisierten Kugel um den Listener. Windows Sonic for Kopfhörer, DTS Headphone: X und Dolby Atmos implementieren die sprecherzuordnung und die Virtualisierung zu den Kopfhörern, aber beachten Sie, dass viele andere Aspekte der Sound Spatial-Simulation, die bereits in der Regel in der Inhalts Ersteller-aktivierten Weise implementiert sind, vorhandenen Engines verbleiben. Inhalts Ersteller verwenden weiterhin die vorhandenen Spiel Tools und-Prozesse, die Sie zuvor für solche räumlichen Hinweise verwendet haben, wie z. b. Doppler, Entfernungs basierte Dämpfung und Filterung, Okklusion und Behinderung und Umgebungs übereinlassung.

## <a name="additional-resources"></a>Weitere Ressourcen

-   [Microsoft Spatial Sound Samples-GitHub-Repository](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio)
-   Dolby bietet eine Reihe von Support Ressourcen im Zusammenhang mit Dolby Atmos und der Dolby Access-app unter <https://developer.dolby.com> .

## <a name="spatial-sound-interfaces"></a>Räumliche Sound Schnittstellen



| Schnittstelle                                                                              | BESCHREIBUNG                                                                                                                    |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**Ispatialaudioclient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)                                     | Ermöglicht einem Client das Erstellen von Audiostreams, die Audiodaten aus einer Position im 3D-Raum ausgeben.                                          |
| [**Ispatialaudioobject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)                                     | Stellt ein Objekt dar, das Audiodaten bereitstellt, die von einer Position im 3D-Raum in Relation zum Benutzer gerendert werden sollen.                |
| [**Ispatialaudioobjectrenderstream**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream)             | Stellt Methoden bereit, mit denen ein räumlicher audioobjektstream gesteuert werden kann, einschließlich starten, beenden und Zurücksetzen des Streams. |
| [**Ispatialaudioobjectrenderstreamnotify**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstreamnotify) | Stellt Benachrichtigungen für räumliche audioclients bereit, um auf Änderungen im Zustand eines ispatialaudioobjectrenderstream zu reagieren.     |



 

> [!Note]  
> Wenn Sie die [**ispatialaudioclient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) -Schnittstellen für einen Xbox One Development Kit (XDK)-Titel verwenden, müssen Sie zuerst **enablespatialaudio** aufrufen, bevor Sie [**immdeviceenumerator:: enumaudioendpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) oder [**immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)aufrufen. Wenn dies nicht der Fall ist, wird ein E \_ nointerface-Fehler vom aufzurufenden Aktivierungsbefehl zurückgegeben. **Enablespatialaudioist** nur für XDK-Titel verfügbar und muss nicht für universelle Windows-Plattform apps, die auf Xbox One ausgeführt werden, oder für nicht-Xbox one-Geräte aufgerufen werden.

 

## <a name="spatial-sound-structures"></a>Räumliche Sound Strukturen



| Struktur                                                                                                 | BESCHREIBUNG                                                                  |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Spatialaudioobjectrenderstreamactivationparametriams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) | Stellt Aktivierungs Parameter für einen räumlichen audiodatenstream dar.          |
| [**Spatialaudioclientactivationparameams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioclientactivationparams)                          | Stellt optionale Aktivierungs Parameter für einen räumlichen audiodatenstream dar. |



 

## <a name="spatial-sound-enumerations"></a>Räumliche audioenumerationen



| Enumeration                                | Beschreibung                                   |
|--------------------------------------------|-----------------------------------------------|
| [**Audioobjecttype**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) | Gibt den Typ eines ispatialaudioobject an. |



 

 

 



