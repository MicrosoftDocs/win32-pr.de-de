---
title: Geräteerweiterungen für die Berichterstellung für erworbene Inhalte
description: Geräteerweiterungen für die Berichterstellung für erworbene Inhalte
ms.assetid: 597d872e-9105-4edb-afa3-9f4407de0f73
keywords:
- Windows Media Player,Geräteerweiterungen
- Windows Media Player,Erweiterungen
- Windows Media Player, Melden von erworbenen Inhalten
- Geräteerweiterungen, Melden von erworbenen Inhalten
- Erweiterungen,Melden von erworbenen Inhalten
- Melden von erworbenen Inhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3389f5b35cedc853d66e6f450836195497628972ea6ae15642d75155d8b83b6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902060"
---
# <a name="device-extensions-for-reporting-acquired-content"></a>Geräteerweiterungen für die Berichterstellung für erworbene Inhalte

Windows Media Player 11 führt neue Funktionen ein, die es portablen Geräten ermöglichen, den Player über Inhalte zu informieren, die dem Gerät seit der letzten Synchronisierung hinzugefügt wurden. Windows Media Player 11 können diese Informationen verwenden, um neu erworbene Inhalte vom Gerät auf den Computer des Benutzers zu kopieren. Gerätehersteller sollten die folgenden Anforderungen für die Unterstützung dieser Funktionalität beachten:

-   Dieses Feature wird nur für MTP-fähige Geräte unterstützt.
-   Dieses Feature funktioniert nur mit Geräten, die eine Partnerschaft mit Windows Media Player haben.
-   Geräte dürfen nur Inhalte melden, die vom Gerät erstellt oder heruntergeladen wurden. Dies schließt Fotos ein, die vom Gerät aufgenommen wurden. Sprachaufzeichnungen, die vom Gerät erstellt wurden; Voicemailaufzeichnungen; downloads from a storage card; (Downloads von einer Kreditkarte; und werden aus dem Internet heruntergeladen. Inhalte, die aufgrund der Synchronisierung mit einem anderen Gerät oder einer anderen Partnerschaft auf dem Gerät gespeichert wurden, dürfen nicht gemeldet werden.

Die Headerdatei mit dem Namen wmpdevices.h, die als Teil des Windows Media Player SDK installiert wird, definiert die Strukturen und Konstanten, die zur Unterstützung Windows Media Player Geräteerweiterungen erforderlich sind.

Damit ein Gerät die Berichterstellung von erworbenen Inhalten über den Windows Media Player MTP-Geräteerweiterungssatz unterstützt, muss es die folgenden Informationen im DeviceInfo-Dataset enthalten. (Weitere Informationen zu diesem Dataset finden Sie in Abschnitt 4.6.1 der MTP-Spezifikation.)



| Datasetfeld          | Feldreihenfolge | Datentyp  | Wert                       |
|------------------------|-------------|------------|-----------------------------|
| VendorExtensionID      | 2           | **UINT32** | 0x00000006                  |
| VendorExtensionVersion | 3           | **UINT16** | 0x0064 (100)                |
| VendorExtensionDesc    | 4           | **String** | "microsoft.com/WMPPD: 11.0" |



 

Die folgende Tabelle enthält Details zum MTP-Vorgang zum Melden von erworbenen Inhalten.



| Element                  | BESCHREIBUNG                                                                                                                                                                                                                     |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vorgangscode        | 0x9202                                                                                                                                                                                                                          |
| Vorgangsparameter 1 | Die Transaktions-ID, die vom Gerät während der vorherigen Sitzung angegeben wurde. Dieser Wert ist 0 (null) für die erste Sitzung.                                                                                                                |
| Vorgangsparameter 2 | Startindex. Dieser Wert ist beim ersten Aufruf einer Sitzung immer 0 (null). Bei nachfolgenden Aufrufen innerhalb derselben Synchronisierungssitzung erhöht sich dieser Wert um die Anzahl der Elemente, die aus den vorherigen Antwortdaten zurückgegeben wurden. |
| Vorgangsparameter 3 | 0x10000. Diese Konstante, die in wmpdevices.h definiert ist, ist die maximale Anzahl von PUOIDs, die in der Antwort zurückgegeben werden können. Beachten Sie, dass der Wert dieser Konstante möglicherweise in zukünftigen Versionen dieser Headerdatei überarbeitet wird.              |
| Vorgangsparameter 4 | 0                                                                                                                                                                                                                               |
| Vorgangsparameter 5 | 0                                                                                                                                                                                                                               |
| Daten                  | Das Gerät gibt ein MTP-Array zurück, das die erworbenen PUOIDs enthält. Das Array beginnt mit einem **DWORD-Wert,** der die Anzahl der Elemente im Array angibt, gefolgt vom Array der Elemente.                               |
| Datenrichtung        | R->I                                                                                                                                                                                                                         |
| Antwortcodeoptionen | **MTP \_ ANTWORT \_ OK** (0x2001) oder gültiger Fehlerantwortcode.                                                                                                                                                                    |
| Antwortparameter 1  | Die aktuelle Transaktions-ID.                                                                                                                                                                                                     |
| Antwortparameter 2  | Die Anzahl der PUOIDs, die von zukünftigen Anforderungen abgerufen werden müssen.                                                                                                                                                            |
| Antwortparameter 3  | **DWORD** mit Statusinformationen. Der Status wird bitweise angegeben. Informationen zu zu verwendenden Flags finden Sie unter Hinweise.                                                                                              |
| Antwortparameter 4  | 0                                                                                                                                                                                                                               |
| Antwortparameter 5  | 0                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Hinweise

Der Status wird durch den Antwortparameter 3 bitweise mithilfe des folgenden Flags angegeben.



| Flag                                              | Wert | BESCHREIBUNG                                                                                                                                                                                                                             |
|---------------------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WMP \_ MDRT \_ FLAGS \_ UNREPORTED \_ ACQUIRED \_ ITEMS** | 0x1   | Das Gerät enthält einige erworbene Elemente, die nicht in der Liste der PUOIDS zurückgegeben werden können. Beachten Sie, dass dieses Flag mit Dem Antwortparameter 2 nicht redundant ist. Legen Sie dieses Flag nur fest, wenn angeforderte Elemente vorhanden sind, die das Gerät nicht zurückgeben kann. |



 

Die Bits 1 bis 31 sind für die zukünftige Verwendung reserviert. Diese Bits sollten auf 0 (null) festgelegt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 




