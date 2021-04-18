---
description: Die Mt.exe-Datei ist ein Tool, das signierte Dateien und Kataloge generiert. Es ist im Microsoft Windows Software Development Kit (SDK) verfügbar. Mt.exe erfordert, dass die Datei, auf die im Manifest verwiesen wird, im gleichen Verzeichnis wie das Manifest vorhanden ist.
ms.assetid: 37f010ee-2658-4547-9871-c913201042de
title: Mt.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df654a943bad272a091dc6ac20cc1dcdab1731a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339727"
---
# <a name="mtexe"></a>Mt.exe

Die Mt.exe-Datei ist ein Tool, das signierte Dateien und Kataloge generiert. Es ist im Microsoft Windows Software Development Kit (SDK) verfügbar. Mt.exe erfordert, dass die Datei, auf die im Manifest verwiesen wird, im gleichen Verzeichnis wie das Manifest vorhanden ist.

Mt.exe generiert Hashes mithilfe der CryptoAPI-Implementierung des Secure Hash-Algorithmus (SHA-1). Weitere Informationen zu Hash Algorithmen finden Sie unter [Hash-und Signatur Algorithmen](/windows/desktop/SecCrypto/hash-and-signature-algorithms). Hashes werden als hexadezimale Zeichenfolge in die **Datei** Tags im Manifest eingefügt. Das Tool generiert zurzeit nur SHA-1-Hashes, obwohl Dateien in Manifesten andere hashingschemas verwenden können.

Mt.exe verwendet Makecat.exe, um Katalogdateien (. cat) aus Katalog Definitions Dateien (. CDF) zu generieren. Dieses Tool füllt eine Standardvorlagen-CDF mit dem Namen und dem Speicherort des Manifests aus. Dies kann mit Makecat.exe verwendet werden, um den assemblykatalog zu generieren.

Die Version von Mt.exe, die in neueren Versionen des Windows SDK bereitgestellt wurde, kann auch verwendet werden, um Manifeste für verwaltete Assemblys und nicht verwaltete parallele Assemblys zu generieren.

## <a name="syntax"></a>Syntax

**mt.exe \[ -Manifest** _<Component1. Manifest><component2. Manifest>_ *_\] \[ -Identity:_* *<identity string> * **\] \[ -RGS:** _<file1. RGS>_* _\] \[ -tlb:_ *_<file2. tlb>_* _\] \[ -dll:_ *_<file3.dll>_* _\] \[ -Ersetzungen:_ *_<XML filename>_* _\] \[ -managedassemblyname:_ *_<managed assembly>_* _\] \[ -nodepen-Category \] \[ \] \[ -out:_ *_<output manifest name>_* _\] \[ -inputresource:_ *_<file4>_* _; \[ \# \]_ *_><0 Ressourcen- \_ ID><1_* _\] \[ -outputresource:_ *_<file5>_* _; \[ \# \]_ *_><2 Ressourcen- \_ ID><3_* _\] \[ -UpdateResource:_ *_<file6>_* _; \[ \# \]_ *_><4 Ressourcen- \_ ID><5_* _\] \[ -hashupdate \[ :_ *_<path to files>_* _\] \] \[ -makecdfs \] \[ -Validate \_ Manifest \] \[ - \_ Dateihashes validieren \_ :_ *_<path to files>_* _\] \[ -Canonicalize \] \[ -Überprüfung \_ auf \_ Duplikate \] \[ -nologo \] \[ -verbose \]_*

## <a name="command-line-options"></a>Befehlszeilenoptionen

Mt.exe verwendet die folgenden Befehlszeilenoptionen für die Groß-und Kleinschreibung.



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
<td>-Manifest</td>
<td>Gibt den Namen der Manifest-Datei an. Geben Sie einen Manifest-Dateinamen an, um ein einzelnes Manifest zu ändern. Beispielsweise Component. manifest.<br/> Wenn Sie mehrere Manifeste zusammenführen möchten, geben Sie die Namen der Quell Manifeste hier an. Geben Sie den Namen des aktualisierten Manifests entweder mit den Optionen " <strong>-out</strong>", " <strong>-outputresource</strong>" oder " <strong>-UpdateResource</strong> " an. Beispielsweise fordert die folgende Befehlszeile einen Vorgang an, der zwei Manifeste, man1. Manifest und man2. Manifest, in einem neuen Manifest, Man3. Manifest, zusammenführt.<br/> <strong>mt.exe-Manifest man1. Manifest man2. Manifest-out: Man3. Manifest</strong><br/>
<blockquote>
[!Note]<br />
Kein Doppelpunkt (:) ist mit der Option <strong>-Manifest</strong> erforderlich.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>-Identität</td>
<td>Stellt die Attributwerte des <strong>assemblyIdentity</strong> -Elements des Manifests bereit. Das-Argument der <strong>-Identity-</strong> Option ist ein Zeichen folgen Wert, der die Attributwerte in Feldern enthält, die durch Kommas getrennt sind. Geben Sie den Wert des <strong>Name</strong> -Attributs im ersten Feld an, ohne " &quot; Name = Substring" einzuschließen &quot; . Alle verbleibenden Felder geben die Attribute und deren Werte im folgenden Format an: <em> <attribute name> </em> = <em> <attribute_value> </em> .<br/> Um z. b. das <strong>assemblyIdentity</strong> -Element des Manifests mit den folgenden Informationen zu aktualisieren:<br/> <assemblyIdentity type=&quot;win32&quot; name=&quot;Microsoft.Windows.SampleAssembly&quot; version=&quot;6.0.0.0&quot; processorArchitecture=&quot;x86&quot; publicKeyToken=&quot;a5aaf5ba15723d5&quot;/> <br/> Fügen Sie die folgende <strong>-Identity-</strong> Option in die Befehlszeile ein:<br/> <strong>-Identität:</strong> &quot; Microsoft. Windows. SampleAssembly, ProcessorArchitecture = x86, Version = 6.0.0.0, Type = Win32, PublicKeyToken = a5aaf5ba15723d5&quot;<br/></td>
</tr>
<tr class="odd">
<td>-RGS</td>
<td>Gibt den Namen der Registrierungs Skriptdatei (. rgs) an. Die Option <strong>-dll</strong> ist erforderlich, um die Option <strong>-RGS</strong> zu verwenden.<br/></td>
</tr>
<tr class="even">
<td>-TLB</td>
<td>Gibt den Namen der Typbibliotheksdatei (.tlb) an. Die Option " <strong>-dll</strong> " ist erforderlich, um die <strong>-tlb-</strong> Option zu verwenden.<br/></td>
</tr>
<tr class="odd">
<td>-dll</td>
<td>Gibt den Namen der DLL-Datei (Dynamic Link Library) an. Die Option <strong>-dll</strong> ist für <strong>mt.exe</strong> erforderlich, wenn die Optionen <strong>-RGS</strong> oder <strong>-tlb</strong> verwendet werden. Geben Sie den Namen der dll an, die Sie schließlich aus den RGS-oder TLB-Dateien erstellen möchten.<br/> Der folgende Befehl fordert beispielsweise einen Vorgang an, der ein Manifest aus RGS-und TLB-Dateien generiert.<br/> <strong>mt.exe-RGS: testreg1. RGS-tlb: testlib1. tlb -dll:test.dll-Ersetzungen: Rep. Manifest-Identity: &quot; Microsoft. Windows. SampleAssembly, ProcessorArchitecture = x86, Version = 6.0.0.0, Type = Win32, PublicKeyToken = a5aaf5ba15723d5 &quot; -out: rgstlb. Manifest</strong><br/></td>
</tr>
<tr class="even">
<td>-Ersetzungen</td>
<td>Gibt die Datei an, die Werte für die ersetzbare Zeichenfolge in der RGS-Datei enthält.<br/></td>
</tr>
<tr class="odd">
<td>-managedassemblyname</td>
<td>Generiert ein Manifest aus der angegebenen verwalteten Assembly. Verwenden Sie mit der Option <strong>-nodependenz</strong> , um ein Manifest ohne Abhängigkeits Elemente zu generieren. Verwenden Sie mit der Option <strong>-Category</strong> , um ein Manifest mit kategorietags zu generieren. Wenn managed.dll z. b. eine verwaltete Assembly ist, generiert die folgende Befehlszeile das out. Manifest aus managed.dll.<br/> <strong>mt.exe -managedassemblyname:managed.dll: out. Manifest</strong> <br/></td>
</tr>
<tr class="even">
<td>-noabhängigkeit</td>
<td>Gibt einen Vorgang an, der ein Manifest ohne Abhängigkeits Elemente generiert. Die Option <strong>-noabhängigkeiten</strong> erfordert die Option <strong>-managedassemblyname</strong> . Wenn managed.dll z. b. eine verwaltete Assembly ist, generiert die folgende Befehlszeile das out. Manifest aus managed.dll ohne Abhängigkeitsinformationen.<br/> <strong>mt.exe -managedassemblyname:managed.dll: out. Manifest-noabhängigkeit</strong><br/></td>
</tr>
<tr class="odd">
<td>-Kategorie</td>
<td>Gibt einen Vorgang an, der ein Manifest mit kategorietags generiert. Die Option <strong>-Category</strong> erfordert die Option <strong>-managedassemblyname</strong> . Wenn managed.dll z. b. eine verwaltete Assembly ist, generiert die folgende Befehlszeile das out. Manifest aus managed.dll mit kategorietags.<br/> <strong>mt.exe -managedassemblyname:managed.dll: out. Manifest-Category</strong><br/></td>
</tr>
<tr class="even">
<td>-nologo</td>
<td>Gibt einen Vorgang an, der ohne Anzeige der standardmäßigen Microsoft-Copyright Daten ausgeführt wird. Wenn <strong>mt.exe</strong> im Rahmen eines Buildprozesses ausgeführt wird, kann diese Option verwendet werden, um zu verhindern, dass unerwünschte Informationen in die Protokolldateien geschrieben werden. <br/></td>
</tr>
<tr class="odd">
<td>-out</td>
<td>Gibt den Namen des aktualisierten Manifests an. Wenn es sich um einen Vorgang mit einem einzelnen Manifest handelt und die Option <strong>-out</strong> weggelassen wird, wird das ursprüngliche Manifest geändert. <br/></td>
</tr>
<tr class="even">
<td>-Input Resource</td>
<td>Gibt einen Vorgang an, der für ein Manifest ausgeführt wird, das von einer Ressource vom Typ RT_MANIFEST abgerufen wurde. Wenn die Option <strong>-inputresource</strong> ohne Angabe des Ressourcen Bezeichners verwendet wird, <em> <resource_id> </em> verwendet der Vorgang den Wert CREATEPROCESS_MANIFEST_RESOURCE. <br/> Der folgende Befehl fordert beispielsweise einen Vorgang an, der ein Manifest aus einer DLL, dll_with_manifest.dll und einer Manifestressource, man2. Manifest, zusammenfasst. Die zusammengeführten Manifeste werden von einem Manifest in der Ressourcen Datei einer anderen dll, dll_with_merged_manifests empfangen. <br/> <strong>mt.exe -inputresource:dll_with_manifest.dll; #1-Manifest man2. Manifest -outputresource:dll_with_merged_manifest.dll; #3</strong><br/> Um das Manifest aus einer DLL zu extrahieren, geben Sie den Namen der DLL-Datei an. Mit dem folgenden Befehl wird z. b. das Manifest aus lib1.dll extrahiert, und Man3. Manifest empfängt das extrahierte Manifest.<br/> <strong>mt.exe -inputresource:lib.dll; #1-out: Man3. Manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-outputresource</td>
<td>Gibt einen Vorgang an, der ein Manifest generiert, das von einer Ressource vom Typ RT_MANIFEST empfangen werden soll. Wenn die Option <strong>-outputresource</strong> ohne Angabe des Ressourcen Bezeichners verwendet wird, <em> <resource_id> </em> verwendet der Vorgang den Wert CREATEPROCESS_MANIFEST_RESOURCE. <br/></td>
</tr>
<tr class="even">
<td>-UpdateResource</td>
<td>Gibt einen Vorgang an, der der Verwendung der Optionen " <strong>-inputresource</strong> " und " <strong>-outputresource</strong> " mit identischen Argumenten entspricht. Der folgende Befehl fordert beispielsweise einen Vorgang an, der einen Hash der Dateien im angegebenen Pfad berechnet und das Manifest einer Ressource einer portablen ausführbaren Datei (PE) aktualisiert.<br/> <strong>mt.exe -updateresource:dll_with_manifest.dll; #1-hashupdate: f: \Files</strong>.<br/></td>
</tr>
<tr class="odd">
<td>-hashupdate</td>
<td>Berechnet den Hashwert der Dateien an den angegebenen Pfaden und aktualisiert den Wert des <strong>Hash</strong> -Attributs des <strong>File</strong> -Elements mit diesem Wert. <br/> Der folgende Befehl fordert z. b. einen Vorgang an, der zwei Manifest-Dateien, man1. Manifest und man2. Manifest, zusammenführt, und aktualisiert den Wert des <strong>Hash</strong> -Attributs des <strong>File</strong> -Elements im Manifest, das die zusammengeführten Informationen empfängt, gemergt. manifest.<br/> <strong>mt.exe-Manifest man1. Manifest man2. Manifest-hashupdate: d: \filerepository-out: gemergt. Manifest</strong><br/> Wenn die Pfade zu den Dateien nicht angegeben werden, durchsucht der Vorgang den Speicherort des angegebenen Manifests, um das Update zu empfangen. Der folgende Befehl fordert z. b. einen Vorgang an, der den aktualisierten Hashwert mithilfe von Dateien berechnet, die Durchsuchen des Speicher Orts von "aktualisierte. Manifest" gefunden wurden.<br/> <strong>mt.exe-Manifest yourcomponent. Manifest-hashupdate-out: aktualisiert. Manifest</strong><br/></td>
</tr>
<tr class="even">
<td>-validate_manifest</td>
<td>Gibt einen Vorgang an, der eine Syntax Überprüfung der Übereinstimmung des Manifests mit dem Manifest-Schema ausführt. Der folgende Befehl fordert z. b. eine Überprüfung an, um die Übereinstimmung von man1. Manifest mit dem Schema zu überprüfen. <br/> <strong>mt.exe-Manifest man1. Manifest-validate_manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-validate_file_hashes</td>
<td>Gibt einen Vorgang an, mit dem die Hashwerte der <strong>Datei</strong> Elemente des Manifests überprüft werden. Der folgende Befehl fordert z. b. einen Vorgang an, der die Hashwerte aller <strong>Datei</strong> Elemente von "man1. Manifest" überprüft.<br/> <strong>mt.exe-Manifest man1. Manifest-validate_file_hashes: &quot; c; \Files&quot;</strong><br/></td>
</tr>
<tr class="even">
<td>-Canonicalize</td>
<td>Gibt einen Vorgang an, um das Manifest in kanonische Form zu aktualisieren. Der folgende Befehl aktualisiert z. b. man1. Manifest in kanonische Form.<br/> <strong>mt.exe-Manifest man1. Manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-check_for_duplicates</td>
<td>Gibt einen Vorgang an, mit dem das Manifest auf doppelte Elemente überprüft wird. Mit dem folgenden Befehl wird z. b. man1. Manifest auf doppelte Elemente überprüft.<br/> <strong>mt.exe-man1. Manifest-check_for_duplicates</strong><br/></td>
</tr>
<tr class="even">
<td>-makecdfs</td>
<td>Generiert CDF-Dateien zum Erstellen von Katalogen. Mit dem folgenden Befehl wird z. b. ein Vorgang angefordert, der den Hashwert aktualisiert und eine CDF-Datei generiert.<br/> <strong>mt.exe-Manifest comp1. Manifest-hashupdate-makecdfs-out: aktualisiert. Manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-verbose</td>
<td>Zeigt ausführliche Debuginformationen an.</td>
</tr>
<tr class="even">
<td>-?</td>
<td>Wenn Sie mit-?, oder ohne Optionen und Argumente ausführen, zeigt Mt.exe Hilfetext an.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Parallele assemblyentwicklungtools](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

