---
description: Es ist nicht möglich, alle Umstände auszuschließen, unter denen die Anwendung eines Patches möglicherweise Zugriff auf die ursprüngliche Installationsquelle erfordert.
ms.assetid: f7028c55-e4a5-4596-af7a-728c9f4f367e
title: Verhindern, dass ein Patch Zugriff auf die ursprüngliche Installationsquelle erfordert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baee8b261ff0a3f6bb94fb141ee765726ffa2ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864387"
---
# <a name="preventing-a-patch-from-requiring-access-to-the-original-installation-source"></a>Verhindern, dass ein Patch Zugriff auf die ursprüngliche Installationsquelle erfordert

Es ist nicht möglich, alle Umstände auszuschließen, unter denen die Anwendung eines Patches möglicherweise Zugriff auf die ursprüngliche Installationsquelle erfordert.

Beachten Sie die folgenden Punkte, um die Möglichkeit zu minimieren, dass Ihr Patch Zugriff auf die ursprüngliche Quelle benötigt:

-   Verwenden Sie nur Dateien mit ganzer Datei. Dadurch entfällt die Notwendigkeit, binäre Patches für alle zuvor veröffentlichten Versionen der Datei zu erstellen. Beachten Sie, dass die Größe ganzer dateipatches in der Regel größer ist als binäre Patches. Sie können problemlos einen Patch als vollständigen dateipatch festlegen, indem Sie die includewholefilesonly-Eigenschaft mit dem Wert 1 (eins) in der Datei mit den patcherstellungs Eigenschaften (PCP) erstellen.
-   Stellen Sie sicher, dass keine Ihrer benutzerdefinierten Aktionen auf den ursprünglichen Quell Speicherort zugreifen.
-   Stellen Sie sicher, dass die ResolveSource-Aktion conditionalisiert ist, damit Sie nur bei Bedarf ausgeführt werden kann, oder alternativ nicht vorhanden ist.
-   Füllen Sie die [Tabelle "msiflehash](msifilehash-table.md) " für alle Dateien mit Versions Angabe auf. Das Windows Installer SDK-Tool, Msifiler.exe, kann dies problemlos für Sie erledigen.
-   Stellen Sie sicher, dass alle Dateien über die richtige Versions-und Sprachinformationen verfügen. Das Windows Installer SDK-Tool, Msifiler.exe, kann dies problemlos für Sie erledigen.

## <a name="source-requirements-when-patching"></a>Quell Anforderungen beim Patchen

Der Zugriff auf die ursprünglichen Installations Quellen ist möglicherweise erforderlich, um den Patch in den folgenden Fällen anzuwenden:

-   Der Patch gilt für ein Feature, das zurzeit von der Quelle ausgeführt wird. In diesem Fall wird die Funktion vom Quell Zustand in den lokalen Zustand umgestellt.
-   Der Patch gilt für eine Komponente, die über eine fehlende oder beschädigte Datei verfügt.
-   Der Patch gilt für eine Datei in einer Komponente, die auch Dateien ohne Versions Angabe ohne msiflehash-Einträge enthält. Eine aufgefüllte [msiflehash-Tabelle](msifilehash-table.md) ist erforderlich, um unnötige neueinfassungen von Dateien ohne Versions Angabe vom Quell Speicherort zu verhindern.
-   Der Patch wurde mit dem REINSTALLMODE von amus oder Emus angewendet. Diese Option ist gefährlich, da Sie Datei Kopiervorgänge unabhängig von der Dateiversion ausführt. Dies kann dazu führen, dass Dateien herabgesetzt werden und fast immer die Quelle erforderlich ist. Der empfohlene REINSTALLMODE-Wert ist omus.
-   Das zwischengespeicherte Paket für das Produkt fehlt. Das zwischengespeicherte Paket ist für die Anwendung eines Patches erforderlich. Das zwischengespeicherte Paket wird im Ordner% windir% \\ Installer gespeichert.
-   Das Paket wird erstellt, um die [ResolveSource-Aktion](resolvesource-action.md)aufzurufen. Diese Aktion sollte in der Regel nicht ordnungsgemäß vermieden oder conditionalisiert werden, da ihre Ausführung immer zu einem Zugriff auf die Quelle führt.
-   Das Paket verfügt über eine benutzerdefinierte Aktion, die versucht, auf eine bestimmte Weise auf die Quelle zuzugreifen. Das häufigste Beispiel ist eine benutzerdefinierte Aktion vom Typ 23 zur gleichzeitigen Installation.
    > [!Note]  
    > Parallele Installationen werden nicht für die Installation von Anwendungen empfohlen, die für die öffentliche Veröffentlichung vorgesehen sind. Weitere Informationen zu gleichzeitigen Installationen finden Sie unter [parallele Installationen](concurrent-installations.md).

     

-   Das Patchpaket besteht aus binären Patches, die nicht für die aktuelle Version der Datei auf dem Computer gelten.

Sehen Sie sich das folgende Beispiel an, in dem Windows Installer beim Anwenden eines Patches Zugriff auf die ursprüngliche Quelle benötigt:

1.  Installieren Sie die RTM-Version des Produkt Beispiels.
2.  Wenden Sie Patch Qfe1. msp auf den Computer an. Dadurch wird Version 1,0 von Example.dll auf Version 1,1 Patches.
3.  Ein neuer Patch, Qfe2. msp, wird bereitgestellt, mit dem Example.dll auf Version 1,2 und Obsoletes Qfe1. msp aktualisiert wird. Der Patch wurde jedoch nur für die Zielversion 1,0 von Example.dll erstellt, da er mit der RTM-Version des Produkts generiert wurde. Example.dll Version 1,2 enthält die in Example.dll Version 1,1 enthaltene Korrektur, aber die MSP-Datei wurde zwischen den RTM-und QFE2-Images generiert. Wenn Qfe2. msp auf den Computer angewendet wird, muss Windows Installer auf die ursprüngliche Quelle zugreifen. Der binäre Patch für Example.dll kann nicht auf Version 1,1, Sie kann nur auf Version 1,0 angewendet werden. Dies führt dazu, dass das Installationsprogramm Version 1,0 von Example.dll vom ursprünglichen Quell Speicherort neu verwendet, damit der Patch erfolgreich angewendet werden kann.

## <a name="source-requirements-when-removing-a-patch"></a>Quell Anforderungen beim Entfernen eines Patches

Der Zugriff auf die ursprünglichen Installations Quellen ist möglicherweise erforderlich, um einen Patch zu entfernen, wenn der Windows Installer keine grundlegenden Informationen zum Patch gespeichert hat. Ab Windows Installer 3,0 speichert das Installationsprogramm selektiv grundlegende Informationen zu Dateien, wenn diese aktualisiert werden. Weitere Informationen zum Baseline-Cache finden Sie unter [verringern der Patchgröße](reducing-patch-size.md) .

 

 



