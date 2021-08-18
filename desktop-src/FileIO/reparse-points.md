---
description: Beschreibt die Wiederholungspunkte.
ms.assetid: 3abb3a08-9a00-43eb-9792-82eab1a25f06
title: Reparse Points
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d129036f954533134656afd02591eba68e3ecd9498de5aceea4b33fd750e786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015158"
---
# <a name="reparse-points"></a>Reparse Points

Eine Datei oder ein Verzeichnis kann einen *Auswertungspunkt* enthalten, bei dem es sich um eine Sammlung benutzerdefinierter Daten handelt. Das Format dieser Daten wird von der Anwendung verstanden, die die Daten speichert, und einem Dateisystemfilter, den Sie installieren, um die Daten zu interpretieren und die Datei zu verarbeiten. Wenn eine Anwendung einen Analysepunkt festlegt, werden diese Daten sowie ein *Analysetag* gespeichert, das die gespeicherten Daten eindeutig identifiziert. Wenn das Dateisystem eine Datei mit einem Auswertungspunkt öffnet, wird versucht, den Dateisystemfilter zu finden, der dem vom Wiederholungstag identifizierten Datenformat zugeordnet ist. Wenn ein Dateisystemfilter gefunden wird, verarbeitet der Filter die Datei gemäß den Anweisungen der Auswertungsdaten. Wenn kein Dateisystemfilter gefunden wird, schlägt der Vorgang zum Öffnen der Datei fehl.

Beispiel: Mithilfe von Wiederholungspunkten werden NTFS-Dateisystemlinks und der Microsoft Remote Storage Server (RSS) implementiert. RSS verwendet einen vom Administrator definierten Regelsatz, um selten verwendete Dateien in die langfristige Speicherung zu verschieben, z. B. Band oder optische Medien. Sie verwendet Dies sind die Informationen, die sie enthält. Diese Informationen werden in einer Stubdatei gespeichert, die einen Auswertungspunkt enthält, dessen Daten auf das Gerät zeigen, auf dem sich die eigentliche Datei jetzt befindet. Der Dateisystemfilter kann diese Informationen verwenden, um die Datei abzurufen.

Reparse Points werden auch verwendet, um bereitgestellte Ordner zu implementieren. Weitere Informationen finden Sie unter [Bestimmen, ob ein Verzeichnis ein eingebundener Ordner ist.](determining-whether-a-directory-is-a-volume-mount-point.md)

Die folgenden Einschränkungen gelten für Dies gilt für die Folgenden:

-   Für ein Verzeichnis können Wiederholungspunkte eingerichtet werden, aber das Verzeichnis muss leer sein. Andernfalls kann das NTFS-Dateisystem den Wiederholungspunkt nicht einrichten. Darüber hinaus können Sie keine Verzeichnisse oder Dateien in einem Verzeichnis erstellen, das einen Replikationspunkt enthält.
-   Die Wiederholungspunkte und erweiterten Attribute schließen sich gegenseitig aus. Das NTFS-Dateisystem kann keinen Wiederholungspunkt erstellen, wenn die Datei erweiterte Attribute enthält, und es können keine erweiterten Attribute für eine Datei erstellt werden, die einen Wiederholungspunkt enthält.
-   Die Daten des Auswertungspunkts, einschließlich tag und **optionaler GUID,** dürfen 16 Kilobyte nicht überschreiten. Beim Festlegen eines Auswertungspunkts tritt ein Fehler auf, wenn die Menge der Daten, die auf dem Auswertungspunkt platziert werden sollen, diesen Grenzwert überschreitet.
-   Für einen bestimmten Pfad gilt ein Grenzwert von 63 Wiederholungspunkten.

    **Windows Server 2003 und Windows XP:** Für einen bestimmten Pfad gilt ein Grenzwert von 31 Wiederholungspunkten.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                   | BESCHREIBUNG                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Punkttags für die Wiederholung](reparse-point-tags.md)<br/>                                 | Jeder Auswertungspunkt verfügt über ein Bezeichnertag, sodass Sie effizient zwischen den verschiedenen Typen von Überprüfungspunkten unterscheiden können, ohne die benutzerdefinierten Daten im Auswertungspunkt untersuchen zu müssen.<br/> |
| [Reparse Point Operations](reparse-point-operations.md)<br/>                     | Beschreibt die Rearse Point-Vorgänge, die Sie mit [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)ausführen können.<br/>                                                                                       |
| [Reparse Points and File Operations](reparse-points-and-file-operations.md)<br/> | Beschreibt, wie die Wiederholungspunkte das Dateisystemverhalten ermöglichen, das von den meisten Windows Entwicklern abweicht.<br/>                                                                                     |



 

 

