---
description: Decodereinstellungen für Windows Media Center Edition
ms.assetid: 019b063f-f215-44d8-a916-3125bee6af93
title: Decodereinstellungen für Windows Media Center Edition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f66b5107fa0316f6ce2547e1f5f066165ed598
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106363889"
---
# <a name="decoder-settings-for-windows-media-center-edition"></a>Decodereinstellungen für Windows Media Center Edition

Windows XP Media Center Edition 2005 und höher verwendet die [**icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) -Schnittstelle, um den audiodecoderfilter für die Fernseh-und DVD-Wiedergabe zu konfigurieren. Die folgenden Eigenschaften werden unterstützt.



| Eigenschaften-GUID                   | BESCHREIBUNG                                      |
|---------------------------------|--------------------------------------------------|
| codecapi \_ - \_ audioausgabeformat \_ | Konfiguriert das audioausgabeformat. Siehe Hinweise. |



 

## <a name="remarks"></a>Bemerkungen

Der Wert der Eigenschaft codecapi \_ - \_ audioausgabeformat \_ ist eine Zeichen folgen Darstellung einer GUID, die als **BSTR** -Wert gespeichert wird. Die folgenden GUIDs sind definiert.



| GUID                                                        | Beschreibung                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| codecapi \_ - \_ audioausgabeformat \_ \_ PCM \_ Stereo \_ matrixencoded | Der Software Audiofilter sollte das Decodieren von Software und das Ausgeben eines Stereo-Audiostreams durchführen, wobei die Multichannel-Audiomatrix auf die beiden Kanäle codiert ist.                                                   |
| codecapi \_ - \_ audioausgabeformat \_ \_ PCM \_ Stereo                | Der Software-Audiofilter sollte Software Decodierung durchführen und einen Stereo-Audiostream ausgeben.                                                                                                                   |
| codecapi \_ - \_ audioausgabeformat \_ \_ SPDIF \_ PCM                 | Der Software Audiofilter sollte Software-Audiodecodierung durchführen, auch wenn die physische Ausgabe des PCs eine digitale Schnittstelle sein kann, z. b. S/PDIF.                                                      |
| codecapi \_ - \_ audioausgabeformat \_ \_ SPDIF \_ Bitstream           | Der softwareupdateifilter sollte keine Software-Audiodecodierung durchführen, sondern den unformatierten, digitalen audiopstream für die externe Verarbeitung durch ein Gerät übergeben, das mit einem digitalen audiolink verbunden ist, z. b. S/PDIF |
| codecapi \_ - \_ audioausgabeformat \_ \_ PCM- \_ Kopfhörer            | Der Software Audiofilter sollte Software-Audiodecodierung durchführen und die proprietäre Verarbeitung anwenden, um für Kopfhörer zu optimieren. Die Unterstützung für diese Einstellung ist optional.                                     |



 

> [!Note]  
> Die **icodecapi** -Schnittstelle speichert Codec-Eigenschaften als Schlüssel-Wert-Paare, wobei der Schlüssel eine GUID und der Wert ein **Variant** -Typ ist.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Encoder-und decoderentwicklung](encoder-and-decoder-development.md)
</dt> </dl>

 

 



