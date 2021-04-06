---
title: Geräte Erweiterungen für Wiedergabelisten Objekt Einstellungen
description: Geräte Erweiterungen für Wiedergabelisten Objekt Einstellungen
ms.assetid: 33b3dd18-fda2-4bf9-a893-5d77cdde6b80
keywords:
- Windows Media Player, Geräte Erweiterungen
- Windows-Media Player, Erweiterungen
- Windows Media Player, Wiedergabelisten Objekt Einstellungen
- Geräte Erweiterungen, Wiedergabelisten Objekt Einstellungen
- Erweiterungen, Wiedergabelisten Objekt Einstellungen
- Wiedergabelisten Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fd9c6301e33307fc49e50b8aa9042752e020e32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712732"
---
# <a name="device-extensions-for-playlist-object-preferences"></a>Geräte Erweiterungen für Wiedergabelisten Objekt Einstellungen

Im Rahmen der Synchronisierung werden von Windows Media Player 10 oder höher Wiedergabelisten Objekte zu MTP-fähigen tragbaren Geräten kopiert. In Windows Media Player 11 werden neue Funktionen eingeführt, die es tragbaren Geräten ermöglichen, die Typen der kopierten Wiedergabelisten Objekte einzuschränken. (Windows Media Player synchronisiert den Wiedergabelisten Inhalt immer gemäß den Synchronisierungs Regeln. Diese Funktion wirkt sich nur auf die Synchronisierung von Wiedergabelisten Objekten aus.) Windows Media Player kopiert drei Arten von Wiedergabelisten Objekten vom Computer auf das Gerät:

-   **Gewöhnliche Wiedergabelisten.** Dabei handelt es sich um Wiedergabelisten, die in der **Bibliotheks** Funktion von Windows Media Player sichtbar sind. Hierzu zählen die vom Benutzer erstellten Wiedergabelisten, der Bibliothek hinzugefügte Wiedergabelisten von Online Stores und mit dem Player installierte Beispiel Wiedergabelisten. Windows Media Player kopiert nur diese Wiedergabelisten auf das Gerät, wenn der Benutzer Sie für die Synchronisierung ausgewählt hat.
-   **Wiedergabe Wiedergabe Wiedergabelisten.** Hierbei handelt es sich um besondere Wiedergabelisten, die mit Windows Media Player installiert und nur für die Synchronisierung verwendet werden. Diese Wiedergabelisten sind nur im Setup-Assistenten für Windows Media Player-Geräte sichtbar.
-   **Implizit erstellte Wiedergabelisten.** Diese Wiedergabelisten werden erstellt, wenn der Benutzer einen Kategorieordner (z. b. " **Artist** " oder " **Album**") auf den Bereich zieht, der die zu synchronisierenden Elemente auflistet.

Die Header Datei mit dem Namen "wmpdevices. h", die für diese Version aktualisiert wurde, definiert die Strukturen und Konstanten, die für die Unterstützung von Windows Media Player-Geräte Erweiterungen erforderlich sind.

Damit ein Gerät mithilfe des Windows Media Player MTP-Geräte Erweiterungs Satzes als unterstützende Wiedergabelisten Objekt Einstellungen erkannt wird, muss es die folgenden Informationen in das deviceInfo-DataSet einschließen. (Weitere Informationen zu diesem Dataset finden Sie im Abschnitt 4.6.1 der MTP-Spezifikation.)



| Datasetfeld          | Feld Reihenfolge | Datentyp  | Wert                       |
|------------------------|-------------|------------|-----------------------------|
| Vendorextensionid      | 2           | **UINT32** | 0x00000006                  |
| Vendorextensionversion | 3           | **UINT16** | 0x0064 (100)                |
| Vendorextensiondesc    | 4           | **String** | "Microsoft.com/WMPPD: 11,0" |



 

In der folgenden Tabelle finden Sie Details zum MTP-Vorgang für Wiedergabelisten Objekt-Einstellungen.



| Element                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vorgangs Code        | 0x9203                                                                                                                                                                                                                                                                                          |
| Vorgangs Parameter 1 | 0                                                                                                                                                                                                                                                                                               |
| Vorgangs Parameter 2 | 0                                                                                                                                                                                                                                                                                               |
| Vorgangs Parameter 3 | 0                                                                                                                                                                                                                                                                                               |
| Vorgangs Parameter 4 | 0                                                                                                                                                                                                                                                                                               |
| Vorgangs Parameter 5 | 0                                                                                                                                                                                                                                                                                               |
| Daten                  | Das Gerät gibt im Antwort Parameter 1 einen Wert zurück, der die Einstellung für die Wiedergabelisten Objekt Synchronisierung angibt.                                                                                                                                                                                      |
| Daten Richtung        | R->I                                                                                                                                                                                                                                                                                         |
| Antwort Code Optionen | MTP- \_ Antwort \_ OK (0x2001) oder gültiger Fehler Antwort Code.                                                                                                                                                                                                                                        |
| Antwort Parameter 1  | 0 oder 1. Der Wert 0 gibt an, dass Windows-Media Player nur gewöhnliche Wiedergabelisten Objekte synchronisieren muss. Der Wert 1 gibt an, dass Windows-Media Player gewöhnliche Wiedergabelisten Objekte, Aktien und implizit erstellte Synchronisierungs Wiedergabelisten-Objekte synchronisieren müssen. Dies ist das Standardverhalten. |
| Antwort Parameter 2  | 0                                                                                                                                                                                                                                                                                               |
| Antwort Parameter 3  | 0                                                                                                                                                                                                                                                                                               |
| Antwort Parameter 4  | 0                                                                                                                                                                                                                                                                                               |
| Antwort Parameter 5  | 0                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Bemerkungen

Die Implementierung dieses Features ist für tragbare Geräte optional. Windows Media Player synchronisiert normale Wiedergabelisten Objekte, Wiedergabelisten Objekte für die endsynchronisierung und implizit erstellte Wiedergabelisten Objekte standardmäßig.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 




