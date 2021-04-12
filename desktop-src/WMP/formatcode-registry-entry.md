---
title: Registrierungs Eintrag "Formatcode"
description: Registrierungs Eintrag "Formatcode"
ms.assetid: cc444eaa-6898-48ab-9573-9e7d5e25d6db
keywords:
- Windows Media Player, Formatcode-Registrierungseinträge
- Windows Media Player, Dateinamen Erweiterungen
- Windows Media Player, Registrierung
- Registrierung, Dateinamen Erweiterungen
- Registrierung, Formatcode-Einträge
- Registrierung, Einstellungen für Windows-Media Player
- Registrierungs Einstellungen für die Dateinamenerweiterung
- Formatcode-Registrierungseinträge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2318d32e9d7a08a2ae23b24e7acd2674b9eecb2
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104208735"
---
# <a name="formatcode-registry-entry"></a>Registrierungs Eintrag "Formatcode"

Wenn Windows Media Player auf eine benutzerdefinierte Dateierweiterung trifft, sucht es nach einem Registrierungs Unterschlüssel, der der Erweiterung entspricht. Der Unterschlüssel wird in [Registrierungs Einstellungen für Dateinamen Erweiterungen](file-name-extension-registry-settings.md)beschrieben. Einer der Registrierungseinträge, der unter dem Unterschlüssel der Erweiterung angezeigt werden kann, ist der **Formatcode** -Eintrag.

Der Registrierungs Eintrag **Formatcode** gibt den MTP-Format Code (Media Transport Protocol) für Dateien an, die über die benutzerdefinierte Erweiterung verfügen. Der Registrierungs Eintrag " **Formatcode** " weist die folgende Form auf:



| Name       | type           | Wert                                                             |
|------------|----------------|-------------------------------------------------------------------|
| Formatcode | **REG \_ DWORD** | Eine positive 16-Bit-Ganzzahl, die das Format der Datei angibt. |



 

Wenn der Benutzer versucht, eine digitale Mediendatei mit einer benutzerdefinierten Dateinamenerweiterung auf ein tragbares Gerät zu kopieren, sucht Windows Media Player in der Registrierung nach einem Format Code, der der benutzerdefinierten Dateinamenerweiterung zugeordnet ist. Wenn Windows Media Player einen Format Code findet, verwendet er MTP, um zu bestimmen, ob das Gerät das benutzerdefinierte Dateiformat unterstützt. Wenn das Gerät das-Format unterstützt, wird die Mediendatei ohne transcoded auf das Gerät kopiert.

Ein Gerät, das MTP unterstützt, kann Windows-Media Player mit einem deviceInfo-DataSet bereitstellen, das unter anderem eine Liste der vom Gerät unterstützten Formatcodes enthält.

Wenn Sie gerade ein benutzerdefiniertes Dateiformat entwickeln, können Sie einen Format Code von Microsoft anfordern. Informationen zum Anfordern eines Formatierungscodes finden Sie im Microsoft Media Transport Protocol Porting Kit, das im [Microsoft Windows Media Developer Center](https://msdn.microsoft.com/windowsmedia/default.aspx)verfügbar ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Registrierungs Einstellungen für die Dateinamenerweiterung**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




