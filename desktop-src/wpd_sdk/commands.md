---
description: Befehle
ms.assetid: f579745a-5327-4c8b-bfa7-fe81d9657a3b
title: Befehle (WPD-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a723e9eff52bf0b0b301d1fba672db5887afebef701a312786aeafb4decb733f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118431113"
---
# <a name="commands-wpd-api"></a>Befehle (WPD-API)

Die Clientanwendung und der Treiber kommunizieren über Befehle, die vom Client (über die Windows PORTABLE DEVICE-API) an den Treiber (über das User-Mode Driver Framework) gesendet werden. Ein Befehl kann einen Parameter enthalten oder nicht enthalten und kann ein Ergebnis zurückgeben. Ein Client kann einen Befehl explizit senden, indem er entweder die [**IPortableDevice::SendCommand-Methode**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) oder die **IPortableDeviceService:SendCommand-Methode** aufruft oder implizit eine der Methoden der Clientschnittstellen aufruft. Einige Befehle können nur explizit gesendet werden. diese sind in der Dokumentation des Befehls angegeben. Die Befehlsreferenzseiten beschreiben den Zweck eines Befehls sowie die parameter, die er erwartet, und welche Parameter er zurückgeben soll.

Ein Befehl wird durch eine **PROPERTYKEY-Struktur** identifiziert. Dies besteht aus zwei Teilen: einem GUID-Teil *(fmtid-Member)* und einem DWORD-Teil *(pid-Member).* Der GUID-Teil wird verwendet, um die Kategorie anzugeben, zu der der Befehl gehört (verwandte Befehle gehören zur gleichen Kategorie und weisen daher denselben *fmtid auf).* Der DWORD-Teil gibt die Befehls-ID an und wird verwendet, um die einzelnen Befehle innerhalb einer Befehlskategorie zu unterscheiden (die *PID-Werte* für Befehle in derselben Kategorie unterscheiden sich).

In der folgenden Tabelle sind die Kategorien von Befehlen aufgeführt, die Windows Portable Devices definiert. Gerätehersteller können eigene Befehle definieren, indem sie eigene Befehlskategorien und Befehls-IDs erstellen. Ein Hersteller sollte den unten aufgeführten Kategorien jedoch keine Befehle hinzufügen, da diese von Microsoft reserviert werden.

**Befehlskategorien**



| Befehlskategorie                         | BESCHREIBUNG                                                                                                                             |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ CATEGORY \_ COMMON**                | Befehle, die allen Objekten und Geräten gemeinsam sind.                                                                                    |
| **WPD \_ CATEGORY DEVICE HINTS (GERÄTEHINWEISE DER KATEGORIE \_ WPD) \_**         | Befehle, die verwendet werden, um optionale Geräteinformationen abzurufen, die zur Verbesserung der Endbenutzererfahrung verwendet werden können.                         |
| **WPD \_ CATEGORY \_ SMS**                   | Befehle, die für Geräte verwendet werden, die die Sms-Funktionalität (Short Message Service) unterstützen, die in der Regel auf Mobiltelefonen verfügbar gemacht wird. |
| **WPD \_ CATEGORY \_ STILL \_ IMAGE \_ CAPTURE** | Befehle, die für Geräte verwendet werden, die die Bilderfassung noch unterstützen.                                                                    |
| **WPD \_ CATEGORY \_ STORAGE**               | Befehle, die für speicherfunktionelle Objekte verwendet werden.                                                                                  |



 

Die spezifischen Befehle, die für jeden dieser Typen definiert sind, werden in den folgenden Tabellen nach Befehlstyp organisiert angegeben.

**WPD \_ CATEGORY \_ COMMON Category**



| Befehl                                                                                | BESCHREIBUNG        |
|----------------------------------------------------------------------------------------|--------------------|
| [**WPD-BEFEHL \_ \_ \_ ALLGEMEINES GERÄT \_ ZURÜCKSETZEN**](wpd-command-common-reset-device-command.md) | Setzt das Gerät zurück. |



 

**WPD \_ CATEGORY \_ DEVICE \_ HINTS Category**



| Befehl                                                                                                              | BESCHREIBUNG                                                                      |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**WPD \_ COMMAND \_ DEVICE \_ HINTS \_ GET \_ CONTENT \_ LOCATION**](wpd-command-device-hints-get-content-location-command.md) | Ruft die Objekt-IDs von Ordnern ab, die ein Objekt eines angegebenen Typs enthalten können. |



 

**WPD \_ CATEGORY \_ STORAGE Category**



| Befehl                                                                     | BESCHREIBUNG                                                         |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**WPD \_ COMMAND \_ STORAGE \_ EJECT**](wpd-command-storage-eject-command.md)   | Wirft ein Speichermedium aus, das vom Treiber remote ausjiziert werden kann. |
| [**\_ \_ WPD-BEFEHLSSPEICHERFORMAT \_**](wpd-command-storage-format-command.md) | Formatiert ein Speicherfunktionsobjekt auf dem Gerät.                  |



 

**WPD \_ CATEGORY \_ SMS Category**



| Befehl                                                         | BESCHREIBUNG                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| [**WPD-BEFEHL \_ \_ SMS \_ SENDEN**](wpd-command-sms-send-command.md) | Initiiert das Senden einer SMS-Nachricht durch ein SMS-Funktionsobjekt. |



 

**WPD \_ CATEGORY \_ STILL \_ IMAGE \_ CAPTURE Category**



| Befehl                                                                                                   | BESCHREIBUNG                                                         |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**WPD-BEFEHL \_ IMMER NOCH IMAGE CAPTURE \_ \_ \_ \_ INITIATE**](wpd-command-still-image-capture-initiate-command.md) | Initiiert eine Noch-Bilderfassung durch ein funktionstüchtiges Bildobjekt. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 



