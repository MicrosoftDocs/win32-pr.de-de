---
title: Neuigkeiten (IMAPI)
description: In der folgenden Tabelle sind die Neuerungen für die einzelnen Releases der Image-Mastering-API aufgeführt.
ms.assetid: a90daec2-5916-4c24-b2ad-94199641a2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77abc9db0c9d976eef632034a5620520bb29d73d
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "103723829"
---
# <a name="whats-new-image-mastering-api"></a>Neuerungen: Bild-Mastering-API

In der folgenden Tabelle sind die Neuerungen für die einzelnen Releases der Image-Mastering-API aufgeführt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Version</th>
<th>Beschreibung der Features</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Version 2.0</td>
<td>Ein Großteil der API wurde umgestaltet. Die meisten Funktionen der Version 1,0 sind weiterhin in Version 2,0 verfügbar. Anwendungen, die Bild-oder Entwicklungsanwendungen schreiben oder eine neue Geräte-und Formatentwicklung durchführen, werden empfohlen, Version 2,0 anstelle von Version 1,0 zu verwenden.<br/> IMAPI 2,0 ist in Windows Vista enthalten. Um die gleiche Funktionalität für Windows XP und Windows Server 2003 zu aktivieren, muss das <a href="https://support.microsoft.com/kb/932716">KB932716</a> -Update Paket installiert werden.<br/> Point-Release Hinweise:<br/>
<ul>
<li>In Windows Vista mit Service Pack 1 (SP1) und Windows Server 2008 wurde ein Update angeboten, das multistartunterstützung über die <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a> -Schnittstelle bietet.<br/></li>
<li>Ein Featureupdate, das die Unterstützung für das BD-R\BD-Re-Format, die unformatierte CD-Disk-at-Once-Image Erstellung sowie die Verbrauchs Überprüfung bietet, ist im <a href="https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05">Windows Feature Pack für den Speicher</a>enthalten. Dieses Feature-Update wird unter Windows Vista mit SP1, Windows XP mit Service Pack 2 (SP2) und höher und Windows Server 2003 mit Service Pack 1 (SP1) und höher unterstützt. Darüber hinaus sind diese Features in Windows 7 und Windows Server 2008 enthalten.<br/></li>
<li>IMAPI 2,0 Features, die in Windows 7 und Windows Server 2008 enthalten sind, enthalten "gapless Burning" für AudioCDs und die Beseitigung von "Double stashing" bei Verbrennungs Vorgängen. Das doppelte stashing ist ein Prozess innerhalb des größeren Brennvorgangs, bei dem jede Datei geblitzt wird, bevor Sie auf der Festplatte gebrannt wird. Mit der neuesten Version von IMAPI 2,0 werden Dateien selektiv für das stashing ausgewählt, sodass die verbleibenden Dateien (größtenteils große Dateien) nicht gestapelt werden. Das Endergebnis ist gespeicherter Speicherplatz und Betriebszeit.<br/></li>
</ul></td>
</tr>
<tr class="even">
<td>Version 1.0</td>
<td>Erste Veröffentlichung Ermöglicht einer Anwendung das Bereitstellen und Brennen eines einfachen Audio-oder Daten Images auf CD-R-und CD-RW-Geräten. Die API unterstützt das Joliet-und ISO 9660-Format für Redbook-Audiodaten und Datenscheiben. Informationen zur Version 1,0 finden Sie <a href="imapiv1.md">unter IMAPIv1-Unterstützung</a>. In Windows XP enthalten.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="version-20"></a>Version 2.0

-   Ermöglicht Anwendungen das Brennen auf die Medienformate DVD-R, DVD + r, DVD-RW, DVD + RW, DVD + DL, DVD-DL und DVD-RAM, BD-r und BD-RE.
-   Ermöglicht das Aufzeichnen auf mehreren Laufwerken gleichzeitig. In Version 1,0 konnte von IMAPI immer nur eine Aufzeichnung auf dem System verwendet werden. Wenn Sie eine Anwendung der Version 1,0 unter Windows Vista ausführen, können andere Anwendungen auf anderen Laufwerken im System gleichzeitig IMAPI 1,0-oder 2,0-Schnittstellen verwenden. Obwohl dies im Allgemeinen als Vorteil angesehen wird, sind für Anwendungen, die auf das einmalige System-Burner-Verhalten basieren, möglicherweise kleinere Updates erforderlich.
-   Der Zugriff auf eine Aufzeichnung wird verweigert, wenn der Recorder Informationen auf die Festplatte schreibt. Andernfalls ist die Aufzeichnung für andere Clients verfügbar.
-   Unterstützt mehr als eine Stash-Datei auf einem Client Computer, während in Version 1,0 nur eine systemweite Stash-Datei zulässig ist.
-   Unter Windows Vista enthält Version 1,0 keine Dienst-oder Kernelmoduskomponenten mehr. Die [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) -Schnittstelle verwendet jedoch weiterhin die Befehle exklusiver Zugriff für den IOCTL \_ -CDROM \_ \_ -und IOCTL- \_ SCSI-Durchlauf, um den \_ \_ \_ Zugriff oder die Kommunikation mit bestimmten Laufwerks Geräten zu verwalten.
-   Unter Windows Vista werden von den Schnittstellen der Version 1,0 nun die Schnittstellen der Version 2,0 aufgerufen.
-   IMAPI erforderliche 2,0 ist in Windows Vista mit SP1 und Windows Server 2008 enthalten und bietet Unterstützung für mehrfach Start über die [**IFileSystemImage2**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2) -Schnittstelle.
-   Ermöglicht die Verwendung von "gapless Burning" für AudioCDs. Wenn Sie weniger stark brennen, kann der akustische Abstand zwischen Audiospuren entfernt werden.
-   "Double stashing" wurde durch einen Prozess ersetzt, bei dem explizit Dateien für das stashing ausgewählt werden und die verbleibenden Dateien (größtenteils große Dateien) nicht geblitzt werden. Das Endergebnis ist gespeicherter Speicherplatz und Betriebszeit.
-   Mit dem [Windows Feature Pack für den Speicher](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05)wurden Optionen für die Überprüfung der Überprüfung über [**iburnverification**](/windows/desktop/api/imapi2/nn-imapi2-iburnverification)verfügbar gemacht.
