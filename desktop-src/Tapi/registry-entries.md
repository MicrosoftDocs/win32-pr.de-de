---
description: Die austauschbaren Terminals werden in Terminal-Superklassen klassifiziert.
ms.assetid: 0ab2896e-3634-47f7-b1f4-e7d1ffcb3592
title: Registrierungseinträge (Telefonie-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd6e4e4d91b65e3ef886fd4d2d44b571f4ac4696697aef8b8d8b2715e273e18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761167"
---
# <a name="registry-entries-telephony-api"></a>Registrierungseinträge (Telefonie-API)

Die austauschbaren Terminals werden in Terminal-Superklassen klassifiziert. Jede Terminal-Superklasse verfügt über einen Eintrag in der Registrierung unter dem folgenden Schlüssel:

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **TelefonieTerminalManager** \\ 

Unterhalb des Schlüssels Terminal superclass befinden sich Einträge für jedes austauschbare Terminal innerhalb der Terminal-Superklasse.

Der Eintrag für jede Terminal superclass wird durch eine Terminal Superclass CLSID identifiziert. Dies ist ein eindeutiger Bezeichner für eine Terminalklasse. Die Terminalklasse verfügt über ein optionales Attribut: name. Dies ist ein Anzeigename für die Terminalklasse. Jedes austauschbare Terminal wird durch eine CLSID-Terminalklasse identifiziert. d.h. eine GUID. Die Attribute für austauschbares Terminal werden in austauschbaren Terminalschlüsselwerten gespeichert. Die Attribute für ein austauschbares Terminal sind die folgenden:



| Terminalklasse | Schlüsselname | Öffentlicher Bezeichner                                                                 |
|----------------|----------|-----------------------------------------------------------------------------------|
| Name           | REG \_ SZ  | Anzeigename des Terminals                                                            |
| Company        | REG \_ SZ  | Unternehmensname                                                                      |
| Version        | REG \_ SZ  | Versionsinformationen                                                               |
| CLSID          | REG \_ SZ  | Terminal-CLSID (wird in der COM [**CoCreateInstance-Methode**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) verwendet) |
| Wegbeschreibungen     | DWORD    | Terminalrichtung                                                                |
| MediaTypes     | DWORD    | Unterstützte Terminalmedientypen                                                    |



 

Für eine Terminalklasse sind die Attribute die folgenden:



| CLSID | Schlüsselname | Öffentlicher Bezeichner            |
|-------|----------|------------------------------|
| Name  | REG \_ SZ  | Anzeigename der Terminalklasse |



 

 

 
