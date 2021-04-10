---
description: Befehle
ms.assetid: f579745a-5327-4c8b-bfa7-fe81d9657a3b
title: Befehle (WPD-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974c6b2b68949e53ae778ed56adcfcb10d2edd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214542"
---
# <a name="commands-wpd-api"></a>Befehle (WPD-API)

Die Client Anwendung und der Treiber kommunizieren mithilfe von Befehlen, die vom Client (über die Portable Windows-Geräte-API) an den Treiber gesendet werden (über das User-Mode Driver-Framework). Ein Befehl kann einen-Parameter enthalten, und er kann ein-Ergebnis zurückgeben. Ein Client kann einen Befehl explizit senden, indem er entweder die [**iportabledevice:: sendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) -Methode oder die **iportabledeviceservice: sendCommand** -Methode oder implizit durch Aufrufen einer der Methoden der Client Schnittstellen aufgerufen wird. Einige Befehle können nur explizit gesendet werden. Diese sind in der Dokumentation des Befehls angegeben. Die Referenzseiten des Befehls beschreiben den Zweck eines Befehls sowie die Parameter, die erwartet werden sollen, und die Parameter, die zurückgegeben werden sollen.

Ein Befehl wird durch eine **PropertyKey** -Struktur identifiziert. Dies besteht aus zwei Teilen: einem GUID-Teil (dem *fmtid* -Member) und einem DWORD-Teil (dem *PID* -Member). Der GUID-Teil wird verwendet, um die Kategorie anzugeben, zu der der Befehl gehört (verwandte Befehle gehören derselben Kategorie an und verfügen daher über dieselbe *fmtid*). Der DWORD-Teil gibt die Befehls-ID an und wird verwendet, um die einzelnen Befehle innerhalb einer Befehls Kategorie zu unterscheiden (die *PID* -Werte für Befehle in derselben Kategorie werden unterschiedlich sein).

In der folgenden Tabelle werden die Kategorien von Befehlen aufgelistet, die von Windows-tragbaren Geräten definiert werden. Gerätehersteller können eigene Befehle definieren, indem Sie Ihre eigenen Befehls Kategorien und Befehls-IDs erstellen. Ein Hersteller sollte jedoch keine Befehle zu den unten aufgeführten Kategorien hinzufügen, da diese von Microsoft reserviert werden.

**Befehls Kategorien**



| Befehlskategorie                         | BESCHREIBUNG                                                                                                                             |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **Allgemeine WPD- \_ Kategorie \_**                | Befehle, die allen Objekten und Geräten gemeinsam sind.                                                                                    |
| **WPD- \_ Kategorie \_ Geräte \_ Hinweise**         | Befehle, die zum Abrufen Optionaler Geräteinformationen verwendet werden, die verwendet werden können, um die Endbenutzer Leistung zu verbessern.                         |
| **WPD- \_ Kategorie \_ SMS**                   | Befehle, die für Geräte verwendet werden, die die SMS (Short Message Service)-Funktionalität unterstützen, die in der Regel auf Mobiltelefonen verfügbar gemacht wird. |
| **WPD- \_ Kategorie \_ trotzdem \_ Image \_ Erfassung** | Befehle, die für Geräte verwendet werden, die die Image Erfassung noch unterstützen.                                                                    |
| **WPD \_ - \_ kategoriespeicher**               | Befehle, die für Speicher funktionale Objekte verwendet werden.                                                                                  |



 

Die spezifischen Befehle, die für jeden dieser Typen definiert sind, werden in den folgenden Tabellen nach Befehlstyp organisiert angegeben.

**Kategorie "Kategorie Allgemein" in WPD \_ \_**



| Get-Help                                                                                | BESCHREIBUNG        |
|----------------------------------------------------------------------------------------|--------------------|
| [**gemeinsamer WPD- \_ Befehl \_ \_ Gerät zurücksetzen \_**](wpd-command-common-reset-device-command.md) | Setzt das Gerät zurück. |



 

**Kategorie " \_ \_ Geräte \_ Hinweise" der WPD-Kategorie**



| Get-Help                                                                                                              | BESCHREIBUNG                                                                      |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**gerätehinweise zum WPD- \_ Befehl \_ \_ \_ get \_ Content \_ Location**](wpd-command-device-hints-get-content-location-command.md) | Ruft die Objekt-IDs der Ordner ab, die ein Objekt eines angegebenen Typs enthalten können. |



 

**Kategorie \_ \_ Speicher Kategorie für WPD**



| Get-Help                                                                     | BESCHREIBUNG                                                         |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**WPD- \_ Befehls \_ Speicher- \_ eject**](wpd-command-storage-eject-command.md)   | Ewirft ein Speichermedium ein, das per Remote Zugriff vom Treiber entfernt werden kann. |
| [**\_ \_ Speicher \_ Format für WPD-Befehl**](wpd-command-storage-format-command.md) | Formatiert ein Speicher funktionales Objekt auf dem Gerät.                  |



 

**Kategorie der Kategorie "WPD" \_ \_**



| Get-Help                                                         | BESCHREIBUNG                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| [**WPD- \_ Befehl \_ SMS \_ senden**](wpd-command-sms-send-command.md) | Initiiert das Senden einer SMS-Nachricht durch ein SMS-Funktions Objekt. |



 

**Kategorie der WPD- \_ Kategorie \_ immer noch \_ Bild \_ Erfassung**



| Get-Help                                                                                                   | BESCHREIBUNG                                                         |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**WPD- \_ Befehl wird \_ immer noch \_ \_ \_ initiiert**](wpd-command-still-image-capture-initiate-command.md) | Initiiert eine immer noch Bild Erfassung durch ein noch Bild funktionales Objekt. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 



