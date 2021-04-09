---
title: So konfigurieren Sie eingeschränkte VBR
description: So konfigurieren Sie eingeschränkte VBR
ms.assetid: a39e7628-0211-48ad-94e5-5003203f30be
keywords:
- Streams, Konfigurieren von VBR-Streams
- Streams, Variable Bitrate (VBR)
- variablenbitrate (VBR), Streams
- VBR (Variable Bitrate), Streams
- Streams, Konfigurieren von eingeschränkten VBR
- variablenbitrate (VBR), Konfigurieren von eingeschränkten
- VBR (Variable Bitrate), Konfigurieren von eingeschränkten
- Profile, Konfigurieren von eingeschränkten VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98d4e2a1bbea1b724fdde1cc820f19caf9dd77be
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104038678"
---
# <a name="to-configure-constrained-vbr"></a>So konfigurieren Sie eingeschränkte VBR

Mit eingeschränkter VBR-Codierung (Variable Bitrate) können Sie eine durchschnittliche Bitrate angeben, die im codierten Inhalt beibehalten wird. Außerdem geben Sie die maximale Bitrate des Streams und das maximal erforderliche Puffer Fenster an.

Sie können nicht wissen, was die durchschnittliche Bitrate für einen eingeschränkten VBR-Stream vor der Codierung ist, aber Sie können eine grobe Schätzung verwenden. Als allgemeine Regel gilt, dass die von Ihnen angegebene maximale Bitrate das zwei-bis Dreifache der durchschnittlichen Bitrate ist.

Eingeschränkter VBR muss in Verbindung mit der zwei-Pass-Codierung verwendet werden. Die zwei-Pass-Codierung ist nicht im Profil festgelegt. Sie müssen den Writer so konfigurieren, dass vor dem Schreiben des Streams ein Vorverarbeitungs Durchlauf durchgeführt wird. Weitere Informationen zur Verwendung von zwei-Pass-Codierungen finden [Sie unter using Two-Pass Encoding](using-two-pass-encoding.md).

Führen Sie die folgenden Schritte aus, um einen Datenstrom in einem Profil für die Verwendung eingeschränkter VBR-Codierung zu konfigurieren.

1.  Erstellen Sie ein Profil-Manager-Objekt, indem Sie die [**wmcreateprofilemanager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) -Funktion aufrufen.
2.  Öffnen Sie ein vorhandenes Profil, dem Sie die VBR-Unterstützung hinzufügen möchten. Weitere Informationen zum Öffnen von Profilen finden Sie unter [Arbeiten mit Profilen](working-with-profiles.md).
3.  Rufen Sie ein streamkonfigurationsobjekt für den Stream ab, den Sie verwenden möchten, indem Sie entweder [**iwmprofile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) oder [**iwmprofile:: getstreambynumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber)aufrufen.
4.  Abrufen eines Zeigers auf die [**iwmpropertyvault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) -Schnittstelle des Stream-Konfigurations Objekts durch Aufrufen von **iwmstreamconfig:: QueryInterface**.
5.  Aktivieren Sie die VBR-Codierung für den Datenstrom, indem Sie [**iwmpropertyvault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) für die **g \_ wszvbrenabled** -Eigenschaft aufrufen.
6.  Verwenden Sie Aufrufe von **iwmpropertyvault:: SetProperty** , um die gewünschten maximalen Werte für die Eigenschaften " **g \_ wszvbrbitratemax** " und " **g \_ wszvbrbufferwindowmax** " festzulegen.
7.  Speichern Sie die am Stream vorgenommenen Änderungen, indem Sie [**iwmprofile:: reconfigstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)aufrufen.
8.  Speichern Sie das Profil, oder übergeben Sie es an das Writer-Objekt.
9.  Konfigurieren Sie den Writer, um einen Vorverarbeitungs Durchlauf auszuführen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konfigurieren von VBR-Streams**](configuring-vbr-streams.md)
</dt> </dl>

 

 




