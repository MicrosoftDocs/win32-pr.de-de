---
description: Geräteobjekt
ms.assetid: 0d403a6e-c22e-4b77-9be4-b8d53092f279
title: Geräteobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5279f63c7dabd8bd5b523d9234e33a60d9cf05608ac7b3f1b7601fd8c25024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083614"
---
# <a name="device-object"></a>Geräteobjekt

Das Geräteobjekt unterstützt die folgenden Eigenschaften. Eine Anwendung kann diese Eigenschaften anfordern, indem sie das Stammobjekt abfragt (unter Angabe der definierten **WPD \_ DEVICE OBJECT \_ \_ ID** konstanten Objekt-ID). Alle Werte des Geräteobjekts sind schreibgeschützt.

Wenn ein bestimmtes Gerät die [KATEGORIE WPD \_ FUNCTIONAL CATEGORY \_ \_ DEVICE](wpd-functional-category-device.md) implementiert, muss es auch die Eigenschaften unterstützen, die dieser Kategorie zugeordnet sind.



| Eigenschaftsname                                                                                                         | Erforderlich oder optional                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [\_WPD-OBJEKT-ID \_](object-properties.md)                                                                | Erforderlich. Der Wert ist **WPD \_ DEVICE OBJECT \_ \_ ID**.                                                         |
| [ÜBERGEORDNETE ID DES \_ \_ WPD-OBJEKTS \_](object-properties.md)                                                 | Erforderlich. Der Wert ist eine leere Zeichenfolge.                                                                     |
| [\_WPD-OBJEKTNAME \_](object-properties.md)                                                            | Erforderlich, wenn das -Objekt eine Datei darstellt.                                                                   |
| [PERSISTENTE EINDEUTIGE ID \_ DES WPD-OBJEKTS \_ \_ \_](object-properties.md)                          | Erforderlich.                                                                                                   |
| [\_WPD-OBJEKT \_ ISHIDDEN](object-properties.md)                                                    | Erforderlich, wenn das Geräteobjekt dem Benutzer nicht angezeigt werden soll.                                              |
| [\_ \_ WPD-OBJEKTVERWEISE](object-properties.md)                                                | Erforderlich, wenn das Geräteobjekt Verweise auf andere Objekte enthält.                                              |
| [\_WPD-OBJEKTSCHLÜSSELWÖRTER \_](object-properties.md)                                                    | Optional.                                                                                                   |
| [\_ \_ WPD-OBJEKTSYNCHRONISIERUNGS-ID \_](object-properties.md)                                                     | Optional.                                                                                                   |
| [\_WPD-OBJEKT \_ GENERIERT \_ \_ MINIATURANSICHT AUS \_ RESSOURCE](object-properties.md) | Optional.                                                                                                   |
| [\_ \_ WPD-GERÄTESYNCHRONISIERUNGSPARTNER \_](device-properties.md)                                           | Optional.                                                                                                   |
| [\_ \_ WPD-GERÄTEFIRMWAREVERSION \_](device-properties.md)                                   | Erforderlich.                                                                                                   |
| [\_ \_ \_ WPD-GERÄTELEISTUNGSSTUFE](device-properties.md)                                             | Empfohlen, wenn das Gerät über einen Akku verfügt.                                                                    |
| [\_ \_ WPD-GERÄTESTROMQUELLE \_](device-properties.md)                                           | Empfohlen.                                                                                                |
| [\_WPD-GERÄTEPROTOKOLL \_](device-properties.md)                                                    | Empfohlen.                                                                                                |
| [\_WPD-GERÄTEHERSTELLER \_](device-properties.md)                                            | Erforderlich.                                                                                                   |
| [\_WPD-GERÄTEMODELL \_](device-properties.md)                                                          | Erforderlich.                                                                                                   |
| [\_ \_ WPD-GERÄTESERIENNUMMER \_](device-properties.md)                                         | Erforderlich.                                                                                                   |
| [\_WPD-GERÄT \_ UNTERSTÜTZT NICHT \_ VERWENDBARE \_ GERÄTE](device-properties.md)                    | Erforderlich, wenn das Gerät nicht gebrauchsbare Objekte unterstützt. Das heißt, wenn es für die einfache Datenspeicherung verwendet werden kann. |
| [WPD \_ DEVICE \_ DATETIME](device-properties.md)                                                    | Optional.                                                                                                   |
| [\_WPD-GERÄTE-FRIENDLY \_ \_ NAME](device-properties.md)                                         | Empfohlen.                                                                                                |
| [VOM \_ WPD-GERÄT \_ \_ UNTERSTÜTZTES DRM-SCHEMA \_](device-properties.md)                          | Empfohlen, wenn das Gerät Digital Rights Management (DRM) unterstützt.                                         |
| [VOM \_ \_ WPD-GERÄT \_ UNTERSTÜTZTE FORMATE \_ WERDEN \_ GEORDNET.](device-properties.md)       | Empfohlen, wenn das Gerät die bevorzugte Formatbestellung unterstützt.                                               |
| [\_WPD-GERÄTETYP \_](device-properties.md)                                                            | Empfohlen.                                                                                                |
| [WPD \_ DEVICE \_ FUNCTIONAL \_ UNIQUE \_ ID](device-properties.md)                          | Optional.                                                                                                   |
| [EINDEUTIGE ID \_ DES WPD-GERÄTEMODELLS \_ \_ \_](device-properties.md)                                    | Optional.                                                                                                   |
| [\_WPD-GERÄTETRANSPORT \_](device-properties.md)                                                  | Empfohlen.                                                                                                |
| [WPD \_ DEVICE \_ USE \_ DEVICE \_ STAGE](device-properties.md)                                  | Optional.                                                                                                   |
| [WPD \_ FUNCTIONAL \_ OBJECT \_ CATEGORY](device-properties.md)                             | Erforderlich.                                                                                                   |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte hosten in der Regel keine Ressourcen.

## <a name="commands"></a>Befehle

Zusätzlich zu den Eigenschaften sollten Geräte einen bestimmten Satz von Befehlen unterstützen, die von portierbaren Windows definiert werden. Welche Befehle ein Objekt oder Gerät unterstützt, hängt vom Typ, der Funktionalität und den Funktionen ab.

In der folgenden Tabelle werden die Befehlsklassen beschrieben, die für Geräte nach Funktionalität gelten. In der Regel fällt ein Gerät in mehrere Kategorien und sollte die Befehle für alle anwendbaren Kategorien unterstützen. Beispielsweise würde ein Mobiltelefon mit einer Kamera in drei Kategorien fallen: alle Geräte, SMS-Geräte und Noch-Bilderfassungsgeräte. Ein benutzerdefinierter Treiber und eine Clientanwendung können zusätzliche Befehle oder Eigenschaften unterstützen, die Sie definieren, müssen jedoch die folgenden Befehle unterstützen. Eine Beschreibung der spezifischen Befehle, die unter die einzelnen Befehlskategorien fallen, finden Sie unter [Befehle](commands.md).



| Beschreibung                                                                                                                                                                                                                      | Befehlskategorien                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Alle Geräte.                                                                                                                                                                                                                     | **WPD \_ CATEGORY \_ CAPABILITIESWPD \_ CATEGORY \_ COMMON**<br/> **WPD \_ CATEGORY \_ OBJECT \_ ENUMERATION**<br/> **WPD \_ CATEGORY \_ OBJECT \_ MANAGEMENT**<br/> **WPD \_ CATEGORY \_ OBJECT \_ PROPERTIES**<br/> **WPD \_ CATEGORY \_ OBJECT \_ PROPERTIES \_ BULK**<br/> **WPD \_ CATEGORY \_ OBJECT \_ RESOURCES**<br/> |
| Geräte, die Stillbilder erfassen können, z. B. Digitalkameras.                                                                                                                                                                  | **WPD \_ CATEGORY \_ STILL \_ IMAGE \_ CAPTURE**                                                                                                                                                                                                                                                                                   |
| Geräte, die SMS-Nachrichten (Short Message Service) senden können, z. B. Mobiltelefone. Das Senden von SMS-Nachrichten wird häufig als "SMS" bezeichnet.                                                                                      | **WPD \_ CATEGORY \_ SMS**                                                                                                                                                                                                                                                                                                     |
| Geräte, die als Speichergeräte funktionieren. Dazu gehören externe Laufwerke. Wenn ein Gerät die Möglichkeit unterstützt, einen Speicher zu formatieren oder Objekte von einem Standort an einen anderen zu verschieben, sollte Ihr Treiber diese Kategorie unterstützen.<br/> | **WPD \_ CATEGORY \_ STORAGE**                                                                                                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 




