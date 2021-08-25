---
title: CLSID-Schlüssel
description: Eine CLSID ist ein global eindeutiger Bezeichner, der ein COM-Klassenobjekt identifiziert. Wenn Ihr Server oder Container das Verknüpfen mit den eingebetteten Objekten zulässt, müssen Sie eine CLSID für jede unterstützte Objektklasse registrieren.
ms.assetid: b5777d87-abf2-45b9-9d95-61db878a5810
keywords:
- CLSID-Registrierungsschlüssel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd390fc6a1ccb15e128245c3b6a80e2b4ca57f41de9e9c21e93ebe4c708783d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854980"
---
# <a name="clsid-key"></a>CLSID-Schlüssel

Eine CLSID ist ein global eindeutiger Bezeichner, der ein COM-Klassenobjekt identifiziert. Wenn Ihr Server oder Container das Verknüpfen mit den eingebetteten Objekten zulässt, müssen Sie eine CLSID für jede unterstützte Objektklasse registrieren.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ LOCAL \_ MACHINE SOFTWARE Classes \\ \\ \\ CLSID** \\ *{* CLSID *}*



| Registrierungsschlüssel                                                 | Beschreibung                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**Appid**](appid.md)                                       | Ordnet eine AppID einer CLSID zu.                                                                                                        |
| [**AutoConvertTo**](autoconvertto.md)                       | Gibt die automatische Konvertierung einer angegebenen Klasse von -Objekten in eine neue Klasse von -Objekten an.                                                |
| [**AutoTreatAs**](autotreatas.md)                           | Legt die CLSID für den [**TreatAs-Schlüssel automatisch**](treatas.md) auf den angegebenen Wert fest.                                              |
| [**AuxUserType**](auxusertype.md)                           | Gibt den kurzen Anzeigenamen und die Anwendungsnamen einer Anwendung an.                                                                     |
| [**Control**](control.md)                                   | Identifiziert ein Objekt als ActiveX Steuerelement.                                                                                              |
| [**Konvertierung**](conversion.md)                             | Wird vom Dialogfeld **Konvertieren** verwendet, um die Formate zu bestimmen, die eine Anwendung lesen und schreiben kann.                                           |
| [**Dataformats**](dataformats.md)                           | Gibt die Standard- und Hauptdatenformate an, die von einer Anwendung unterstützt werden.                                                                 |
| [**DefaultIcon**](defaulticon.md)                           | Stellt Standardsymbolinformationen für symboldarstellungen von Objekten zur Verfügung.                                                                   |
| [**InprocHandler**](inprochandler.md)                       | Gibt an, ob eine Anwendung einen benutzerdefinierten Handler verwendet.                                                                                  |
| [**InprocHandler32**](inprochandler32.md)                   | Gibt an, ob eine Anwendung einen benutzerdefinierten Handler verwendet.                                                                                  |
| [**InprocServer**](inprocserver.md)                         | Gibt den Pfad zur Prozessserver-DLL an.                                                                                         |
| [**Inprocserver32**](inprocserver32.md)                     | Registriert einen 32-Bit-In-Process-Server und gibt das Threadingmodell des Apartments an, in dem der Server ausgeführt werden kann.                           |
| [**Insertierbaren**](insertable.md)                             | Gibt an, dass Objekte dieser Klasse im Dialogfeld **Objekt** einfügen angezeigt werden sollen, wenn sie von COM-Containeranwendungen verwendet werden. |
| [**Schnittstelle**](interface.md)                               | Ein optionaler Eintrag, der alle Schnittstellen-IDs (IIDs) angibt, die von der zugeordneten Klasse unterstützt werden.                                             |
| [**LocalServer**](localserver.md)                           | Gibt den vollständigen Pfad zu einer lokalen 16-Bit-Serveranwendung an.                                                                            |
| [**LocalServer32**](localserver32.md)                       | Gibt den vollständigen Pfad zu einer lokalen 32-Bit-Serveranwendung an.                                                                            |
| [**MiscStatus**](miscstatus.md)                             | Gibt an, wie ein Objekt erstellt und angezeigt wird.                                                                                           |
| [**ProgID**](progid.md)                                     | Ordnet eine ProgID einer CLSID zu.                                                                                                        |
| [**ToolBoxBitmap32**](toolboxbitmap32.md)                   | Identifiziert den Modulnamen und die Ressourcen-ID für eine 16 x 16-Bitmap, die für das Gesicht einer Symbolleiste oder Toolboxschaltfläche verwendet werden soll.                      |
| [**TreatAs**](treatas.md)                                   | Gibt die CLSID einer Klasse an, die die aktuelle Klasse emulieren kann.                                                                       |
| [**Verb**](verb.md)                                         | Gibt die Verben an, die für eine Anwendung registriert werden sollen.                                                                                 |
| [**Version**](version.md)                                   | Gibt die Versionsnummer des Steuerelements an.                                                                                             |
| [**VersionIndependentProgID**](versionindependentprogid.md) | Ordnet eine ProgID einer CLSID zu. Dieser Wert wird verwendet, um die neueste Version einer Objektanwendung zu bestimmen.                           |



 

## <a name="remarks"></a>Hinweise

Der **Schlüssel HKEY \_ LOCAL MACHINE \_ SOFTWARE \\ \\ Classes** entspricht dem **HKEY CLASSES \_ \_ ROOT-Schlüssel,** der aus Kompatibilitäts- mit früheren Versionen von COM beibehalten wurde.

Der CLSID-Schlüssel enthält Informationen, die vom COM-Standardhandler verwendet werden, um Informationen zu einer Klasse zurück zu geben, wenn sie sich im Ausführungszustand befindet.

Um eine CLSID für Ihre Anwendung zu erhalten, können Sie die Uuidgen.exe oder die [**CoCreateGuid-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) verwenden.

Die CLSID ist eine hexadezimale 128-Bit-Zahl innerhalb eines Paars geschweifter Klammern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid)
</dt> </dl>

 

 




