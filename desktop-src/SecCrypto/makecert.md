---
description: Erstellt ein X. 509-Zertifikat, das mit dem Test Stamm Schlüssel oder einem anderen angegebenen Schlüssel signiert ist, das Ihren Namen an den öffentlichen Teil des Schlüssel Paars bindet. Das Zertifikat wird in einer Datei, einem Systemzertifikat Speicher oder beiden gespeichert.
ms.assetid: a28e77dd-72c9-42a3-a72d-1b3eaf59d9cf
title: MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980ba379688f2dc61c44b06d66ed5255e5b2e988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356508"
---
# <a name="makecert"></a>MakeCert

> [!Note]  
> MakeCert ist veraltet. Verwenden Sie zum Erstellen selbst signierter Zertifikate das PowerShell-Cmdlet [New-selfsignedcertificate](/powershell/module/pkiclient/new-selfsignedcertificate).

 

Das MakeCert-Tool erstellt ein [*X. 509*](../secgloss/x-gly.md) -Zertifikat, das mit dem Test Stamm Schlüssel oder einem anderen angegebenen Schlüssel signiert ist, das den Namen an den öffentlichen Teil des Schlüssel Paars bindet. Das Zertifikat wird in einer Datei, einem Systemzertifikat Speicher oder beiden gespeichert. Das Tool wird im \\ Ordner bin des Installations Pfads des Microsoft Windows Software Development Kit (SDK) installiert.

Das MakeCert-Tool verwendet die folgende Befehlssyntax:

**Makecert** \[ *Basicoptions* \| *Extendedoptions* \] *OutputFile*

*OutputFile* ist der Name der Datei, in die das Zertifikat geschrieben wird. Sie können *OutputFile* weglassen, wenn das Zertifikat nicht in eine Datei geschrieben werden soll.

## <a name="options"></a>Optionen

Makecert enthält grundlegende und erweiterte Optionen. Meistens werden die Basisoptionen zum Erstellen von Zertifikaten verwendet. Die erweiterten Optionen stellen eine höhere Flexibilität zur Verfügung.

Die Optionen für Makecert sind auch in drei Funktionsgruppen unterteilt:

-   Grundlegende Optionen, die nur für die Zertifikat Speichertechnologie spezifisch sind.
-   Erweiterte Optionen, die nur für die SPC-Datei und die private Schlüsseltechnologie spezifisch sind.
-   Erweiterte Optionen für die Technologie "SPC-Datei", "privater Schlüssel" und "Zertifikat Speicher".

Die in den folgenden Tabellen angegebenen Optionen können nur mit Internet Explorer 4,0 oder höher verwendet werden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Basic-Option</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>-a</strong> <strong></strong> <em>Algorithmus</em></td>
<td><a href="/windows/desktop/SecGloss/h-gly"><em>Hash</em></a> Algorithmus. Muss entweder auf <strong>SHA-1</strong> oder <strong>MD5</strong> (Standard) festgelegt werden. Weitere Informationen zu MD5 finden Sie unter <a href="/windows/desktop/SecGloss/m-gly"><em>MD5</em></a>.</td>
</tr>
<tr class="even">
<td><strong>-b</strong> <strong></strong> <em>DateStart</em></td>
<td>Datum, an dem das Zertifikat zuerst gültig wird. Der Standardwert ist, wenn das Zertifikat erstellt wird. <em>DateStart</em> hat das Format mm/dd/yyyy.</td>
</tr>
<tr class="odd">
<td><strong>-CY</strong> <strong></strong> <em>Certifipeetypes</em></td>
<td>Der Zertifikattyp. <em>Certifipeetypes</em> <strong>können für die</strong> Endentität oder die Zertifizierungsstelle für die <a href="/windows/desktop/SecGloss/c-gly"><em>Zertifizierungs</em></a>Stelle <strong>enden</strong> .</td>
</tr>
<tr class="even">
<td><strong>-e</strong> <strong></strong> <em>DateEnd</em></td>
<td>Datum, an dem die Gültigkeitsdauer endet. Der Standardwert ist das Jahr 2039.</td>
</tr>
<tr class="odd">
<td><strong>-EKU</strong> <strong></strong> <em>OID1</em><strong>,</strong> <em>OID2</em> ...</td>
<td>Fügt eine Liste mit einem oder mehreren durch Trennzeichen getrennten, <a href="/windows/desktop/SecGloss/e-gly"><em>erweiterten Schlüssel Verwendungs</em></a> <a href="/windows/desktop/SecGloss/o-gly"><em>Objekt</em></a> -IDs (OIDs) in das Zertifikat ein. Beispielsweise fügt <strong>-EKU 1.3.6.1.5.5.7.3.2</strong> die Clientauthentifizierungs-OID ein. Definitionen zulässiger OIDs finden Sie in der Datei Wincrypt. h in CryptoAPI 2.0.</td>
</tr>
<tr class="even">
<td><strong>-h</strong> <strong></strong> <em>NumChildren</em></td>
<td>Maximale Höhe des Baums unter diesem Zertifikat.</td>
</tr>
<tr class="odd">
<td><strong>-l</strong> <strong></strong> <em>PolicyLink</em></td>
<td>Link zu den Richtlinien Informationen der SPC-Agentur (z. b. eine URL).</td>
</tr>
<tr class="even">
<td><strong>-m</strong> <strong></strong> <em>nmonate</em></td>
<td>Dauer der Gültigkeitsdauer.</td>
</tr>
<tr class="odd">
<td><strong>-n</strong> <strong>&quot;</strong> <em>Name</em><strong>&quot;</strong></td>
<td>Der Name für das Zertifikat des Herausgebers. Dieser Name muss dem <a href="/windows/desktop/SecGloss/x-gly"><em>X. 500</em></a> -Standard entsprechen. Die einfachste Methode besteht darin, das &quot; Format "CN =<em>myname</em> " zu verwenden &quot; . Beispiel: <strong>-n &quot; CN = Test &quot; </strong>.</td>
</tr>
<tr class="even">
<td><strong>-nscp</strong></td>
<td>Die Netscape-Client Authentifizierungs Erweiterung sollte eingeschlossen werden.</td>
</tr>
<tr class="odd">
<td><strong>-PE</strong></td>
<td>Markiert den privaten Schlüssel als exportierbar.</td>
</tr>
<tr class="even">
<td><strong>-r</strong></td>
<td>Erstellen eines selbstsignierten Zertifikats</td>
</tr>
<tr class="odd">
<td><strong>-SC</strong> <strong></strong> " <em>Subjetcertfile</em> "</td>
<td>Der Name der Zertifikatsdatei, für die der vorhandene öffentliche Schlüssel des Antragstellers verwendet werden soll.</td>
</tr>
<tr class="even">
<td><strong>-SK</strong> <strong></strong> <em>Subjetkey</em></td>
<td>Speicherort des Schlüssel Containers des Subjekts, der den <a href="/windows/desktop/SecGloss/p-gly"><em>privaten Schlüssel</em></a>enthält. Wenn kein Schlüsselcontainer vorhanden ist, wird ein Schlüsselcontainer erstellt. Wenn weder die Option " <strong>-SK</strong> " noch die Option " <strong>-SV</strong> " verwendet wird, wird standardmäßig ein Standardschlüssel Container erstellt und verwendet.</td>
</tr>
<tr class="odd">
<td><strong>-Sky</strong> <strong></strong> <em>Subjetkeyspec</em></td>
<td>Schlüssel Spezifikation des Subjekts. ' <em>Subjetkeyspec</em> ' muss einen von drei möglichen Werten aufweisen:<br/>
<ul>
<li><strong>Signatur</strong> (AT_SIGNATURE Schlüssel Spezifikation)</li>
<li><strong>Exchange</strong> (AT_KEYEXCHANGE-Schlüssel Spezifikation)</li>
<li>Eine ganze Zahl, z. b. <strong>3</strong></li>
</ul>
Weitere Informationen finden Sie im Hinweis in der folgenden Tabelle.<br/></td>
</tr>
<tr class="even">
<td><strong>-SP</strong> <strong></strong> <em>Subjetprovidername</em></td>
<td>Kryptoapi-Anbieter für Betreff. Der Standardwert ist der Anbieter des Benutzers. Weitere Informationen zu CryptoAPI-Anbietern finden Sie in der CryptoAPI 2.0-Dokumentation.</td>
</tr>
<tr class="odd">
<td><strong>-SR</strong> <strong></strong> <em>Subjetcertstoreloation</em></td>
<td>Der Registrierungs Speicherort für den Zertifikat Speicher des Subjekts. " <em>Subjetcertstoreloation</em> " muss entweder " <strong>LocalMachine</strong> " (Registrierungsschlüssel HKEY_LOCAL_MACHINE) oder " <strong>CurrentUser</strong> " (Registrierungsschlüssel HKEY_CURRENT_USER) sein. <strong>CurrentUser</strong> ist die Standardeinstellung.</td>
</tr>
<tr class="even">
<td><strong>-SS</strong> <strong></strong> <em>Subjetcertstorename</em></td>
<td>Der Name des Zertifikats Speicher des Subjekts, in dem das generierte Zertifikat gespeichert wird.</td>
</tr>
<tr class="odd">
<td><strong>-SV</strong> <strong></strong> " <em>Subjetkeyfile</em> "</td>
<td>Der Name der PVK-Datei des Subjekts. Wenn weder die Option " <strong>-SK</strong> " noch die Option " <strong>-SV</strong> " verwendet wird, wird standardmäßig ein Standardschlüssel Container erstellt und verwendet.</td>
</tr>
<tr class="even">
<td><strong>-Sy</strong> <strong></strong> <em>nsubjetprovidertype</em></td>
<td>CryptoAPI-Anbietertyp für Betreff. Der Standardwert ist <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>. Informationen zu kryptoapi-Anbieter Typen finden Sie in der CryptoAPI 2.0-Dokumentation.</td>
</tr>
<tr class="odd">
<td><strong>-#</strong><strong></strong> <em>SerialNumber</em></td>
<td>Seriennummer des Zertifikats. Der Maximalwert ist 2 ^ 31. Der Standardwert ist ein Wert, der vom Tool generiert wird, das garantiert eindeutig ist.</td>
</tr>
<tr class="even">
<td><strong>-$</strong><strong></strong> <em>CertificateAuthority</em></td>
<td>Der Typ der <a href="/windows/desktop/SecGloss/c-gly"><em>Zertifizierungs</em></a>Stelle. <em>CertificateAuthority</em> muss entweder <strong>kommerziell</strong> (für Zertifikate, die von kommerziellen Software Herausgebern verwendet werden) oder <strong>Einzelpersonen</strong> (für Zertifikate, die von einzelnen Software Verlegern verwendet werden) festgelegt werden.</td>
</tr>
<tr class="odd">
<td><strong>-?</strong></td>
<td>Zeigt die grundlegenden Optionen an.</td>
</tr>
<tr class="even">
<td><strong>-!</strong></td>
<td>Zeigt die erweiterten Optionen an.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Wenn die Option **-Sky** Key Specification in Internet Explorer Version 4,0 oder höher verwendet wird, muss die Spezifikation mit der durch die Datei des [*privaten Schlüssels*](../secgloss/p-gly.md) oder dem privaten [*Schlüssel Container*](../secgloss/k-gly.md)gekennzeichneten Schlüssel Spezifikation identisch sein. Wenn die Schlüssel Spezifikations Option nicht verwendet wird, wird die von der Datei mit dem privaten Schlüssel oder dem Container für den privaten Schlüssel festgestellte Schlüssel Spezifikation verwendet. Wenn im Schlüssel Container mehr als eine Schlüssel Spezifikation vorhanden ist, wird von MakeCert zuerst versucht, die Spezifikation für den \_ Signatur Schlüssel zu verwenden. Wenn dies fehlschlägt, versucht Makecert, bei \_ keyexchange zu verwenden. Da die meisten Benutzer entweder über einen at- \_ Signatur Schlüssel oder über einen Schlüssel \_ Austausch Schlüssel verfügen, muss diese Option in den meisten Fällen nicht verwendet werden.

 

Die folgenden Optionen gelten nur für SPC-Dateien ( [*Software Publisher Certificate*](../secgloss/s-gly.md) ) und private Schlüsseltechnologie.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Option "SPC und privater Schlüssel"</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>-IC</strong> <strong></strong> <em>Issuercertfile</em></td>
<td>Speicherort des Zertifikats des Ausstellers.</td>
</tr>
<tr class="even">
<td><strong>-IK</strong> <strong></strong> <em>Issuerkey</em></td>
<td>Speicherort des Schlüssel Containers des Ausstellers. Der Standardwert ist der Test Stamm Schlüssel.</td>
</tr>
<tr class="odd">
<td><strong>-IKY</strong> <strong></strong> <em>Issuerkeyspec</em></td>
<td>Schlüssel Spezifikation des Ausstellers, die einen von drei möglichen Werten aufweisen muss:<br/>
<ul>
<li><strong>Signatur</strong> (AT_SIGNATURE Schlüssel Spezifikation)</li>
<li><strong>Exchange</strong> (AT_KEYEXCHANGE-Schlüssel Spezifikation)</li>
<li>Eine ganze Zahl, z. b. <strong>3</strong></li>
</ul>
Weitere Informationen finden Sie im Hinweis in der folgenden Tabelle.<br/></td>
</tr>
<tr class="even">
<td><strong>-IP</strong> <strong></strong> <em>Issuerprovidername</em></td>
<td>CryptoAPI-Anbieter für Aussteller. Der Standardwert ist der Anbieter des Benutzers. Weitere Informationen zu CryptoAPI-Anbietern finden Sie in der CryptoAPI 2.0-Dokumentation.</td>
</tr>
<tr class="odd">
<td><strong>-IV</strong> <strong></strong> <em>Issuerkeyfile</em></td>
<td>Die Datei mit dem privaten Schlüssel des Ausstellers. Der Standardwert ist der Test Stamm.</td>
</tr>
<tr class="even">
<td><strong>-iy</strong> <strong></strong> <em>nissuerprovidertype</em></td>
<td>Der CryptoAPI-Anbietertyp für den Aussteller. Der Standardwert ist <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>. Informationen zu kryptoapi-Anbieter Typen finden Sie in der CryptoAPI 2.0-Dokumentation.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Wenn die Option **-IKY** Key Specification in Internet Explorer 4,0 oder höher verwendet wird, muss die Spezifikation mit der durch die Datei des [*privaten Schlüssels*](../secgloss/p-gly.md) oder dem privaten [*Schlüssel Container*](../secgloss/k-gly.md)gekennzeichneten Schlüssel Spezifikation identisch sein. Wenn die Schlüssel Spezifikations Option nicht verwendet wird, wird die von der Datei mit dem privaten Schlüssel oder dem Container für den privaten Schlüssel festgestellte Schlüssel Spezifikation verwendet. Wenn im Schlüssel Container mehr als eine Schlüssel Spezifikation vorhanden ist, wird von MakeCert zuerst versucht, die Spezifikation für den \_ Signatur Schlüssel zu verwenden. Wenn dies fehlschlägt, versucht Makecert, bei \_ keyexchange zu verwenden. Da die meisten Benutzer entweder über einen at- \_ Signatur Schlüssel oder über einen Schlüssel \_ Austausch Schlüssel verfügen, muss diese Option in den meisten Fällen nicht verwendet werden.

 

Die folgenden Optionen gelten nur für die [*Zertifikat Speicher*](../secgloss/c-gly.md) Technologie.



| Zertifikat Speicher Option          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-IC** *issuercertfile*          | Die Datei, die das Zertifikat des Ausstellers enthält. Makecert sucht im Zertifikat Speicher nach einem Zertifikat mit einer genauen Entsprechung.                                                                                                                                                                                                        |
| **-in** *issuernamestring*        | Der allgemeine Name des Zertifikats des Ausstellers. Makecert sucht im Zertifikat Speicher nach einem Zertifikat, dessen gemeinsamer Name *issuernamestring* enthält.                                                                                                                                                                                  |
| **-IR** *issuercertstoreloation* | Der Registrierungs Speicherort für den Zertifikat Speicher des Ausstellers. *Issuercertstoreloation* muss entweder **LocalMachine** (Registrierungsschlüssel HKEY \_ local \_ Machine) oder **CurrentUser** (Registrierungsschlüssel HKEY \_ aktueller \_ Benutzer) sein. **CurrentUser** ist die Standardeinstellung.                                                                                                |
| **-ist** *issuercertstorename*     | Der Zertifikat Speicher des Ausstellers, der das Zertifikat des Ausstellers und die zugehörigen Informationen zum privaten Schlüssel enthält. Wenn sich mehr als ein Zertifikat im Speicher befindet, muss der Benutzer es mithilfe der Option **-IC** oder **-in** eindeutig identifizieren. Wenn das Zertifikat im Zertifikat Speicher nicht eindeutig identifiziert wird, tritt bei Makecert ein Fehler auf. |



 

 

 
