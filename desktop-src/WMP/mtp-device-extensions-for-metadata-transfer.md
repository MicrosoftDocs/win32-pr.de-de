---
title: MTP-Geräteerweiterungen für die Metadatenübertragung
description: MTP-Geräteerweiterungen für die Metadatenübertragung
ms.assetid: 9cf68373-e84f-4568-a9da-16ddee0fc4e9
keywords:
- Windows Media Player,MTP-Geräteerweiterungen
- Windows Media Player,Geräteerweiterungen
- Windows Media Player,Erweiterungen
- Windows Media Player,metadata
- Windows Media Player,Media Transfer Protocol (MTP)
- Medienübertragungsprotokoll (Media Transfer Protocol, MTP)
- MTP (Media Transfer Protocol)
- Metadaten,MTP-Geräteerweiterungen
- Metadaten,Geräteerweiterungen
- Metadaten,Erweiterungen
- Geräteerweiterungen,Metadatenübertragung
- Erweiterungen,Metadatenübertragung
- MTP-Geräteerweiterungen für die Metadatenübertragung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c56f633d7cd4ca44a90d311c1e4c1c2e6d213e1d2ad1a43b802e4795a59a7d47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572440"
---
# <a name="mtp-device-extensions-for-metadata-transfer"></a>MTP-Geräteerweiterungen für die Metadatenübertragung

Media Transfer Protocol (MTP) ist ein Protokoll, das für portable Mediengeräte entwickelt wurde. Der Hauptzweck dieses Protokolls besteht in der Bereitstellung eines gemeinsamen Protokolls für den Datenaustausch zwischen einem Computer und einem portablen Mediengerät. Dies umfasst das Empfangen und Senden von Medienobjekten und das Aufzählen der Inhalte und Funktionen des Geräts.

MTP verwendet persistente eindeutige Objektbezeichner (PUOIDs), um auf einem Gerät gespeicherte digitale Medienelemente (und andere Objekte) eindeutig zu identifizieren. Beim Austausch von Informationen zu Änderungen, die auf einem Gerät aufgetreten sind, das MTP unterstützt, verwenden das Gerät und Windows Media Player PUOIDs, um zu ermitteln, welche Objekte sich geändert haben.

Die Headerdatei mit dem Namen wmpdevices.h, die als Teil des Windows Media Player SDK installiert wird, definiert die Strukturen und Konstanten, die zur Unterstützung Windows Media Player Geräteerweiterungen erforderlich sind.

Damit ein Gerät als unterstützende Metadatenübertragung über den MTP Windows Media Player-Geräteerweiterungssatz erkannt wird, muss es die folgenden Informationen in das DeviceInfo-Dataset enthalten. (Weitere Informationen zu diesem Dataset finden Sie in Abschnitt 4.6.1 der MTP-Spezifikation.)



| Datasetfeld          | Feld reihenfolge | Datentyp  | Wert                       |
|------------------------|-------------|------------|-----------------------------|
| VendorExtensionID      | 2           | **UINT32** | 0x00000006                  |
| VendorExtensionVersion | 3           | **UINT16** | 0x0064 (100)                |
| VendorExtensionDesc    | 4           | **String** | "microsoft.com/WMPPD: 10.0" |



 

Die folgende Tabelle enthält Details zum MTP-Vorgang für die beschleunigte Metadatenübertragung.



| Element                  | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vorgangscode        | 0x9201                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Operation-Parameter 1 | Die Transaktions-ID, die vom Gerät während der vorherigen Sitzung angegeben wurde. Dieser Wert ist 0 (null) für die erste Sitzung.                                                                                                                                                                                                                                                                                                                                                                                       |
| Operation-Parameter 2 | Startindex. Dieser Wert ist beim ersten Aufruf einer Sitzung immer 0 (null). Bei nachfolgenden Aufrufen innerhalb derselben Synchronisierungssitzung erhöht sich dieser Wert um die Summe der Anzahl der geänderten und gelöschten Elemente aus den vorherigen Antwortdaten.                                                                                                                                                                                                                                             |
| Operation-Parameter 3 | 0x10000. Diese Konstante, die in wmpdevices.h definiert ist, ist die maximale Anzahl von PUOIDs, die in der Antwort zurückgegeben werden können. Beachten Sie, dass der Wert dieser Konstante in zukünftigen Releases dieser Headerdatei überarbeitet werden kann.                                                                                                                                                                                                                                                                                     |
| Operation Parameter 4 | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Operation Parameter 5 | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Daten                  | Das Gerät gibt zwei zusammenhängende MTP-Arrays zurück, die PUOIDs enthalten. Jedes MTP-Array beginnt mit einem **DWORD-Wert,** der die Anzahl der Elemente im Array angibt, gefolgt vom Array von Elementen. Das erste MTP-Array enthält die Liste der PUOIDs, die hinzugefügt oder geändert wurden. Das zweite MTP-Array enthält die Liste der PUOIDs, die vom portablen Gerät gelöscht wurden. Beachten Sie, dass die Summe der PUOID-Anzahl in den beiden Arrays den in Operation Parameter 3 übergebenen Wert nicht überschreiten darf.<br/> |
| Datenrichtung        | R->I                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Antwortcodeoptionen | **MTP \_ RESPONSE \_ OK** (0x2001) oder gültiger Fehlerantwortcode.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Antwortparameter 1  | Die aktuelle Transaktions-ID des Geräts.                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Antwortparameter 2  | Die Anzahl der PUOIDs, die von zukünftigen Anforderungen abgerufen werden müssen.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Antwortparameter 3  | **DWORD mit** Statusinformationen. Der Status wird bitweise angegeben. Weitere Informationen zu zu verwendenden Flags finden Sie unter Hinweise.                                                                                                                                                                                                                                                                                                                                                                     |
| Antwortparameter 4  | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Antwortparameter 5  | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Hinweise

Der Status wird bitweise durch den Antwortparameter 3 mithilfe der folgenden Flags angegeben.



| Flag                                             | Wert | Beschreibung                                                                                                                                                                                                                          |
|--------------------------------------------------|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WMP \_ MDRT \_ KENNZEICHNET NICHT \_ GEMELDETE \_ GELÖSCHTE \_ ELEMENTE** | 0x1   | Elemente wurden gelöscht, bevor der erste Objektpfadname gemeldet wurde. Dies deutet häufig darauf hin, dass das Gerät neu formatiert wurde.                                                                                                           |
| **WMP \_ MDRT \_ FLAGS \_ UNREPORTED \_ ADDED \_ ITEMS**   | 0x2   | Das Gerät enthält einige hinzugefügte Elemente, die nicht in der Liste der PUOIDS zurückgegeben werden können. Beachten Sie, dass dieses Flag mit dem Antwortparameter 2 nicht redundant ist. Legen Sie dieses Flag nur fest, wenn angeforderte Elemente vom Gerät nicht zurückgeben werden können. |



 

Bits 2 bis 31 sind für die zukünftige Verwendung reserviert. Diese Bits sollten auf 0 (null) festgelegt werden.

Windows Media Player den MTP-Befehl zu Beginn einer Synchronisierungssitzung an ein Gerät sendet, bevor Mediendateien übertragen werden. Das Gerät sollte so schnell wie möglich seine Antwort zurückgeben, um Verzögerungen beim Synchronisierungsvorgang zu vermeiden.

Windows Media Player fordert Werte für die Attribute an, die unter [About the Metadata (Informationen](about-the-metadata.md) zu den Metadaten) für jede geänderte POUID aufgeführt sind, die in der Antwort zurückgegeben wird. Windows Media Player in nachfolgenden Befehlen aktualisierte Werte für diese Attribute an das Gerät senden.

Dateien, die als vom Gerät entfernt gemeldet wurden, können erneut auf das Gerät kopiert werden, wenn die Einstellungen des Benutzers dies erfordern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Geräteerweiterungen für die beschleunigte Metadatenübertragung**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 





