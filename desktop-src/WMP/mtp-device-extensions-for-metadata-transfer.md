---
title: MTP-Geräte Erweiterungen für die metadatenübertragung
description: MTP-Geräte Erweiterungen für die metadatenübertragung
ms.assetid: 9cf68373-e84f-4568-a9da-16ddee0fc4e9
keywords:
- Windows Media Player, MTP-Geräte Erweiterungen
- Windows Media Player, Geräte Erweiterungen
- Windows-Media Player, Erweiterungen
- Windows-Media Player, Metadaten
- Windows Media Player, Media Transfer Protocol (MTP)
- Media Transfer Protocol (MTP)
- MTP (Media Transfer Protocol)
- Metadaten, MTP-Geräte Erweiterungen
- Metadaten, Geräte Erweiterungen
- Metadaten, Erweiterungen
- Geräte Erweiterungen, metadatenübertragung
- Erweiterungen, metadatenübertragung
- MTP-Geräte Erweiterungen für die metadatenübertragung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f64ff16fd97f135d7f8c902af823b967079408fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036286"
---
# <a name="mtp-device-extensions-for-metadata-transfer"></a>MTP-Geräte Erweiterungen für die metadatenübertragung

Bei Media Transfer Protocol (MTP) handelt es sich um ein für tragbare Mediengeräte konzipiertes Protokoll. Der Hauptzweck dieses Protokolls besteht darin, ein allgemeines Protokoll zum Austauschen von Daten zwischen einem Computer und einem tragbaren Medien Gerät bereitzustellen. Dies umfasst das empfangen und Senden von Medienobjekten und das Auflisten des Inhalts und der Funktionen des Geräts.

MTP verwendet persistente eindeutige Objekt Bezeichner (puoids), um digitale Medienelemente (und andere Objekte) eindeutig zu identifizieren, die auf einem Gerät gespeichert sind. Beim Austauschen von Informationen zu Änderungen, die auf einem Gerät aufgetreten sind, das MTP unterstützt, verwenden das Gerät und Windows Media Player puoids, um zu ermitteln, welche Objekte geändert wurden.

Die Header Datei "wmpdevices. h", die als Teil des Windows Media Player SDK installiert wird, definiert die Strukturen und Konstanten, die für die Unterstützung von Windows Media Player-Geräte Erweiterungen erforderlich sind.

Damit ein Gerät als unterstützende metadatenübertragung über den Windows Media Player MTP-Geräte Erweiterungs Satz erkannt wird, muss es die folgenden Informationen in das deviceInfo-DataSet einschließen. (Weitere Informationen zu diesem Dataset finden Sie im Abschnitt 4.6.1 der MTP-Spezifikation.)



| Datasetfeld          | Feld Reihenfolge | Datentyp  | Wert                       |
|------------------------|-------------|------------|-----------------------------|
| Vendorextensionid      | 2           | **UINT32** | 0x00000006                  |
| Vendorextensionversion | 3           | **UINT16** | 0x0064 (100)                |
| Vendorextensiondesc    | 4           | **String** | "Microsoft.com/WMPPD: 10,0" |



 

In der folgenden Tabelle finden Sie Details zum MTP-Vorgang für die beschleunigte metadatenübertragung.



| Element                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vorgangs Code        | 0x9201                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Vorgangs Parameter 1 | Die Transaktions-ID, die während der letzten Sitzung vom Gerät bereitgestellt wurde. Dieser Wert ist für die erste Sitzung 0 (null).                                                                                                                                                                                                                                                                                                                                                                                       |
| Vorgangs Parameter 2 | Start Index. Dieser Wert ist beim ersten Aufrufe einer Sitzung immer 0 (null). Bei nachfolgenden Aufrufen innerhalb derselben Synchronisierungs Sitzung erhöht sich dieser Wert um die Summe der Anzahl der geänderten und gelöschten Elemente aus den vorherigen Antwortdaten.                                                                                                                                                                                                                                             |
| Vorgangs Parameter 3 | 0x10000. Diese Konstante, die in wmpdevices. h definiert ist, ist die maximale Anzahl von puoids, die in der Antwort zurückgegeben werden können. Beachten Sie, dass der Wert dieser Konstante in zukünftigen Versionen dieser Header Datei möglicherweise überarbeitet wird.                                                                                                                                                                                                                                                                                     |
| Vorgangs Parameter 4 | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Vorgangs Parameter 5 | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Daten                  | Das Gerät gibt zwei zusammenhängende MTP-Arrays mit puoids zurück. Jedes MTP-Array beginnt mit einem **DWORD** -Wert, der die Anzahl der Elemente im Array angibt, gefolgt vom Array von Elementen. Das erste MTP-Array enthält die Liste der puoids, die hinzugefügt oder geändert wurden. Das zweite MTP-Array enthält die Liste der puoids, die vom tragbaren Gerät gelöscht wurden. Beachten Sie, dass die Summe der puoid-Anzahl in den beiden Arrays den in Vorgangs Parameter 3 übergebenen Wert nicht überschreiten darf.<br/> |
| Daten Richtung        | R->I                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Antwort Code Optionen | **MTP \_ Antwort \_ OK** (0x2001) oder gültiger Fehler Antwort Code.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Antwort Parameter 1  | Die aktuelle Transaktions-ID des Geräts.                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Antwort Parameter 2  | Die Anzahl der puoids, die von zukünftigen Anforderungen abgerufen werden.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Antwort Parameter 3  | **DWORD** , das Statusinformationen enthält. Der Status wird auf bitweise angegeben. Informationen zu den zu verwendenden Flags finden Sie unter "Hinweise".                                                                                                                                                                                                                                                                                                                                                                     |
| Antwort Parameter 4  | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Antwort Parameter 5  | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Bemerkungen

Der Status wird durch den Antwort Parameter 3 in einer bitweisen Weise mithilfe der folgenden Flags angegeben.



| Flag                                             | Wert | BESCHREIBUNG                                                                                                                                                                                                                          |
|--------------------------------------------------|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WMP- \_ MDRT- \_ Flags \_ nicht gemeldete \_ Gelöschte \_ Elemente** | 0x1   | Elemente wurden gelöscht, bevor der erste Objekt Pfadname gemeldet wird. Dies deutet häufig darauf hin, dass das Gerät neu formatiert wurde.                                                                                                           |
| **WMP- \_ MDRT- \_ Flags \_ nicht gemeldete \_ hinzugefügte \_ Elemente**   | 0x2   | Das Gerät enthält einige hinzugefügte Elemente, die in der Liste der puoids nicht zurückgegeben werden können. Beachten Sie, dass dieses Flag mit dem Antwort Parameter 2 nicht redundant ist. Legen Sie dieses Flag nur fest, wenn angeforderte Elemente vorhanden sind, die das Gerät nicht zurückgeben kann. |



 

BITS 2 bis 31 sind für die zukünftige Verwendung reserviert. Diese Bits sollten auf 0 (null) festgelegt werden.

Windows Media Player sendet den MTP-Befehl zu Beginn einer Synchronisierungs Sitzung an ein Gerät, bevor Mediendateien übertragen werden. Das Gerät sollte seine Antwort so schnell wie möglich zurückgeben, um Verzögerungen beim Synchronisierungs Vorgang zu vermeiden.

Windows Media Player fordert Werte für die in aufgeführten Attribute [über die Metadaten](about-the-metadata.md) für jede geänderte pouid an, die in der Antwort zurückgegeben wird. Windows Media Player kann in nachfolgenden Befehlen aktualisierte Werte für diese Attribute an das Gerät senden.

Dateien, die als vom Gerät entfernt wurden, können erneut auf das Gerät kopiert werden, wenn Sie für die Benutzereinstellungen erforderlich sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Geräte Erweiterungen für die beschleunigte metadatenübertragung**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 





