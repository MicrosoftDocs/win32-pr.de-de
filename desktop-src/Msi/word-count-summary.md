---
description: In den Zusammenfassungs Informationen eines-Installationspakets gibt die Eigenschaft für die Wort Zähl Zusammenfassung den Typ des Quelldatei Images an.
ms.assetid: 1eeece25-4f24-4efe-879d-66ebbb6a9391
title: Zusammenfassende Eigenschaft der Wort Zählung
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c4200cb946f6948770d0c900c2df651b8fbff11
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368450"
---
# <a name="word-count-summary-property"></a>Zusammenfassende Eigenschaft der Wort Zählung

In den Zusammenfassungs Informationen eines-Installationspakets gibt die Eigenschaft für die **Wort Zähl Zusammenfassung** den Typ des Quelldatei Images an. Wenn diese Eigenschaft nicht vorhanden ist, wird standardmäßig NULL (0) verwendet.

Diese Eigenschaft ist ein Bitfeld. In Zukunft können neue Bits hinzugefügt werden. Derzeit sind die folgenden Bits verfügbar.



| bit   | Wert          | BESCHREIBUNG                                                                                                                                                                                                                                      |
|-------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bit 0 | 0 1<br/> | Lange Dateinamen. Kurze Dateinamen.<br/>                                                                                                                                                                                                    |
| Bit 1 | 0 2<br/> | Die Quelle ist nicht komprimiert. Die Quelle ist komprimiert.<br/>                                                                                                                                                                                         |
| Bit 2 | 0 4<br/> | Quelle ist ursprüngliches Medium. Die Quelle ist ein administratives Image, das durch eine administrative Installation erstellt wurde.<br/>                                                                                                                                 |
| Bit 3 | 0 8<br/> | Zum Installieren dieses Pakets sind erhöhte Rechte erforderlich. Erweiterte Berechtigungen sind nicht erforderlich, um dieses Paket zu installieren.<br/> Verfügbar ab Windows Installer Version 4,0 und Windows Vista oder Windows Server 2008.<br/> |



 

Diese werden kombiniert, um der **Wort count Summary** -Eigenschaft einen der folgenden Werte zuzuweisen, die auf einen Typ von Quelldatei Image hinweisen.



| Wert | type                                                                                                                                                                                                                                                                                            |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Ursprüngliche Quelle mit langen Dateinamen. Entspricht der Struktur in der [Verzeichnis Tabelle](directory-table.md). Zum Installieren dieses Pakets sind erhöhte Rechte erforderlich.                                                                                                                                     |
| 1     | Ursprüngliche Quelle mit kurzen Dateinamen. Entspricht der Struktur in der [Verzeichnis Tabelle](directory-table.md). Zum Installieren dieses Pakets sind erhöhte Rechte erforderlich.                                                                                                                                    |
| 2     | Komprimierte Quelldateien mit langen Dateinamen. Vergleicht Schränke und Dateien in der [Medien Tabelle](media-table.md). Zum Installieren dieses Pakets sind erhöhte Rechte erforderlich.                                                                                                                   |
| 3     | Komprimierte Quelldateien mit kurzen Dateinamen. Vergleicht Schränke und Dateien in der [Medien Tabelle](media-table.md). Zum Installieren dieses Pakets sind erhöhte Rechte erforderlich.                                                                                                                  |
| 4     | Administratives Image mit langen Dateinamen. Entspricht der Struktur in der [Verzeichnis Tabelle](directory-table.md). Zum Installieren dieses Pakets sind erhöhte Rechte erforderlich.                                                                                                                                |
| 5     | Administratives Image mit kurzen Dateinamen. Entspricht der Struktur in der [Verzeichnis Tabelle](directory-table.md). Zum Installieren dieses Pakets sind erhöhte Rechte erforderlich.                                                                                                                               |
| 8     | Erweiterte Berechtigungen sind nicht erforderlich, um dieses Paket zu installieren. Verwenden Sie diesen Wert, wenn Sie [Pakete ohne das UAC-Dialog Feld erstellen](authoring-packages-without-the-uac-dialog-box.md). Verfügbar ab Windows Installer Version 4,0 und Windows Vista oder Windows Server 2008.<br/> |



 

Beachten Sie, dass die Windows Installer nur Dateien installiert, die sich im Stammverzeichnis der Quelle befinden, wenn das Paket als komprimiert gekennzeichnet ist (Bit 1 ist festgelegt). In diesem Fall müssen sich sogar Dateien, die in der [Dateitabelle](file-table.md) als nicht komprimiert gekennzeichnet sind, im zu installierenden Stammverzeichnis befinden. Zum Angeben eines Quell Bilds, das sowohl eine CAB-Datei (komprimierte Dateien) als auch unkomprimierte Dateien enthält, die der Struktur in der [Verzeichnis Tabelle](directory-table.md)entsprechen, markieren Sie das Paket als nicht komprimiert, indem Sie in der Eigenschaft für die **Wort Zähl Zusammenfassung die Angabe** von Bit 1 aufheben (Wert = 0) und in der Spalte Attribute der [Dateitabelle](file-table.md) für jede Datei in der CAB-Datei " **msidbfileattributescompressed** (Value = 16384)" festlegen.

In einer Transformation sollte die **Wort Zähl Zusammenfassungs** Eigenschaft NULL sein.

Im Zusammenfassungs Informationsdaten Strom eines Patchpakets gibt die Eigenschaft für die **Wort Anzahl Zusammenfassung** den minimalen Windows Installer Version an, die zum Installieren des Patches erforderlich ist.



| Wert | Bedeutung                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Der Standardwert, der angibt, dass mspatch zum Erstellen des Patches verwendet wurde.                                                                                                        |
| 2     | Erfordert mindestens Windows Installer 1,2, damit der Patch angewendet werden muss. Ein Patch mit der Wort Anzahl "2" schlägt sofort fehl, wenn er mit einer Windows Installer Version vor 1,2 verwendet wird. |
| 3     | Erfordert mindestens Windows Installer 2,0, damit der Patch angewendet werden muss. Ein Patch mit der Wort Zählung "3" schlägt sofort fehl, wenn er mit einer Windows Installer Version vor 2,0 verwendet wird. |
| 4     | Erfordert mindestens Windows Installer 3,0, damit der Patch angewendet werden muss. Ein Patch mit der Wort Anzahl "4" schlägt fehl, wenn er mit einer Windows Installer Version vor 3,0 verwendet wird.             |
| 5     | Erfordert mindestens Windows Installer 3,1, damit der Patch angewendet werden muss.                                                                                                               |



 

Diese Zusammenfassungs Eigenschaft ist erforderlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Beschreibungen der Zusammenfassungs Eigenschaften](summary-property-descriptions.md)
</dt> </dl>

 

 




