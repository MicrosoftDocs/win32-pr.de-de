---
description: Bei der Eigenschaft Transformationen handelt es sich um eine Liste der Transformationen, die das Installationsprogramm bei der Installation des Pakets anwendet.
ms.assetid: da20f99e-3022-4382-97bb-8f1206072347
title: Transformationen (Eigenschaft)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1abbb45db507f7ab813b96e9023634cbe217b554
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361394"
---
# <a name="transforms-property"></a>Transformationen (Eigenschaft)

Bei der Eigenschaft **Transformationen** handelt es sich um eine Liste der Transformationen, die das Installationsprogramm bei der Installation des Pakets anwendet. Das Installationsprogramm wendet die Transformationen in derselben Reihenfolge an, in der Sie in der-Eigenschaft aufgeführt sind. Transformationen können mithilfe Ihres Datei namens oder des vollständigen Pfads angegeben werden. Zum Angeben mehrerer Transformationen trennen Sie die einzelnen Dateinamen oder den vollständigen Pfad durch ein Semikolon (;). Wenn Sie z. b. drei Transformationen auf ein Paket anwenden möchten, legen Sie **Transformationen** auf eine Liste von Dateinamen oder auf eine Liste vollständiger Pfade fest.

``` syntax
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
TRANSFORMS=\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst;\\server3\share3\path3\transform3.mst
```

Sie können angeben, dass eine Transformations Datei in einen Speicher der MSI-Datei eingebettet ist, nicht als eigenständige Datei, indem Sie dem Dateinamen einen Doppelpunkt (:). Das folgende Beispiel zeigt beispielsweise an, dass transform1. MST und transform2. MST in die MSI-Datei eingebettet sind und transform3. MST eine eigenständige Datei ist.

``` syntax
TRANSFORMS=:transform1.mst;:transform2.mst;transform3.mst
```

Das Installationsprogramm erfordert die in **Transformationen** aufgeführten Transformationen bei jeder Installation, Ankündigung, Installation nach Bedarf oder Wartungs Installation des Pakets. Die [transformssecure-Richtlinien](transformssecure-policy.md) Richtlinie, die Transform **-Eigenschaft und** das erste Zeichen der Transformations Zeichenfolge **informieren** das Installationsprogramm darüber, wie die Quell Resilienz von eigenständigen Transformations Dateien bewältigt werden kann. Windows Installer behandelt das Festlegen der [transformsatsource-Richtlinie](transformsatsource-policy.md) oder [**transformsatsource**](transformsatsource.md) mit der transformssecure-Richtlinie und [**transformssecure**](transformssecure.md). Beachten Sie, dass in die MSI-Datei eingebettete Transformationen nicht zwischengespeichert werden und immer aus dem Paket abgerufen werden.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Transformationen (Eigenschaft)</th>
<th>Sichere Transformationen</th>
<th>Caching und Resilienz</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>@ [<em>Liste der Dateinamen</em>] Beispiel:<br/> @transform1.mst; transform2. MST; transform3. MST<br/></td>
<td>Keine Auswirkung.</td>
<td><a href="secure-at-source-transforms.md">Secure-at-Source-Transformationen</a>. Die Quelle der Transformationen muss sich im Stammverzeichnis der Quelle für das Paket befinden. Wenn das Paket installiert oder angekündigt wird, speichert das Installationsprogramm die Transformationen auf dem Computer des Benutzers in einem Cache, in dem der Benutzer keinen Schreibzugriff hat. Wenn die lokale Kopie der Transformation nicht verfügbar ist, sucht der Installer nach einer Quelle, um den Cache wiederherzustellen. Die-Methode ist identisch mit dem Durchsuchen der Quell Liste nach einer MSI-Datei. Siehe <a href="source-resiliency.md">quellresilienz</a>.</td>
</tr>
<tr class="even">
<td>| [<em>Liste der Pfade</em>] Beispiel<br/>
<pre class="syntax" data-space="preserve"><code>|\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst</code></pre></td>
<td>Keine Auswirkung.</td>
<td><a href="secure-full-path-transforms.md">Sichere vollständige Pfad Transformationen</a>. Die Quelle jeder Transformation muss sich am vollständigen Pfad befinden, der an <strong>Transformationen</strong>übermittelt wird. Die Transformations Quelle muss sich nicht an der Quelle des Pakets befinden. Wenn das Paket installiert oder angekündigt wird, speichert das Installationsprogramm die Transformationen auf dem Computer des Benutzers in einem Cache, in dem der Benutzer keinen Schreibzugriff hat. Wenn die lokale Kopie der Transformation nicht verfügbar ist, kann der Installer den Cache nur aus der Quelle unter dem angegebenen Pfad wiederherstellen.</td>
</tr>
<tr class="odd">
<td>[<em>Liste der Dateinamen</em>] Das erste Zeichen ist nicht @ oder |.<br/> Beispiel:<br/> transform1. MST; transform2. MST; transform3. MST<br/></td>
<td><a href="transformssecure-policy.md">Transformssecure-Richtlinie</a> oder <a href="transformssecure.md"><strong>transformssecure</strong></a> auf 1 oder festgelegt<br/> <a href="transformsatsource-policy.md">Transformsatsource-Richtlinie</a> oder <a href="transformsatsource.md"><strong>transformsatsource</strong></a> auf 1 festgelegt.<br/></td>
<td>Wenn <strong>Transformationen</strong> eine Liste von Dateinamen sind, behandelt das Installationsprogramm Sie als <a href="secure-at-source-transforms.md">sichere Transformationen</a>. Wenn <strong>Transformationen</strong> eine Liste vollständiger Pfade sind, behandelt das Installationsprogramm Sie als <a href="secure-full-path-transforms.md">sichere vollständige Pfad Transformationen</a>.<br/></td>
</tr>
<tr class="even">
<td>[<em>Liste der Dateinamen</em>] Das erste Zeichen ist nicht @ oder |.<br/> Beispiel:<br/> transform1. MST; transform2. MST; transform3. MST<br/></td>
<td>Die <a href="transformssecure-policy.md">transformssecure-Richtlinie</a> und <a href="transformssecure.md"><strong>transformssecure</strong></a> sind nicht festgelegt.<br/> <a href="transformsatsource-policy.md">Transformsatsource-Richtlinie</a> und <a href="transformsatsource.md"><strong>transformsatsource</strong></a> sind nicht festgelegt.<br/></td>
<td><a href="unsecured-transforms.md">Unsichere Transformationen</a>. Die Quelle der Transformationen muss sich im Stammverzeichnis der Quelle für das Paket befinden. Wenn das Paket pro Benutzer installiert oder angekündigt wird, speichert das Installationsprogramm die Transformationen im Profil des Benutzers. Dies ermöglicht es einem Benutzer, zwischen Computern zu wechseln, während die Anpassungen beibehalten werden. Für eine Computer spezifische Installation wird die Transformation im Ordner%windir%\Installer gespeichert. Wenn die lokale Kopie der Transformation nicht verfügbar ist, sucht der Installer nach einer Quelle, um den Cache wiederherzustellen. Die-Methode ist identisch mit dem Durchsuchen der Quell Liste nach einer MSI-Datei. Siehe <a href="source-resiliency.md">quellresilienz</a>.</td>
</tr>
<tr class="odd">
<td>[<em>Liste der Pfade</em>] Das erste Zeichen ist nicht @ oder |.<br/> Beispiel:<br/>
<pre class="syntax" data-space="preserve"><code>\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst.</code></pre></td>
<td><a href="transformsatsource-policy.md">Transformsatsource-Richtlinie</a> und <a href="transformssecure.md"><strong>transformssecure</strong></a> sind nicht festgelegt.<br/> <a href="transformsatsource-policy.md">Transformsatsource-Richtlinie</a> und <a href="transformssecure.md"><strong>transformssecure</strong></a> sind nicht festgelegt.<br/></td>
<td><a href="unsecured-transforms.md">Unsichere Transformationen</a>. Wenn das Paket pro Benutzer installiert oder angekündigt wird, speichert das Installationsprogramm die Transformationen im Profil des Benutzers. Dies ermöglicht es einem Benutzer, zwischen Computern zu wechseln, während die Anpassungen beibehalten werden. Für eine Computer spezifische Installation wird die Transformation im Ordner%windir%\Installer gespeichert. Wenn die lokale Kopie der Transformation nicht verfügbar ist, sucht der Installer nach einer Quelle, um den Cache wiederherzustellen. Die-Methode ist identisch mit dem Durchsuchen der Quell Liste nach einer MSI-Datei. Siehe <a href="source-resiliency.md">quellresilienz</a>.</td>
</tr>
</tbody>
</table>



 

Dateinamen und Pfade können nicht in **der gleichen Transformations** Liste verwendet werden. Es ist nicht möglich, sichere und Profil Transformationen in derselben Liste anzugeben. Sie können Transformationen, die in das Paket eingebettet sind, in eine Liste mit anderen Transformationen einschließen.

``` syntax
@transform1.mst;:transform2.mst 
|\\server\share\path\transform1.mst;:transform2.mst
```

Beachten Sie Folgendes: da das Listen Trennzeichen für Transformationen das Semikolon ist, dürfen Semikolons nicht in einem Transformations Dateinamen oder-Pfad verwendet werden.

## <a name="remarks"></a>Bemerkungen

In Fällen, in denen die [transformssecure-Richtlinie](transformssecure-policy.md) oder die [**transformssecure**](transformssecure.md) -Eigenschaft mit Windows Installer festgelegt wurde, ist es nicht notwendig, beim \| Festlegen von **Transformationen** mithilfe der Befehlszeile das @-oder-Symbol zu übergeben. Das Installationsprogramm setzt den Wert "Secure-at-Source" oder "Secure-Full-Path" voraus, wenn die Liste vollständig aus Dateinamen besteht, die sich in der Quelle befinden oder ausschließlich vollständige Pfade Es ist immer noch nicht möglich, die beiden Typen von Transformations Quellen zu mischen.

Beachten Sie, dass das Installationsprogramm eine andere Such Reihenfolge für unsichere Transformationen verwendet, die bei der erstmaligen Installation und Wartung der Wartung Weitere Informationen finden Sie unter [unsichere Transformationen](unsecured-transforms.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Daten Bank Transformationen](database-transforms.md)
</dt> <dt>

[Zusammenführungen und Transformationen](merges-and-transforms.md)
</dt> <dt>

[Quellen Resilienz](source-resiliency.md)
</dt> </dl>

 

 




