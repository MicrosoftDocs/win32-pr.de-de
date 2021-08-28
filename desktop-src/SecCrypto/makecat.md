---
description: Ein CryptoAPI-Tool, das eine Katalogdatei erstellt.
ms.assetid: 233b3644-f2a5-4166-bac0-30bf2f54e957
title: MakeCat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3b9d8698e3c3694368813b19bd3be692c6c8f3
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623145"
---
# <a name="makecat"></a>MakeCat

Das MakeCat-Tool ist ein CryptoAPI-Tool, das eine Katalogdatei erstellt. MakeCat ist als Teil des Microsoft Windows Software Development Kit (SDK) für Windows 7 und .NET Framework 4.0 verfügbar und wird standardmäßig im Ordner Bin des SDK-Installationspfads \\ installiert.

Das MakeCat-Tool verwendet die folgende Befehlssyntax:

**MakeCat** \[ **-n** \| **-r** \| **-v** \] *FileName*

## <a name="parameters"></a>Parameter



| Parameter             | Beschreibung                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-n**<br/>     | Beenden Sie nicht bei einem wiederherstellbaren Fehler.<br/>                                                                                                                           |
| **-r**<br/>     | Erzwingt, dass MakeCat beendet wird, wenn wiederherstellbare Fehler auftreten. Insbesondere endet sie, wenn die Einträge im Katalogdateiabschnitt einer CDF-Datei verarbeitet werden.<br/> |
| **-v**<br/>     | Ausführlich. Zeigt alle Status- und Fehlermeldungen an.<br/>                                                                                                            |
| *FileName*<br/> | Name der zu analysierenden CDF-Datei. Informationen zu erforderlichen Strukturen und Inhalten finden Sie unter Hinweise.<br/>                                                                         |



 

## <a name="remarks"></a>Hinweise

Die CDF-Datei muss mit den folgenden Spezifikationen erstellt werden.

``` syntax
[CatalogHeader]
Name=Name              
ResultDir=ResultDir   
PublicVersion=[|1]
CatalogVersion = [|1|2]
HashAlgorithms=[|SHA1|SHA256]
PageHashes=[true|false]
EncodingType=Encodingtype 
CATATTR1={type}:{oid}:{value} (optional)
CATATTR2={type}:{oid}:{value} (optional)

[CatalogFiles]
{reference tag}=file path and name
{reference tag}ALTSIPID={guid} (optional)
{reference tag}ATTR1={type}:{oid}:{value} (optional)
{reference tag}ATTR2={type}:{oid}:{value} (optional)
<HASH>kernel32.dll=kernel32.dll
<HASH>ntdll.dll=ntdll.dll
```

> [!Note]  
> Der letzte Eintrag in der CDF-Datei muss immer ein explizites Zeilenumzeilenzeichen am Ende der Zeile enthalten.

 

Im \[ Abschnitt CatalogHeader \] werden Informationen zur gesamten Katalogdatei definiert.



| Option                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Name<br/>           | Name der Katalogdatei, einschließlich der Erweiterung.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ResultDir<br/>      | Verzeichnis, in dem die erstellte CAT-Datei platziert wird. Wenn nicht angegeben, wird das aktuelle Standardverzeichnis verwendet. Wenn das Verzeichnis nicht vorhanden ist, wird es erstellt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| PublicVersion<br/>  | Diese Option wird nicht unterstützt. <br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003** und Windows XP: Katalogversion. Wenn dieses Feld leer gelassen wird, wird der Standardwert 1 verwendet.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| CatalogVersion<br/> | Katalogversion. Wenn die Version nicht vorhanden oder auf 1 festgelegt ist, wird "0x100" an den *dwPublicVersion-Parameter* der [**CryptCATOpen-Funktion**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) übergeben, und eine Katalogdatei der Version 1 wird erstellt. Die HashAlgorithms-Option muss leer sein oder SHA1 enthalten.<br/> Wenn die Version auf 2 festgelegt ist, wird "0x200" an den *dwPublicVersion-Parameter* der [**CryptCATOpen-Funktion**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) übergeben, und eine Katalogdatei der Version 2 wird erstellt. Die HashAlgorithms-Option muss SHA256 enthalten.<br/> Wenn diese Option vorhanden ist, aber einen anderen Wert als 1 oder 2 enthält, tritt beim MakeCat-Tool ein Fehler auf.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003** und Windows XP: Diese Option wird nicht unterstützt.<br/> <br/> |
| HashAlgorithms<br/> | Name des verwendeten Hashalgorithmus. Weitere Informationen finden Sie unter der CatalogVersion-Option.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003** und Windows XP: Diese Option wird nicht unterstützt.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| PageHashes<br/>     | Gibt an, ob für die in der Option im Abschnitt CatalogFiles aufgeführten Dateien <HASH> ein \[ Hashwert erstellt werden \] soll.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003** und Windows XP: Diese Option wird nicht unterstützt.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| EncodingType<br/>   | Typ der verwendeten Nachrichtencodierung. Wenn sie leer gelassen wird, lautet der Standardwert EncodingType PKCS \_ 7 \_ ASN \_ ENCODING \| X509 \_ ASN \_ ENCODING, 0x00010001. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Der Abschnitt CatalogFiles definiert jedes Mitglied der Katalogdatei mit Dateien verschiedener Typen und Attribute verschiedener Typen \[ \] in separaten Gruppen.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Verweistag<br/></td>
<td>Textverweis auf die Datei. Dies kann beliebige ASCII-Textzeichen mit Ausnahme des Gleichheitszeichens (=) enthalten. Das System muss dieses Tag nach der Installation reproduzieren können. <br/> Verwenden <HASH> Sie als Präfix des Dateinamens. Dies führt dazu, dass das Tag der Hash der Datei in ASCII-Zeichenfolgenform ist. <br/></td>
</tr>
<tr class="even">
<td>Dateipfad und -name<br/></td>
<td>Der Dateiname, einschließlich der zu analysierenden Erweiterung und des relativen Pfads zur Datei. Jeder Dateityp, der mit SignTool signiert werden kann, kann einem Katalog hinzugefügt werden. Beispielsweise können Dateinamen mit den folgenden Erweiterungen einem Katalog hinzugefügt werden: .exe, .cab, .cat, .ocx, .dll und .stl.<br/></td>
</tr>
<tr class="odd">
<td>ALTSIPID<br/></td>
<td>DIE SIP-GUID, die für hashbasiertes Hashing anstelle des standardmäßigen SIP basierend auf dem Dateityp verwendet werden soll. Dieser Eintrag ist optional. Wenn dieser Eintrag ausgelassen wird, wird für das Mitglied ein Hash mit dem Standard-SIP verwendet. Wenn kein standardmäßig installierter SIP gefunden wird, wird Flat SIP verwendet.<br/></td>
</tr>
<tr class="even">
<td>guid<br/></td>
<td>Textdarstellung einer GUID.<br/></td>
</tr>
<tr class="odd">
<td>ATTRx<br/></td>
<td>Optional. Attribut oder Anweisung zur Datei oder zum Inhalt. Es kann eine beliebige Anzahl von Attributen geben, einschließlich keiner.<br/></td>
</tr>
<tr class="even">
<td>Typ<br/></td>
<td>Definiert, welcher Attributtyp im Format 0x00000000 (Text) hinzugefügt wird. Diese Option kann eine bitweise<strong>OR-Kombination</strong> von 0 (null) oder mehr der folgenden Werte sein:<br/>
<ul>
<li>0x10000000 Authenticated-Attribut (signiert, im Hash enthalten).</li>
<li>0x20000000 nicht authentifizierte Attribut (ohne Vorzeichen, nicht im Hash enthalten, nicht überprüfbar).</li>
<li>0x01000000 Attribute wird nicht in SHA1-Einträge in einem CatalogVersion 2-Katalog repliziert.</li>
<li>0x00010000 Attribute wird als Klartext dargestellt. Es wird keine Konvertierung durchgeführt.</li>
<li>0x00020000 Attribute wird in Base64-Codierung dargestellt. Dies wird verwendet, um Binärdaten zu darstellen.</li>
<li>0x00000001 Attribut ist ein Name-Wert-Paar. Verwenden Sie die oid-Option für den Namen. Dieses Attribut ist langsam. Verwenden Sie diese Option daher nur wenig.</li>
<li>0x00000002 Attribute wird von einem <a href="/windows/desktop/SecGloss/o-gly"><em>Objektbezeichner (OID)</em></a> referenziert.</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>oid<br/></td>
<td>Die Textdarstellung des Verweisschlüssels des Attributs. Es handelt sich um eine OID in Form einer Textzeichenfolge in gepunkteter Quad-Notation (z.B. a.b.c.d) oder einen Textnamen.<br/></td>
</tr>
<tr class="even">
<td>value<br/></td>
<td>Die Textdarstellung des Werts des Attributs. Der Typ der verwendeten Textdarstellung hängt vom Wert der Typoption ab. Die Länge wird durch die EOL-Zeichen bestimmt.<br/></td>
</tr>
<tr class="odd">
<td><HASH><br/></td>
<td>Hashing der angegebenen Datei.<br/></td>
</tr>
</tbody>
</table>



 

Die generierte Katalogdatei ist nicht signiert. Wenn es vor der Übertragung signiert werden soll, wird es mit [SignTool signiert.](signtool.md)

 

 
