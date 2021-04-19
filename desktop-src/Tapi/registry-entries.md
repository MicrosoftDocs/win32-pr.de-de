---
description: Die austauschbaren Terminals werden in Terminal SuperClasses klassifiziert.
ms.assetid: 0ab2896e-3634-47f7-b1f4-e7d1ffcb3592
title: Registrierungseinträge (telefonieapi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035126f614e526f3b1557f5323d52b3bf6b2b12c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357125"
---
# <a name="registry-entries-telephony-api"></a>Registrierungseinträge (telefonieapi)

Die austauschbaren Terminals werden in Terminal SuperClasses klassifiziert. Jede Terminal Superclass verfügt über einen Eintrag in der Registrierung unter folgendem Schlüssel:

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Telefonie** \\ **Terminalmanager**

Unter dem Schlüssel "Terminal Superclass" finden Sie Einträge für jedes austauschbare Terminal innerhalb der Terminal-Superclass.

Der Eintrag für jede Terminal Superclass wird durch eine Terminal-Superclass-CLSID identifiziert. Dies ist ein eindeutiger Bezeichner für eine Terminal Klasse. Die Terminal Klasse verfügt über ein optionales Attribut: Name, bei dem es sich um einen anzeigen Amen für die Terminal Klasse handelt. Jedes austauschbare Terminal wird durch eine CLSID-Terminal Klasse identifiziert. Das heißt, eine GUID. Die Attribute für austauschbares Terminal werden in austauschbaren Terminal Schlüsselwerten gespeichert. Die Attribute für ein austauschbares Terminal sind die folgenden.



| Terminal Klasse | Schlüsselname | Öffentlicher Bezeichner                                                                 |
|----------------|----------|-----------------------------------------------------------------------------------|
| Name           | REG- \_ SZ  | Anzeige Name für das Terminal                                                            |
| Company        | REG- \_ SZ  | Unternehmensname                                                                      |
| Version        | REG- \_ SZ  | Versionsinformationen                                                               |
| CLSID          | REG- \_ SZ  | Terminal-CLSID (in com [**cokreatumstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode verwendet) |
| Wegbeschreibungen     | DWORD    | Terminal Richtung                                                                |
| MediaTypes     | DWORD    | Unterstützte Terminal Medientypen                                                    |



 

Bei einer Terminal Klasse sind die Attribute wie folgt.



| CLSID | Schlüsselname | Öffentlicher Bezeichner            |
|-------|----------|------------------------------|
| Name  | REG- \_ SZ  | Anzeige Name der Terminal Klasse |



 

 

 
