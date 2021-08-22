---
description: Konfigurieren der Audiodecodierung
ms.assetid: 362bd3bc-1474-4132-a8a8-e5dc0bba80e7
title: Konfigurieren der Audiodecodierung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee274fd714065a1c89c9d634dd80de4d59c9eb567d67ed8045d2b89bece87d74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664644"
---
# <a name="configuring-audio-decoding-microsoft-media-foundation"></a>Konfigurieren der Audiodecodierung (Microsoft Media Foundation)

Das Decodieren Windows Medienaudioinhalts ist viel einfacher als das Codieren. Legen Sie nach dem Erstellen eines Audiodecoderobjekts den Eingabetyp fest, indem Sie die **IMediaObject::SetInputType-** oder **DIENStransform::SetInputType-Methode** verwenden. Der Medientyp, den Sie für die Decodereingabe verwenden, muss mit dem Ausgabetyp übereinstimmen, der verwendet wurde, als der Inhalt codiert wurde. Dies schließt die erweiterten Formatdaten ein, die an die **WAVEFORMATEX-Struktur angefügt** werden. Sie müssen sicherstellen, dass diese Daten korrekt sind, da der Decoder keine Stichproben ohne sie verarbeiten kann.

Nach dem Festlegen des Eingabetyps können Sie alle Decoderfunktionen konfigurieren, die Sie verwenden möchten. Decoderfeatures, wie sie für die Codierung verwendet werden, werden mithilfe der Methoden **von IPropertyBag** oder **IPropertyStore festgelegt.**

Nachdem der Eingabetyp festgelegt wurde und alle Decoderfeatures konfiguriert wurden, können Sie die vom Decoder unterstützten Ausgabetypen aufzählen, indem Sie **IMediaObject::GetOutputType** oder **EINETRANSFORM::GetOutputType** aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Audio](workingwithaudio.md)
</dt> </dl>

 

 



