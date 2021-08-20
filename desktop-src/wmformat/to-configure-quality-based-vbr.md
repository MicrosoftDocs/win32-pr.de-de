---
title: So konfigurieren Quality-Based VBR
description: So konfigurieren Quality-Based VBR
ms.assetid: 077a18c5-1895-4241-8c31-5f7caf38b22e
keywords:
- Streams,Konfigurieren von VBR-Streams
- Streams, variable Bitrate (VBR)
- Variable Bitrate (VBR), Streams
- VBR (variable Bitrate), Streams
- Streams,Konfigurieren der qualitätsbasierten VBR
- Variable Bitrate (VBR), Konfigurieren der qualitätsbasierten
- VBR (variable Bitrate), Konfigurieren qualitätsbasierter Daten
- Profile,Konfigurieren der qualitätsbasierten VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34b1181d722909478b29e1ffbe5f5b53cb919d80e3922e055eecdf34c334a382
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845635"
---
# <a name="to-configure-quality-based-vbr"></a>So konfigurieren Quality-Based VBR

Sie können die qualitätsbasierte VBR-Codierung (Variable Bit Rate) für einen Stream verwenden, um eine Qualitätsstufe anzugeben, die für den gesamten Stream beibehalten wird, unabhängig von den daraus folgenden Bitratenanforderungen.

Für qualitätsbasierte VBR-Videostreams müssen Sie einen Qualitätsgrad von 1 bis 100 angeben, bei dem 100 die höchste Qualität darstellt. Derzeit gibt es nur 30 diskrete Qualitätseinstellungen. Die folgenden Qualitätsstufen sind diskreten Qualitätseinstellungen gleichzusetzen: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, 100. Zahlen zwischen zwei aufeinander folgenden Werten in der vorherigen Liste entspricht der gleichen Qualitätseinstellung wie die niedrigere Zahl. Beispielsweise werden 1 und 4 aufgeführt, sodass 2 und 3 beide zur gleichen Qualitätseinstellung wie 1 führen.

Für Audiostreams können Sie die verfügbaren Modi aufzählen und ein Streamkonfigurationsobjekt abrufen. Weitere Informationen finden Sie unter [Aufzählen von Codecformaten.](to-enumerate-codec-formats.md)

Wenn Sie qualitätsbasierte VBR-Videos verwenden, müssen Sie den **dwBitrate-Member** der [**WMVIDEOINFOHEADER-Struktur**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) auf einen positiven Wert festlegen. Dieser Wert wird nicht vom Writer verwendet, aber die Übergabe von 0 (null) oder einer negativen Zahl kann beim Schreiben Fehler verursachen.

Führen Sie die folgenden Schritte aus, um einen Stream in einem Profil so zu konfigurieren, dass er mit einer qualitätsbasierten VBR codiert wird.

1.  Erstellen Sie ein Profil-Manager-Objekt, indem Sie die [**WMCreateProfileManager-Funktion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) aufrufen.
2.  Öffnen Sie ein vorhandenes Profil, dem Sie VBR-Unterstützung hinzufügen möchten. Weitere Informationen zum Öffnen von Profilen finden Sie unter [Arbeiten mit Profilen.](working-with-profiles.md)
3.  Rufen Sie ein Streamkonfigurationsobjekt für den Stream ab, den Sie verwenden möchten, indem Sie [**entweder IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) oder [**IWMProfile::GetStreamByNumber aufrufen.**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber)
4.  Rufen Sie einen Zeiger auf die [**IWMPropertyVault-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) des Streamkonfigurationsobjekts ab, indem **Sie IWMStreamConfig::QueryInterface aufrufen.**
5.  Aktivieren Sie VBR für den Stream, indem Sie [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) für die **\_ g wszVBREnabled-Eigenschaft** aufrufen.
6.  Legen Sie die Qualitätsstufe für den VBR-Stream fest, indem **Sie IWMPropertyVault::SetProperty** für die **g \_ wszVBRQuality-Eigenschaft** aufrufen.
7.  Legen **Sie g \_ wszVBRBitrateMax** und **g \_ wszVBRBufferWindowMax** mit **IWMPropertyVault::SetProperty** auf 0 fest.
8.  Speichern Sie die am Stream vorgenommenen Änderungen, indem Sie [**IWMProfile::ReconfigStream aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)
9.  Speichern Sie das Profil, oder übergeben Sie es an das Writer-Objekt, und beginnen Sie mit dem Schreiben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konfigurieren von VBR-Streams**](configuring-vbr-streams.md)
</dt> </dl>

 

 




