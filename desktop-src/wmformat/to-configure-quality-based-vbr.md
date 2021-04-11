---
title: So konfigurieren Sie Quality-Based VBR
description: So konfigurieren Sie Quality-Based VBR
ms.assetid: 077a18c5-1895-4241-8c31-5f7caf38b22e
keywords:
- Streams, Konfigurieren von VBR-Streams
- Streams, Variable Bitrate (VBR)
- variablenbitrate (VBR), Streams
- VBR (Variable Bitrate), Streams
- Streams, Konfigurieren der Qualitäts basierten VBR
- variablenbitrate (VBR), Konfigurieren von Qualitäts basierter
- VBR (Variable Bitrate), Konfigurieren von Qualitäts basierter
- Profile, Konfigurieren von Qualitäts basiertem VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0b7a6ecb83c7242f82f5626a086c8aba23881f
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103948506"
---
# <a name="to-configure-quality-based-vbr"></a>So konfigurieren Sie Quality-Based VBR

Mit der Qualitäts basierten VBR-Codierung (Variable Bitrate) in einem Stream können Sie eine Qualitätsstufe angeben, die für den gesamten Datenstrom beibehalten wird, unabhängig von den Anforderungen für die Bitrate.

Bei Qualitäts basierten VBR-Videostreams müssen Sie eine Qualitätsstufe von 1 bis 100 angeben, wobei 100 die höchste Qualität darstellt. Zurzeit sind nur 30 diskrete Qualitätseinstellungen vorhanden. Die folgenden Qualitätsstufen entsprechen den diskreten Qualitätseinstellungen: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, 100,,,,. Zahlen zwischen zwei aufeinander folgenden Werten in der vorangehenden Liste entsprechen der gleichen Qualitätseinstellung wie die niedrigere Zahl. Beispielsweise werden 1 und 4 aufgelistet, sodass 2 und 3 die gleiche Qualitätseinstellung wie 1 ergeben.

Für Audiostreams können Sie die verfügbaren Modi auflisten und ein streamkonfigurationsobjekt abrufen. Weitere Informationen finden [Sie unter to Enumerate Codec Formats](to-enumerate-codec-formats.md).

Wenn Sie ein Qualitäts basiertes VBR-Video verwenden, müssen Sie den **dwbitrate** -Member der [**wmvideoinfoheader**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) -Struktur auf einen positiven Wert festlegen. Dieser Wert wird vom Writer nicht verwendet, aber das Übergeben von 0 (null) oder einer negativen Zahl kann beim Schreiben zu Fehlern führen.

Führen Sie die folgenden Schritte aus, um einen Datenstrom in einem Profil zu konfigurieren, der mit einem Qualitäts basierten VBR codiert werden soll.

1.  Erstellen Sie ein Profil-Manager-Objekt, indem Sie die [**wmcreateprofilemanager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) -Funktion aufrufen.
2.  Öffnen Sie ein vorhandenes Profil, dem Sie die VBR-Unterstützung hinzufügen möchten. Weitere Informationen zum Öffnen von Profilen finden Sie unter [Arbeiten mit Profilen](working-with-profiles.md).
3.  Rufen Sie ein streamkonfigurationsobjekt für den Stream ab, den Sie verwenden möchten, indem Sie entweder [**iwmprofile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) oder [**iwmprofile:: getstreambynumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber)aufrufen.
4.  Abrufen eines Zeigers auf die [**iwmpropertyvault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) -Schnittstelle des Stream-Konfigurations Objekts durch Aufrufen von **iwmstreamconfig:: QueryInterface**.
5.  Aktivieren Sie VBR für den Datenstrom, indem Sie [**iwmpropertyvault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) für die Eigenschaft **g \_ wszvbrenabled** aufrufen.
6.  Legen Sie die Qualitätsstufe für den VBR-Stream fest, indem Sie **iwmpropertyvault:: SetProperty** für die Eigenschaft **g \_ wszvbrquality** aufrufen.
7.  Legen Sie **g \_ wszvbrbitratemax** und **g \_ wszvbrbufferwindowmax** mit **iwmpropertyvault:: SetProperty** auf NULL fest.
8.  Speichern Sie die am Stream vorgenommenen Änderungen, indem Sie [**iwmprofile:: reconfigstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)aufrufen.
9.  Speichern Sie das Profil, oder übergeben Sie es an das Writer-Objekt, und beginnen Sie mit dem Schreiben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konfigurieren von VBR-Streams**](configuring-vbr-streams.md)
</dt> </dl>

 

 




