---
title: Windows Media Format SDK-Beispielanwendungen
description: Windows Media Format SDK-Beispielanwendungen
ms.assetid: 037741cb-c5fb-485f-bf62-79b5465abfe4
keywords:
- Windows Medienformat-SDK, Beispielanwendungen
- Digital Rights Management (DRM), Beispielanwendungen
- DRM (Digital Rights Management), Beispielanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c778ef1613359f6f3dc6c08d918e32f2f29bade
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475006"
---
# <a name="windows-media-format-sdk-sample-applications"></a>Windows Media Format SDK-Beispielanwendungen

Der mit diesem SDK bereitgestellte Beispielcode liegt in Form von Projekten für Microsoft Visual Studio 2005 vor. Die meisten Beispiele befinden sich in C++, aber ManagedWMFSDKWrapper und ManagedMetadataEdit erfordern C#.

Diese Beispiele funktionieren nur, wenn das Windows Media Format SDK oder das Windows Player SDK installiert wurde.

Die Verwendungsinformationen für jedes Beispiel sind in einer readme.txt in jedem Beispielverzeichnis enthalten.




| Samle | BESCHREIBUNG | 
|-------|-------------|
| Audioplayer | Gibt Windows Mediendateien einschließlich DRM-geschützter Dateien wieder. Sie wird über eine grafische Benutzeroberfläche gesteuert, und befehle umfassen Wiedergabe, Pause, Suchen und Beenden. Sie können lokale Dateien oder Dateien wiederverlesen, die aus dem Internet gelesen werden (einschließlich der Ausgaben in das Internet mithilfe des WMVNetWrite-Beispiels).<blockquote>[!Note]<br />Die DRM-Teile dieses Beispiels werden in x64-basierten Versionen von Windows.</blockquote><br /> | 
| DRMHeader | DRMHeader ist eine Konsolenanwendung, die die <a href="/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor"><strong>IWMDRMEditor-Schnittstelle</strong></a> des Metadaten-Editors verwendet, um DRM-Attribute von Dateien zu lesen, ohne eine Verknüpfung mit der statischen DRM-Bibliothek zu erstellen.<blockquote>[!Note]<br />Dieses Beispiel wird für x64-basierte Versionen von Windows.</blockquote><br /> | 
| DRMShow | DRMShow ist eine Konsolenanwendung, die zeigt, wie <a href="wmformat-glossary.md"><em>DRM-Eigenschaften</em></a> einer Windows Media-Datei mithilfe der <strong>IWMDRMReader::GetDRMProperty-Methode gelesen</strong> werden. Dieses Beispiel veranschaulicht die Verwendung der <strong>IWMDRMReader::GetDRMProperty-Methode</strong> und der Eigenschaften, die vom DRM-Reader abgerufen werden können. Es wird nicht veranschaulicht, wie Sie eine Lizenz für DRM-geschützte Inhalte erwerben. Für dieses Beispiel muss die DRM-Stubbibliothek WMStubDRM.lib erstellt werden.<br /><blockquote>[!Note]<br />Dieses Beispiel wird für x64-basierte Versionen von Windows.</blockquote><br /> Wenn Sie wmstubDRM.lib von Microsoft erwerben, wird der Bibliothek eine Anwendungssicherheitsebene zugewiesen. Wenn die Sicherheitsstufe der Bibliothek, die Sie erhalten, nicht ausreicht, um eine geschützte Datei wieder zu spielen, wird in diesem Beispiel ein Fehler angezeigt.<br /> | 
| DirectShowInterop/DSCopy | Transcodiert eine oder mehrere Dateien mithilfe des DirectShow WM ASF Writer-Filters in eine ASF-Datei. Die Eingabedatei kann ein beliebiges komprimiertes oder nicht komprimiertes Format sein, das von DirectShow unterstützt wird. | 
| DirectShowInterop/DSPlay | Dieses Beispiel ist ein interaktiver Audio-/Videomediendateiplayer mit <a href="wmformat-glossary.md"><em>DRM-Unterstützung.</em></a> Sie verwendet den WM ASF-Readerfilter von DirectShow, um Windows-Mediendateien (ASF, WMA, WMV) ohne DRM-Schutz und Dateien mit DRM mit einer Ebene von mindestens 100 wieder abspielen. Weitere readme.txt sie im Verzeichnis des Beispiels. | 
| DirectShowInterop/DSSeekFm | In diesem Beispiel wird veranschaulicht, wie Sie den DirectShow WM ASF-Readerfilter verwenden, um ASF-Inhalte in einem DirectShow-Filterdiagramm wieder anzuzeigen, und wie Sie den Frame verwenden, der Unterstützung im Windows Media Format SDK sucht. | 
| Managed/WMFSDKWrapper | Diese verwaltete Assembly dient als Wrapper, der von Beispielen mit verwaltetem Code für den Zugriff auf einige Metadatenschnittstellen dieses SDK verwendet wird. | 
| Verwaltet/MetadatenEdit | Diese C#-Anwendung kann zum Anzeigen und Bearbeiten von Metadaten aus Windows Mediendateien verwendet werden. | 
| MetaDataEdit | Dies ist eine C++-Version der Anwendung Managed MetadataEdit. | 
| ReadFromStream | Dieses Konsolenanwendungsbeispiel zeigt, wie Daten aus <strong>IStream mit</strong> WMReader gelesen werden. <strong>Die IStream-Quelle</strong> wurde implementiert, um eine Datei im Windows Medienformat (WMA/WMV/ASF) zu verwenden.<blockquote>[!Note]<br />In diesem Beispiel wird nicht gezeigt, wie die Medienbeispiele aus WMReader zu verarbeiten sind. Beispiele zum Verarbeiten von Audio/Video oder anderen Arten von Medienbeispielen finden Sie in anderen Beispielen, z. B. AudioPlayer, die im Windows Media Format SDK enthalten sind.</blockquote><br /> | 
| UncompAVIToWMV | Dieses Konsolenanwendungsbeispiel zeigt den erforderlichen Code zum Komprimieren einer AVI-Datei in eine WMV-Datei. Es wird gezeigt, wie Sie Beispiele für Audio- und Videostreams aus mehreren AVI-Dateien zusammenführen und diese entweder in ähnlichen Streams zusammenführen oder einen neuen Stream basierend auf dem Quellstreamprofil erstellen. Außerdem wird gezeigt, wie Sie einen beliebigen Stream erstellen, multipass-Codierungen ausführen, SMPTE-Zeitcode hinzufügen und DRM-Schutz der Version 1 anwenden. | 
| WMGenProfile/exe | Dieses Beispiel wurde von Release 7.1 aktualisiert. Es handelt sich nun um eine MFC-Dialoganwendung. Das WMGenProfile-Beispiel veranschaulicht die Verwendung der statischen WMGenProfile-Bibliothek. Sie dient auch als Tool für die Erstellung von Profilen. Dieses Tool ist für Entwickler gedacht, die mit dem Windows Medienformat vertraut sind. Die Benutzeroberfläche wurde nicht auf Benutzerfreundlichkeit getestet und ist nicht als Empfehlung zur Präsentation dieser Informationen für einen Benutzer gedacht. | 
| WMGenProfile/lib | Das GenProfile-Bibliotheksbeispiel veranschaulicht die Erstellung von Profilen. Es wird gezeigt, wie Medientypen und Streams für verschiedene Streamtypen (Audio, Video, Skript, Bild, Dateiübertragung und Web) erstellt werden. Es wird nicht veranschaulicht, wie Sie mit Systemprofilen arbeiten oder Systemprofile in Profile konvertieren, die die Codecs Windows Medienaudio- und Video 9-Serie angeben. | 
| WMProp | Diese Konsolenanwendung veranschaulicht, wie Attribute mithilfe des Metadaten-Editorobjekts und der Profilinformationen aus dem Reader abgerufen werden. | 
| WMStats | Diese Konsolenanwendung zeigt Reader- und Writer-Statistiken an. Mehrere Instanzen von WMStats können auch gleichzeitig auf einem Computer verwendet werden. Starten Sie eine Instanz als Server, um den Stream an das Netzwerk zu senden, und führen Sie dann eine zweite Instanz als Client aus, um sicherzustellen, dass der Server ordnungsgemäß gestreamt wird. | 
| WMSyncReader | Dieses Konsolenanwendungsbeispiel zeigt, wie Sie eine Mediendatei <strong>mitHILFE von IWMSyncReader</strong> lesen, ohne zusätzliche Threads zu erstellen oder Rückrufe zu verwenden. Die folgenden Features werden implementiert: Lesen komprimierter oder dekomprimierten Beispiele<br /> Zeitbasierte Suche<br /> Framebasierte Suche<br /><strong>Von IStream</strong> abgeleitete Quelle<br /> | 
| WMVAppend | Diese Konsolenanwendung verwendet zwei Windows Mediendateien für die Eingabe und versucht, eine Ausgabedatei mit dem Inhalt der ersten datei zu erstellen, gefolgt von der zweiten. Im Beispiel werden die Profile der beiden Eingabedateien verglichen, um sicherzustellen, dass sie ähnlich genug sind, um angefügt zu werden. Wenn dies nicht der Fall ist, wird eine Fehlermeldung angezeigt. Eine Fehlermeldung tritt z. B. auf, wenn eine Datei nur Audio und die zweite eine Audiovideodatei ist oder wenn zwei Audiodateien unterschiedliche Bitraten haben. Im Beispiel werden VBR-Quellen (Variable Bit Rate) akzeptiert. Beim Vergleich der Profile der beiden VBR-Quellen ignoriert das Beispiel jedoch die durchschnittliche Bitratendifferenz, da zwei VBR-Datenströme unterschiedliche durchschnittliche Bitraten haben, selbst wenn sie mit demselben Profil erstellt wurden. WMVAppend kann die Spitzenbitrate von nicht konstraineden bitratenbasierten VBR-Datenströmen oder die Qualitätsstufe qualitätsbasierter VBR-Datenströme nicht vergleichen, da diese Informationen in den Quelldateien nicht vorhanden sind. Es liegt daher in der Verantwortung des Benutzers, sicherzustellen, dass zwei Quelldateien mit demselben Profil erstellt werden. Andernfalls kann ungültiger Inhalt erstellt werden.<br /> | 
| WMVCopy | Dieses Beispiel zeigt den Code, der zum Kopieren einer WMV-Datei erforderlich ist. Es wird gezeigt, wie Komprimierte Beispiele gelesen und geschrieben, Headerattribute und Skripts gelesen und Headerattribute geändert werden. | 
| WMVNetWrite | Diese Konsolenanwendung zeigt, wie Windows Mediendatei über das Internet gestreamt wird. Für das Beispiel muss ein Port angegeben werden, und die Datei kann dann mithilfe eines Players abgespielt werden. | 
| WMVRecompress | Diese Konsolenanwendung zeigt, wie Sie eine WMV-Datei erneut dekomprimieren. Es veranschaulicht das Lesen von unkomprimierten Beispielen, das Schreiben von nicht komprimierten Beispielen und das Verwenden von Multipasscodierung, Multikanalausgabe und intelligenter Rekomprimierung. | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Windows Media Format SDK**](about-the-windows-media-format-sdk.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 





