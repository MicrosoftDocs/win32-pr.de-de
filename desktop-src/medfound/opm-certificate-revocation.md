---
description: .
ms.assetid: 21faf809-1335-4d93-be06-628c5a05a4c8
title: OPM-Zertifikat Sperrung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4b20dc00b0bd23644ef9dca22558a304ca9438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527890"
---
# <a name="opm-certificate-revocation"></a>OPM-Zertifikat Sperrung

Ein Ausgabe Schutz-Manager-Zertifikat (OPM) kann von Microsoft gesperrt werden. Die Liste der gesperrten Zertifikate wird in einer globalen Sperr Liste (GRL) gespeichert. Die GRL weist das folgende Format auf:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>`Section`</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Header</td>
<td>Eine <a href="grl-header.md"><strong>GRL_HEADER</strong></a> -Struktur.</td>
</tr>
<tr class="even">
<td>Kernspeicher</td>
<td>Enthält die folgenden Sperr Listen:
<ul>
<li>Binäre Kernel-Sperren</li>
<li>Binäre widerrufen im Benutzermodus</li>
<li>Zertifikat Widerruf</li>
<li>Vertrauenswürdige Stämme (reserviert)</li>
</ul>
Die Liste der vertrauenswürdigen Stämme wird derzeit nicht verwendet und ist für die zukünftige Verwendung reserviert.</td>
</tr>
<tr class="odd">
<td>Erweiterbare Einträge</td>
<td>Enthält Informationen, die von anderen Komponenten verwendet werden. Dieser Abschnitt ist für OPM nicht relevant.</td>
</tr>
<tr class="even">
<td>Erneuerungen</td>
<td>Enthält GUIDs, die Windows Update Bezeichner definieren. Dieser Abschnitt enthält Bezeichner für die folgenden Listen:
<ul>
<li>Binäre Kernel-Sperren</li>
<li>Binäre widerrufen im Benutzermodus</li>
<li>Zertifikat Widerruf</li>
</ul>
Eine Anwendung kann diese Bezeichner verwenden, um eine erneuerte Version einer gesperrten Binärdatei anzufordern, sofern eine solche vorhanden ist.</td>
</tr>
<tr class="odd">
<td>Signatur: Abschnitt "Core"</td>
<td>Signiert die Header-und Kern Abschnitte.</td>
</tr>
<tr class="even">
<td>Signatur: erweiterbarer Abschnitt</td>
<td>Signiert den Header und erweiterbare Abschnitte.</td>
</tr>
</tbody>
</table>



 

Der GRL-Header ist eine [**GRL- \_ Header**](grl-header.md) Struktur. Der **dwsequencenenumber** -Member der-Struktur enthält die GRL-Versionsnummer. Diese Zahl wird bei jedem Update der GRL und einer neuen Version auf dem Computer des Benutzers inkrementiert.

Widerrufene OPM-Zertifikate werden in der Liste der Zertifikat Widerrufungen des Core-Abschnitts aufgeführt. Jeder Kern Eintrag in der GRL ist ein 20-Byte-Array, das den SHA-1-Hash des öffentlichen Schlüssels des widerrufenen Zertifikats enthält.

Die Signatur Abschnitte enthalten Signaturen, die verwendet werden können, um zu überprüfen, ob die GRL nicht manipuliert wurde. Jeder Signatur Abschnitt enthält die "am MF"- [**\_ Signatur**](mf-signature.md) Struktur. Die erste Signatur signiert den Header und den Abschnitt Core. Die zweite Signatur signiert den Header und den erweiterbaren Abschnitt. Diese Signatur ist für OPM nicht relevant.

Um sicherzustellen, dass die GRL selbst nicht manipuliert wurde, überprüfen Sie die Signatur wie folgt:

1.  Ermitteln des Starts der [**MF- \_ Signatur**](mf-signature.md) Struktur. Der Speicherort der **MF- \_ Signatur** Struktur wird im **cbsignaturecoreoffset** -Member der [**GRL- \_ Header**](grl-header.md) Struktur angegeben. Der Speicherort wird als Offset in Bytes vom Anfang der GRL angegeben.
2.  Analysieren Sie die [**MF- \_ Signatur**](mf-signature.md) Struktur als PKCS \# 7-Signatur mit einer Zertifikat Kette.
3.  Überprüfen Sie die Zertifikat Kette bis zu einer vertrauenswürdigen Stamm Zertifizierungsstelle.
4.  Vergewissern Sie sich, dass das Blatt Zertifikat den folgenden Objekt Bezeichner in der EKU enthält: "1.3.6.1.4.1.311.10.5.4".
5.  Berechnen Sie einen Hashwert der Bytes, die den Header und die Kern Abschnitte der GRL enthalten.
6.  Vergewissern Sie sich, dass der Hash mit der Signatur im Blatt Zertifikat übereinstimmt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Output Protection Manager](output-protection-manager.md)
</dt> <dt>

[**GRL- \_ Header**](grl-header.md)
</dt> <dt>

[**MF- \_ Signatur**](mf-signature.md)
</dt> </dl>

 

 



