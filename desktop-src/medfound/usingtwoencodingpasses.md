---
description: Die zwei-Pass-Codierung kann für die Konstante Bitrate (CBR) und für die Codierung der Variablen Bitrate (VBR) mit einigen Windows Media-Codecs verwendet werden.
ms.assetid: eec5085c-9441-496a-8127-cf5d2686d917
title: Verwenden von Two-Pass Encoding (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993af0015452db410b5a9f2c13233566fc17a3a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356889"
---
# <a name="using-two-pass-encoding-microsoft-media-foundation"></a>Verwenden von Two-Pass Encoding (Microsoft Media Foundation)

Die zwei-Pass-Codierung kann für die Konstante Bitrate (CBR) und für die Codierung der Variablen Bitrate (VBR) mit einigen Windows Media-Codecs verwendet werden. Sie können die maximale Anzahl von Codierungs Durchläufen ermitteln, die von einem Codec unterstützt werden, indem Sie die Eigenschaft " [mfpkey \_ passesrecommended](mfpkey-passesrecommendedproperty.md) " abrufen. Keines der Codecs unterstützt mehr als zwei Durchgänge. Konfigurieren Sie den DMO so, dass zwei Durchgänge verwendet werden, indem Sie die Eigenschaft " [ \_ passesused" für mfpkey](mfpkey-passesusedproperty.md) auf 2

Übermitteln Sie die Beispiele für den Encoder DMO nacheinander, wie Sie es in einem Modus mit nur einem Durchlauf tun würden. Wenn Sie die Eingabe Beispiele für den Vorverarbeitungs Durchlauf verarbeiten, werden bei Aufrufen von [**imediaobject::P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) oder [**imftransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) **S \_ false** zurückgegeben, um anzugeben, dass keine Ausgabe erzeugt wird.

Am Ende der ersten Ausführung (nachdem die letzte Eingabe zum ersten Mal verarbeitet wurde) müssen Sie die Eigenschaft " [mfpkey \_ endofpass](mfpkey-endofpassproperty.md) " so festlegen, dass der Codec benachrichtigt wird, dass die nächste verarbeitete Eingabe die erste Eingabe des zweiten bestanden ist. Für diese Eigenschaft ist kein Wert erforderlich. Daher sollten Sie eine leere **Variant** -Struktur verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Media-Codecs](windows-media-codecs.md)
</dt> </dl>

 

 
