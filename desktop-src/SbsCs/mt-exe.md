---
description: Die Mt.exe ist ein Tool, das signierte Dateien und Kataloge generiert. Sie ist im Microsoft Windows Software Development Kit (SDK) verfügbar. Mt.exe muss die Datei, auf die im Manifest verwiesen wird, im gleichen Verzeichnis wie das Manifest vorhanden sein.
ms.assetid: 37f010ee-2658-4547-9871-c913201042de
title: Mt.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb81f3e0b7bf6b67236f1bd6037d1eceb11e0b89
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623906"
---
# <a name="mtexe"></a>Mt.exe

Die Mt.exe ist ein Tool, das signierte Dateien und Kataloge generiert. Sie ist im Microsoft Windows Software Development Kit (SDK) verfügbar. Mt.exe muss die Datei, auf die im Manifest verwiesen wird, im gleichen Verzeichnis wie das Manifest vorhanden sein.

Mt.exe generiert Hashes mithilfe der CryptoAPI-Implementierung des Secure Hash Algorithm (SHA-1). Weitere Informationen zu Hashalgorithmen finden Sie unter [Hash- und Signaturalgorithmen](/windows/desktop/SecCrypto/hash-and-signature-algorithms). Hashes werden als hexadezimale Zeichenfolge in die **Dateitags** im Manifest eingefügt. Das Tool generiert derzeit nur SHA-1-Hashes, obwohl Dateien in Manifesten möglicherweise andere Hashschemas verwenden.

Mt.exe verwendet Makecat.exe, um Katalogdateien (CAT) aus Katalogdefinitionsdateien (CDF) zu generieren. Dieses Tool füllt eine CDF-Standardvorlage mit dem Namen und Speicherort Ihres Manifests aus. Sie können dies mit Makecat.exe, um den Assemblykatalog zu generieren.

Die version of Mt.exe, die in neueren Versionen des Windows SDK bereitgestellt wurde, kann auch verwendet werden, um Manifeste für verwaltete Assemblys und nicht verwaltete, nebenseitige Assemblys zu generieren.

## <a name="syntax"></a>Syntax

**mt.exe \[ -manifest** _<component1.manifest><component2.manifest>_ *_\] \[ -identity:_* *<identity string> * **\] \[ -rgs:**<_file1.rgs>_* _\] \[ -tlb:_<*_file2.tlb>_* _\] \[ -dll:_ *_<file3.dll>_* _\] \[ -replacements:_ *_<XML filename>_* _\] \[ -managedassemblyname:_ *_<managed assembly>_* _\] \[ -nodependency \] \[ -category \] \[ -out:_ *_<output manifest name>_* _\] \[ -inputresource:_ *_<file4>_* _; \[ \# \]_ *_><0 \_ Ressourcen-ID><1_* _\] \[ -outputresource:_ *_<file5>_* _; \[ \# \]_ *_><2 \_ Ressourcen-ID><3_* _\] \[ -updateresource:_ *_<file6>_* _; \[ \# \]_ *_><4 \_ ressourcen-id><5_* _\] \[ -hashupdate \[ :_ *_<path to files>_* _\] \] \[ -makecdfs \] \[ -validate \_ manifest \] \[ -validate file \_ \_ hashes:_ *_<path to files>_* _\] \[ -canonicalize \] \[ -check \_ for \_ duplicates \] \[ -nologo \] \[ -verbose \]_*

## <a name="command-line-options"></a>Befehlszeilenoptionen

Mt.exe verwendet die folgenden Befehlszeilenoptionen, bei der die Groß-/Kleinschreibung nicht beachtet wird.



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
<td>-manifest</td>
<td>Gibt den Namen der Manifestdatei an. Um ein einzelnes Manifest zu ändern, geben Sie einen Manifestdateinamen an. Beispiel: component.manifest.<br/> Wenn Sie mehrere Manifeste zusammenführen möchten, geben Sie hier die Namen der Quellmanifeste an. Geben Sie den Namen des aktualisierten Manifests mit den Optionen <strong>-out,</strong> <strong>-outputresource</strong>oder <strong>-updateresource</strong> an. Beispielsweise fordert die folgende Befehlszeile einen Vorgang an, der zwei Manifeste, man1.manifest und man2.manifest, in einem neuen Manifest, man3.manifest, zusammenführung.<br/> <strong>mt.exe -manifest man1.manifest man2.manifest -out:man3.manifest</strong><br/>
<blockquote>
[!Note]<br />
Kein Doppelpunkt (:) ist für die Option <strong>-manifest</strong> erforderlich.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>-identity</td>
<td>Stellt die Attributwerte des <strong>assemblyIdentity-Elements</strong> des Manifests dar. Das Argument der <strong>Option -identity</strong> ist ein Zeichenfolgenwert, der die Attributwerte in durch Kommas getrennten Feldern enthält. Geben Sie den Wert des <strong>Namensattributs</strong> im ersten Feld an, ohne eine &quot; &quot; name=-Teilzeichenfolge ein beispielbar zu machen. Alle verbleibenden Felder geben die Attribute und ihre Werte mithilfe des folgenden Formulars an: <em> <attribute name> </em> = <em> <attribute_value> </em> .<br/> Um beispielsweise das <strong>assemblyIdentity-Element</strong> des Manifests mit den folgenden Informationen zu aktualisieren:<br/> <assemblyIdentity type=&quot;win32&quot; name=&quot;Microsoft.Windows.SampleAssembly&quot; version=&quot;6.0.0.0&quot; processorArchitecture=&quot;x86&quot; publicKeyToken=&quot;a5aaf5ba15723d5&quot;/> <br/> Fügen Sie die folgende <strong>Option -identity</strong> in die Befehlszeile ein:<br/> <strong>-identity:</strong> &quot; Microsoft. Windows. SampleAssembly, processorArchitecture=x86, version=6.0.0.0, type=win32, publicKeyToken=a5aaf5ba15723d5&quot;<br/></td>
</tr>
<tr class="odd">
<td>-rgs</td>
<td>Gibt den Namen der Registrierungsskriptdatei (.rgs) an. Die <strong>Option -dll</strong> ist erforderlich, um die <strong>Option -rgs zu</strong> verwenden.<br/></td>
</tr>
<tr class="even">
<td>-tlb</td>
<td>Gibt den Namen der Typbibliotheksdatei (.tlb) an. Die <strong>Option -dll</strong> ist erforderlich, um die <strong>Option -tlb zu</strong> verwenden.<br/></td>
</tr>
<tr class="odd">
<td>-dll</td>
<td>Gibt den Namen der DLL-Datei (Dynamic Link Library) an. Die <strong>Option -dll</strong> ist für <strong>mt.exe</strong> erforderlich, wenn die <strong>Optionen -rgs</strong> oder <strong>-tlb</strong> verwendet werden. Geben Sie den Namen der DLL an, die Sie letztendlich aus den RGS- oder TLB-Dateien erstellen möchten.<br/> Der folgende Befehl fordert beispielsweise einen Vorgang an, der ein Manifest aus RGS- und TLB-Dateien generiert.<br/> <strong>mt.exe -rgs:testreg1.rgs -tlb:testlib1.tlb -dll:test.dll -replacements:rep.manifest -identity: &quot; Microsoft.Windows. SampleAssembly, processorArchitecture=x86, version=6.0.0.0, type=win32, publicKeyToken=a5aaf5ba15723d5 &quot; -out:rgstlb.manifest</strong><br/></td>
</tr>
<tr class="even">
<td>-replacements</td>
<td>Gibt die Datei an, die Werte für die ersetzbare Zeichenfolge in der RGS-Datei enthält.<br/></td>
</tr>
<tr class="odd">
<td>-managedassemblyname</td>
<td>Generiert ein Manifest aus der angegebenen verwalteten Assembly. Verwenden Sie mit der <strong>Option -nodependency,</strong> um ein Manifest ohne Abhängigkeitselemente zu generieren. Verwenden Sie mit der <strong>Option -category,</strong> um ein Manifest mit Kategorietags zu generieren. Wenn es sich bei managed.dll um eine verwaltete Assembly handelt, generiert die folgende Befehlszeile die Datei out.manifest aus managed.dll.<br/> <strong>mt.exe -managedassemblyname:managed.dll -out:out.manifest</strong> <br/></td>
</tr>
<tr class="even">
<td>-nodependency</td>
<td>Gibt einen Vorgang an, der ein Manifest ohne Abhängigkeitselemente generiert. Für <strong>die Option -nodependency</strong> ist die <strong>Option -managedassemblyname</strong> erforderlich. Wenn es sich managed.dll um eine verwaltete Assembly handelt, generiert die folgende Befehlszeile die Datei out.manifest aus managed.dll Abhängigkeitsinformationen.<br/> <strong>mt.exe -managedassemblyname:managed.dll -out:out.manifest -nodependency</strong><br/></td>
</tr>
<tr class="odd">
<td>-category</td>
<td>Gibt einen Vorgang an, der ein Manifest mit Kategorietags generiert. Für <strong>die Option -category</strong> ist die <strong>Option -managedassemblyname</strong> erforderlich. Wenn es sich managed.dll um eine verwaltete Assembly handelt, generiert die folgende Befehlszeile die Datei out.manifest aus managed.dll Kategorietags.<br/> <strong>mt.exe -managedassemblyname:managed.dll -out:out.manifest -category</strong><br/></td>
</tr>
<tr class="even">
<td>-nologo</td>
<td>Gibt einen Vorgang an, der ausgeführt wird, ohne standardmäßige Microsoft-Copyrightdaten anzuzeigen. Wenn <strong>mt.exe</strong> im Rahmen eines Buildprozesses ausgeführt wird, kann diese Option verwendet werden, um zu verhindern, dass unerwünschte Informationen in die Protokolldateien geschrieben werden. <br/></td>
</tr>
<tr class="odd">
<td>-out</td>
<td>Gibt den Namen des aktualisierten Manifests an. Wenn es sich um einen Einzelmanifestvorgang handelt und die <strong>Option -out</strong> weggelassen wird, wird das ursprüngliche Manifest geändert. <br/></td>
</tr>
<tr class="even">
<td>-inputresource</td>
<td>Gibt einen Vorgang an, der für ein Manifest ausgeführt wird, das von einer Ressource vom Typ RT_MANIFEST. Wenn die <strong>Option -inputresource</strong> verwendet wird, ohne den Ressourcenbezeichner anzugeben, verwendet der Vorgang den <em> <resource_id> </em> wertbasierten CREATEPROCESS_MANIFEST_RESOURCE. <br/> Beispielsweise fordert der folgende Befehl einen Vorgang an, der ein Manifest aus einer DLL, einem dll_with_manifest.dll und einer Manifestdatei, man2.manifest, zusammenführung. Die zusammengeführten Manifeste werden von einem Manifest in der Ressourcendatei einer anderen DLL empfangen, dll_with_merged_manifests. <br/> <strong>mt.exe -inputresource:dll_with_manifest.dll;#1 -manifest man2.manifest -outputresource:dll_with_merged_manifest.dll;#3</strong><br/> Um das Manifest aus einer DLL zu extrahieren, geben Sie den Namen der DLL-Datei an. Beispielsweise extrahiert der folgende Befehl das Manifest aus lib1.dll und man3.manifest empfängt das extrahierte Manifest.<br/> <strong>mt.exe -inputresource:lib.dll;#1 -out:man3.manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-outputresource</td>
<td>Gibt einen Vorgang an, der ein Manifest generiert, das von einer Ressource vom Typ RT_MANIFEST. Wenn die <strong>Option -outputresource</strong> verwendet wird, ohne den Ressourcenbezeichner anzugeben, verwendet der Vorgang <em> <resource_id> </em> den wertbasierten CREATEPROCESS_MANIFEST_RESOURCE. <br/></td>
</tr>
<tr class="even">
<td>-updateresource</td>
<td>Gibt einen Vorgang an, der der Verwendung der <strong>Optionen -inputresource</strong> und <strong>-outputresource</strong> mit identischen Argumenten entspricht. Der folgende Befehl fordert beispielsweise einen Vorgang an, der einen Hash der Dateien unter dem angegebenen Pfad berechnet und das Manifest einer Ressource einer portierbaren ausführbaren Datei (PORTABLE EXECUTABLE, PE) aktualisiert.<br/> <strong>mt.exe -updateresource:dll_with_manifest.dll;#1 -hashupdate:f:\files</strong>.<br/></td>
</tr>
<tr class="odd">
<td>-hashupdate</td>
<td>Berechnet den Hashwert der Dateien in den angegebenen <strong></strong> Pfaden und aktualisiert den Wert des Hashattributs des <strong>File-Elements</strong> mit diesem Wert. <br/> Der folgende Befehl fordert beispielsweise einen Vorgang an, der zwei Manifestdateien ( man1.manifest und <strong></strong> man2.manifest) zusammenführung und den Wert des Hashattributs des <strong>File-Elements</strong> im Manifest aktualisiert, das die zusammengeführten Informationen (merged.manifest) empfängt.<br/> <strong>mt.exe -manifest man1.manifest man2.manifest -hashupdate:d:\filerepository -out:merged.manifest</strong><br/> Wenn die Pfade zu den Dateien nicht angegeben sind, durchsucht der Vorgang den Speicherort des angegebenen Manifests, um das Update zu empfangen. Der folgende Befehl fordert beispielsweise einen Vorgang an, der den aktualisierten Hashwert anhand von Dateien berechnet, die durch Durchsuchen des Speicherorts von updated.manifest gefunden wurden.<br/> <strong>mt.exe -manifest yourComponent.manifest -hashupdate -out:updated.manifest</strong><br/></td>
</tr>
<tr class="even">
<td>-validate_manifest</td>
<td>Gibt einen Vorgang an, der eine Syntaxprüfung der Übereinstimmung des Manifests mit dem Manifestschema ausführt. Beispielsweise fordert der folgende Befehl eine Überprüfung an, um die Konformität von man1.manifest mit dem Schema zu überprüfen. <br/> <strong>mt.exe -manifest man1.manifest -validate_manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-validate_file_hashes</td>
<td>Gibt einen Vorgang an, der die Hashwerte der <strong>File-Elemente</strong> des Manifests überprüft. Der folgende Befehl fordert beispielsweise einen Vorgang an, der die Hashwerte aller <strong>File-Elemente</strong> von man1.manifest überprüft.<br/> <strong>mt.exe -manifest man1.manifest -validate_file_hashes: &quot; c;\files&quot;</strong><br/></td>
</tr>
<tr class="even">
<td>-canonicalize</td>
<td>Gibt einen Vorgang zum Aktualisieren des Manifests in kanonische Form an. Beispielsweise aktualisiert der folgende Befehl man1.manifest in kanonische Form.<br/> <strong>mt.exe -manifest man1.manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-check_for_duplicates</td>
<td>Gibt einen Vorgang an, der das Manifest auf doppelte Elemente überprüft. Mit dem folgenden Befehl wird beispielsweise "man1.manifest" auf doppelte Elemente überprüft.<br/> <strong>mt.exe -man1.manifest -check_for_duplicates</strong><br/></td>
</tr>
<tr class="even">
<td>-makecdfs</td>
<td>Generiert CDF-Dateien, um Kataloge zu erstellen. Beispielsweise fordert mit dem folgenden Befehl einen Vorgang an, der den Hashwert aktualisiert und eine CDF-Datei generiert.<br/> <strong>mt.exe -manifest comp1.manifest -hashupdate -makecdfs -out:updated.manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-verbose</td>
<td>Zeigt ausführliche Debuginformationen an.</td>
</tr>
<tr class="even">
<td>-?</td>
<td>Wenn die Ausführung mit -?, oder ohne Optionen und Argumente ausgeführt wird, Mt.exe Hilfetext angezeigt.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwicklungstools für die side-by-side-Assembly](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

