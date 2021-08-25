---
description: Allgemeine Registrierungseinträge
ms.assetid: 6a140c7f-df8c-4a8e-9e4d-dbb38901e14f
title: Allgemeine Registrierungseinträge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7420124f47f904712c7e955465b88972e77c8eeac26a6d42eca7fcb306ec158
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118033127"
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

Die Einträge FriendlyName, VendorGUID, ContainerFormat, MimeTypes, FileExtensions und Formats sind erforderlich. Alle anderen sind optional.

Beachten Sie, dass die Einträge DeviceManufacturer und DeviceModels spezifisch für Unformatierungscodecs sind und sich auf den Kamerahersteller und die Kameramodelle beziehen, auf die der Codec anwendbar ist. Die Spezifikationsversion ist die Version der Imageformatspezifikation, mit der der Codec konform ist. Der Eintrag Formate gibt die vom Codec unterstützten Pixelformate an. Ein Codec unterstützt möglicherweise mehr als ein Pixelformat. In diesem Fall geben Sie mehrere Schlüssel unter HKEY \_ CLASSES \_ ROOT \\ CLSID \\ {Encoder/Decoder CLSID}-Formate \\ ein.

## <a name="arbitrationpriority"></a>ArbitrationPriority

Ab Windows 8 ist "PanelPriority" ein neuer Registrierungseintrag. Gültige Werte sind 0 bis 10. Wenn der Schlüssel "ArbitrationPriority" vorhanden ist, weist der Wert dieses Schlüssels WIC an, den zugeordneten Codec hinter allen anderen Codecs mit einem niedrigeren Wert von "ArbitrationPriority" zu priorisieren. Diese Auswertung erfolgt, bevor die vorhandene WIC-Codec-Vermittlung erfolgt, und stellt sicher, dass der zugeordnete Codec unterhalb eines konkurrierenden Codecs priorisiert wird, auch wenn er als oder besser geeignet ist. Für jeden Codec, für den in der Registrierung kein expliziter Wert für den "ArbitrationPriority"-Wert definiert ist, wird standardmäßig Priorität 0 verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[CODEC-Installation und -Registrierung](-wic-codecinstallandreg.md)
</dt> <dt>

[Encoderspezifische Registrierungseinträge](-wic-encoderregentries.md)
</dt> <dt>

[Schreiben eines WIC-Enabled CODEC](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[**Funktionsweise der Windows Imaging-Komponente: Codecermittlung und Vermittlung**](-wic-howwicworks.md)
</dt> </dl>

 

 



