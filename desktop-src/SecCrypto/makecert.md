---
description: Erstellt ein vom Teststammschlüssel oder einem anderen angegebenen Schlüssel signiertes X.509-Zertifikat, das Ihren Namen an den öffentlichen Teil des Schlüsselpaars bindet. Das Zertifikat wird in einer Datei, in einem Systemzertifikatspeicher oder in beiden gespeichert.
ms.assetid: a28e77dd-72c9-42a3-a72d-1b3eaf59d9cf
title: MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff9fb79b5db5a6a71eee981166742b4e1680184
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471926"
---
# <a name="makecert"></a>MakeCert

> [!Note]  
> MakeCert ist veraltet. Verwenden Sie das PowerShell-Cmdlet [New-SelfSignedCertificate,](/powershell/module/pki/new-selfsignedcertificate)um selbstsignierte Zertifikate zu erstellen.

 

Das MakeCert-Tool erstellt ein [*X.509-Zertifikat,*](../secgloss/x-gly.md) das vom Teststammschlüssel oder einem anderen angegebenen Schlüssel signiert wurde und Ihren Namen an den öffentlichen Teil des Schlüsselpaars bindet. Das Zertifikat wird in einer Datei, in einem Systemzertifikatspeicher oder in beiden gespeichert. Das Tool wird im \\ Ordner Bin des Installationspfads des Microsoft Windows Software Development Kit (SDK) installiert.

Das MakeCert-Tool verwendet die folgende Befehlssyntax:

**MakeCert** \[ *BasicOptions* \| *ExtendedOptions* \] *OutputFile*

*OutputFile* ist der Name der Datei, in die das Zertifikat geschrieben wird. Sie können *OutputFile* weglassen, wenn das Zertifikat nicht in eine Datei geschrieben werden soll.

## <a name="options"></a>Optionen

MakeCert enthält grundlegende und erweiterte Optionen. Meistens werden die Basisoptionen zum Erstellen von Zertifikaten verwendet. Die erweiterten Optionen stellen eine höhere Flexibilität zur Verfügung.

Die Optionen für MakeCert sind auch in drei Funktionsgruppen unterteilt:

-   Grundlegende Optionen, die nur für Zertifikatspeichertechnologie spezifisch sind.
-   Erweiterte Optionen, die nur für SPC-Datei- und Private Key-Technologien spezifisch sind.
-   Erweiterte Optionen für SPC-Datei, privaten Schlüssel und Zertifikatspeichertechnologie.

Die in den folgenden Tabellen angegebenen Optionen können nur mit Internet Explorer 4.0 oder höher verwendet werden.




| Basic-Option | BESCHREIBUNG | 
|--------------|-------------|
| <strong>-a</strong> <strong></strong> <em>Algorithmus</em> | <a href="/windows/desktop/SecGloss/h-gly"><em>Hashalgorithmus.</em></a> Muss entweder auf <strong>SHA-1</strong> oder <strong>MD5</strong> (Standard) festgelegt werden. Weitere Informationen zu MD5 finden Sie unter <a href="/windows/desktop/SecGloss/m-gly"><em>MD5.</em></a> | 
| <strong>-b</strong> <strong></strong> <em>DateStart</em> | Datum, an dem das Zertifikat zum ersten Mal gültig wird. Der Standardwert ist , wenn das Zertifikat erstellt wird. Das Format von <em>DateStart</em> ist mm/dd/yyyy. | 
| <strong>-cy</strong> <strong></strong> <em>CertificateTypes</em> | Zertifikattyp. <em>CertificateTypes</em> kann <strong>end</strong> für die Endentität oder <strong>authority</strong> für <a href="/windows/desktop/SecGloss/c-gly"><em>die Zertifizierungsstelle</em></a>sein. | 
| <strong>-e</strong> <strong></strong> <em>DateEnd</em> | Datum, an dem die Gültigkeitsdauer endet. Der Standardwert ist das Jahr 2039. | 
| <strong>-eku</strong> <strong></strong> <em>OID1</em><strong>,</strong><em>OID2</em> ... | Fügt eine Liste mit einem oder mehreren durch Trennzeichen<a href="/windows/desktop/SecGloss/o-gly"><em>getrennten, erweiterten Schlüsselverwendungsobjektbezeichnern</em></a> (OIDs) in das Zertifikat ein. <a href="/windows/desktop/SecGloss/e-gly"><em></em></a> Beispielsweise fügt <strong>-eku 1.3.6.1.5.5.7.3.2</strong> die Clientauthentifizierungs-OID ein. Definitionen zulässiger OIDs finden Sie in der Wincrypt.h-Datei in CryptoAPI 2.0. | 
| <strong>-h</strong> <strong></strong> <em>NumChildren</em> | Maximale Höhe der Struktur unter diesem Zertifikat. | 
| <strong>-l</strong> <strong></strong> <em>PolicyLink</em> | Link zu Richtlinieninformationen der SPC-Behörde (z. B. eine URL). | 
| <strong>-m</strong> <strong></strong> <em>nMonthen</em> | Dauer der Gültigkeitsdauer. | 
| <strong>-n</strong><strong>"</strong><em>Name</em><strong>"</strong> | Name für das Zertifikat des Herausgebers. Dieser Name muss dem <a href="/windows/desktop/SecGloss/x-gly"><em>X.500-Standard</em></a> entsprechen. Die einfachste Methode ist die Verwendung des Formats "CN=<em>MyName".</em> Beispiel: <strong>-n "CN=Test"</strong>. | 
| <strong>-nscp</strong> | Die Netscape-Clientauthentifizierungserweiterung sollte enthalten sein. | 
| <strong>-pe</strong> | Markiert den privaten Schlüssel als exportierbar. | 
| <strong>-r</strong> | Erstellen eines selbstsignierten Zertifikats | 
| <strong>-sc</strong> <strong></strong> <em>SubjectCertFile</em> | Name der Zertifikatdatei mit dem vorhandenen öffentlichen Schlüssel des Antragstellers, der verwendet werden soll. | 
| <strong>-sk</strong> <strong></strong> <em>SubjectKey</em> | Speicherort des Schlüsselcontainers des Antragstellers, der den <a href="/windows/desktop/SecGloss/p-gly"><em>privaten Schlüssel</em></a>enthält. Wenn kein Schlüsselcontainer vorhanden ist, wird ein Schlüsselcontainer erstellt. Wenn weder die Option <strong>-sk</strong> noch <strong>-sv</strong> verwendet wird, wird standardmäßig ein Standardschlüsselcontainer erstellt und verwendet. | 
| <strong>-sky</strong> <strong></strong> <em>SubjectKeySpec</em> | Schlüsselspezifikation des Antragstellers. <em>SubjectKeySpec</em> muss einer von drei möglichen Werten sein:<br /><ul><li><strong>Signatur</strong> (AT_SIGNATURE Schlüsselspezifikation)</li><li><strong>Exchange</strong> (AT_KEYEXCHANGE Schlüsselspezifikation)</li><li>Eine ganze Zahl, z. B. <strong>3</strong></li></ul>Weitere Informationen finden Sie im Hinweis, der auf diese Tabelle folgt.<br /> | 
| <strong>-sp</strong> <strong></strong> <em>SubjectProviderName</em> | CryptoAPI-Anbieter für Betreff. Der Standardwert ist der Anbieter des Benutzers. Informationen zu CryptoAPI-Anbietern finden Sie in der CryptoAPI 2.0-Dokumentation. | 
| <strong>-sr</strong> <strong></strong> <em>SubjectCertStoreLocation</em> | Registrierungsspeicherort des Zertifikatspeichers des Antragstellers. <em>SubjectCertStoreLocation</em> muss entweder <strong>LocalMachine</strong> (Registrierungsschlüssel HKEY_LOCAL_MACHINE) oder <strong>CurrentUser</strong> (Registrierungsschlüssel HKEY_CURRENT_USER) sein. <strong>CurrentUser</strong> ist die Standardeinstellung. | 
| <strong>-ss</strong> <strong></strong> <em>SubjectCertStoreName</em> | Name des Zertifikatspeichers des Antragstellers, in dem das generierte Zertifikat gespeichert wird. | 
| <strong>-sv</strong> <strong></strong> <em>SubjectKeyFile</em> | Name der PVK-Datei des Antragstellers. Wenn weder die Option <strong>-sk</strong> noch <strong>-sv</strong> verwendet wird, wird standardmäßig ein Standardschlüsselcontainer erstellt und verwendet. | 
| <strong>-sy</strong> <strong></strong> <em>nSubjectProviderType</em> | CryptoAPI-Anbietertyp für Betreff. Der Standardwert ist <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>. Informationen zu CryptoAPI-Anbietertypen finden Sie in der CryptoAPI 2.0-Dokumentation. | 
| <strong>-#</strong><strong></strong><em>Serialnumber</em> | Seriennummer des Zertifikats. Der Höchstwert ist 2^31. Der Standardwert ist ein vom Tool generierter Wert, der garantiert eindeutig ist. | 
| <strong>-$</strong><strong></strong><em>CertificateAuthority</em> | Typ der <a href="/windows/desktop/SecGloss/c-gly"><em>Zertifizierungsstelle.</em></a> <em>CertificateAuthority</em> muss entweder auf <strong>"commercial"</strong> (für Zertifikate, die von kommerziellen Softwareverlegern verwendet werden sollen) oder <strong>"Individual"</strong> (für Zertifikate, die von einzelnen Softwareverlegern verwendet werden sollen) festgelegt werden. | 
| <strong>-?</strong> | Zeigt die grundlegenden Optionen an. | 
| <strong>-!</strong> | Zeigt die erweiterten Optionen an. | 




 

> [!Note]  
> Wenn die **-sky-Schlüsselspezifikationsoption** in Internet Explorer Version 4.0 oder höher verwendet wird, muss die Spezifikation mit der Schlüsselspezifikation übereinstimmen, die durch die Datei mit dem [*privaten Schlüssel*](../secgloss/p-gly.md) oder den Container für den privaten [*Schlüssel*](../secgloss/k-gly.md)angegeben wird. Wenn die Schlüsselspezifikationsoption nicht verwendet wird, wird die durch die Datei des privaten Schlüssels oder den Privaten Schlüsselcontainer angegebene Schlüsselspezifikation verwendet. Wenn im Schlüsselcontainer mehrere Schlüsselspezifikationen enthalten sind, versucht MakeCert zunächst, die AT \_ SIGNATURE-Schlüsselspezifikation zu verwenden. Wenn dies fehlschlägt, versucht MakeCert, AT \_ KEYEXCHANGE zu verwenden. Da die meisten Benutzer entweder über einen AT SIGNATURE-Schlüssel oder einen \_ AT KEYEXCHANGE-Schlüssel verfügen, muss diese Option in den \_ meisten Fällen nicht verwendet werden.

 

Die folgenden Optionen gelten nur für [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC)-Dateien und private Schlüsseltechnologie.




| SPC- und private Schlüsseloption | BESCHREIBUNG | 
|----------------------------|-------------|
| <strong>-ic</strong> <strong></strong> <em>IssuerCertFile</em> | Speicherort des Zertifikats des Ausstellers. | 
| <strong>-ik</strong> <strong></strong> <em>IssuerKey</em> | Speicherort des Schlüsselcontainers des Ausstellers. Der Standardwert ist der Stammschlüssel des Tests. | 
| <strong>-iky</strong> <strong></strong> <em>IssuerKeySpec</em> | Die Schlüsselspezifikation des Ausstellers, die einer von drei möglichen Werten sein muss:<br /><ul><li><strong>Signatur</strong> (AT_SIGNATURE Schlüsselspezifikation)</li><li><strong>Exchange</strong> (AT_KEYEXCHANGE-Schlüsselspezifikation)</li><li>Eine ganze Zahl, z. <strong>B. 3</strong></li></ul>Weitere Informationen finden Sie im Hinweis, der auf diese Tabelle folgt.<br /> | 
| <strong>-ip</strong> <strong></strong> <em>IssuerProviderName</em> | CryptoAPI-Anbieter für Aussteller. Der Standardwert ist der Anbieter des Benutzers. Informationen zu CryptoAPI-Anbietern finden Sie in der CryptoAPI 2.0 dokumentation. | 
| <strong>-iv</strong> <strong></strong> <em>IssuerKeyFile</em> | Die Datei mit dem privaten Schlüssel des Ausstellers. Der Standardwert ist der Teststamm. | 
| <strong>-iy</strong> <strong></strong> <em>nIssuerProviderType</em> | CryptoAPI-Anbietertyp für Aussteller. Der Standardwert ist <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL.</em></a> Informationen zu CryptoAPI-Anbietertypen finden Sie in der CryptoAPI 2.0 Dokumentation. | 




 

> [!Note]  
> Wenn die **Option -iky** key specification in Internet Explorer 4.0 oder höher verwendet wird, [](../secgloss/p-gly.md) muss die Spezifikation mit der Schlüsselspezifikation übereinstimmen, die durch die Datei des privaten Schlüssels oder den Privaten Schlüsselcontainer [*angegeben wird.*](../secgloss/k-gly.md) Wenn die Schlüsselspezifikationsoption nicht verwendet wird, wird die von der Datei mit dem privaten Schlüssel oder dem Container für den privaten Schlüssel angegebene Schlüsselspezifikation verwendet. Wenn im Schlüsselcontainer mehrere Schlüsselspezifikationen enthalten sind, versucht MakeCert zunächst, die AT \_ SIGNATURE-Schlüsselspezifikation zu verwenden. Wenn dies fehlschlägt, versucht MakeCert, AT \_ KEYEXCHANGE zu verwenden. Da die meisten Benutzer entweder über einen AT SIGNATURE-Schlüssel oder einen \_ AT KEYEXCHANGE-Schlüssel verfügen, muss diese Option in den \_ meisten Fällen nicht verwendet werden.

 

Die folgenden Optionen gelten nur für [*die Zertifikatspeichertechnologie.*](../secgloss/c-gly.md)



| Option "Zertifikatspeicher"          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-ic** *IssuerCertFile*          | Datei, die das Zertifikat des Ausstellers enthält. MakeCert sucht im Zertifikatspeicher nach einem Zertifikat mit einer genauen Übereinstimmung.                                                                                                                                                                                                        |
| **-in** *IssuerNameString*        | Der allgemeine Name des Zertifikats des Ausstellers. MakeCert sucht im Zertifikatspeicher nach einem Zertifikat, dessen gemeinsamer Name *IssuerNameString enthält.*                                                                                                                                                                                  |
| **-ir** *IssuerCertStoreLocation* | Der Registrierungsspeicherort des Zertifikatspeichers des Ausstellers. *IssuerCertStoreLocation* muss entweder **LocalMachine** (Registrierungsschlüssel HKEY \_ LOCAL \_ MACHINE) oder **CurrentUser** (Registrierungsschlüssel HKEY \_ CURRENT \_ USER) sein. **CurrentUser** ist die Standardeinstellung.                                                                                                |
| **-is** *IssuerCertStoreName*     | Der Zertifikatspeicher des Ausstellers, der das Zertifikat des Ausstellers und die zugehörigen Informationen zum privaten Schlüssel enthält. Wenn sich mehr als ein Zertifikat im Speicher befindet, muss der Benutzer es mithilfe der Option **-ic** oder **-in eindeutig** identifizieren. Wenn das Zertifikat im Zertifikatspeicher nicht eindeutig identifiziert wird, kann MakeCert nicht eindeutig identifiziert werden. |



 

 

 
