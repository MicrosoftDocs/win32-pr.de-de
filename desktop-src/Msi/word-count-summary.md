---
description: In den Zusammenfassungsinformationen eines Installationspakets gibt die Eigenschaft Zusammenfassung der Wortanzahl den Typ des Quelldateiimages an.
ms.assetid: 1eeece25-4f24-4efe-879d-66ebbb6a9391
title: Zusammenfassungseigenschaft der Wortanzahl
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0eb167c50db0894ea658bb93b97bfb9f49362d32cca8976a2ea3ec590b716450
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145233"
---
# <a name="word-count-summary-property"></a>Zusammenfassungseigenschaft der Wortanzahl

In den Zusammenfassungsinformationen eines Installationspakets gibt die Eigenschaft Zusammenfassung der **Wortanzahl** den Typ des Quelldateiimages an. Wenn diese Eigenschaft nicht vorhanden ist, wird standardmäßig 0 (null) verwendet.

Diese Eigenschaft ist ein Bitfeld. Neue Bits können in Zukunft hinzugefügt werden. Derzeit sind die folgenden Bits verfügbar.



| bit   | Wert          | Beschreibung                                                                                                                                                                                                                                      |
|-------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bit 0 | 0 1<br/> | Lange Dateinamen. Kurze Dateinamen.<br/>                                                                                                                                                                                                    |
| Bit 1 | 0 2<br/> | Die Quelle ist unkomprimiert. Die Quelle ist komprimiert.<br/>                                                                                                                                                                                         |
| Bit 2 | 0 4<br/> | Die Quelle ist das originale Medium. Die Quelle ist ein administratives Image, das von einer Administratorinstallation erstellt wurde.<br/>                                                                                                                                 |
| Bit 3 | 0 8<br/> | Zum Installieren dieses Pakets können erhöhte Rechte erforderlich sein. Für die Installation dieses Pakets sind keine erhöhten Rechte erforderlich.<br/> Verfügbar ab Windows Installer Version 4.0 und Windows Vista oder Windows Server 2008.<br/> |



 

Diese werden kombiniert, um der Eigenschaft Zusammenfassung der **Wortanzahl** einen der folgenden Werte zu geben, die einen Typ des Quelldateibilds angeben.



| Wert | type                                                                                                                                                                                                                                                                                            |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Ursprüngliche Quelle mit langen Dateinamen. Entspricht der Struktur in [der Verzeichnistabelle](directory-table.md). Zum Installieren dieses Pakets können erhöhte Rechte erforderlich sein.                                                                                                                                     |
| 1     | Ursprüngliche Quelle mit kurzen Dateinamen. Entspricht der Struktur in [der Verzeichnistabelle](directory-table.md). Zum Installieren dieses Pakets können erhöhte Rechte erforderlich sein.                                                                                                                                    |
| 2     | Komprimierte Quelldateien mit langen Dateinamen. Entspricht Schränken und Dateien in der [Medientabelle](media-table.md). Zum Installieren dieses Pakets können erhöhte Rechte erforderlich sein.                                                                                                                   |
| 3     | Komprimierte Quelldateien mit kurzen Dateinamen. Entspricht Schränken und Dateien in der [Medientabelle](media-table.md). Zum Installieren dieses Pakets können erhöhte Rechte erforderlich sein.                                                                                                                  |
| 4     | Administratives Image mit langen Dateinamen. Entspricht der Struktur in [der Verzeichnistabelle](directory-table.md). Zum Installieren dieses Pakets können erhöhte Rechte erforderlich sein.                                                                                                                                |
| 5     | Administratives Image mit kurzen Dateinamen. Entspricht der Struktur in [der Verzeichnistabelle](directory-table.md). Zum Installieren dieses Pakets können erhöhte Rechte erforderlich sein.                                                                                                                               |
| 8     | Für die Installation dieses Pakets sind keine erhöhten Rechte erforderlich. Verwenden Sie diesen Wert, [wenn Sie Pakete ohne das UAC-Dialogfeld erstellen.](authoring-packages-without-the-uac-dialog-box.md) Verfügbar ab Windows Installer Version 4.0 und Windows Vista oder Windows Server 2008.<br/> |



 

Beachten Sie, dass der Windows Installer nur Dateien installiert, die sich im Stammverzeichnis der Quelle befinden, wenn das Paket als komprimiert markiert ist (Bit 1 ist festgelegt). In diesem Fall müssen sich sogar Dateien, [](file-table.md) die in der Dateitabelle als unkomprimiert markiert sind, im Stammverzeichnis befinden, um installiert zu werden. Wenn Sie ein Quellbild angeben möchten, das sowohl über eine Cabinet-Datei (komprimierte Dateien) als auch über nicht komprimierte Dateien verfügt, die mit der  Struktur in der [Verzeichnistabelle](directory-table.md)übereinstimmen, markieren Sie das Paket als unkomprimiert, indem Sie Bit 1 unet (value=0) in der Eigenschaft Zusammenfassung der Wortanzahl belässt und **msidbFileAttributesCompressed** (value=16384) in der Spalte Attribute der [Dateitabelle](file-table.md) für jede Datei im Speicher festlegen.

In einer Transformation sollte die **Eigenschaft Zusammenfassung der Wortanzahl** NULL sein.

Im Zusammenfassungsinformationsstream eines Patchpakets gibt die **Eigenschaft** Zusammenfassung der Wortanzahl die Mindestversion Windows Installer an, die zum Installieren des Patches erforderlich ist.



| Wert | Bedeutung                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Der Standardwert, der angibt, dass MSPATCH zum Erstellen des Patches verwendet wurde.                                                                                                        |
| 2     | Erfordert mindestens Windows Installer 1.2, damit der Patch angewendet wird. Ein Patch mit der Wortanzahl "2" schlägt sofort fehl, wenn er mit einer Windows Installer-Version vor 1.2 verwendet wird. |
| 3     | Erfordert mindestens Windows Installer 2.0, damit der Patch angewendet wird. Ein Patch mit der Wortanzahl "3" schlägt sofort fehl, wenn er mit einer Windows Installer-Version vor 2.0 verwendet wird. |
| 4     | Erfordert mindestens Windows Installer 3.0, damit der Patch angewendet wird. Ein Patch mit der Wortanzahl "4" schlägt fehl, wenn er mit einer Windows Installer-Version vor 3.0 verwendet wird.             |
| 5     | Erfordert mindestens Windows Installer 3.1, damit der Patch angewendet wird.                                                                                                               |



 

Diese Zusammenfassungseigenschaft ist ERFORDERLICH.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Zusammenfassungseigenschaftsbeschreibungen](summary-property-descriptions.md)
</dt> </dl>

 

 




