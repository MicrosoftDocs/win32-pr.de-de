---
description: Allgemeine Registrierungseinträge
ms.assetid: 6a140c7f-df8c-4a8e-9e4d-dbb38901e14f
title: Allgemeine Registrierungseinträge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7c3514adcc0aeaaf9adadd2b71dfdffcd8d408
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373147"
---
# <a name="general-registry-entries"></a>Allgemeine Registrierungseinträge


Die folgenden Registrierungseinträge müssen für den Decoder und den Encoder separat erstellt werden:

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Encoder/Decoder CLSID}
         Author = Author's Name
         Description = Your Codec Description
         DeviceManufacturer = Manufacturer's Name
         DeviceModels = Device,Device
         FriendlyName = Codec Friendly Name
         Date = mm-dd-yyyy
         Vendor = {GUID_Vendor}
         ContainerFormat = {GUID_ContainerFormat}
         Version = Major.Minor.Build.Number
         SpecVersion = Major.Minor.Build.Number
         MimeTypes = Your Mime Type
         SupportAnimation = 0|1
         SupportChromakey = 0|1
         SupportLossless = 0|1
         SupportMultiframe = 0|1
         Formats
            {Supported PixelFormat GUID 1}
            {Supported PixelFormat GUID ...}
            {Supported PixelFormat GUID N}
         ArbitrationPriority  = 0-10
```

Die Einträge FriendlyName, VendorGUID, Containerformat, mimeTypes, File Extensions und Formats sind erforderlich. Alle anderen sind optional.

Beachten Sie, dass die Einträge "de vicemanufakturer" und "DeviceModels" spezifisch für Rohdaten-Codecs sind und sich auf den Kamerahersteller und die Kameramodelle beziehen, auf die der Codec anwendbar ist. Die spec-Version ist die Version der Abbild Format Spezifikation, der der Codec entspricht. Der-Format Eintrag gibt die Pixel Formate an, die vom Codec unterstützt werden. Ein Codec unterstützt möglicherweise mehr als ein Pixel Format. In diesem Fall würden Sie mehrere Schlüssel unter HKEY \_ Classes \_ root \\ CLSID \\ {Encoder/Decoder CLSID} Formats eingeben \\ .

## <a name="arbitrationpriority"></a>Arbitrationpriority

Ab Windows 8 ist arbitrationpriority ein neuer Registrierungs Eintrag. Gültige Werte sind 0 bis 10. Wenn der Schlüssel arbitrationpriority vorhanden ist, weist der Wert dieses Schlüssels WIC an, den zugeordneten Codec hinter allen anderen Codecs mit einem niedrigeren arbitrationpriority-Wert zu priorisieren. Diese Auswertung erfolgt vor dem Auftreten der vorhandenen WIC-Codec-Schiedsgerichtsbarkeit und stellt sicher, dass der zugehörige Codec unter jedem konkurrierenden Codec priorisiert wird, auch wenn er als oder besser geeignet ist. Jeder Codec, der keinen expliziten arbitrationpriority-Wert besitzt, der in der Registrierung definiert ist, erhält standardmäßig die Priorität 0.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Codec-Installation und-Registrierung](-wic-codecinstallandreg.md)
</dt> <dt>

[Codierungs spezifische Registrierungseinträge](-wic-encoderregentries.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[**Funktionsweise der Windows Imaging-Komponente: Codec-Ermittlung und-Vermittlung**](-wic-howwicworks.md)
</dt> </dl>

 

 



