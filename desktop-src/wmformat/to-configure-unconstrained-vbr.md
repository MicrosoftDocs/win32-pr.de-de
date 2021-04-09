---
title: So konfigurieren Sie einen nicht eingeschränkten VBR
description: So konfigurieren Sie einen nicht eingeschränkten VBR
ms.assetid: 69ef951f-d08b-401b-a285-2ffdf43ea35d
keywords:
- Streams, Konfigurieren von VBR-Streams
- Streams, Variable Bitrate (VBR)
- variablenbitrate (VBR), Streams
- VBR (Variable Bitrate), Streams
- Streams, Konfigurieren von nicht eingeschränktem VBR
- variablenbitrate (VBR), Konfigurieren der nicht eingeschränkten
- VBR (variablenbitrate), Konfiguration nicht eingeschränkt
- Profile, Konfigurieren von nicht eingeschränktem VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24c022c79bb38414ab201db11abd0cf260dfafe
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104101339"
---
# <a name="to-configure-unconstrained-vbr"></a>So konfigurieren Sie einen nicht eingeschränkten VBR

Sie können die unbeschränkte VBR-Codierung (Variable Bitrate) für einen Stream verwenden, um eine durchschnittliche Bitrate anzugeben, die im codierten Inhalt beibehalten wird. Der uneingeschränkte VBR unterscheidet sich insofern von der normalen CBR, dass die Varianz der Bitrate im gesamten Datenstrom größer sein kann.

Die Bitrate des Datenstroms, der mit [**iwmstreamconfig:: setbitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate)festgelegt wird, wird als die gewünschte durchschnittliche Bitrate verwendet. Wenn die Codierung des Streams beendet ist, können Sie mit [**iwmpropertyvault:: GetPropertyByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyname) zwei zusätzliche Eigenschaften abrufen: **g \_ wszvbrpeak** und **g \_ wszbufferaverage**. Diese Eigenschaften beschreiben die Spitzen Bitrate des codierten Inhalts und das durchschnittliche Puffer Fenster des Inhalts bzw.

Nicht eingeschränkter VBR muss in Verbindung mit der zwei-Pass-Codierung verwendet werden. Die zwei-Pass-Codierung ist nicht im Profil festgelegt. Sie müssen den Writer so konfigurieren, dass vor dem Schreiben des Streams ein Vorverarbeitungs Durchlauf durchgeführt wird. Weitere Informationen zur Verwendung von zwei-Pass-Codierungen finden [Sie unter using Two-Pass Encoding](using-two-pass-encoding.md).

Führen Sie die folgenden Schritte aus, um einen Datenstrom in einem Profil zu konfigurieren, der mit unbeschränkter VBR codiert werden soll:

1.  Erstellen Sie ein Profil-Manager-Objekt, indem Sie die [**wmcreateprofilemanager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) -Funktion aufrufen.
2.  Öffnen Sie ein vorhandenes Profil, dem Sie die VBR-Unterstützung hinzufügen möchten. Weitere Informationen zum Öffnen von Profilen finden Sie unter [Arbeiten mit Profilen](working-with-profiles.md).
3.  Rufen Sie ein streamkonfigurationsobjekt für den Stream ab, den Sie verwenden möchten, indem Sie entweder [**iwmprofile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) oder [**iwmprofile:: getstreambynumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber)aufrufen.
4.  Abrufen eines Zeigers auf die [**iwmpropertyvault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) -Schnittstelle des Stream-Konfigurations Objekts durch Aufrufen von **iwmstreamconfig:: QueryInterface**.
5.  Aktivieren Sie die VBR-Codierung für den Datenstrom, indem Sie [**iwmpropertyvault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) für die **g \_ wszvbrenabled** -Eigenschaft aufrufen.
6.  Legen Sie **g \_ wszvbrbitratemax** und **g \_ wszvbrbufferwindowmax** mit **iwmpropertyvault:: SetProperty** auf NULL fest.
7.  Speichern Sie die am Stream vorgenommenen Änderungen, indem Sie [**iwmprofile:: reconfigstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)aufrufen.
8.  Speichern Sie das Profil, oder übergeben Sie es an das Writer-Objekt.
9.  Konfigurieren Sie den Writer, um einen Vorverarbeitungs Durchlauf auszuführen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konfigurieren von VBR-Streams**](configuring-vbr-streams.md)
</dt> </dl>

 

 




