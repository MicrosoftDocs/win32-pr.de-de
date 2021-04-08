---
title: Hinzufügen von Metadaten zu konvertierten Dateien
description: Hinzufügen von Metadaten zu konvertierten Dateien
ms.assetid: 97588651-23de-43ab-b884-76d8af95ab93
keywords:
- Windows Media Player, Konvertierungsprozess
- Windows Media Player-Plug-ins, Konvertierung
- Plug-ins, Konvertierung
- Konvertierungs-Plug-ins, Hinzufügen von Metadaten zu konvertierten Dateien
- Hinzufügen von Metadaten zu konvertierten Dateien
- Metadaten, hinzufügen zu konvertierten Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4ae47318089149564f64832c95e4cee1b27f26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727736"
---
# <a name="adding-metadata-to-converted-files"></a>Hinzufügen von Metadaten zu konvertierten Dateien

Konvertierte Dateien müssen bestimmte Metadaten enthalten, um eine gute Benutzer Leistung sicherzustellen. Konvertierte Dateien müssen mindestens die in den [Windows Media Metadata Usage Guidelines](/previous-versions/ms867702(v=msdn.10))aufgeführten primären Attribute enthalten.

Legen Sie für Musikdateien den Wert für **WM/mediaclassprimaryid** auf D1607DBC-E323-4BE2-86A1-48A42A28441E fest.

Legen Sie für Voicemaildateien den Wert für **WM/mediaclassprimaryid** auf 01cd0f29-da4e-4157-897b-6275d50c4f11 fest. Hierbei handelt es sich um die primäre Klassen-GUID für Audiodateien. Legen Sie den Wert für **WM/MediaClassSecondaryID** auf 193c8824-4d52-4178-90bd-305240b04636 fest.

Legen Sie für Sprachnotizen den Wert für **WM/mediaclassprimaryid** auf 01cd0f29-da4e-4157-897b-6275d50c4f11 fest. Legen Sie den Wert für **WM/MediaClassSecondaryID** auf 3a172 A13-2bd9-4831-835b-114f6a95943f fest.

Legen Sie den Wert für **WM/contentdistributor** auf den Schlüsselnamen für den Musikdienst fest, der den Inhalt bereitgestellt hat.

Legen Sie den Wert für **WM/UniqueFileIdentifier** auf die Inhalts-ID fest. Auf diese Weise können Sie bestimmte Inhaltselemente zu einem späteren Zeitpunkt abrufen.

Legen Sie einen Wert für **WM/wmshadowfilesourcefiletype** fest.

Verwenden Sie für geschützten Inhalt das SDK für das Windows Media-Format, um das DRM-Attribut " **\_ drmHeader \_ contentid** " auf die Inhalts-ID festzulegen.

Legen Sie für geschützten Inhalt einen Wert für **WM/wmshadowfilesourcedrmtype** fest.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Konvertierungs-Plug-ins**](about-conversion-plug-ins.md)
</dt> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 