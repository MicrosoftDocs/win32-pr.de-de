---
title: So konfigurieren Sie die nicht trainierte VBR
description: So konfigurieren Sie die nicht trainierte VBR
ms.assetid: 69ef951f-d08b-401b-a285-2ffdf43ea35d
keywords:
- Streams,Konfigurieren von VBR-Streams
- Streams, variable Bitrate (VBR)
- Variable Bitrate (VBR), Streams
- VBR (variable Bitrate), Streams
- Streams,Konfigurieren von nicht trainierten VBR-Datenströmen
- Variable Bitrate (VBR), Konfigurieren von nicht trainierten
- VBR (variable Bitrate), Konfigurieren von nicht trainierten
- Profile,Konfigurieren von nicht trainierten VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ff73a0aac8d13f015175080aac6eb580fc9686c67d892b14e4714746c8cea34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807760"
---
# <a name="to-configure-unconstrained-vbr"></a>So konfigurieren Sie die nicht trainierte VBR

Sie können die Codierung der nicht trainierten Variable Bitrate (VBR) für einen Stream verwenden, um eine durchschnittliche Bitrate anzugeben, die im codierten Inhalt beibehalten wird. Die constrained VBR unterscheidet sich von der normalen CBR, da die Varianz der Bitrate im gesamten Stream größer sein kann.

Die Bitrate des Streams, festgelegt mit [**IWMStreamConfig::SetBitrate,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate)wird als gewünschte durchschnittliche Bitrate verwendet. Wenn die Codierung des Streams abgeschlossen ist, können Sie [**IWMPropertyVault::GetPropertyByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyname) verwenden, um zwei zusätzliche Eigenschaften abzurufen: **g \_ wszVBRPeak** und **g \_ wszBufferAverage**. Diese Eigenschaften beschreiben die Spitzenbitrate des codierten Inhalts bzw. das durchschnittliche Pufferfenster des Inhalts.

Die nicht trainierte VBR muss zusammen mit der Codierung mit zwei Durchgangen verwendet werden. Die Codierung mit zwei Durchgangen ist im Profil nicht festgelegt. Sie müssen den Writer so konfigurieren, dass er einen Vorverarbeitungslauf vor dem Schreiben des Streams vorbereitet. Weitere Informationen zur Verwendung der Codierung mit zwei Durchgangen finden Sie unter [Using Two-Pass Encoding](using-two-pass-encoding.md).

Führen Sie die folgenden Schritte aus, um einen Stream in einem Profil so zu konfigurieren, dass er mit einer nicht trainierten VBR codiert wird:

1.  Erstellen Sie ein Profil-Manager-Objekt, indem Sie die [**WMCreateProfileManager-Funktion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) aufrufen.
2.  Öffnen Sie ein vorhandenes Profil, dem Sie VBR-Unterstützung hinzufügen möchten. Weitere Informationen zum Öffnen von Profilen finden Sie unter [Arbeiten mit Profilen.](working-with-profiles.md)
3.  Rufen Sie ein Streamkonfigurationsobjekt für den Stream ab, den Sie verwenden möchten, indem Sie [**entweder IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) oder [**IWMProfile::GetStreamByNumber aufrufen.**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber)
4.  Rufen Sie einen Zeiger auf die [**IWMPropertyVault-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) des Streamkonfigurationsobjekts ab, indem **Sie IWMStreamConfig::QueryInterface aufrufen.**
5.  Aktivieren Sie die VBR-Codierung für den Stream, indem [**Sie IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) für die **g \_ wszVBREnabled-Eigenschaft** aufrufen.
6.  Legen **Sie g \_ wszVBRBitrateMax** und **g \_ wszVBRBufferWindowMax** mit **IWMPropertyVault::SetProperty** auf 0 fest.
7.  Speichern Sie die am Stream vorgenommenen Änderungen, indem Sie [**IWMProfile::ReconfigStream aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)
8.  Speichern Sie das Profil, oder übergeben Sie es an das Writer-Objekt.
9.  Konfigurieren Sie den Writer für die Ausführung eines Vorverarbeitungspasses.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konfigurieren von VBR-Streams**](configuring-vbr-streams.md)
</dt> </dl>

 

 




