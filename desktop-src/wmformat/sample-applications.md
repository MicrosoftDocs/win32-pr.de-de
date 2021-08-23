---
title: Windows Beispielanwendungen für das Medienformat-SDK
description: Windows Beispielanwendungen für das Medienformat-SDK
ms.assetid: 037741cb-c5fb-485f-bf62-79b5465abfe4
keywords:
- Windows Medienformat-SDK, Beispielanwendungen
- Digital Rights Management (DRM), Beispielanwendungen
- DRM (Digital Rights Management), Beispielanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 381f489cf00aa044a26e25438c3c2a724b23e1975e2de5712f695e4ddb6e8a0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547140"
---
# <a name="windows-media-format-sdk-sample-applications"></a>Windows Beispielanwendungen für das Medienformat-SDK

Der mit diesem SDK bereitgestellte Beispielcode hat die Form von Projekten für Microsoft Visual Studio 2005. Die meisten Beispiele befinden sich in C++, aber ManagedWMFSDKWrapper und ManagedMetadataEdit erfordern C#.

Diese Beispiele funktionieren nur, wenn das Windows Media Format SDK oder das Windows Player SDK installiert wurde.

Nutzungsinformationen für jedes Beispiel sind in einer readme.txt-Datei in jedem Beispielverzeichnis enthalten.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Samle</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Audioplayer</td>
<td>Gibt Windows Mediendateien ab, einschließlich DRM-geschützter Dateien. Sie wird über eine GRAFISCHE Benutzeroberfläche gesteuert, und befehle umfassen Play, Pause, Seek und Stop. Sie kann lokale Dateien oder Dateien wiedergeben, die aus dem Internet gelesen werden (einschließlich der Ausgabe in das Internet mithilfe des WMVNetWrite-Beispiels).
<blockquote>
[!Note]<br />
Die DRM-Teile dieses Beispiels werden in x64-basierten Versionen von Windows nicht unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>DRMHeader</td>
<td>DRMHeader ist eine Konsolenanwendung, die die <a href="/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor"><strong>IWMDRMEditor-Schnittstelle</strong></a> des Metadaten-Editors verwendet, um DRM-Attribute von Dateien zu lesen, ohne eine Verknüpfung mit der statischen DRM-Bibliothek herzustellen.
<blockquote>
[!Note]<br />
Dieses Beispiel wird für x64-basierte Versionen von Windows nicht unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>DRMShow</td>
<td>DRMShow ist eine Konsolenanwendung, die zeigt, wie <a href="wmformat-glossary.md"><em>DRM-Eigenschaften</em></a> einer Windows Mediendatei mithilfe der <strong>IWMDRMReader::GetDRMProperty-Methode</strong> gelesen werden. Dieses Beispiel veranschaulicht die Verwendung der <strong>IWMDRMReader::GetDRMProperty-Methode</strong> und der Eigenschaften, die aus dem DRM-Reader abgerufen werden können. Es wird nicht veranschaulicht, wie eine Lizenz für DRM-geschützte Inhalte erworben wird. Für dieses Beispiel muss die DRM-Stubbibliothek WMStubDRM.lib erstellt werden.<br/>
<blockquote>
[!Note]<br />
Dieses Beispiel wird für x64-basierte Versionen von Windows nicht unterstützt.
</blockquote>
<br/> Wenn Sie WMStubDRM.lib von Microsoft erwerben, wird der Bibliothek eine Anwendungssicherheitsstufe zugewiesen. Wenn die Sicherheitsstufe der bibliothek, die Sie erhalten, nicht ausreicht, um eine geschützte Datei wiederzuspielen, wird in diesem Beispiel ein Fehler angezeigt.<br/></td>
</tr>
<tr class="even">
<td>DirectShowInterop/DSCopy</td>
<td>Transcodiert eine oder mehrere Dateien mit dem DirectShow WM ASF Writer-Filter in eine ASF-Datei. Die Eingabedatei kann ein beliebiges komprimiertes oder unkomprimiertes Format sein, das von DirectShow unterstützt wird.</td>
</tr>
<tr class="odd">
<td>DirectShowInterop/DSPlay</td>
<td>Dieses Beispiel ist ein interaktiver Audio-/Videomediendateiplayer mit <a href="wmformat-glossary.md"><em>DRM-Unterstützung.</em></a> Der WM-ASF-Readerfilter von DirectShow wird verwendet, um Windows Mediendateien (ASF, WMA, WMV) ohne DRM-Schutz und Dateien wiederzuspielen, die DRM auf einer Ebene von 100 oder darunter verwenden. Weitere Informationen finden Sie unter readme.txt im Verzeichnis des Beispiels.</td>
</tr>
<tr class="even">
<td>DirectShowInterop/DSSeekFm</td>
<td>In diesem Beispiel wird veranschaulicht, wie Sie den DirectShow WM ASF-Leserfilter verwenden, um ASF-Inhalte in einem DirectShow-Filterdiagramm wiederzuspielen, und wie Sie die Framesucheunterstützung im Windows Media Format SDK verwenden.</td>
</tr>
<tr class="odd">
<td>Managed/WMFSDKWrapper</td>
<td>Diese verwaltete Assembly dient als Wrapper, der von Beispielen mit verwaltetem Code für den Zugriff auf einige Metadatenschnittstellen dieses SDK verwendet wird.</td>
</tr>
<tr class="even">
<td>Managed/MetadataEdit</td>
<td>Diese C#-Anwendung kann verwendet werden, um Metadaten aus Windows Mediendateien anzuzeigen und zu bearbeiten.</td>
</tr>
<tr class="odd">
<td>MetaDataEdit</td>
<td>Dies ist eine C++-Version der Anwendung Managed MetadataEdit.</td>
</tr>
<tr class="even">
<td>ReadFromStream</td>
<td>Dieses Konsolenanwendungsbeispiel zeigt, wie Daten aus <strong>IStream</strong> mit WMReader gelesen werden. <strong>Die IStream-Quelle</strong> wurde implementiert, um eine Datei im Windows Medienformat (WMA/WMV/ASF) zu verwenden.
<blockquote>
[!Note]<br />
In diesem Beispiel wird nicht gezeigt, wie die Medienbeispiele verarbeitet werden, die von WMReader stammen. Beispiele zum Verarbeiten von Audio-/Video- oder anderen Medienbeispielen finden Sie in anderen Beispielen, z. B. AudioPlayer, die im Windows Media Format SDK enthalten sind.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>UncompAVIToWMV</td>
<td>Dieses Konsolenanwendungsbeispiel zeigt den erforderlichen Code zum Komprimieren einer AVI-Datei in eine WMV-Datei. Es wird gezeigt, wie Sie Beispiele für Audio- und Videostreams aus mehreren AVI-Dateien zusammenführen und diese entweder in ähnlichen Datenströmen zusammenführen oder einen neuen Stream basierend auf dem Quellstreamprofil erstellen. Außerdem wird gezeigt, wie Sie einen beliebigen Stream erstellen, Multipasscodierung durchführen, SMPTE-Zeitcode hinzufügen und DRM-Schutz der Version 1 anwenden.</td>
</tr>
<tr class="even">
<td>WMGenProfile/exe</td>
<td>Dieses Beispiel wurde ab Version 7.1 aktualisiert. Es handelt sich jetzt um eine MFC-Dialogfeldanwendung. Das WMGenProfile-Beispiel veranschaulicht die Verwendung der statischen WMGenProfile-Bibliothek. Es dient auch als Tool für die Erstellung von Profilen. Dieses Tool ist für Entwickler gedacht, die mit dem Windows Medienformat vertraut sind. Die Benutzeroberfläche wurde nicht auf Benutzerfreundlichkeit getestet und ist nicht als Empfehlung zur Darstellung dieser Informationen für einen Benutzer gedacht.</td>
</tr>
<tr class="odd">
<td>WMGenProfile/lib</td>
<td>Das GenProfile-Bibliotheksbeispiel veranschaulicht die Erstellung von Profilen. Es wird gezeigt, wie Medientypen und Streams für verschiedene Streamtypen (Audio, Video, Skript, Bild, Dateiübertragung und Web) erstellt werden. Es wird nicht veranschaulicht, wie mit Systemprofilen gearbeitet wird oder wie Systemprofile in Profile konvertiert werden, die die Codecs der Windows Medienaudio- und Video 9-Serie angeben.</td>
</tr>
<tr class="even">
<td>WMProp</td>
<td>Diese Konsolenanwendung veranschaulicht, wie Attribute mithilfe des Metadaten-Editor-Objekts und der Profilinformationen vom Reader abgerufen werden.</td>
</tr>
<tr class="odd">
<td>WMStats</td>
<td>Diese Konsolenanwendung zeigt Reader- und Writer-Statistiken an. Mehrere WMStats-Instanzen können auch gleichzeitig auf einem Computer verwendet werden. Starten Sie eine Instanz als Server, um den Stream an das Netzwerk zu senden, und führen Sie dann eine zweite Instanz als Client aus, um zu überprüfen, ob der Server ordnungsgemäß gestreamt wird.</td>
</tr>
<tr class="even">
<td>WMSyncReader</td>
<td>Dieses Konsolenanwendungsbeispiel zeigt, wie Sie eine Mediendatei mithilfe von <strong>IWMSyncReader</strong> lesen, ohne zusätzlichen Thread zu erstellen oder Rückrufe zu verwenden. Die folgenden Features sind implementiert: Lesen von komprimierten oder dekomprimierten Beispielen<br/> Zeitbasierte Suche<br/> Framebasierte Suche<br/> <strong>Von IStream</strong> abgeleitete Quelle<br/></td>
</tr>
<tr class="odd">
<td>WMVAppend</td>
<td>Diese Konsolenanwendung verwendet zwei Windows Mediendateien für die Eingabe und versucht, eine Ausgabedatei mit dem Inhalt der ersten und dann der zweiten zu erstellen. Im Beispiel werden die Profile der beiden Eingabedateien verglichen, um sicherzustellen, dass sie ähnlich genug sind, um angefügt zu werden. Wenn dies nicht der Fall ist, wird eine Fehlermeldung angezeigt. Beispielsweise tritt eine Fehlermeldung auf, wenn eine Datei nur audio ist und die zweite eine Audiovideodatei ist oder wenn zwei Audiodateien unterschiedliche Bitraten aufweisen. Das Beispiel akzeptiert Datenquellen mit variabler Bitrate (VBR). Beim Vergleich der Profile der beiden VBR-Quellen ignoriert das Beispiel jedoch die durchschnittliche Bitratendifferenz, da zwei VBR-Datenströme unterschiedliche durchschnittliche Bitraten aufweisen, auch wenn sie mit demselben Profil erstellt wurden. WMVAppend kann die Spitzenbitrate von nicht eingeschränkten bitratenbasierten VBR-Datenströmen oder die Qualitätsstufe von qualitätsbasierten VBR-Streams nicht vergleichen, da diese Informationen in den Quelldateien nicht vorhanden sind. Daher liegt es in der Verantwortung des Benutzers sicherzustellen, dass zwei Quelldateien mit demselben Profil erstellt werden. Andernfalls können ungültige Inhalte erstellt werden.<br/></td>
</tr>
<tr class="even">
<td>WMVCopy</td>
<td>Dieses Beispiel zeigt den Code, der zum Kopieren einer WMV-Datei erforderlich ist. Es wird gezeigt, wie komprimierte Beispiele gelesen und geschrieben, Headerattribute und Skripts gelesen und Headerattribute geändert werden.</td>
</tr>
<tr class="odd">
<td>WMVNetWrite</td>
<td>Diese Konsolenanwendung zeigt, wie eine Windows Mediendatei über das Internet gestreamt wird. Für das Beispiel muss ein Port angegeben werden, und dann kann die Datei mit einem Player wiedergegeben werden.</td>
</tr>
<tr class="even">
<td>WMVRecompress</td>
<td>Diese Konsolenanwendung zeigt, wie eine WMV-Datei neu komprimiert wird. Es veranschaulicht das Lesen von unkomprimierten Beispielen, das Schreiben von unkomprimierten Beispielen und das Durchführen von Multipasscodierung, Mehrkanalausgabe und intelligenter Neukomprimierung.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Windows Media Format SDK**](about-the-windows-media-format-sdk.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 





