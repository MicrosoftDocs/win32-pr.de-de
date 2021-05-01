---
description: Erstellt ein vom Teststammschlüssel oder einem anderen angegebenen Schlüssel signiertes X.509-Zertifikat, das Ihren Namen an den öffentlichen Teil des Schlüsselpaars bindet. Das Zertifikat wird in einer Datei, in einem Systemzertifikatspeicher oder in beiden gespeichert.
ms.assetid: a28e77dd-72c9-42a3-a72d-1b3eaf59d9cf
title: MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461c15db364066d9edadb6a0c4d2c24dceab5cc9
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327144"
---
# <a name="makecert"></a>MakeCert

> [!Note]  
> MakeCert ist veraltet. Verwenden Sie das PowerShell-Cmdlet [New-SelfSignedCertificate,](/powershell/module/pki/new-selfsignedcertificate)um selbstsignierte Zertifikate zu erstellen.

 

Das MakeCert-Tool erstellt ein [*X.509-Zertifikat,*](../secgloss/x-gly.md) das vom Teststammschlüssel oder einem anderen angegebenen Schlüssel signiert wurde, das Ihren Namen an den öffentlichen Teil des Schlüsselpaars bindet. Das Zertifikat wird in einer Datei, in einem Systemzertifikatspeicher oder in beiden gespeichert. Das Tool wird im \\ Ordner Bin des Installationspfads microsoft Windows Software Development Kit (SDK) installiert.

Das MakeCert-Tool verwendet die folgende Befehlssyntax:

**MakeCert** \[ *BasicOptions* \| *ExtendedOptions* \] *OutputFile*

*OutputFile* ist der Name der Datei, in die das Zertifikat geschrieben wird. Sie können *OutputFile* weglassen, wenn das Zertifikat nicht in eine Datei geschrieben werden soll.

## <a name="options"></a>Optionen

MakeCert enthält grundlegende und erweiterte Optionen. Meistens werden die Basisoptionen zum Erstellen von Zertifikaten verwendet. Die erweiterten Optionen stellen eine höhere Flexibilität zur Verfügung.

Die Optionen für MakeCert sind auch in drei Funktionsgruppen unterteilt:

-   Grundlegende Optionen, die nur für Zertifikatspeichertechnologie spezifisch sind.
-   Erweiterte Optionen, die nur für SPC-Datei- und Private Key-Technologie spezifisch sind.
-   Erweiterte Optionen für SPC-Datei, privaten Schlüssel und Zertifikatspeichertechnologie.

Die in den folgenden Tabellen angegebenen Optionen können nur mit Internet Explorer 4.0 oder höher verwendet werden.



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
<td><a href="/windows/desktop/SecGloss/h-gly"><em>Hashalgorithmus.</em></a> Muss entweder auf <strong>SHA-1</strong> oder <strong>MD5</strong> (Standard) festgelegt werden. Informationen zu MD5 finden Sie unter <a href="/windows/desktop/SecGloss/m-gly"><em>MD5</em></a>.</td>
</tr>
<tr class="even">
<td><strong>-b</strong> <strong></strong> <em>DateStart</em></td>
<td>Datum, an dem das Zertifikat zuerst gültig wird. Der Standardwert ist, wenn das Zertifikat erstellt wird. Das Format von <em>DateStart</em> ist mm/tt/yyyy.</td>
</tr>
<tr class="odd">
<td><strong>-cy</strong> <strong></strong> <em>CertificateTypes</em></td>
<td>Zertifikattyp. <em>CertificateTypes können</em> end <strong>für end-entity</strong> oder <strong>authority for</strong> certification <a href="/windows/desktop/SecGloss/c-gly"><em>authority sein.</em></a></td>
</tr>
<tr class="even">
<td><strong>-e</strong> <strong></strong> <em>DateEnd</em></td>
<td>Datum, an dem die Gültigkeitsdauer endet. Der Standardwert ist das Jahr 2039.</td>
</tr>
<tr class="odd">
<td><strong>-eku</strong> <strong></strong> <em>OID1,</em><strong></strong> <em>OID2</em> ...</td>
<td>Fügt eine Liste von durch Komma <a href="/windows/desktop/SecGloss/e-gly"><em>getrennten,</em></a> erweiterten Schlüsselverwendungsobjektbezeichnern (OIDs) in das Zertifikat ein. <a href="/windows/desktop/SecGloss/o-gly"><em></em></a> Beispielsweise fügt <strong>-eku 1.3.6.1.5.5.7.3.2</strong> die Clientauthentifizierungs-OID ein. Definitionen von zulässigen OIDs finden Sie in der Datei Wincrypt.h in CryptoAPI 2.0.</td>
</tr>
<tr class="even">
<td><strong>-h</strong> <strong></strong> <em>NumChildren</em></td>
<td>Maximale Höhe der Struktur unter diesem Zertifikat.</td>
</tr>
<tr class="odd">
<td><strong>-l</strong> <strong></strong> <em>PolicyLink</em></td>
<td>Link zu Richtlinieninformationen der SPC-Agentur (z. B. eine URL).</td>
</tr>
<tr class="even">
<td><strong>-m</strong> <strong></strong> <em>nMonths</em></td>
<td>Dauer der Gültigkeitsdauer.</td>
</tr>
<tr class="odd">
<td><strong>-n</strong> <strong>&quot;</strong> <em>Name</em><strong>&quot;</strong></td>
<td>Name für das Zertifikat des Herausgebers. Dieser Name muss dem <a href="/windows/desktop/SecGloss/x-gly"><em>X.500-Standard</em></a> entsprechen. Die einfachste Methode ist die Verwendung des &quot; CN=<em>MyName-Formats.</em> &quot; Beispiel: <strong>-n &quot; CN=Test &quot; </strong>.</td>
</tr>
<tr class="even">
<td><strong>-nscp</strong></td>
<td>Die Netscape-Clientauthentifizierungserweiterung sollte enthalten sein.</td>
</tr>
<tr class="odd">
<td><strong>-pe</strong></td>
<td>Markiert den privaten Schlüssel als exportierbar.</td>
</tr>
<tr class="even">
<td><strong>-r</strong></td>
<td>Erstellen eines selbstsignierten Zertifikats</td>
</tr>
<tr class="odd">
<td><strong>-sc</strong> <strong></strong> <em>SubjectCertFile</em></td>
<td>Name der Zertifikatdatei mit dem vorhandenen öffentlichen Schlüssel des Antragstellers, der verwendet werden soll.</td>
</tr>
<tr class="even">
<td><strong>-sk</strong> <strong></strong> <em>SubjectKey</em></td>
<td>Speicherort des Schlüsselcontainers des Antragstellers, der den <a href="/windows/desktop/SecGloss/p-gly"><em>privaten Schlüssel</em></a>enthält. Wenn kein Schlüsselcontainer vorhanden ist, wird ein Schlüsselcontainer erstellt. Wenn weder die Option <strong>-sk</strong> noch <strong>-sv</strong> verwendet wird, wird standardmäßig ein Standardschlüsselcontainer erstellt und verwendet.</td>
</tr>
<tr class="odd">
<td><strong>-sky</strong> <strong></strong> <em>SubjectKeySpec</em></td>
<td>Schlüsselspezifikation des Antragstellers. <em>SubjectKeySpec</em> muss einer von drei möglichen Werten sein:<br/>
<ul>
<li><strong>Signatur</strong> (AT_SIGNATURE Schlüsselspezifikation)</li>
<li><strong>Exchange</strong> (AT_KEYEXCHANGE Schlüsselspezifikation)</li>
<li>Eine ganze Zahl, z. <strong>B. 3</strong></li>
</ul>
Weitere Informationen finden Sie im Hinweis, der auf diese Tabelle folgt.<br/></td>
</tr>
<tr class="even">
<td><strong>-sp</strong> <strong></strong> <em>SubjectProviderName</em></td>
<td>CryptoAPI-Anbieter für Betreff. Der Standardwert ist der Anbieter des Benutzers. Informationen zu CryptoAPI-Anbietern finden Sie in der CryptoAPI 2.0 Dokumentation.</td>
</tr>
<tr class="odd">
<td><strong>-sr</strong> <strong></strong> <em>SubjectCertStoreLocation</em></td>
<td>Der Registrierungsspeicherort des Zertifikatspeichers des Subjekts. <em>SubjectCertStoreLocation</em> muss entweder <strong>LocalMachine (Registrierungsschlüssel</strong> HKEY_LOCAL_MACHINE) oder <strong>CurrentUser</strong> (Registrierungsschlüssel)HKEY_CURRENT_USER. <strong>CurrentUser</strong> ist die Standardeinstellung.</td>
</tr>
<tr class="even">
<td><strong>-ss</strong> <strong></strong> <em>SubjectCertStoreName</em></td>
<td>Name des Zertifikatspeichers des Subjekts, in dem das generierte Zertifikat gespeichert wird.</td>
</tr>
<tr class="odd">
<td><strong>-sv</strong> <strong></strong> <em>SubjectKeyFile</em></td>
<td>Name der PVK-Datei des Betreffs. Wenn weder <strong>die Option -sk</strong> noch <strong>-sv</strong> verwendet wird, wird standardmäßig ein Standardschlüsselcontainer erstellt und verwendet.</td>
</tr>
<tr class="even">
<td><strong>-sy</strong> <strong></strong> <em>nSubjectProviderType</em></td>
<td>CryptoAPI-Anbietertyp für Betreff. Der Standardwert ist <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>. Informationen zu CryptoAPI-Anbietertypen finden Sie in der CryptoAPI 2.0 Dokumentation.</td>
</tr>
<tr class="odd">
<td><strong>-#</strong><strong></strong> <em>SerialNumber</em></td>
<td>Seriennummer des Zertifikats. Der Höchstwert ist 2^31. Der Standardwert ist ein vom Tool generierter Wert, der garantiert eindeutig ist.</td>
</tr>
<tr class="even">
<td><strong>-$</strong><strong></strong> <em>CertificateAuthority</em></td>
<td>Typ der <a href="/windows/desktop/SecGloss/c-gly"><em>Zertifizierungsstelle.</em></a> <em>CertificateAuthority</em> muss entweder auf <strong>"commercial"</strong> (für Zertifikate, die von kommerziellen Softwareverlegern verwendet werden sollen) oder <strong>"Individual"</strong> (für Zertifikate, die von einzelnen Softwareverlegern verwendet werden sollen) festgelegt werden.</td>
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
> Wenn die -sky-Schlüsselspezifikationsoption in Internet Explorer Version 4.0 oder höher verwendet wird, muss die Spezifikation mit der Schlüsselspezifikation übereinstimmen, die durch die Datei mit dem [*privaten Schlüssel*](../secgloss/p-gly.md) oder den [*Privaten Schlüsselcontainer*](../secgloss/k-gly.md)angegeben wird.  Wenn die Schlüsselspezifikationsoption nicht verwendet wird, wird die durch die Datei mit dem privaten Schlüssel oder den Privaten Schlüsselcontainer angegebene Schlüsselspezifikation verwendet. Wenn im Schlüsselcontainer mehrere Schlüsselspezifikationen vorhanden sind, versucht MakeCert zunächst, die AT \_ SIGNATURE-Schlüsselspezifikation zu verwenden. Wenn dies fehlschlägt, versucht MakeCert, AT \_ KEYEXCHANGE zu verwenden. Da die meisten Benutzer entweder über einen AT \_ SIGNATURE-Schlüssel oder einen AT \_ KEYEXCHANGE-Schlüssel verfügen, muss diese Option in den meisten Fällen nicht verwendet werden.

 

Die folgenden Optionen gelten nur für SPC-Dateien [*(Software Publisher Certificate)*](../secgloss/s-gly.md) und Technologie für private Schlüssel.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>SPC- und private Schlüsseloption</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>-ic</strong> <strong></strong> <em>IssuerCertFile</em></td>
<td>Speicherort des Zertifikats des Ausstellers.</td>
</tr>
<tr class="even">
<td><strong>-ik</strong> <strong></strong> <em>IssuerKey</em></td>
<td>Speicherort des Schlüsselcontainers des Ausstellers. Der Standardwert ist der Teststammschlüssel.</td>
</tr>
<tr class="odd">
<td><strong>-iky</strong> <strong></strong> <em>IssuerKeySpec</em></td>
<td>Die Schlüsselspezifikation des Ausstellers, die einer von drei möglichen Werten sein muss:<br/>
<ul>
<li><strong>Signatur</strong> (AT_SIGNATURE Schlüsselspezifikation)</li>
<li><strong>Exchange</strong> (AT_KEYEXCHANGE-Schlüsselspezifikation)</li>
<li>Eine ganze Zahl, z. <strong>B. 3</strong></li>
</ul>
Weitere Informationen finden Sie im Hinweis, der auf diese Tabelle folgt.<br/></td>
</tr>
<tr class="even">
<td><strong>-ip</strong> <strong></strong> <em>IssuerProviderName</em></td>
<td>CryptoAPI-Anbieter für Aussteller. Der Standardwert ist der Anbieter des Benutzers. Informationen zu CryptoAPI-Anbietern finden Sie in der CryptoAPI 2.0 Dokumentation.</td>
</tr>
<tr class="odd">
<td><strong>-iv</strong> <strong></strong> <em>IssuerKeyFile</em></td>
<td>Die Datei mit dem privaten Schlüssel des Ausstellers. Der Standardwert ist der Teststamm.</td>
</tr>
<tr class="even">
<td><strong>-iy</strong> <strong></strong> <em>nIssuerProviderType</em></td>
<td>CryptoAPI-Anbietertyp für Aussteller. Der Standardwert ist <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>. Informationen zu CryptoAPI-Anbietertypen finden Sie in der CryptoAPI 2.0 Dokumentation.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Wenn die **Option -iky** key specification in Internet Explorer 4.0 oder höher verwendet wird, [](../secgloss/p-gly.md) muss die Spezifikation mit der Schlüsselspezifikation übereinstimmen, die durch die Datei mit dem privaten Schlüssel oder den Privaten Schlüsselcontainer [*angegeben wird.*](../secgloss/k-gly.md) Wenn die Schlüsselspezifikationsoption nicht verwendet wird, wird die von der Datei mit dem privaten Schlüssel oder dem Container für den privaten Schlüssel angegebene Schlüsselspezifikation verwendet. Wenn im Schlüsselcontainer mehrere Schlüsselspezifikationen enthalten sind, versucht MakeCert zunächst, die AT \_ SIGNATURE-Schlüsselspezifikation zu verwenden. Wenn dies fehlschlägt, versucht MakeCert, AT \_ KEYEXCHANGE zu verwenden. Da die meisten Benutzer entweder über einen AT \_ SIGNATURE-Schlüssel oder einen AT \_ KEYEXCHANGE-Schlüssel verfügen, muss diese Option in den meisten Fällen nicht verwendet werden.

 

Die folgenden Optionen gelten nur für [*Zertifikatspeichertechnologien.*](../secgloss/c-gly.md)



| Zertifikatspeicheroption          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-ic** *IssuerCertFile*          | Datei, die das Zertifikat des Ausstellers enthält. MakeCert sucht im Zertifikatspeicher nach einem Zertifikat mit einer genauen Übereinstimmung.                                                                                                                                                                                                        |
| **-in** *IssuerNameString*        | Allgemeiner Name des Zertifikats des Ausstellers. MakeCert sucht im Zertifikatspeicher nach einem Zertifikat, dessen allgemeiner Name *IssuerNameString* enthält.                                                                                                                                                                                  |
| **-ir** *IssuerCertStoreLocation* | Registrierungsspeicherort des Zertifikatspeichers des Ausstellers. *IssuerCertStoreLocation* muss entweder **LocalMachine** (Registrierungsschlüssel HKEY \_ LOCAL \_ MACHINE) oder **CurrentUser** (Registrierungsschlüssel HKEY \_ CURRENT \_ USER) sein. **CurrentUser** ist die Standardeinstellung.                                                                                                |
| **-is** *IssuerCertStoreName*     | Der Zertifikatspeicher des Ausstellers, der das Zertifikat des Ausstellers und die zugehörigen Informationen zum privaten Schlüssel enthält. Wenn mehr als ein Zertifikat im Speicher vorhanden ist, muss der Benutzer es mithilfe der Option **-ic** oder **-in** eindeutig identifizieren. Wenn das Zertifikat im Zertifikatspeicher nicht eindeutig identifiziert wird, schlägt MakeCert fehl. |



 

 

 
