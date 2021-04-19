---
description: Konfigurieren des ASF-Writers
ms.assetid: 5708c4a0-6197-4a42-adfd-01c6dfe86302
title: Konfigurieren des ASF-Writers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62a6dfc1827743dce946188ebf9e050226b5c484
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342958"
---
# <a name="configuring-the-asf-writer"></a>Konfigurieren des ASF-Writers

Wenn der [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter erstellt wird, wird er automatisch mit dem Video Profil "wmprofile \_ V80 256" konfiguriert \_ . In diesem Profil werden die Codecs Windows Media Audio und Windows Media Video Version 8 verwendet, die nicht so aktuell sind wie die Codecs der Windows Media 9-Serie. Es wird empfohlen, ein benutzerdefiniertes Profil zu erstellen, das die Codecs der Windows Media 9-Serie verwendet, und den WM-ASF-Writer mit dem benutzerdefinierten Profil zu konfigurieren, wie unter [Konfigurieren von Profilen und anderen Eigenschaften von ASF-Dateien](configuring-profiles-and-other-asf-file-properties.md)beschrieben Sie müssen den WM-ASF-Writer-Filter vor dem Konfigurieren des Filters dem Filter Diagramm hinzufügen und den Filter konfigurieren, bevor Sie ihn mit anderen Filtern verbinden.

Alle Eingabedaten müssen mit einem Zeitstempel versehen werden, und alle Eingabe Pins müssen verbunden sein, bevor der Filter ausgeführt oder angehalten werden kann. Wenn Sie den Filter mit einem Profil konfigurieren, das über einen Audiostream und einen Videostream verfügt, erstellt der Filter daher eine Audiodatei und eine Videoeingabe-PIN. beide Pins müssen miteinander verbunden sein, bevor der Filter ausgeführt werden kann. Da das Windows Media-Format-SDK erfordert, dass ein Audiostream funktioniert, muss der WM-ASF-Writer immer über eine eingabeaudiopin verfügen, selbst wenn es sich um einen Pseudo Datenstrom handelt – d. h. um einen stumm geschalteter Audiostream mit niedriger Bitrate.

Hinzufügen von Dateneinheiten Erweiterungen

Sie können einen profilstream für dateneinheits Erweiterungen konfigurieren, wie z. b. SMPTE-Zeit Codes, entweder vor oder nach dem Verbinden des Filters, solange Sie dieser Reihenfolge von Vorgängen folgen:

1.  Fügen Sie dem Stream mithilfe von **IWMStreamConfig2:: adddataunitextension** eine oder mehrere Dateneinheiten Erweiterungen hinzu.
2.  Nennen Sie **iwmprofile:: reconfigstream** , um das Profil zu aktualisieren.
3.  Nennen Sie [**iconfigasfwriter:: konfigurierfilterusingprofile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) mit dem aktualisierten Profil Objekt.
4.  Suchen Sie die Videoeingabe-PIN, und wenden Sie Ihre [**iamwmbufferpass:: setnotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) -Methode an, um Ihre Anwendungs definierte [**iamwmbufferpasscallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) -Schnittstelle zu registrieren.

Wenn das Diagramm ausgeführt wird, wird die [**iamwmbufferpasscallback:: notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) -Methode für jeden Frame aufgerufen, und Sie können Eigenschaften für das Beispiel mithilfe der **INSSBuffer3** -Schnittstellen Methoden erhalten und festlegen.

> [!Note]  
> In einigen Prozessor intensiven Szenarien wie z. b. Inverse Telecine benötigt der WM-ASF-Writer möglicherweise mehr Ausgabepuffer, als von einigen downstreamfiltern unterstützt werden kann. Der DV-Decoder nimmt z. b. für die Ausgabepin nicht mehr als einen Puffer an, und dasselbe gilt für den AVI-Dekompressor unter bestimmten Bedingungen. Wenn beim Versuch, eine Verbindung mit diesen Filtern herzustellen, oder möglicherweise beim Ausführen des Diagramms Probleme auftreten, kann es erforderlich sein, einen Vermittler Filter zu schreiben, der eine beliebige Anzahl von Puffern in der Ausgabe-PIN akzeptiert.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von ASF-Dateien in DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



