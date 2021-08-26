---
description: Die TRANSFORMS-Eigenschaft ist eine Liste der Transformationen, die das Installationsprogramm beim Installieren des Pakets angewendet.
ms.assetid: da20f99e-3022-4382-97bb-8f1206072347
title: TRANSFORMS-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f873e439ef9542efa618a8e86c9667a3c962939f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474316"
---
# <a name="transforms-property"></a>TRANSFORMS-Eigenschaft

Die **TRANSFORMS-Eigenschaft** ist eine Liste der Transformationen, die das Installationsprogramm beim Installieren des Pakets angewendet. Das Installationsprogramm wendet die Transformationen in der reihenfolge an, in der sie in der -Eigenschaft aufgeführt sind. Transformationen können durch ihren Dateinamen oder vollständigen Pfad angegeben werden. Um mehrere Transformationen anzugeben, trennen Sie jeden Dateinamen oder vollständigen Pfad durch ein Semikolon (;). Wenn Sie beispielsweise drei Transformationen auf ein Paket anwenden möchten, legen Sie **TRANSFORMS** auf eine Liste von Dateinamen oder auf eine Liste vollständiger Pfade fest.

``` syntax
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
TRANSFORMS=\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst;\\server3\share3\path3\transform3.mst
```

Sie können angeben, dass eine Transformationsdatei in einen Speicher der .msi-Datei eingebettet ist, anstatt als eigenständige Datei, indem Sie dem Dateinamen einen Doppelpunkt (:). Im folgenden Beispiel wird beispielsweise angegeben, dass transform1.mst und transform2.mst in die .msi-Datei eingebettet sind und dass transform3.mst eine eigenständige Datei ist.

``` syntax
TRANSFORMS=:transform1.mst;:transform2.mst;transform3.mst
```

Das Installationsprogramm erfordert die **transformationen,** die in TRANSFORMS bei jeder Installation, Ankündigung, Bedarfsbasierten Installation oder Wartungsinstallation des Pakets aufgeführt sind. Die [Richtlinie TransformsSecure,](transformssecure-policy.md) die **TRANSFORMS-Eigenschaft** und das erste Zeichen der **TRANSFORMS-Zeichenfolge** informieren das Installationsprogramm darüber, wie die Quellresilienz eigenständiger Transformationsdateien behandelt werden soll. Windows Das Installationsprogramm behandelt das Festlegen der [TransformsAtSource-Richtlinie](transformsatsource-policy.md) oder [**TRANSFORMSATSOURCE**](transformsatsource.md) genauso wie TransformsSecure-Richtlinie und [**TRANSFORMSSECURE.**](transformssecure.md) Beachten Sie, dass in die .msi-Datei eingebettete Transformationen nicht zwischengespeichert und immer aus dem Paket erhalten werden.




| TRANSFORMS-Eigenschaft | Sichere Transformationen | Caching und Resilienz | 
|---------------------|-------------------|------------------------|
| @[<em>Liste der Dateinamen</em>] Beispiel:<br /> @transform1.mst;transform2.mst; transform3.mst<br /> | Keine Auswirkung. | <a href="secure-at-source-transforms.md">Secure-At-Source transformiert</a>. Die Quelle der Transformationen muss sich im Stammverzeichnis der Quelle für das Paket finden. Wenn das Paket installiert oder angekündigt wird, speichert das Installationsprogramm die Transformationen auf dem Computer des Benutzers in einem Cache, in dem der Benutzer keinen Schreibzugriff hat. Wenn die lokale Kopie der Transformation nicht mehr verfügbar ist, sucht das Installationsprogramm nach einer Quelle, um den Cache wiederherzustellen. Die -Methode ist identisch mit der Suche in der Quellliste nach einer .msi Datei. Weitere Informationen <a href="source-resiliency.md">finden Sie unter Quellresilienz.</a> | 
| |[<em>Liste der Pfade</em>] Beispiel:<br /><pre class="syntax" data-space="preserve"><code>|\\server\share\path\transform1.mst; \\ server2\share2\path2\transform2.mst</code></pre> | Keine Auswirkung. | <a href="secure-full-path-transforms.md">Secure-Full-Path transformiert</a>. Die Quelle jeder Transformation muss sich auf dem vollständigen Pfad beziehen, der an <strong>TRANSFORMS übergeben wird.</strong> Die Transformationsquelle muss sich nicht an der Quelle des Pakets befinden. Wenn das Paket installiert oder angekündigt wird, speichert das Installationsprogramm die Transformationen auf dem Computer des Benutzers in einem Cache, in dem der Benutzer keinen Schreibzugriff hat. Wenn die lokale Kopie der Transformation nicht mehr verfügbar ist, kann das Installationsprogramm den Cache nur aus der Quelle unter dem angegebenen Pfad wiederherstellen. | 
| [<em>Liste der Dateinamen</em>] Das erste Zeichen ist nicht @ oder |.<br /> Beispiel:<br /> transform1.mst;transform2.mst; transform3.mst<br /> | <a href="transformssecure-policy.md">TransformationenSicherer Richtlinien-</a> oder <a href="transformssecure.md"><strong>TRANSFORMSSECURE-Satz</strong></a> auf 1 OR<br /><a href="transformsatsource-policy.md">TransformsAtSource-Richtlinie</a> oder <a href="transformsatsource.md"><strong>TRANSFORMSATSOURCE</strong></a> auf 1 festgelegt.<br /> | Wenn <strong>TRANSFORMS</strong> eine Liste von Dateinamen ist, behandelt das Installationsprogramm sie als <a href="secure-at-source-transforms.md">Secure-At-Source-Transformationen.</a> Wenn <strong>TRANSFORMS eine</strong> Liste vollständiger Pfade ist, behandelt das Installationsprogramm sie als <a href="secure-full-path-transforms.md">Secure-Full-Path-Transformationen.</a><br /> | 
| [<em>Liste der Dateinamen</em>] Das erste Zeichen ist nicht @ oder |.<br /> Beispiel:<br /> transform1.mst;transform2.mst; transform3.mst<br /> | <a href="transformssecure-policy.md">TransformationenSichere Richtlinien</a> und <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> sind nicht festgelegt UND<br /><a href="transformsatsource-policy.md">TransformsAtSource-Richtlinie</a> <a href="transformsatsource.md"><strong>und TRANSFORMSATSOURCE</strong></a> sind nicht festgelegt.<br /> | <a href="unsecured-transforms.md">Ungesicherte Transformationen.</a> Die Quelle der Transformationen muss sich im Stammverzeichnis der Quelle für das Paket finden. Wenn das Paket pro Benutzer installiert oder angekündigt wird, speichert das Installationsprogramm die Transformationen im Profil des Benutzers. Dies ermöglicht es einem Benutzer, zwischen Computern zu roamingen, während seine Anpassungen beibehalten werden. Bei einer Computerinstallation wird die Transformation im Ordner %windir%\Installer gespeichert. Wenn die lokale Kopie der Transformation nicht mehr verfügbar ist, sucht das Installationsprogramm nach einer Quelle, um den Cache wiederherzustellen. Die -Methode ist identisch mit der Suche in der Quellliste nach einer .msi Datei. Weitere Informationen <a href="source-resiliency.md">finden Sie unter Quellresilienz.</a> | 
| [<em>Liste der Pfade</em>] Das erste Zeichen ist nicht @ oder |.<br /> Beispiel:<br /><pre class="syntax" data-space="preserve"><code>\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst.</code></pre> | <a href="transformsatsource-policy.md">TransformsAtSource-Richtlinie</a> und <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> sind nicht festgelegt UND<br /><a href="transformsatsource-policy.md">TransformsAtSource-Richtlinie</a> <a href="transformssecure.md"><strong>und TRANSFORMSSECURE</strong></a> sind nicht festgelegt.<br /> | <a href="unsecured-transforms.md">Ungesicherte Transformationen.</a> Wenn das Paket pro Benutzer installiert oder angekündigt wird, speichert das Installationsprogramm die Transformationen im Profil des Benutzers. Dies ermöglicht es einem Benutzer, zwischen Computern zu roamingen, während seine Anpassungen beibehalten werden. Bei einer Computerinstallation wird die Transformation im Ordner %windir%\Installer gespeichert. Wenn die lokale Kopie der Transformation nicht mehr verfügbar ist, sucht das Installationsprogramm nach einer Quelle, um den Cache wiederherzustellen. Die -Methode ist identisch mit der Suche in der Quellliste nach einer .msi Datei. Weitere Informationen <a href="source-resiliency.md">finden Sie unter Quellresilienz.</a> | 




 

Dateinamen und Pfade können nicht zusammen in derselben **TRANSFORMS-Liste verwendet** werden. Sie können sichere Transformationen und Profiltransformationen nicht zusammen in derselben Liste angeben. Sie können Transformationen, die in das Paket eingebettet sind, in eine Liste mit anderen Transformationen einbetten.

``` syntax
@transform1.mst;:transform2.mst 
|\\server\share\path\transform1.mst;:transform2.mst
```

Beachten Sie, dass Semikolons nicht in einem Transformationsdateinamen oder -pfad verwendet werden dürfen, da das Listentrennzeichen für Transformationen das Semikolon ist.

## <a name="remarks"></a>Hinweise

In Fällen, in denen die [TransformsSecure-Richtlinie](transformssecure-policy.md) oder die [**TRANSFORMSSECURE-Eigenschaft**](transformssecure.md) mit dem Windows-Installer festgelegt wurde, ist es nicht erforderlich, das @- oder -Symbol zu übergeben, wenn TRANSFORMS über die Befehlszeile festgelegt \| wird.  Das Installationsprogramm geht von Secure-At-Source oder Secure-Full-Path aus, wenn die Liste vollständig aus Dateinamen besteht, die sich in der Quelle befinden, oder vollständig aus vollständigen Pfaden besteht. Sie können immer noch nicht die beiden Arten von Transformationsquellen kombinieren.

Beachten Sie, dass das Installationsprogramm eine andere Such reihenfolge für unsichere Transformationen verwendet, die bei der erstmaligen Installation und bei Wartungsinstallationen angewendet werden. Weitere Informationen finden Sie unter [Ungesicherte Transformationen.](unsecured-transforms.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Windows Service Pack,](windows-installer-portal.md) das für eine Windows Installer-Version erforderlich ist, finden Sie im Run-Time-Installer.<br/> |



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

 

 




