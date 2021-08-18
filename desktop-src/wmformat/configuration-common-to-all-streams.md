---
title: Configuration Common to All Streams
description: Configuration Common to All Streams
ms.assetid: 63e655b7-a4ef-4580-a0f3-03cedd2cbf9a
keywords:
- Profile, Konfigurationen, die allen Streams gemeinsam sind
- Streams, allgemeine Konfigurationen
- Streams, Namen
- Streams, Verbindungsnamen
- Streams, Zahlen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e8b58e97ce2add4b6ff139aebacbc6d510af4424b2d3ae2bff3ea4577c429b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964179"
---
# <a name="configuration-common-to-all-streams"></a>Configuration Common to All Streams

Allen Streams sollten unabhängig vom Typ ein Streamname, ein Verbindungsname und eine Streamnummer zugewiesen werden.

Der Streamname ist einfach ein beschreibender Name, den Sie dem Stream zuweisen. Ein Stream benötigt keinen Streamnamen, hilft Ihnen jedoch dabei, den Datenstrom zu identifizieren, wenn Sie das Profil zu einem späteren Zeitpunkt bearbeiten. Sie können einen Namen für den Stream festlegen, indem Sie [**IWMStreamConfig::SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname)aufrufen.

Jeder Stream sollte über einen Verbindungsnamen verfügen, der auch als Eingabename bezeichnet wird. Wenn Sie das Profil im Writer-Objekt so festlegen, dass eine Datei geschrieben wird, verknüpft der Writer jeden Verbindungsnamen mit einer Eingabe. Um die Eingaben zu identifizieren, müssen Sie [**IWMInputMediaProps::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname) aufrufen, um den Verbindungsnamen abzurufen. Typische Verbindungsnamen sind einfache Beschreibungen des Inhalts, z. B. "Audio". Wenn Ihr Profil Datenströme enthält, die sich durch die Bitrate gegenseitig ausschließen, muss jeder der sich gegenseitig ausschließenden Datenströme den gleichen Verbindungsnamen aufweisen. Andernfalls ist das Profil ungültig und wird vom Writer abgelehnt. Sie können einen Verbindungsnamen festlegen, indem Sie [**IWMStreamConfig::SetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setconnectionname)aufrufen.

Die Streamnummer identifiziert den Stream innerhalb der Datei. Im Gegensatz zu Eingabe- und Ausgabenummern beginnen Streamnummern bei 1 und nicht bei 0. Eine Streamnummer unterscheidet sich von einem Streamindex, den Sie beim Abrufen von Datenströmen in einem Profil mithilfe von [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)verwenden. Der Streamindex ist eine Zahl, die dem Stream vom Profilobjekt zugewiesen wird. Streamindizes liegen zwischen 0 und 1 kleiner als die Anzahl von Streams, die von [**IWMProfile::GetStreamCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreamcount)abgerufen werden. Streamnummern müssen nicht sequenziell sein, obwohl sie in der Regel sind und zwischen 1 und 63 liegen können. Sie können eine Streamnummer festlegen, indem Sie [**IWMStreamConfig::SetStreamNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamnumber)aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konfigurieren von Streams**](configuring-streams.md)
</dt> <dt>

[**Eingaben, Streams und Ausgaben**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




