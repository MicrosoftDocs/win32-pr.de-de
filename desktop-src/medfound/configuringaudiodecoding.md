---
description: Konfigurieren der Audiodecodierung
ms.assetid: 362bd3bc-1474-4132-a8a8-e5dc0bba80e7
title: Konfigurieren der Audiodecodierung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da4d6a9d41b5c504ff60f25db20265072218caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749329"
---
# <a name="configuring-audio-decoding-microsoft-media-foundation"></a>Konfigurieren der Audiodecodierung (Microsoft Media Foundation)

Das Decodieren Windows Media Audio Inhalts ist viel einfacher als das Codieren. Legen Sie nach dem Erstellen eines audiodecoderobjekts den Eingabetyp mithilfe der **imediaobject:: setinputtype** -Methode oder der **IMF Transform:: setinputtype** -Methode fest. Der Medientyp, den Sie für die Decoder-Eingabe verwenden, muss dem Ausgabetyp entsprechen, der beim Codieren des Inhalts verwendet wurde. Dies schließt die erweiterten Formatierungsdaten ein, die an die **WaveFormatEx** -Struktur angehängt werden. Sie müssen sicherstellen, dass diese Daten korrekt sind, da der Decoder keine Stichproben verarbeiten kann.

Nachdem Sie den Eingabetyp festgelegt haben, können Sie alle Decoder-Funktionen konfigurieren, die Sie verwenden möchten. Decoderfeatures, wie z. b. die für die Codierung verwendeten, werden mithilfe der Methoden von **IPropertyBag** oder **IPropertyStore** festgelegt.

Nachdem der Eingabetyp festgelegt und alle Decoder-Funktionen konfiguriert wurden, können Sie die vom Decoder unterstützten Ausgabetypen auflisten, indem Sie **imediaobject:: getoutputtype** oder **imftransform:: getoutputtype** aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Audiodaten](workingwithaudio.md)
</dt> </dl>

 

 



