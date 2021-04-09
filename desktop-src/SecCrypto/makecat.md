---
description: Ein CryptoAPI-Tool, mit dem eine Katalog Datei erstellt wird.
ms.assetid: 233b3644-f2a5-4166-bac0-30bf2f54e957
title: MakeCat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e6c2c3cb1d7df5a9f717143465d48d4c066466d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862843"
---
# <a name="makecat"></a>MakeCat

Das Tool MakeCat ist ein CryptoAPI-Tool, mit dem eine Katalog Datei erstellt wird. MakeCat ist als Teil des Microsoft Windows Software Development Kit (SDK) für Windows 7 und .NET Framework 4,0 verfügbar und wird standardmäßig im \\ Ordner "bin" des SDK-Installations Pfads installiert.

Das MakeCat-Tool verwendet die folgende Befehlssyntax:

**MakeCat** \[ **-n** \| **-r** \| **-v** \] *Dateiname*

## <a name="parameters"></a>Parameter



| Parameter             | Beschreibung                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-n**<br/>     | Bei einem BEHEB baren Fehler nicht anzuhalten.<br/>                                                                                                                           |
| **-r**<br/>     | Erzwingt das Beenden von MakeCat, wenn wiederherstellbare Fehler auftreten. Dies gilt insbesondere, wenn die Einträge im Abschnitt Katalogdateien einer CDF-Datei verarbeitet werden.<br/> |
| **-v**<br/>     | Ausführlich. Zeigt alle Status-und Fehlermeldungen an.<br/>                                                                                                            |
| *FileName*<br/> | Der Name der zu analysierten CDF-Datei. Informationen zu den erforderlichen Strukturen und Inhalten finden Sie unter "Hinweise".<br/>                                                                         |



 

## <a name="remarks"></a>Bemerkungen

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
> Der letzte Eintrag in der CDF-Datei muss immer über ein explizites Zeilen Trennzeichen am Ende der Zeile verfügen.

 

Der \[ Abschnitt catalogheader \] definiert Informationen über die gesamte Katalog Datei.



| Option                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Name<br/>           | Name der Katalog Datei, einschließlich der Erweiterung.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Resultdir<br/>      | Verzeichnis, in dem die erstellte. cat-Datei platziert wird. Wenn dies nicht angegeben ist, wird das aktuelle Standardverzeichnis verwendet. Wenn das Verzeichnis nicht vorhanden ist, wird es erstellt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Veröffentlichversion<br/>  | Diese Option wird nicht unterstützt. <br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Katalogversion. Wenn das Feld leer gelassen wird, wird der Standardwert 1 verwendet.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| CatalogVersion<br/> | Katalogversion. Wenn die Version nicht vorhanden ist oder auf 1 festgelegt ist, wird "0x100" an den *dwpublicversion* -Parameter der [**cryptgatopen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) -Funktion übergeben, und es wird eine Katalog Datei der Version 1 erstellt. Die hashalgorithms-Option muss leer sein oder SHA1 enthalten.<br/> Wenn die Version auf 2 festgelegt ist, wird "0x200" an den *dwpublicversion* -Parameter der [**cryptgatopen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) -Funktion übergeben, und es wird eine Katalog Datei der Version 2 erstellt. Die hashalgorithms-Option muss SHA256 enthalten.<br/> Wenn diese Option vorhanden ist, aber einen anderen Wert als 1 oder 2 enthält, führt das MakeCat-Tool zu einem Fehler.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Diese Option wird nicht unterstützt.<br/> <br/> |
| Hashalgorithms<br/> | Der Name des verwendeten Hash Algorithmus. Weitere Informationen finden Sie unter der CatalogVersion-Option.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Diese Option wird nicht unterstützt.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Einschleusen<br/>     | Gibt an, ob die Dateien, die in der <HASH> Option im \[ Abschnitt catalogfiles aufgeführt sind, mit Hash Hash \]<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Diese Option wird nicht unterstützt.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| EncodingType<br/>   | Der Typ der verwendeten Nachrichten Codierung. Wenn das Feld leer gelassen wird, ist der Standard Codierungstyp PKCS \_ 7 \_ ASN \_ Encoding \| X509 \_ ASN \_ Encoding, 0x00010001. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Der \[ Abschnitt catalogfiles \] definiert jeden Member der Katalog Datei mit Dateien verschiedener Typen und Attribute verschiedener Typen in separaten Gruppen.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Verweistag<br/></td>
<td>Text Verweis auf die Datei. Dies kann beliebige ASCII-Textzeichen außer dem Gleichheitszeichen (=) enthalten. Das System muss dieses Tag nach der Installation reproduzieren können. <br/> Verwenden Sie <HASH> als Präfix des Datei namens. Dies führt dazu, dass das-Tag der Datei Hash in ASCII-Zeichen folgen Form ist. <br/></td>
</tr>
<tr class="even">
<td>Dateipfad und-Name<br/></td>
<td>Der Dateiname, einschließlich der zu erteilenden Erweiterung und des relativen Pfads zur Datei. Jeder Dateityp, der mit SignTool signiert werden kann, kann einem Katalog hinzugefügt werden. Dateinamen mit den folgenden Erweiterungen können z. b. zu einem Katalog hinzugefügt werden:. exe,. cab,. cat,. ocx,. dll und. STL.<br/></td>
</tr>
<tr class="odd">
<td>Altsipid<br/></td>
<td>SIP-GUID, die für Hashwerte anstelle des Standard-SIP basierend auf dem Dateityp verwendet werden soll. Dieser Eintrag ist optional. Wenn dieser Eintrag weggelassen wird, wird der Member mithilfe des standardsip Hashwert. Wenn kein installiertes Standard-SIP gefunden wird, wird der flatsip verwendet.<br/></td>
</tr>
<tr class="even">
<td>guid<br/></td>
<td>Text Darstellung einer GUID.<br/></td>
</tr>
<tr class="odd">
<td>Attrx<br/></td>
<td>Dies ist optional. Attribut oder Anweisung über die Datei oder den Inhalt. Es kann eine beliebige Anzahl von Attributen, einschließlich None, vorhanden sein.<br/></td>
</tr>
<tr class="even">
<td>type<br/></td>
<td>Definiert, welcher Attributtyp im Format 0x00000000 (Text) hinzugefügt wird. Diese Option kann eine bitweise<strong>or</strong> -Kombination von 0 (null) oder mehreren der folgenden Werte sein:<br/>
<ul>
<li>0x10000000 Authenticated-Attribut (signiert, in den Hash eingeschlossen).</li>
<li>0x20000000 nicht authentifiziertes Attribut (ohne Vorzeichen, nicht in den Hash eingeschlossen, nicht überprüfbar).</li>
<li>Das 0x01000000-Attribut wird nicht in SHA1-Einträge in einem CatalogVersion 2-Katalog repliziert.</li>
<li>Das 0x00010000 bis-Attribut wird als Klartext dargestellt. Es wird keine Konvertierung durchgeführt.</li>
<li>Das 0x00020000-Attribut wird in der Base-64-Codierung dargestellt. Diese wird verwendet, um Binärdaten darzustellen.</li>
<li>Das 0x00000001-Attribut ist ein Name-Wert-Paar. Verwenden Sie die OID-Option für den Namen. Dieses Attribut ist langsam. Verwenden Sie daher diese Option sparsam.</li>
<li>auf das 0x00000002-Attribut wird von einem <a href="/windows/desktop/SecGloss/o-gly"><em>Objekt Bezeichner</em></a> (OID) verwiesen.</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>oid<br/></td>
<td>Die Textdarstellung des Verweis Schlüssels des Attributs. Dies ist eine OID in Form einer Text Zeichenfolge in gepunkteter Quad-Notation (z. b. a. b. c. d) oder eines textnamens.<br/></td>
</tr>
<tr class="even">
<td>value<br/></td>
<td>Die Textdarstellung des Werts des Attributs. Der Typ der verwendeten Textdarstellung hängt vom Wert der Type-Option ab. Die EOL-Zeichen bestimmen die Länge.<br/></td>
</tr>
<tr class="odd">
<td><HASH><br/></td>
<td>Hashes der angegebenen Datei.<br/></td>
</tr>
</tbody>
</table>



 

Die generierte Katalog Datei ist nicht signiert. Wenn Sie vor der Übertragung signiert werden soll, wird Sie mithilfe von [SignTool](signtool.md)signiert.

 

 
