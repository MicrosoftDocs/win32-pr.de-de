---
title: Geräte Erweiterungen für die Berichterstellung über den Inhalt
description: Geräte Erweiterungen für die Berichterstellung über den Inhalt
ms.assetid: 597d872e-9105-4edb-afa3-9f4407de0f73
keywords:
- Windows Media Player, Geräte Erweiterungen
- Windows-Media Player, Erweiterungen
- Windows Media Player, von der Berichterstellung erworbene Inhalte
- Geräte Erweiterungen, von der Berichterstellung erworbene Inhalte
- Erweiterungen, von der Berichterstellung erworbene Inhalte
- Bericht erfassten Inhalte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 831312457427cc9fe4ceed004772f3b174f77989
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338400"
---
# <a name="device-extensions-for-reporting-acquired-content"></a>Geräte Erweiterungen für die Berichterstellung über den Inhalt

Mit Windows Media Player 11 werden neue Funktionen eingeführt, die es tragbaren Geräten ermöglichen, den Player über Inhalte zu informieren, die seit der letzten Synchronisierung zum Gerät hinzugefügt wurden. Windows Media Player 11 kann diese Informationen verwenden, um neu erworbenen Inhalt vom Gerät auf den Computer des Benutzers zu kopieren. Gerätehersteller sollten die folgenden Anforderungen beachten, um diese Funktionalität zu unterstützen:

-   Diese Funktion wird nur für MTP-aktivierte Geräte unterstützt.
-   Diese Funktion funktioniert nur mit Geräten, die eine Partnerschaft mit Windows Media Player haben.
-   Geräte dürfen nur Inhalt melden, den das Gerät erstellt oder heruntergeladen hat. Dies schließt Fotos ein, die vom Gerät entnommen werden. vom Gerät erstellte Sprachaufzeichnungen; Voicemail-Aufzeichnungen; Downloads von einer Speicherkarte und werden aus dem Internet heruntergeladen. Inhalte, die als Ergebnis der Synchronisierung mit einem anderen Gerät oder einer anderen Partnerschaft auf dem Gerät gespeichert wurden, dürfen nicht gemeldet werden.

Die Header Datei "wmpdevices. h", die als Teil des Windows Media Player SDK installiert wird, definiert die Strukturen und Konstanten, die für die Unterstützung von Windows Media Player-Geräte Erweiterungen erforderlich sind.

Damit ein Gerät als Unterstützung für die Berichterstellung von erworbenen Inhalten über den Windows Media Player MTP-Geräte Erweiterungs Satz erkannt wird, muss es die folgenden Informationen in das deviceInfo-DataSet einschließen. (Weitere Informationen zu diesem Dataset finden Sie im Abschnitt 4.6.1 der MTP-Spezifikation.)



| Datasetfeld          | Feld Reihenfolge | Datentyp  | Wert                       |
|------------------------|-------------|------------|-----------------------------|
| Vendorextensionid      | 2           | **UINT32** | 0x00000006                  |
| Vendorextensionversion | 3           | **UINT16** | 0x0064 (100)                |
| Vendorextensiondesc    | 4           | **String** | "Microsoft.com/WMPPD: 11,0" |



 

In der folgenden Tabelle finden Sie Details zum MTP-Vorgang für den Bericht erfassten Inhalt.



| Element                  | BESCHREIBUNG                                                                                                                                                                                                                     |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vorgangs Code        | 0x9202                                                                                                                                                                                                                          |
| Vorgangs Parameter 1 | Die Transaktions-ID, die während der letzten Sitzung vom Gerät bereitgestellt wurde. Dieser Wert ist für die erste Sitzung 0 (null).                                                                                                                |
| Vorgangs Parameter 2 | Start Index. Dieser Wert ist beim ersten Aufrufe einer Sitzung immer 0 (null). Bei nachfolgenden Aufrufen innerhalb derselben Synchronisierungs Sitzung erhöht sich dieser Wert um die Anzahl der Elemente, die von den vorherigen Antwortdaten zurückgegeben wurden. |
| Vorgangs Parameter 3 | 0x10000. Diese Konstante, die in wmpdevices. h definiert ist, ist die maximale Anzahl von puoids, die in der Antwort zurückgegeben werden können. Beachten Sie, dass der Wert dieser Konstante in zukünftigen Versionen dieser Header Datei möglicherweise überarbeitet wird.              |
| Vorgangs Parameter 4 | 0                                                                                                                                                                                                                               |
| Vorgangs Parameter 5 | 0                                                                                                                                                                                                                               |
| Daten                  | Das Gerät gibt ein MTP-Array mit den puoids zurück, die abgerufen wurden. Das Array beginnt mit einem **DWORD** -Wert, der die Anzahl der Elemente im Array angibt, gefolgt vom Array von Elementen.                               |
| Daten Richtung        | R->I                                                                                                                                                                                                                         |
| Antwort Code Optionen | **MTP \_ Antwort \_ OK** (0x2001) oder gültiger Fehler Antwort Code.                                                                                                                                                                    |
| Antwort Parameter 1  | Die aktuelle Transaktions-ID.                                                                                                                                                                                                     |
| Antwort Parameter 2  | Die Anzahl der puoids, die von zukünftigen Anforderungen abgerufen werden.                                                                                                                                                            |
| Antwort Parameter 3  | **DWORD** , das Statusinformationen enthält. Der Status wird auf bitweise angegeben. Informationen zu den zu verwendenden Flags finden Sie unter "Hinweise".                                                                                              |
| Antwort Parameter 4  | 0                                                                                                                                                                                                                               |
| Antwort Parameter 5  | 0                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Bemerkungen

Der Status wird durch den Antwort Parameter 3 in einer bitweisen Vorgehensweise mit dem folgenden Flag angegeben.



| Flag                                              | Wert | BESCHREIBUNG                                                                                                                                                                                                                             |
|---------------------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WMP- \_ MDRT- \_ Flags \_ nicht gemeldete \_ erfassten \_ Elemente** | 0x1   | Das Gerät enthält einige erworbene Elemente, die in der Liste der puoids nicht zurückgegeben werden können. Beachten Sie, dass dieses Flag mit dem Antwort Parameter 2 nicht redundant ist. Legen Sie dieses Flag nur fest, wenn angeforderte Elemente vorhanden sind, die das Gerät nicht zurückgeben kann. |



 

Bits 1 bis 31 sind für die zukünftige Verwendung reserviert. Diese Bits sollten auf 0 (null) festgelegt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 




