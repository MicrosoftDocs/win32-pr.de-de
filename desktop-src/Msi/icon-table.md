---
description: Diese Tabelle enthält die Symbol Dateien. Jedes Symbol aus der Tabelle wird als Teil der Produktankündigung in eine Datei kopiert, die für angekündigte Verknüpfungen und OLE-Server verwendet werden soll. Siehe OLE-Einschränkungen für Datenströme.
ms.assetid: a59c552a-21c0-4dd4-9146-88a5f9a22962
title: Symboltabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8e8e38575dc6f6e6bda10b2c1047f3940f7559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215701"
---
# <a name="icon-table"></a>Symboltabelle

Diese Tabelle enthält die Symbol Dateien. Jedes Symbol aus der Tabelle wird als Teil der Produktankündigung in eine Datei kopiert, die für angekündigte Verknüpfungen und OLE-Server verwendet werden soll. Siehe [OLE-Einschränkungen für Datenströme](ole-limitations-on-streams.md).

Die Symboltabelle enthält die folgenden Spalten.



| Spalte | Typ                         | Schlüssel | Nullwerte zulässig |
|--------|------------------------------|-----|----------|
| Name   | [Bezeichner](identifier.md) | J   | N        |
| Daten   | [Binär (Binary)](binary.md)         | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen
</dt> <dd>

Der Name der Symbol Datei.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Vorrats
</dt> <dd>

Die Binär Symbol Daten im PE-Format (dll-oder exe-Datei) oder im Symbol Format (. ico).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Tabelle wird beim Ausführen der [publishproduct-Aktion](publishproduct-action.md) bezeichnet.

Die Symbole für Verknüpfungen, Dateinamen Erweiterungen und CLSIDs müssen in Dateien gespeichert werden, die von der Zieldatei selbst getrennt sind. Dies ist erforderlich, da das Installationsprogramm nur die kleinen Symbol Dateien auf den Computer des Benutzers kopieren soll, wenn die Ressource angekündigt wird. Ein Entwickler eines Installationspakets muss daher separate Dateien erstellen, die nur die Symbole enthalten. Diese Symbol Dateien werden dann als Binärdaten in der Symboltabelle gespeichert.

Symbol Dateien, die ausschließlich Dateinamen Erweiterungen oder CLSIDs zugeordnet sind, können eine beliebige Erweiterung haben, z. b. ico. Symbol Dateien, die Verknüpfungen zugeordnet sind, müssen sich jedoch im Binärformat der exe-Datei befinden und müssen so benannt werden, dass Ihre Erweiterung mit der Erweiterung des Ziels übereinstimmt. Die Verknüpfung funktioniert nicht, wenn diese Regel nicht befolgt wird. Wenn eine Verknüpfung z. b. auf eine Ressource mit der Schlüsseldatei Red.Bar zeigen soll, muss die Symbol Datei auch die Erweiterung. Bar aufweisen. Mehrere Symbole können in dieselbe Symbol Datei gefüllt werden, solange alle Zieldateien dieselbe Erweiterung aufweisen.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE50](ice50.md)  
</dl>

 

 



