---
title: Beispielanwendungen für das Windows Media-Format-SDK
description: Beispielanwendungen für das Windows Media-Format-SDK
ms.assetid: 037741cb-c5fb-485f-bf62-79b5465abfe4
keywords:
- Windows Media-Format-SDK, Beispielanwendungen
- Digital Rights Management (DRM), Beispielanwendungen
- DRM (Digital Rights Management), Beispielanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ce7a9baf53c289e9420cf3c226bf21a3c6bd16
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474868"
---
# <a name="windows-media-format-sdk-sample-applications"></a>Beispielanwendungen für das Windows Media-Format-SDK

Der Beispielcode, der mit diesem SDK bereitgestellt wird, ist in Form von Projekten für Microsoft Visual Studio 2005. Die meisten Beispiele sind in C++, aber managedwmf sdkwrapper und ManagedMetadataEdit erfordern c#.

Diese Beispiele können nur verwendet werden, wenn das Windows Media-Format-SDK oder das Windows Player SDK installiert wurde.

Verwendungs Informationen für die einzelnen Beispiele sind in einer readme.txt-Datei in jedem Beispiel Verzeichnis enthalten.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Samle</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Audioplayer</td>
<td>Gibt Windows Media-Dateien einschließlich von DRM-geschützten Dateien wieder. Sie wird über eine grafische Benutzeroberfläche gesteuert, und die Befehle umfassen abspielen, anhalten, suchen und anhalten. Es können lokale Dateien oder Dateien wiedergegeben werden, die aus dem Internet gelesen wurden (einschließlich der Ausgabe im Internet mithilfe des wmvnetwrite-Beispiels).
<blockquote>
[!Note]<br />
Die DRM-Teile dieses Beispiels werden auf x64-basierten Versionen von Windows nicht unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>DrmHeader</td>
<td>DrmHeader ist eine Konsolenanwendung, die die <a href="/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor"><strong>iwmdrmeditor</strong></a> -Schnittstelle des Metadaten-Editors zum Lesen von DRM-Attributen von Dateien verwendet, ohne mit der statischen DRM-Bibliothek zu verknüpfen.
<blockquote>
[!Note]<br />
Dieses Beispiel wird in x64-basierten Versionen von Windows nicht unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Drmshow</td>
<td>Drmshow ist eine Konsolenanwendung, die zeigt, wie <a href="wmformat-glossary.md"><em>DRM</em></a> -Eigenschaften einer Windows Media-Datei mithilfe der Methode " <strong>iwmdrmreader:: getdrmproperty</strong> " gelesen werden. Dieses Beispiel veranschaulicht die Verwendung der <strong>iwmdrmreader:: getdrmproperty</strong> -Methode und die Eigenschaften, die vom DRM-Reader abgerufen werden können. Es wird nicht gezeigt, wie Sie eine Lizenz für DRM-geschützte Inhalte erwerben. Für dieses Beispiel ist die DRM-Stub-Bibliothek wmstubdrm. lib erforderlich, um zu erstellen.<br/>
<blockquote>
[!Note]<br />
Dieses Beispiel wird in x64-basierten Versionen von Windows nicht unterstützt.
</blockquote>
<br/> Wenn Sie wmstubdrm. lib von Microsoft abrufen, wird der Bibliothek eine Anwendungs Sicherheitsstufe zugewiesen. Wenn die Sicherheitsstufe der Bibliothek, die Sie erhalten, nicht ausreichen, um eine geschützte Datei wiederzugeben, wird in diesem Beispiel ein Fehler angezeigt.<br/></td>
</tr>
<tr class="even">
<td>Directshowinterop/dscopy</td>
<td>Transcodiert eine oder mehrere Dateien in eine ASF-Datei mithilfe des DirectShow WM ASF Writer-Filters. Die Eingabedatei kann jedes komprimierte oder nicht komprimierte Format aufweisen, das von DirectShow unterstützt wird.</td>
</tr>
<tr class="odd">
<td>Directshowinterop/dsplay</td>
<td>Dieses Beispiel ist ein interaktiver Audiodatei-Player mit <a href="wmformat-glossary.md"><em>DRM</em></a> -Unterstützung. Er verwendet den WM-"WM-ASF-Reader"-Filter von DirectShow, um Windows Media-Dateien (ASF, WMA, WMV) ohne DRM-Schutz und Dateien wiederzugeben, die DRM auf der Ebene 100 oder niedriger verwenden. Weitere Informationen finden Sie unter readme.txt im Verzeichnis des Beispiels.</td>
</tr>
<tr class="even">
<td>Directshowinterop/dsseekfm</td>
<td>In diesem Beispiel wird veranschaulicht, wie Sie den DirectShow-WM-,-und-Filter zum Wiedergeben von ASF-Inhalten in einem DirectShow-Filter Diagramm verwenden. Außerdem wird erläutert, wie Sie den Frame suchen, der Unterstützung im Windows Media SDK</td>
</tr>
<tr class="odd">
<td>Verwaltet/WMF sdkwrapper</td>
<td>Diese verwaltete Assembly dient als Wrapper, der von Beispielen für verwalteten Code für den Zugriff auf einige Metadatenschnittstellen dieses SDK verwendet wird.</td>
</tr>
<tr class="even">
<td>Verwaltet/MetadataEdit</td>
<td>Diese c#-Anwendung kann verwendet werden, um Metadaten aus Windows-Mediendateien anzuzeigen und zu bearbeiten.</td>
</tr>
<tr class="odd">
<td>MetaDataEdit</td>
<td>Dies ist eine C++-Version der verwalteten MetadataEdit-Anwendung.</td>
</tr>
<tr class="even">
<td>"Read FromStream"</td>
<td>In diesem Beispiel für eine Konsolenanwendung wird gezeigt, wie Daten aus <strong>IStream</strong> mit wmreader gelesen werden. Die <strong>IStream</strong> -Quelle wurde implementiert, um eine Datei im Windows Media-Format (WMA/WMV/ASF) zu verwenden.
<blockquote>
[!Note]<br />
In diesem Beispiel wird nicht gezeigt, wie die aus wmreader ausgehenden Medien Beispiele verarbeitet werden. Beispiele zum Verarbeiten von Audiodateien/Videos oder anderen Typen von Medien Beispielen finden Sie in den anderen Beispielen, z.b. Audioplayer, die im Windows Media-Format-SDK enthalten sind.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Uncompavitowmv</td>
<td>In diesem Beispiel für eine Konsolenanwendung wird der erforderliche Code zum Komprimieren einer AVI-Datei in eine WMV-Datei gezeigt. Es zeigt, wie Sie Beispiele für Audiodaten und Videostreams aus verschiedenen AVI-Dateien zusammenführen und entweder in ähnliche Streams zusammenführen oder basierend auf dem Quelldaten Strom Profil einen neuen Stream erstellen. Außerdem wird gezeigt, wie ein beliebiger Stream erstellt, Multipass-Codierung ausgeführt, SMPTE-Zeit Code hinzugefügt und der DRM-Schutz auf Version 1 angewendet wird.</td>
</tr>
<tr class="even">
<td>Wmgenprofil/exe</td>
<td>Dieses Beispiel wurde von Version 7,1 aktualisiert. Es ist jetzt eine MFC-Dialog Feld Anwendung. Das wmgenprofile-Beispiel veranschaulicht die Verwendung der statischen wmgenprofile-Bibliothek. Es dient auch als Tool für die Erstellung von Profilen. Dieses Tool ist für Entwickler bestimmt, die mit dem Windows Media-Format vertraut sind. Die Benutzeroberfläche wurde nicht für die Benutzeroberfläche getestet und ist nicht als Empfehlung zur Darstellung dieser Informationen für einen Benutzer gedacht.</td>
</tr>
<tr class="odd">
<td>Wmgenprofil/lib</td>
<td>Das Beispiel für die genprofile-Bibliothek veranschaulicht die Erstellung von Profilen. Es wird gezeigt, wie Medientypen und Streams für verschiedene Streamtypen (Audiodaten, Videos, Skripts, Bilder, Dateiübertragungen und Web) erstellt werden. Es wird nicht gezeigt, wie Sie mit Systemprofilen arbeiten oder Systemprofile in Profile konvertieren, die die Codecs für die Windows Media Audio-und Video 9-Serie angeben.</td>
</tr>
<tr class="even">
<td>Wmprop</td>
<td>Diese Konsolenanwendung veranschaulicht, wie Attribute mithilfe des Metadateneditor-Objekts und der Profilinformationen des Readers abgerufen werden.</td>
</tr>
<tr class="odd">
<td>Wmstats</td>
<td>Diese Konsolenanwendung zeigt Reader-und Writer-Statistiken an. Mehrere Instanzen von wmstats können auch gleichzeitig auf einem Computer verwendet werden. Starten Sie eine Instanz als Server, um den Datenstrom an das Netzwerk zu senden, und führen Sie dann eine zweite Instanz als Client aus, um zu überprüfen, ob der Server ordnungsgemäß Streaming.</td>
</tr>
<tr class="even">
<td>Wmsynkreader</td>
<td>In diesem Beispiel für eine Konsolenanwendung wird gezeigt, wie eine Mediendatei mithilfe von <strong>iwmsynanader</strong> gelesen wird, ohne dass ein zusätzlicher Thread erstellt oder Rückrufe verwendet werden. Die folgenden Features werden implementiert: Lesen von komprimierten oder dekomprimierten Beispielen<br/> Zeitbasierte Suche<br/> Frame basiertes suchen<br/> Von <strong>IStream</strong> abgeleitete Quelle<br/></td>
</tr>
<tr class="odd">
<td>Wmvappend</td>
<td>Diese Konsolenanwendung nimmt zwei Windows Media-Dateien für die Eingabe an und versucht, eine Ausgabedatei mit dem Inhalt der ersten, gefolgt von der zweiten, zu erstellen. Im Beispiel werden die Profile der beiden Eingabedateien verglichen, um sicherzustellen, dass Sie so ähnlich sind, dass Sie angefügt werden. Wenn dies nicht der Fall ist, wird eine Fehlermeldung angezeigt. Beispielsweise tritt eine Fehlermeldung auf, wenn eine Datei nur Audiodaten und das zweite eine audiovideodatei ist oder wenn zwei Audiodateien unterschiedliche Bitraten aufweisen. Das Beispiel akzeptiert VBR-Quellen (Variable Bitrate). Beim Vergleich der Profile der beiden VBR-Quellen ignoriert das Beispiel die durchschnittliche Bitrate Differenz, da zwei VBR-Streams verschiedene durchschnittliche Bitraten aufweisen, auch wenn Sie mit demselben Profil erstellt wurden. Wmvappend kann die Spitzen Bitrate von nicht eingeschränkten Bitrate-basierten VBR-Streams oder die Qualitätsstufe von Qualitäts basierten VBR-Streams nicht vergleichen, da diese Informationen nicht in den Quelldateien vorhanden sind. Daher liegt es in der Verantwortung des Benutzers, sicherzustellen, dass zwei Quelldateien mit demselben Profil erstellt werden. Andernfalls kann ein ungültiger Inhalt erstellt werden.<br/></td>
</tr>
<tr class="even">
<td>Wmvcopy</td>
<td>Dieses Beispiel zeigt den Code, der zum Kopieren einer WMV-Datei erforderlich ist. Es wird gezeigt, wie komprimierte Beispiele, Lese Header Attribute und Skripts gelesen und geschrieben und Header Attribute geändert werden.</td>
</tr>
<tr class="odd">
<td>Wmvnetwrite</td>
<td>Diese Konsolenanwendung zeigt, wie eine Windows Media-Datei über das Internet gestreamt wird. Für das Beispiel muss ein Port angegeben werden, und anschließend kann die Datei mit einem Player abgespielt werden.</td>
</tr>
<tr class="even">
<td>Wmvrecompress</td>
<td>Diese Konsolenanwendung zeigt, wie eine WMV-Datei erneut komprimiert wird. Es veranschaulicht das Lesen von nicht komprimierten Beispielen, das Schreiben von nicht komprimierten Beispielen und das Durchlaufen von Multipass-Codierung, multikanalausgabe und intelligenter Neukomprimierung.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Windows Media-Format-SDK**](about-the-windows-media-format-sdk.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 





