---
description: Die Codierung mit zwei Durchgangen kann für die Codierung mit konstanter Bitrate (CONSTANT BIT Rate, CBR) und für die VBR-Codierung (Variable Bit Rate) mit einigen der Windows Mediencodecs verwendet werden.
ms.assetid: eec5085c-9441-496a-8127-cf5d2686d917
title: Verwenden Two-Pass -Codierung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58a79678e3b4396dfe87b93dfda7c9fd26487b8fdba83d2214509675ee742951
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887110"
---
# <a name="using-two-pass-encoding-microsoft-media-foundation"></a>Verwenden Two-Pass -Codierung (Microsoft Media Foundation)

Die Codierung mit zwei Durchgangen kann für die Codierung mit konstanter Bitrate (CONSTANT BIT Rate, CBR) und für die VBR-Codierung (Variable Bit Rate) mit einigen der Windows Mediencodecs verwendet werden. Sie können die maximale Anzahl von Codierungsüberläufen ermitteln, die von einem Codec unterstützt werden, indem Sie die [MFPKEY \_ PASSESRECOMMENDED-Eigenschaft](mfpkey-passesrecommendedproperty.md) abrufen. Keiner der Codecs unterstützt mehr als zwei Durchläufe. Konfigurieren Sie die DMO, um zwei Durchläufe zu verwenden, indem Sie die [MFPKEY \_ PASSESUSED-Eigenschaft](mfpkey-passesusedproperty.md) auf 2 festlegen.

Stellen Sie die Beispiele an den Encoder DMO, wie Sie es in einem 1-Pass-Modus machen würden. Wenn Sie die Eingabebeispiele für Ihren Vorverarbeitungsdurchgang verarbeiten, geben die Aufrufe von [**IMediaObject::P rocessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) oder [**FALSETransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) **S \_ FALSE** zurück, um anzugeben, dass keine Ausgabe erzeugt wird.

Am Ende des ersten Durchgangs (nachdem die letzte Eingabe zum ersten Mal verarbeitet wurde) müssen Sie dann die [MFPKEY \_ ENDOFPASS-Eigenschaft](mfpkey-endofpassproperty.md) festlegen, um den Codec zu benachrichtigen, dass die nächste verarbeitete Eingabe die erste Eingabe des zweiten Durchgangs ist. Für diese Eigenschaft ist kein Wert erforderlich, daher sollten Sie eine leere **VARIANT-Struktur** verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Media-Codecs](windows-media-codecs.md)
</dt> </dl>

 

 
