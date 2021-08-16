---
title: Geräteerweiterungen für Wiedergabelistenobjekteinstellungen
description: Geräteerweiterungen für Wiedergabelistenobjekteinstellungen
ms.assetid: 33b3dd18-fda2-4bf9-a893-5d77cdde6b80
keywords:
- Windows Media Player,Geräteerweiterungen
- Windows Media Player,Erweiterungen
- Windows Media Player,Playlist-Objekteinstellungen
- Geräteerweiterungen, Wiedergabelistenobjekteinstellungen
- Erweiterungen,Playlist-Objekteinstellungen
- Wiedergabelistenobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f2acb01de41b753a85fee1c69e0bf015c687da04f50a10531ee5c67b0a13cc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340919"
---
# <a name="device-extensions-for-playlist-object-preferences"></a>Geräteerweiterungen für Wiedergabelistenobjekteinstellungen

Im Rahmen des Synchronisierungsprozesses kopiert Windows Media Player 10 oder höher Wiedergabelistenobjekte auf MTP-fähige portable Geräte. Windows Media Player 11 führt neue Funktionen ein, mit denen portable Geräte die Typen der kopierten Wiedergabelistenobjekte einschränken können. (Windows Media Player synchronisiert wiedergabelistenden Inhalt immer gemäß den Synchronisierungsregeln. Dieses Feature wirkt sich nur auf die Synchronisierung von Wiedergabelistenobjekten aus.) Windows Media Player kopiert drei Arten von Wiedergabelistenobjekten vom Computer auf das Gerät:

-   **Normale Wiedergabelisten.** Dies sind Wiedergabelisten, die im **Bibliotheksfeature** des Windows Media Player. Dazu gehören wiedergabelisten, die vom Benutzer erstellt wurden, Wiedergabelisten, die der Bibliothek von Onlineshops hinzugefügt wurden, und Beispielwiedergabelisten, die mit dem Player installiert wurden. Windows Media Player werden nur diese Wiedergabelisten auf das Gerät kopiert, wenn der Benutzer sie für die Synchronisierung ausgewählt hat.
-   **Wiedergabelisten für die Synchronisierung auf Lager.** Hierbei handelt es sich um spezielle Wiedergabelisten, die mit Windows Media Player installiert und nur für die Synchronisierung verwendet werden. Diese Wiedergabelisten sind nur in der Windows Media Player Geräteliste Setup-Assistant.
-   **Implizit erstellte Wiedergabelisten.** Diese Wiedergabelisten werden erstellt, wenn der Benutzer einen Kategorieordner, z. B. **Interpret** oder **Album,** in den Bereich mit den zu synchronisierenden Elementen zieht und abstürzt.

Die Headerdatei mit dem Namen wmpdevices.h, die für dieses Release aktualisiert wurde, definiert die Strukturen und Konstanten, die zur Unterstützung Windows Media Player Geräteerweiterungen erforderlich sind.

Damit ein Gerät über den MTP-Geräteerweiterungssatz Windows Media Player als unterstützende Wiedergabelistenobjekteinstellungen erkannt wird, muss es die folgenden Informationen im DeviceInfo-Dataset enthalten. (Weitere Informationen zu diesem Dataset finden Sie in Abschnitt 4.6.1 der MTP-Spezifikation.)



| Datasetfeld          | Feld reihenfolge | Datentyp  | Wert                       |
|------------------------|-------------|------------|-----------------------------|
| VendorExtensionID      | 2           | **UINT32** | 0x00000006                  |
| VendorExtensionVersion | 3           | **UINT16** | 0x0064 (100)                |
| VendorExtensionDesc    | 4           | **String** | "microsoft.com/WMPPD: 11.0" |



 

Die folgende Tabelle enthält Details zum MTP-Vorgang für Wiedergabelistenobjekteinstellungen.



| Element                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vorgangscode        | 0x9203                                                                                                                                                                                                                                                                                          |
| Operation-Parameter 1 | 0                                                                                                                                                                                                                                                                                               |
| Operation-Parameter 2 | 0                                                                                                                                                                                                                                                                                               |
| Operation-Parameter 3 | 0                                                                                                                                                                                                                                                                                               |
| Operation Parameter 4 | 0                                                                                                                                                                                                                                                                                               |
| Operation Parameter 5 | 0                                                                                                                                                                                                                                                                                               |
| Daten                  | Das Gerät gibt einen Wert in Antwortparameter 1 zurück, um die Synchronisierungseinstellung für Wiedergabelistenobjekt anzugeben.                                                                                                                                                                                      |
| Datenrichtung        | R->I                                                                                                                                                                                                                                                                                         |
| Antwortcodeoptionen | MTP \_ RESPONSE \_ OK (0x2001) oder gültiger Fehlerantwortcode.                                                                                                                                                                                                                                        |
| Antwortparameter 1  | 0 oder 1. Der Wert 0 gibt an, dass Windows Media Player nur normale Wiedergabelistenobjekte synchronisieren müssen. Der Wert 1 gibt an, dass Windows Media Player normale Wiedergabelistenobjekte, Zusammengestellte und implizit erstellte Synchronisierungswiedergabelistenobjekte synchronisieren muss. Dies ist das Standardverhalten. |
| Antwortparameter 2  | 0                                                                                                                                                                                                                                                                                               |
| Antwortparameter 3  | 0                                                                                                                                                                                                                                                                                               |
| Antwortparameter 4  | 0                                                                                                                                                                                                                                                                                               |
| Antwortparameter 5  | 0                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Hinweise

Die Implementierung dieses Features ist für portable Geräte optional. Windows Media Player synchronisiert standardmäßig normale Wiedergabelistenobjekte, Synchronisierungswiedergabelistenobjekte und implizit erstellte Wiedergabelistenobjekte.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 




