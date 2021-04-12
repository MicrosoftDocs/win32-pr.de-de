---
description: Geräte Objekt
ms.assetid: 0d403a6e-c22e-4b77-9be4-b8d53092f279
title: Geräte Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef76dbe26b1fd2c8d2bfd6da708728c9eb2177b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525910"
---
# <a name="device-object"></a>Geräte Objekt

Das Device-Objekt unterstützt die folgenden Eigenschaften. Eine Anwendung kann diese Eigenschaften anfordern, indem Sie das Stamm Objekt abfragt (wobei die definierte Objekt-ID für die **\_ Objekt- \_ \_ ID des WPD-Geräts** angegeben wird). Alle Werte des Geräte Objekts sind schreibgeschützt.

Wenn ein bestimmtes Gerät die Gerätekategorie der [WPD- \_ Funktions \_ Kategorie \_ ](wpd-functional-category-device.md) implementiert, muss es auch die Eigenschaften unterstützen, die dieser Kategorie zugeordnet sind.



| Eigenschaftsname                                                                                                         | Erforderlich oder optional                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [WPD- \_ Objekt- \_ ID](object-properties.md)                                                                | Erforderlich. Der Wert ist die **WPD- \_ Geräte \_ Objekt- \_ ID**.                                                         |
| [übergeordnete WPD- \_ Objekt- \_ \_ ID](object-properties.md)                                                 | Erforderlich. Der Wert ist eine leere Zeichenfolge.                                                                     |
| [WPD- \_ Objekt \_ Name](object-properties.md)                                                            | Erforderlich, wenn das-Objekt eine Datei darstellt.                                                                   |
| [\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt](object-properties.md)                          | Erforderlich.                                                                                                   |
| [WPD- \_ Objekt \_ IsHidden](object-properties.md)                                                    | Erforderlich, wenn das Geräte Objekt dem Benutzer nicht angezeigt werden soll.                                              |
| [Verweise auf WPD- \_ Objekte \_](object-properties.md)                                                | Erforderlich, wenn das Geräte Objekt Verweise auf andere Objekte hat.                                              |
| [WPD- \_ Objekt \_ Schlüsselwörter](object-properties.md)                                                    | Dies ist optional.                                                                                                   |
| [WPD- \_ Objekt \_ Synchronisierungs- \_ ID](object-properties.md)                                                     | Dies ist optional.                                                                                                   |
| [WPD \_ - \_ Objekt \_ generieren \_ der Miniaturansicht aus der \_ Ressource](object-properties.md) | Dies ist optional.                                                                                                   |
| [WPD- \_ Geräte \_ Synchronisierungs \_ Partner](device-properties.md)                                           | Dies ist optional.                                                                                                   |
| [Version der WPD- \_ Geräte \_ Firmware \_](device-properties.md)                                   | Erforderlich.                                                                                                   |
| [\_ \_ Energie \_ Pegel des WPD-Geräts](device-properties.md)                                             | Empfohlen, wenn das Gerät über einen Akku verfügt.                                                                    |
| [WPD \_ - \_ Geräte \_ Stromquelle](device-properties.md)                                           | Empfohlen.                                                                                                |
| [WPD- \_ Geräte \_ Protokoll](device-properties.md)                                                    | Empfohlen.                                                                                                |
| [WPD- \_ Geräte \_ Hersteller](device-properties.md)                                            | Erforderlich.                                                                                                   |
| [WPD- \_ Geräte \_ Modell](device-properties.md)                                                          | Erforderlich.                                                                                                   |
| [\_ \_ Serien \_ Nummer des WPD-Geräts](device-properties.md)                                         | Erforderlich.                                                                                                   |
| [WPD- \_ Gerät \_ unterstützt \_ nicht \_ verwendbar](device-properties.md)                    | Erforderlich, wenn das Gerät nicht verwendbare Objekte unterstützt. Das heißt, wenn Sie für die einfache Datenspeicherung verwendet werden kann. |
| [DateTime für WPD- \_ Gerät \_](device-properties.md)                                                    | Dies ist optional.                                                                                                   |
| [Anzeige Name des WPD- \_ Geräts \_ \_](device-properties.md)                                         | Empfohlen.                                                                                                |
| [vom WPD- \_ Gerät \_ unterstütztes \_ DRM- \_ Schema](device-properties.md)                          | Empfohlen, wenn das Gerät Digital Rights Management (DRM) unterstützt.                                         |
| [vom WPD- \_ Gerät \_ unterstützte \_ Formate \_ sind \_ geordnet](device-properties.md)       | Empfohlen, wenn das Gerät eine bevorzugte Format Anordnung unterstützt.                                               |
| [WPD \_ - \_ Gerätetyp](device-properties.md)                                                            | Empfohlen.                                                                                                |
| [eindeutige ID der WPD- \_ Geräte \_ Funktion \_ \_](device-properties.md)                          | Dies ist optional.                                                                                                   |
| [eindeutige ID des WPD- \_ Geräte \_ Modells \_ \_](device-properties.md)                                    | Dies ist optional.                                                                                                   |
| [WPD- \_ Geräte \_ Transport](device-properties.md)                                                  | Empfohlen.                                                                                                |
| [WPD- \_ Gerät \_ verwendet \_ Geräte \_ Stufe](device-properties.md)                                  | Dies ist optional.                                                                                                   |
| [WPD- \_ Funktions \_ Objekt \_ Kategorie](device-properties.md)                             | Erforderlich.                                                                                                   |



 

## <a name="typical-resources"></a>Typische Ressourcen

Diese Objekte Hosten in der Regel keine Ressourcen.

## <a name="commands"></a>Befehle

Zusätzlich zu den Eigenschaften sollten Geräte einen bestimmten Satz von Befehlen unterstützen, die von tragbaren Windows-Geräten definiert werden. Welche Befehle ein Objekt oder ein Gerät unterstützt, hängt vom Typ, der Funktionalität und den Funktionen ab.

In der folgenden Tabelle werden die Befehls Klassen beschrieben, die auf Geräte angewendet werden. In der Regel fällt ein Gerät unter mehrere Kategorien und sollte die Befehle für alle anwendbaren Kategorien unterstützen. Beispielsweise würde ein Mobiltelefon mit einer Kamera in drei Kategorien unterteilt: alle Geräte, SMS-Geräte und noch Abbild Erfassungsgeräte. Ein benutzerdefinierter Treiber und eine Client Anwendung können zusätzliche Befehle oder Eigenschaften unterstützen, die Sie definieren, aber die folgenden Befehle müssen unterstützt werden. Eine Beschreibung der spezifischen Befehle, die unter jede Befehls Kategorie fallen, finden Sie unter [Befehle](commands.md).



| BESCHREIBUNG                                                                                                                                                                                                                      | Befehls Kategorien                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Alle Geräte.                                                                                                                                                                                                                     | **Kategorie der Kategorie " \_ Kategorie \_ capabilitieswpd" \_ in WPD \_**<br/> **WPD \_ - \_ kategorieobjektenumeration \_**<br/> **WPD- \_ Kategorie \_ Objekt \_ Verwaltung**<br/> **\_ \_ Objekt \_ Eigenschaften der WPD-Kategorie**<br/> **WPD \_ - \_ kategorieobjekteigenschaften \_ \_ Bulk**<br/> **\_ \_ Objekt \_ Ressourcen für WPD-Kategorie**<br/> |
| Geräte, auf denen weiterhin Images, z. b. digitale Kameras, erfasst werden können.                                                                                                                                                                  | **WPD- \_ Kategorie \_ trotzdem \_ Image \_ Erfassung**                                                                                                                                                                                                                                                                                   |
| Geräte, die SMS (Short Message Service)-Nachrichten (z. b. Mobiltelefone) senden können. Das Senden von SMS-Nachrichten wird häufig als "Text Messaging" bezeichnet.                                                                                      | **WPD- \_ Kategorie \_ SMS**                                                                                                                                                                                                                                                                                                     |
| Geräte, die als Speichergeräte fungieren. Dies schließt externe Laufwerke ein. Wenn ein Gerät die Möglichkeit unterstützt, einen Speicher zu formatieren oder Objekte von einem Speicherort auf einen anderen zu verschieben, sollte der Treiber diese Kategorie unterstützen.<br/> | **WPD \_ - \_ kategoriespeicher**                                                                                                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anforderungen für Objekte**](requirements-for-objects.md)
</dt> </dl>

 

 




