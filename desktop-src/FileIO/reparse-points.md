---
description: Beschreibt Analyse Punkte.
ms.assetid: 3abb3a08-9a00-43eb-9792-82eab1a25f06
title: Reparse Points
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21ad17af8993da500154dd88690420a563886f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867480"
---
# <a name="reparse-points"></a>Reparse Points

Eine Datei oder ein Verzeichnis kann einen Analyse *Punkt* enthalten, bei dem es sich um eine Sammlung benutzerdefinierter Daten handelt. Das Format dieser Daten wird von der Anwendung, in der die Daten gespeichert werden, und einem Dateisystem Filter verstanden, den Sie zum Interpretieren der Daten und zum Verarbeiten der Datei installieren. Wenn eine Anwendung einen Analyse Punkt festlegt, speichert Sie diese Daten sowie ein Analyse- *Tag*, mit dem die Daten, die gespeichert werden, eindeutig identifiziert werden. Wenn das Dateisystem eine Datei mit einem Analyse Punkt öffnet, wird versucht, den Dateisystem Filter zu finden, der dem durch das Analyse-Tag identifizierten Datenformat zugeordnet ist. Wenn ein Dateisystem Filter gefunden wird, verarbeitet der Filter die Datei gemäß den Analysedaten. Wenn kein Dateisystem Filter gefunden wird, schlägt der Datei Öffnungsvorgang fehl.

Analyse Punkte werden z. b. verwendet, um NTFS-Dateisystem Verknüpfungen und den Microsoft-Remote Speicher Server (RSS) zu implementieren. RSS verwendet einen vom Administrator definierten Satz von Regeln, um selten verwendete Dateien in langfristige Speicher zu verschieben, z. b. Bänder oder optische Medien. Er verwendet Analyse Punkte, um Informationen über die Datei im Dateisystem zu speichern. Diese Informationen werden in einer Stub-Datei gespeichert, die einen Analyse Punkt enthält, dessen Daten auf das Gerät verweist, auf dem sich die tatsächliche Datei jetzt befindet. Der Dateisystem Filter kann diese Informationen verwenden, um die Datei abzurufen.

Analyse Punkte werden auch verwendet, um bereitgestellte Ordner zu implementieren. Weitere Informationen finden Sie unter [bestimmen, ob ein Verzeichnis ein](determining-whether-a-directory-is-a-volume-mount-point.md)bereitgestellter Ordner ist.

Für Analyse Punkte gelten die folgenden Einschränkungen:

-   Analyse Punkte können für ein Verzeichnis eingerichtet werden, das Verzeichnis muss jedoch leer sein. Andernfalls kann das NTFS-Dateisystem den Analyse Punkt nicht einrichten. Außerdem können Sie Verzeichnisse oder Dateien nicht in einem Verzeichnis erstellen, das einen Analyse Punkt enthält.
-   Analyse Punkte und erweiterte Attribute schließen sich gegenseitig aus. Das NTFS-Dateisystem kann keinen Analyse Punkt erstellen, wenn die Datei Erweiterte Attribute enthält, und es kann keine erweiterten Attribute für eine Datei erstellen, die einen Analyse Punkt enthält.
-   Analyse Punktdaten, einschließlich des Tags und der optionalen **GUID**, dürfen nicht länger als 16 Kilobyte sein. Beim Festlegen eines Analyse Punkts tritt ein Fehler auf, wenn die Menge der Daten, die im Analyse Punkt platziert werden soll, diesen Grenzwert überschreitet.
-   Es gibt ein Limit von 63 Analyse Punkten für einen beliebigen Pfad.

    **Windows Server 2003 und Windows XP:** Es gibt ein Limit von 31 Analyse Punkten für einen beliebigen Pfad.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                   | BESCHREIBUNG                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Analyse Punkt Tags](reparse-point-tags.md)<br/>                                 | Jeder Analyse Punkt verfügt über ein bezeichnertag, sodass Sie effizient zwischen den verschiedenen Arten von Analyse Punkten unterscheiden können, ohne die benutzerdefinierten Daten im Analyse Punkt untersuchen zu müssen.<br/> |
| [Analyse Punkt Vorgänge](reparse-point-operations.md)<br/>                     | Beschreibt die Analyse Punkt Vorgänge, die Sie mithilfe von [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)ausführen können.<br/>                                                                                       |
| [Analyse Punkte und Datei Vorgänge](reparse-points-and-file-operations.md)<br/> | Beschreibt, wie Analyse Punkte das Verhalten von Dateisystemen ermöglichen, die von den meisten Windows-Entwicklern erwartet werden.<br/>                                                                                     |



 

 

