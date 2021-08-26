---
description: Die TRANSFORMS-Eigenschaft ist eine Liste der Transformationen, die das Installationsprogramm beim Installieren des Pakets anwendet.
ms.assetid: da20f99e-3022-4382-97bb-8f1206072347
title: TRANSFORMS-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a0482e660de981e5071526df9b508d948e74ae910c29df7916ac6e497344447
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039420"
---
# <a name="transforms-property"></a>TRANSFORMS-Eigenschaft

Die **TRANSFORMS-Eigenschaft** ist eine Liste der Transformationen, die das Installationsprogramm beim Installieren des Pakets anwendet. Das Installationsprogramm wendet die Transformationen in der gleichen Reihenfolge an, in der sie in der -Eigenschaft aufgeführt sind. Transformationen können anhand ihres Dateinamens oder vollständigen Pfads angegeben werden. Um mehrere Transformationen anzugeben, trennen Sie jeden Dateinamen oder vollständigen Pfad durch ein Semikolon (;). Um beispielsweise drei Transformationen auf ein Paket anzuwenden, legen **Sie TRANSFORMS** auf eine Liste von Dateinamen oder auf eine Liste mit vollständigen Pfaden fest.

``` syntax
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
TRANSFORMS=\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst;\\server3\share3\path3\transform3.mst
```

Sie können angeben, dass eine Transformationsdatei in einen Speicher der .msi Datei eingebettet ist, anstatt als eigenständige Datei, indem Sie dem Dateinamen einen Doppelpunkt (:) voranstellen. Das folgende Beispiel gibt beispielsweise an, dass transform1.mst und transform2.mst in die .msi-Datei eingebettet sind und dass transform3.mst eine eigenständige Datei ist.

``` syntax
TRANSFORMS=:transform1.mst;:transform2.mst;transform3.mst
```

Das Installationsprogramm erfordert die in **TRANSFORMS** aufgeführten Transformationen bei jeder Installation, Ankündigung, Installation bei Bedarf oder Wartungsinstallation des Pakets. Die [Richtlinie TransformsSecure,](transformssecure-policy.md) die **TRANSFORMS-Eigenschaft** und das erste Zeichen der **TRANSFORMS-Zeichenfolge** informieren das Installationsprogramm darüber, wie die Quellresilienz eigenständiger Transformationsdateien behandelt werden kann. Windows Das Installationsprogramm behandelt das Festlegen der [TransformsAtSource-Richtlinie](transformsatsource-policy.md) oder [**TRANSFORMSATSOURCE**](transformsatsource.md) genauso wie die TransformsSecure-Richtlinie und [**TRANSFORMSSECURE.**](transformssecure.md) Beachten Sie, dass in die .msi Datei eingebettete Transformationen nicht zwischengespeichert und immer aus dem Paket abgerufen werden.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>TRANSFORMS-Eigenschaft</th>
<th>Transforms Secure</th>
<th>Zwischenspeicherung und Resilienz</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>@[<em>liste der Dateinamen</em>] Beispiel:<br/> @transform1.mst;transform2.mst; transform3.mst<br/></td>
<td>Keine Auswirkung.</td>
<td><a href="secure-at-source-transforms.md">Secure-At-Source-Transformationen.</a> Die Quelle der Transformationen muss sich im Stammverzeichnis der Quelle für das Paket enthalten. Wenn das Paket installiert oder angekündigt wird, speichert das Installationsprogramm die Transformationen auf dem Computer des Benutzers in einem Cache, in dem der Benutzer keinen Schreibzugriff hat. Wenn die lokale Kopie der Transformation nicht mehr verfügbar ist, sucht das Installationsprogramm nach einer Quelle, um den Cache wiederherzustellen. Die -Methode entspricht der Suche in der Quellliste nach einer .msi-Datei. Weitere Informationen finden Sie unter <a href="source-resiliency.md">Quellresilienz.</a></td>
</tr>
<tr class="even">
<td>| [<em>Liste der Pfade</em>] Beispiel:<br/>
<pre class="syntax" data-space="preserve"><code>|\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst</code></pre></td>
<td>Keine Auswirkung.</td>
<td><a href="secure-full-path-transforms.md">Secure-Full-Path transformiert</a>. Die Quelle jeder Transformation muss sich am vollständigen Pfad befinden, der an <strong>TRANSFORMS</strong>übergeben wird. Die Transformationsquelle muss sich nicht an der Quelle des Pakets befinden. Wenn das Paket installiert oder angekündigt wird, speichert das Installationsprogramm die Transformationen auf dem Computer des Benutzers in einem Cache, in dem der Benutzer keinen Schreibzugriff hat. Wenn die lokale Kopie der Transformation nicht mehr verfügbar ist, kann das Installationsprogramm den Cache nur aus der Quelle unter dem angegebenen Pfad wiederherstellen.</td>
</tr>
<tr class="odd">
<td>[<em>Liste der Dateinamen</em>] Das erste Zeichen ist nicht @ oder |.<br/> Beispiel:<br/> transform1.mst;transform2.mst; transform3.mst<br/></td>
<td><a href="transformssecure-policy.md">TransformsSecure-Richtlinie</a> oder <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> auf 1 ODER festgelegt<br/> <a href="transformsatsource-policy.md">TransformsAtSource-Richtlinie</a> oder <a href="transformsatsource.md"><strong>TRANSFORMSATSOURCE</strong></a> auf 1 festgelegt.<br/></td>
<td>Wenn <strong>TRANSFORMS</strong> eine Liste von Dateinamen ist, behandelt das Installationsprogramm diese als <a href="secure-at-source-transforms.md">Secure-At-Source-Transformationen.</a> Wenn <strong>TRANSFORMS</strong> eine Liste mit vollständigen Pfaden ist, behandelt das Installationsprogramm diese als <a href="secure-full-path-transforms.md">Secure-Full-Path-Transformationen.</a><br/></td>
</tr>
<tr class="even">
<td>[<em>Liste der Dateinamen</em>] Das erste Zeichen ist nicht @ oder |.<br/> Beispiel:<br/> transform1.mst;transform2.mst; transform3.mst<br/></td>
<td><a href="transformssecure-policy.md">TransformsSecure-Richtlinie</a> und <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> sind nicht auf AND festgelegt.<br/> <a href="transformsatsource-policy.md">TransformsAtSource-Richtlinie</a> und <a href="transformsatsource.md"><strong>TRANSFORMSATSOURCE</strong></a> sind nicht festgelegt.<br/></td>
<td><a href="unsecured-transforms.md">Ungesicherte Transformationen.</a> Die Quelle der Transformationen muss sich im Stammverzeichnis der Quelle für das Paket enthalten. Wenn das Paket pro Benutzer installiert oder angekündigt wird, speichert das Installationsprogramm die Transformationen im Profil des Benutzers. Dadurch kann ein Benutzer zwischen Computern roaming, während seine Anpassungen beibehalten werden. Bei einer Computerinstallation wird die Transformation im Ordner %windir%\Installer gespeichert. Wenn die lokale Kopie der Transformation nicht mehr verfügbar ist, sucht das Installationsprogramm nach einer Quelle, um den Cache wiederherzustellen. Die -Methode entspricht der Suche in der Quellliste nach einer .msi-Datei. Weitere Informationen finden Sie unter <a href="source-resiliency.md">Quellresilienz.</a></td>
</tr>
<tr class="odd">
<td>[<em>Liste der Pfade</em>] Das erste Zeichen ist nicht @ oder |.<br/> Beispiel:<br/>
<pre class="syntax" data-space="preserve"><code>\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst.</code></pre></td>
<td><a href="transformsatsource-policy.md">TransformsAtSource-Richtlinie</a> und <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> sind nicht auf AND festgelegt.<br/> <a href="transformsatsource-policy.md">TransformsAtSource-Richtlinie</a> und <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> sind nicht festgelegt.<br/></td>
<td><a href="unsecured-transforms.md">Ungesicherte Transformationen.</a> Wenn das Paket pro Benutzer installiert oder angekündigt wird, speichert das Installationsprogramm die Transformationen im Profil des Benutzers. Dadurch kann ein Benutzer zwischen Computern roaming, während seine Anpassungen beibehalten werden. Bei einer Computerinstallation wird die Transformation im Ordner %windir%\Installer gespeichert. Wenn die lokale Kopie der Transformation nicht mehr verfügbar ist, sucht das Installationsprogramm nach einer Quelle, um den Cache wiederherzustellen. Die -Methode entspricht der Suche in der Quellliste nach einer .msi-Datei. Weitere Informationen finden Sie unter <a href="source-resiliency.md">Quellresilienz.</a></td>
</tr>
</tbody>
</table>



 

Sie können Dateinamen und Pfade nicht zusammen in derselben **TRANSFORMS-Liste** verwenden. Sie können keine sicheren Und Profiltransformationen zusammen in derselben Liste angeben. Sie können Transformationen, die in das Paket eingebettet sind, in eine Liste mit anderen Transformationen einschließen.

``` syntax
@transform1.mst;:transform2.mst 
|\\server\share\path\transform1.mst;:transform2.mst
```

Beachten Sie, dass Semikolons nicht in einem Transformationsdateinamen oder -pfad verwendet werden dürfen, da das Listentrennzeichen für Transformationen das Semikolon ist.

## <a name="remarks"></a>Hinweise

In Fällen, in denen die [TransformsSecure-Richtlinie](transformssecure-policy.md) oder die [**TRANSFORMSSECURE-Eigenschaft**](transformssecure.md) mit Windows Installer festgelegt wurde, ist es nicht erforderlich, das @- oder das \| -Symbol zu übergeben, wenn **TRANSFORMS** über die Befehlszeile festgelegt wird. Das Installationsprogramm setzt Secure-At-Source oder Secure-Full-Path voraus, wenn die Liste vollständig aus Dateinamen besteht, die sich in der Quelle befinden, oder vollständig aus vollständigen Pfaden. Sie können die beiden Arten von Transformationsquellen immer noch nicht mischen.

Beachten Sie, dass das Installationsprogramm eine andere Suchreihenfolge für unsichere Transformationen verwendet, die bei der erstmaligen Installation und bei Wartungsinstallationen angewendet werden. Weitere Informationen finden Sie unter [Unsecured Transforms](unsecured-transforms.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Unter [Windows Installer Run-Time Requirements (Anforderungen für](windows-installer-portal.md) Windows Installer) finden Sie Informationen zu den mindest erforderlichen Windows Service Packs für eine Windows Installer-Version.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Datenbanktransformationen](database-transforms.md)
</dt> <dt>

[Zusammenführungen und Transformationen](merges-and-transforms.md)
</dt> <dt>

[Quellresilienz](source-resiliency.md)
</dt> </dl>

 

 




