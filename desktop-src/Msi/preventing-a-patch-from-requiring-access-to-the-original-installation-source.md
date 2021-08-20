---
description: Es ist nicht möglich, alle Umstände zu beseitigen, unter denen die Anwendung eines Patches möglicherweise Zugriff auf die ursprüngliche Installationsquelle erfordert.
ms.assetid: f7028c55-e4a5-4596-af7a-728c9f4f367e
title: Verhindern, dass ein Patch Zugriff auf die ursprüngliche Installationsquelle erfordert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5dcadae12b733d76dee8c3acd5ec6af6169c47cfd8c7eeb22ad9693a75859a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376789"
---
# <a name="preventing-a-patch-from-requiring-access-to-the-original-installation-source"></a>Verhindern, dass ein Patch Zugriff auf die ursprüngliche Installationsquelle erfordert

Es ist nicht möglich, alle Umstände zu beseitigen, unter denen die Anwendung eines Patches möglicherweise Zugriff auf die ursprüngliche Installationsquelle erfordert.

Befolgen Sie die folgenden Punkte, um die Wahrscheinlichkeit zu minimieren, dass Ihr Patch Zugriff auf die ursprüngliche Quelle benötigt:

-   Verwenden Sie patches nur für ganze Dateien. Dadurch entfällt die Notwendigkeit, binäre Patches für alle zuvor veröffentlichten Versionen der Datei zu erstellen. Beachten Sie, dass ganze Dateipatches im Allgemeinen größer sind als binäre Patches. Sie können einen Patch problemlos als gesamten Dateipatch festlegen, indem Sie die IncludeWholeFilesOnly-Eigenschaft mit dem Wert 1 (eins) in der PcP-Datei (Patch Creation Properties) erstellen.
-   Stellen Sie sicher, dass keine Ihrer benutzerdefinierten Aktionen auf den ursprünglichen Quellspeicherort zutritt.
-   Stellen Sie sicher, dass die ResolveSource-Aktion bedingt ist, sodass sie nur bei Bedarf ausgeführt wird oder alternativ überhaupt nicht vorhanden ist.
-   Füllen Sie die [MsiFileHash-Tabelle](msifilehash-table.md) für alle Nichtversionsdateien auf. Das Windows Installer SDK,Msifiler.exe, kann dies ganz einfach für Sie tun.
-   Stellen Sie sicher, dass alle Dateien über die richtige Version und die richtigen Sprachinformationen verfügen. Das Windows Installer SDK,Msifiler.exe, kann dies ganz einfach für Sie tun.

## <a name="source-requirements-when-patching"></a>Quellanforderungen beim Patchen

Der Zugriff auf die ursprünglichen Installationsquellen ist möglicherweise erforderlich, um den Patch in den folgenden Fällen anzuwenden:

-   Der Patch gilt für ein Feature, das derzeit aus der Quelle ausgeführt wird. In diesem Fall wird das Feature vom Zustand "Run-from-Source" in den lokalen Zustand übergewechselt.
-   Der Patch gilt für eine Komponente mit einer fehlenden oder beschädigten Datei.
-   Der Patch gilt für eine Datei in einer Komponente, die auch nicht versionierte Dateien ohne MsiFileHash-Einträge enthält. Eine aufgefüllte [MsiFileHash-Tabelle](msifilehash-table.md) ist erforderlich, um unnötiges Erneutes Kopieren von Nichtversionsdateien vom Quellspeicherort zu verhindern.
-   Der Patch wurde mit einem REINSTALLMODE von amus oder emus angewendet. Diese Option ist gefährlich, da sie Unabhängig von der Dateiversion Dateikopiervorgänge ausführt. Dies kann zu einer Verfeinerung von Dateien führen und erfordert fast immer die Quelle. Der empfohlene REINSTALLMODE-Wert ist omus.
-   Das zwischengespeicherte Paket für das Produkt fehlt. Das zwischengespeicherte Paket wird für die Anwendung eines Patches benötigt. Das zwischengespeicherte Paket wird im Ordner %windir% \\ Installer gespeichert.
-   Das Paket wird erstellt, um einen Aufruf der [ResolveSource-Aktion zu erstellen.](resolvesource-action.md) Diese Aktion sollte im Allgemeinen vermieden oder entsprechend bedingt werden, da ihre Ausführung immer zu einem Zugriff auf die Quelle führt.
-   Das Paket verfügt über eine benutzerdefinierte Aktion, die versucht, auf die Quelle in irgendeiner Weise zu zugreifen. Das häufigste Beispiel ist eine benutzerdefinierte Aktion vom Typ 23 für die gleichzeitige Installation.
    > [!Note]  
    > Gleichzeitige Installationen werden nicht für die Installation von Anwendungen empfohlen, die für die Veröffentlichung an die Öffentlichkeit vorgesehen sind. Informationen zu gleichzeitigen Installationen finden Sie unter [Gleichzeitige Installationen.](concurrent-installations.md)

     

-   Das Patchpaket besteht aus binären Patches, die nicht für die aktuelle Version der Datei auf dem Computer gelten.

Betrachten Sie das folgende Beispiel, Windows Installer beim Anwenden eines Patches Zugriff auf die ursprüngliche Quelle benötigt:

1.  Installieren Sie die RTM-Version des Produkts Beispiel.
2.  Wenden Sie patch Qfe1.msp auf den Computer an. Dadurch wird Version 1.0 von Example.dll Version 1.1 gepatcht.
3.  Es wird ein neuer Patch Qfe2.msp bereitgestellt, der Example.dll Version 1.2 aktualisiert und Qfe1.msp veraltet ist. Der Patch wurde jedoch nur für Version 1.0 von Example.dll erstellt, da er mithilfe der RTM-Version des Produkts generiert wurde. Example.dll Version 1.2 enthält die in Example.dll Version 1.1 enthaltene Korrektur, aber die MSP-Datei wurde zwischen den RTM- und QFE2-Images generiert. Wenn Qfe2.msp also auf den Computer angewendet wird, Windows Installer auf die ursprüngliche Quelle zugreifen. Der binäre Patch für Example.dll kann nicht auf Version 1.1 angewendet werden. sie kann nur auf Version 1.0 angewendet werden. Dies führt dazu, dass der Installer Version 1.0 von Example.dll am ursprünglichen Quellspeicherort erneut kopiert, damit der Patch erfolgreich angewendet werden kann.

## <a name="source-requirements-when-removing-a-patch"></a>Quellanforderungen beim Entfernen eines Patches

Der Zugriff auf die ursprünglichen Installationsquellen ist möglicherweise erforderlich, um einen Patch zu entfernen, wenn der Windows Installer keine Baselineinformationen zum Patch gespeichert hat. Ab Windows Installer 3.0 speichert das Installationsprogramm selektiv Baselineinformationen zu Dateien, wenn sie aktualisiert werden. Weitere Informationen zum Baselinecache finden Sie unter [Reduzieren der Patchgröße.](reducing-patch-size.md)

 

 



