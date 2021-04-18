---
title: Unterstützung von Wasserzeichen
description: Unterstützung von Wasserzeichen
ms.assetid: 1fafb15e-57b8-4dd0-8f0c-ccf460f05157
keywords:
- Windows Media-Format-SDK, Unterstützung von Wasserzeichen
- Windows Media-Format-SDK, digitales Wasserzeichen
- Advanced Systems Format (ASF), Unterstützung von Wasserzeichen
- ASF (Advanced Systems Format), Unterstützung von Wasserzeichen
- Advanced Systems Format (ASF), digitales Wasserzeichen
- ASF (Advanced Systems Format), digitales Wasserzeichen
- Windows Media-Format-SDK, DMO
- Advanced Systems Format (ASF), DMO
- ASF (Advanced Systems Format), DMO
- Windows Media-Format-SDK, iwmwatermarkinfo-Schnittstelle
- Advanced Systems Format (ASF), iwmwatermarkinfo-Schnittstelle
- ASF (Advanced Systems Format), iwmwatermarkinfo-Schnittstelle
- Wasserzeichen, Info
- digitales Wasserzeichen
- DirectX-Medienobjekt (DMO), Informationen zu
- DMO (DirectX-Medienobjekt), Informationen zu
- Iwmwatermarkinfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417012cb165c0028e71af6f8b50052fdd2fab208
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106341705"
---
# <a name="watermarking-support"></a>Unterstützung von Wasserzeichen

Das digitale Wasserzeichen ist eine Möglichkeit, Copyright-oder sonstige Informationen in die Daten eines Medien Stroms einzubetten. Die Verfahren für die wassermarkierung variieren stark von einer Lösung zum nächsten. Die einfachste Art von Wasserzeichen ist das einfache Hinzufügen eines identifizierenden Bilds zu jedem Frame eines Videodaten Stroms. Diese Technik wird häufig von Fernsehstationen verwendet, um ein semitransparentes Logo in der unteren Ecke der Übertragung einzufügen. Anspruchsvollere Formen digitaler Wasserzeichen sind nicht wahrnehmbar für den Benutzer, der den Inhalt überwacht oder überwacht.

Das Windows Media-Format-SDK unterstützt die Verwendung digitaler Wasserzeichen- [*DMOS*](wmformat-glossary.md). In der Praxis ist ein Wasserzeichen System sehr ähnlich wie ein Codec: es nimmt Medien Beispiele an, führt Algorithmen für die Daten aus und gibt die geänderten Beispiele aus. Wenn ein Wasserzeichen System für einen Stream angegeben wird, schließt das Writer-Objekt den DMO in seine Verarbeitung von Eingabe Beispielen ein.

Sie müssen Informationen zur Wasserzeichen Konfiguration angeben, wenn Sie einen Datenstrom für das Wasserzeichen konfigurieren. Die Konfigurationswerte unterscheiden sich je nach dem Wasserzeichen DMO. Der verwendete DMO sollte Anweisungen enthalten, in denen die von ihm unterstützten Konfigurationswerte beschrieben werden.

Informationen zu den Einstellungen, die zum Angeben eines Wasserzeichen Systems verwendet werden, finden Sie unter [ **IWMWriterAdvanced2:: setinputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)

Sie können Ihre Anwendung so programmieren, dass Sie die auf dem Client Computer installierten Wasserzeichen DMOS aufzählt. Weitere Informationen finden Sie unter der [**iwmwatermarkinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo) -Schnittstelle.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktionen zum Schreiben von Dateien**](file-writing-features.md)
</dt> </dl>

 

 




