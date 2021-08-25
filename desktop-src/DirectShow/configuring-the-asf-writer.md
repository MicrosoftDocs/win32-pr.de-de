---
description: Konfigurieren des ASF Writer
ms.assetid: 5708c4a0-6197-4a42-adfd-01c6dfe86302
title: Konfigurieren des ASF Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e3d28b3b6178a383909f53a98fef98a5c3e69297f71615010f505d28b77375a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871700"
---
# <a name="configuring-the-asf-writer"></a>Konfigurieren des ASF Writer

Wenn der [WM ASF Writer-Filter](wm-asf-writer-filter.md) erstellt wird, wird er automatisch mit dem Profil WMProfile \_ V80 \_ 256Video konfiguriert. Dieses Profil verwendet die Codecs Windows Media Audio und Windows Media Video Version 8, die nicht so neu sind wie die Codecs der Windows Media 9-Serie. Es wird empfohlen, ein benutzerdefiniertes Profil zu erstellen, das die Codecs der Windows Media 9-Serie verwendet, und den WM ASF Writer mit dem benutzerdefinierten Profil zu konfigurieren, wie unter Konfigurieren von Profilen und anderen [ASF-Dateieigenschaften beschrieben.](configuring-profiles-and-other-asf-file-properties.md) Sie müssen dem Filterdiagramm den WM ASF Writer-Filter hinzufügen, bevor Sie den Filter konfigurieren, und den Filter konfigurieren, bevor Sie ihn mit anderen Filtern verbinden.

Alle Eingabedaten müssen mit einem Zeitstempel versehen werden, und alle Eingabepins müssen verbunden werden, bevor der Filter ausgeführt oder angehalten werden kann. Wenn Sie den Filter daher mit einem Profil konfigurieren, das über einen Audiostream und einen Videostream verfügt, erstellt der Filter eine Audio- und einen Videoeingabepin, und beide Pins müssen verbunden sein, bevor der Filter ausgeführt werden kann. Da für das Windows Media Format SDK ein Audiostream erforderlich ist, muss der WM ASF Writer immer über einen Audioeingabepin verfügen, auch wenn er für einen Dummystream gilt, d.&a; ein stummgeschalteter Audiostream mit niedriger Bitrate.

Hinzufügen von Dateneinheitserweiterungen

Sie können einen Profilstream für Dateneinheitserweiterungen konfigurieren, z. B. SMPTE-Zeitcodes, entweder vor oder nach dem Verbinden des Filters, solange Sie die folgende Reihenfolge von Vorgängen befolgen:

1.  Fügen Sie dem Stream mithilfe von **IWMStreamConfig2::AddDataUnitExtension eine oder mehrere Dateneinheitserweiterungen hinzu.**
2.  Rufen **Sie IWMProfile::ReconfigStream auf,** um das Profil zu aktualisieren.
3.  Rufen [**Sie IConfigAsfWriter::ConfigureFilterUsingProfile mit**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) dem aktualisierten Profilobjekt auf.
4.  Suchen Sie den Videoeingabepin, und rufen Sie dessen [**IAMWMBufferPass::SetNotify-Methode**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) auf, um Ihre anwendungsdefinierte [**IAMWMBufferPassCallback-Schnittstelle zu**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) registrieren.

Wenn das Diagramm ausgeführt wird, wird ihre [**IAMWMBufferPassCallback::Notify-Methode**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) für jeden Frame aufgerufen, und Sie können eigenschaften für das Beispiel mithilfe der **INSSBuffer3-Schnittstellenmethoden** erhalten und festlegen.

> [!Note]  
> In einigen prozessorintensiven Szenarien wie inversem Telecine benötigt der WM ASF Writer möglicherweise mehr Ausgabepuffer, als einige Downstreamfilter unterstützen können. Der DV-Decoder akzeptiert beispielsweise nicht mehr als einen Puffer für seinen Ausgabepin, und dasselbe gilt für den AVI-Dekomprimierer unter bestimmten Bedingungen. Wenn beim Herstellen einer Verbindung mit diesen Filtern oder beim Ausführen des Diagramms Probleme auftreten, kann es erforderlich sein, einen Zwischenfilter zu schreiben, der eine beliebige Anzahl von Puffern auf dem Ausgabepin akzeptiert.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von ASF-Dateien in DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



