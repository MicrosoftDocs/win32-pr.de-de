---
title: Neuerungen (IMAPI)
description: In der folgenden Tabelle sind die Neuerungen für jedes Release der Image Mastering-API aufgeführt.
ms.assetid: a90daec2-5916-4c24-b2ad-94199641a2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a3b0ceb966f3f6db6583b86b616608da3bee4f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472176"
---
# <a name="whats-new-image-mastering-api"></a>Neuerungen: Imagemastering-API

In der folgenden Tabelle sind die Neuerungen für jedes Release der Image Mastering-API aufgeführt.




| Version | Beschreibung der Features | 
|---------|-------------------------|
| Version 2.0 | Ein Großteil der API wurde umgestaltet. Die meisten Funktionen der Version 1.0 sind in Version 2.0 weiterhin verfügbar. Personen, die Imagemasteranwendungen schreiben oder die Entwicklung neuer Geräte und Formate durchführen, sollten version 2.0 anstelle von Version 1.0 verwenden.<br /> IMAPI 2.0 ist in Windows Vista enthalten. Um die gleiche Funktionalität für Windows XP und Windows Server 2003 zu aktivieren, muss das Updatepaket <a href="https://support.microsoft.com/kb/932716">KB932716</a> installiert werden.<br /> Point-Release Hinweise:<br /><ul><li>Ein Update, das Multistartunterstützung über die <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2-Schnittstelle</strong></a> bietet, wurde in Windows Vista mit Service Pack 1 (SP1) und Windows Server 2008 eingeführt.<br /></li><li>Ein Featureupdate, das mastering-Unterstützung für das BD-R\BD-RE-Format, die Erstellung von UN-CD-Datenträgern beim Einmaligen Erstellen von Images sowie die Überprüfung des Burnings bietet, wurde im <a href="https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05">Windows Feature Pack für Storage</a>enthalten. Dieses Featureupdate wird unter Windows Vista mit SP1, Windows XP mit Service Pack 2 (SP2) und höher und Windows Server 2003 mit Service Pack 1 (SP1) und höher unterstützt. Darüber hinaus sind diese Features in Windows 7 und Windows Server 2008 enthalten.<br /></li><li>ImAPI 2.0-Features, die für Windows 7 und Windows Server 2008 nativ sind, umfassen "Gapless Elimination" für Audio-CDs und die Beseitigung von "Double Stashing" bei Burn-Vorgängen. Double Stashing ist ein Prozess innerhalb des größeren Burn-Vorgangs, bei dem jede Datei stasht wird, bevor sie auf den Datenträger geworfen wird. Mit der aktuellen Version von IMAPI 2.0 werden Dateien selektiv für das Stashing ausgewählt, sodass die verbleibenden Dateien (größtenteils große Dateien) nicht stasht werden. Das Endergebnis ist gespeicherter Speicherplatz und die Betriebszeit.<br /></li></ul> | 
| Version 1.0 | Erste Veröffentlichung Ermöglicht es einer Anwendung, ein einfaches Audio- oder Datenbild auf CD-R- und CD-RW-Geräten zu verarbeiten und zu verwerten. Die API unterstützt das Joliet- und ISO 9660-Format für Redbook-Audio- und Datendatenträger. Informationen zu Version 1.0 finden Sie unter <a href="imapiv1.md">IMAPIv1-Unterstützung.</a> In Windows XP enthalten.<br /> | 




 

## <a name="version-20"></a>Version 2.0

-   Ermöglicht Es Anwendungen, die Medienformate DVD-R, DVD+R, DVD-RW, DVD+RW, DVD+DL, DVD-DL und DVD-RAM, BD-R und BD-RE zu speichern.
-   Ermöglicht die Gleichzeitige Aufzeichnung auf mehreren Laufwerken. In Version 1.0 konnte nur ein Aufzeichnungsgerät auf dem System gleichzeitig von DER IMAPI verwendet werden. Wenn Sie eine Anwendung der Version 1.0 auf Windows Vista ausführen, können andere Anwendungen gleichzeitig IMAPI 1.0- oder 2.0-Schnittstellen auf anderen Laufwerken im System verwenden. Obwohl dies im Allgemeinen als Vorteil angesehen wird, erfordern Anwendungen, die auf dem Verhalten des einzelnen System-Burners basierten, möglicherweise kleinere Updates.
-   Der Zugriff auf eine Aufzeichnung wird verweigert, wenn der Aufzeichnungsaufzeichnung Informationen auf den Datenträger schreibt. Andernfalls ist die Aufzeichnung für andere Clients verfügbar.
-   Unterstützt mehr als eine Stashdatei auf einem Clientcomputer, während Version 1.0 nur eine systemweite Stashdatei zulässt.
-   Auf Windows Vista enthält Version 1.0 keine Dienst- oder Kernelmoduskomponenten mehr. Die [**IDiscRecorder2-Schnittstelle**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) verwendet jedoch weiterhin die Befehle IOCTL \_ C EXCLUSIVE ACCESS und \_ \_ IOCTL \_ SCSI PASS THROUGH DIRECT, um den Zugriff oder die Kommunikation mit \_ \_ \_ bestimmten Laufwerksgeräten zu verwalten.
-   Auf Windows Vista rufen die Schnittstellen der Version 1.0 jetzt die Schnittstellen der Version 2.0 auf.
-   In Windows Vista mit SP1 und Windows Server 2008 enthalten, bietet IMAPI vesion 2.0 Multiboot-Unterstützung über die [**IFileSystemImage2-Schnittstelle.**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2)
-   Ermöglicht die Verwendung von "Gapless Ausnutzung" für Audio-CDs. Mit Gapless Dose kann die akustische Lücke zwischen Audiospuren entfernt werden.
-   "Double Stashing" wurde durch einen Prozess ersetzt, bei dem dateien speziell für das Stashing ausgewählt werden und die verbleibenden Dateien (größtenteils große Dateien) nicht stasht werden. Das Endergebnis ist gespeicherter Speicherplatz und die Betriebszeit.
-   Mit dem [Windows Feature Pack für Storage](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05)wurden die Optionen für die Burn-Überprüfung mit einer Eigenschaft verfügbar gemacht, auf die über [**IFeatureVerification**](/windows/desktop/api/imapi2/nn-imapi2-iburnverification)zugegriffen wird.
