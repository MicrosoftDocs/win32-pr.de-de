---
title: CLSID-Schlüssel
description: Eine CLSID ist eine Globally Unique Identifier, die ein com-Klassenobjekt identifiziert. Wenn Ihr Server oder Container das Verknüpfen mit den eingebetteten Objekten zulässt, müssen Sie für jede unterstützte Objektklasse eine CLSID registrieren.
ms.assetid: b5777d87-abf2-45b9-9d95-61db878a5810
keywords:
- CLSID-Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9253446a039e47996366c7dfdb51c01f9b1993
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388538"
---
# <a name="clsid-key"></a>CLSID-Schlüssel

Eine CLSID ist eine Globally Unique Identifier, die ein com-Klassenobjekt identifiziert. Wenn Ihr Server oder Container das Verknüpfen mit den eingebetteten Objekten zulässt, müssen Sie für jede unterstützte Objektklasse eine CLSID registrieren.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ \_Software Klassen der lokalen Maschine \\ \\ \\ CLSID** \\ *{* CLSID *}*



| Registrierungsschlüssel                                                 | Beschreibung                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppID**](appid.md)                                       | Ordnet eine AppID einer CLSID zu.                                                                                                        |
| [**Autoconvertto**](autoconvertto.md)                       | Gibt die automatische Konvertierung einer bestimmten Klasse von Objekten in eine neue Klasse von Objekten an.                                                |
| [**AutoTreatAs**](autotreatas.md)                           | Legt die CLSID für den " [**TreatAs**](treatas.md) "-Schlüssel automatisch auf den angegebenen Wert fest.                                              |
| [**"Auxusertype"**](auxusertype.md)                           | Gibt den kurzen anzeigen Amen und Anwendungsnamen einer Anwendung an.                                                                     |
| [**Control**](control.md)                                   | Identifiziert ein Objekt als ActiveX-Steuerelement.                                                                                              |
| [**Konvertierung**](conversion.md)                             | Wird vom Dialogfeld **konvertieren** verwendet, um die Formate zu ermitteln, die eine Anwendung lesen und schreiben kann.                                           |
| [**DataFormats**](dataformats.md)                           | Gibt die von einer Anwendung unterstützten Standard-und Hauptdaten Formate an.                                                                 |
| [**DefaultIcon**](defaulticon.md)                           | Stellt Standard Symbol Informationen für die ikonischen Präsentationen von Objekten bereit.                                                                   |
| [**InprocHandler**](inprochandler.md)                       | Gibt an, ob eine Anwendung einen benutzerdefinierten Handler verwendet.                                                                                  |
| [**InprocHandler32**](inprochandler32.md)                   | Gibt an, ob eine Anwendung einen benutzerdefinierten Handler verwendet.                                                                                  |
| [**InprocServer**](inprocserver.md)                         | Gibt den Pfad zur Prozess internen Server-DLL an.                                                                                         |
| [**InprocServer32**](inprocserver32.md)                     | Registriert einen 32-Bit-in-Process-Server und gibt das Threading Modell des Apartment an, in dem der Server ausgeführt werden kann.                           |
| [**Einfügbar**](insertable.md)                             | Gibt an, dass Objekte dieser Klasse im Listenfeld **Objekt einfügen** angezeigt werden sollen, wenn Sie von com-Container Anwendungen verwendet werden. |
| [**Schnittstelle**](interface.md)                               | Ein optionaler Eintrag, der alle von der zugeordneten-Klasse unterstützten Schnittstellen-IDs (IIDs) angibt.                                             |
| [**LocalServer**](localserver.md)                           | Gibt den vollständigen Pfad zu einer 16-Bit-Anwendung für den lokalen Server an.                                                                            |
| [**LocalServer32**](localserver32.md)                       | Gibt den vollständigen Pfad zu einer lokalen 32-Bit-Serveranwendung an.                                                                            |
| [**Fehlstatus**](miscstatus.md)                             | Gibt an, wie ein Objekt erstellt und angezeigt wird.                                                                                           |
| [**ProgID**](progid.md)                                     | Ordnet eine ProgID einer CLSID zu.                                                                                                        |
| [**ToolBoxBitmap32**](toolboxbitmap32.md)                   | Identifiziert den Modulnamen und die Ressourcen-ID für eine 16 x 16-Bitmap, die für die Vorderseite einer Symbolleiste oder Toolbox Schaltfläche verwendet werden soll.                      |
| [**Behandlungen**](treatas.md)                                   | Gibt die CLSID einer Klasse an, die die aktuelle Klasse emulieren kann.                                                                       |
| [**Verb**](verb.md)                                         | Gibt die Verben an, die für eine Anwendung registriert werden sollen.                                                                                 |
| [**Version**](version.md)                                   | Gibt die Versionsnummer des Steuer Elements an.                                                                                             |
| [**VersionIndependentProgId**](versionindependentprogid.md) | Ordnet eine ProgID einer CLSID zu. Dieser Wert wird verwendet, um die neueste Version einer Objekt Anwendung zu bestimmen.                           |



 

## <a name="remarks"></a>Bemerkungen

Der Schlüssel **HKEY- \_ \_ \\ Software \\ Klassen für lokale Computer** entspricht dem Stamm Schlüssel der **HKEY- \_ Klassen \_** , der für die Kompatibilität mit früheren Versionen von com beibehalten wurde.

Der CLSID-Schlüssel enthält Informationen, die vom Standard-com-Handler verwendet werden, um Informationen zu einer Klasse zurückzugeben, wenn Sie sich im Zustand wird ausgeführt befindet.

Zum Abrufen einer CLSID für Ihre Anwendung können Sie das Uuidgen.exe verwenden oder die [**cokreateguid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) -Funktion verwenden.

Die CLSID ist eine 128-Bit-Zahl in Hex innerhalb eines Paares aus geschweiften Klammern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid)
</dt> </dl>

 

 




