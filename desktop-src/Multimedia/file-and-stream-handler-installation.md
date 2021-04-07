---
title: Datei-und streamhandlerinstallation
description: Datei-und streamhandlerinstallation
ms.assetid: 8d007ea4-b75a-4b3f-965f-8091fcd4cb2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be94137df69ed35b57b1b8fbeb5c9640dd7636d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713596"
---
# <a name="file-and-stream-handler-installation"></a>Datei-und streamhandlerinstallation

Die avifile-Bibliothek verwendet installierte Datenstrom-und Datei Handler zum Lesen und Schreiben von AVI-Dateien und Streams. Ein-Handler wird installiert, wenn er sich im Windows-System Verzeichnis befindet, und die Registrierung enthält die folgenden Informationen, die zum beschreiben und Identifizieren eines Handlers erforderlich sind:

-   Der 16-Byte-Klassen Bezeichner für den Handler.
-   Eine kurze Beschreibung des Handlers.
-   Der Name der Datei, die den Handler enthält.
-   Die Dateierweiterung, die von einem Datei Handler verarbeitet werden kann.
-   Dateizugriff und andere Eigenschaften, die einem Datei Handler zugeordnet sind
-   Vier Zeichen Codes zur Identifizierung von Streamtypen, die von einem streamhandler verarbeitet werden können

Die avifile-Bibliothek fragt die Registrierung nach Handlern ab, die für eine Anwendung extern sind, wenn Sie Dateien öffnen und auf Datenströme zugreifen. Das Ergebnis einer erfolgreichen Abfrage gibt den Dateinamen eines Handlers zurück, der die in der Abfrage angegebene Datei oder den Streamtyp verarbeiten kann. Die Registrierung Listet jeden Handler auf, indem er drei Einträge erstellt, die das folgende Format aufweisen:


```C++
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000-000000000046}] 
@="Wave File reader/writer" 
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000- 
000000000046}\InprocServer32] 
@="wavefile.dll" 
"ThreadingModel"="Apartment" 
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000- 
000000000046}\AVIFile] 
@="3" 
 
```



Diese Einträge bestehen aus den folgenden Teilen:



| Teil                                   | BESCHREIBUNG                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HKEY- \_ Klassen Stamm \_                    | Identifiziert den Stamm Eintrag der Registrierung.                                                                                                                                               |
| Clsid                                  | Identifiziert diesen Eintrag als Klassen Bezeichner.                                                                                                                                             |
| {00010023-0000-0000-C000-000000000046} | Gibt einen Schnittstellen Bezeichner (IID) oder einen Klassen Bezeichner an. Dieser Wert ist ein eindeutiger 16-Byte-Bezeichner. (Der Bezeichner kann auch als GUID oder als uuid in anderen Handbüchern bezeichnet werden.) |
| Wave File Reader/Writer                | Gibt eine Zeichenfolge zur Beschreibung des Handlers an. Diese Zeichenfolge kann in Dialogfeldern zum Auswählen von Stream-und Datei Handlern angezeigt werden.                                                         |
| InprocServer32                         | Gibt die Datei an (in diesem Beispiel WAVEFILE.DLL), die zum Verarbeiten dieser Klasse geladen werden kann.                                                                                              |
| Avifile                                | Gibt die Eigenschaften eines Datei Handlers an. In diesem Beispiel kann der Handler eine AVI-Datei lesen und in diese schreiben.                                                                              |



 

Ein Datei Handler kann über eine oder mehrere seiner Eigenschaften verfügen, die in der Registrierung gespeichert sind. Die folgenden Konstanten geben die Eigenschaften an, die derzeit einer Datei zugeordnet sind.



| Konstante                        | BESCHREIBUNG                                                          |
|---------------------------------|----------------------------------------------------------------------|
| avifilehandler \_ canaccept-nonrgb | Gibt an, dass ein Datei Handler andere Bilddaten als RGB verarbeiten kann. |
| avifilehandler- \_ CanRead         | Gibt an, dass ein Datei Handler eine Datei mit Lesezugriff öffnen kann.      |
| avifilehandler- \_ CanWrite        | Gibt an, dass ein Datei Handler eine Datei mit Schreibzugriff öffnen kann.     |



 

Beim Erstellen eines Datei-oder streamhandlers können Sie einen neuen Bezeichner abrufen, indem Sie UUIDGEN.EXE ausführen. Verwenden Sie immer UUIDGEN.EXE, um einen neuen Bezeichner zu erstellen. Die 16-Byte-hexadezimal Zahl, die von dieser ausführbaren Datei erstellt wird, identifiziert den Handler eindeutig.

Die avifile-Bibliothek verwendet zusätzliche Einträge in der Registrierung, um einen Klassen Bezeichner auf der Grundlage der Dateierweiterung zu identifizieren, die von einem Datei Handler verarbeitet werden kann, oder einen aus vier Zeichen bestehende Code, der von einer Datei oder einem streamhandler verarbeitet werden kann Die folgenden Einträge ordnen z. b. der Dateierweiterung einen Klassen Bezeichner zu. WAV und der aus vier Zeichen bestehende Code "Wave":


```C++
[HKEY_CLASSES_ROOT\AVIFile\Extensions\WAV] 
@="{00010023-0000-0000-C000-000000000046}" 
[HKEY_CLASSES_ROOT\AVIFile\RIFFHandlers\WAVE] 
@="{00010023-0000-0000-C000-000000000046}" 
 
```



Diese Einträge bestehen aus den folgenden Teilen:



| Teil                                   | BESCHREIBUNG                                                                                       |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| HKEY- \_ Klassen Stamm \_                    | Identifiziert den Stamm Eintrag der Registrierung.                                                        |
| Avifile                                | Identifiziert diesen Eintrag als einen von avifile verwendeten Eintrag.                                                |
| Erweiterungen                             | Gibt die Dateierweiterung an (in diesem Beispiel. WAV), die von einem Datei Handler verarbeitet werden kann.             |
| Riffhandlers                           | Gibt den aus vier Zeichen bestehende Code (in diesem Beispiel "Wave") an, der von einem Datei-oder streamhandler verarbeitet werden kann. |
| {00010023-0000-0000-C000-000000000046} | Gibt einen Schnittstellen Bezeichner (IID) oder einen Klassen Bezeichner an.                                      |



 

Wenn Sie Ihren Stream oder Datei Handler ohne Setup Anwendung verteilen, um ihn im System des Benutzers zu installieren, müssen Sie einen einschließen. REG-Datei, sodass der Benutzer den Handler installieren kann. Der Benutzer verwendet den Registrierungs-Editor, um Registrierungseinträge für den Stream oder Datei Handler zu erstellen.

Das folgende Beispiel zeigt den Inhalt eines typischen. REG-Datei. Der erste Eintrag im folgenden Beispiel ist die beschreibende Zeichenfolge für den-Handler. Der zweite Eintrag identifiziert die Datei, die den Handler enthält. Mit dem dritten Eintrag werden die Eigenschaften des Datei Handlers (in diesem Fall Schreib geschützter Zugriff auf Dateien) identifiziert. Der vierte Eintrag ordnet den Typ der Datei zu, die der Handler verarbeitet (in diesem Falldateien mit einem. JPG-Dateinamenerweiterung) mit dem Klassen Bezeichner.


```C++
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}] 
@="JFIF (JPEG) Files" 
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}]\InprocServer32] 
@="jfiffile.dll" 
[HKEY_CLASSES_ROOT\AVIFile\Extensions\JPG] 
@="{5C2B8200-E2C8-1068-B1CA-6066188C6002}" 
 
```



Wenn Sie diese Datei erstellen, speichern Sie Sie mit. REG-Erweiterung, um Sie als Update Datei für die Registrierung zu identifizieren. Ersetzen Sie außerdem eine eindeutige IID für den 16-Byte-Code, der im Beispiel verwendet wird.

 

 




