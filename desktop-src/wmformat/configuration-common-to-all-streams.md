---
title: Allgemeine Konfiguration für alle Streams
description: Allgemeine Konfiguration für alle Streams
ms.assetid: 63e655b7-a4ef-4580-a0f3-03cedd2cbf9a
keywords:
- Profile, Konfigurationen, die für alle Streams gemeinsam sind
- Streams, allgemeine Konfigurationen
- Streams, Namen
- Streams, Verbindungs Namen
- Streams, Zahlen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f1a398256da99092da45e83ebc91de713f9ab71
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "104390080"
---
# <a name="configuration-common-to-all-streams"></a>Allgemeine Konfiguration für alle Streams

Allen Streams sollten unabhängig vom Typ ein Datenstrom Name, ein Verbindungs Name und eine streamnummer zugewiesen werden.

Der Datenstrom Name ist einfach ein beschreibender Name, den Sie dem Stream zuweisen. Ein Datenstrom benötigt keinen Datenstrom Namen, aber er hilft Ihnen, den Stream zu identifizieren, wenn er das Profil zu einem späteren Zeitpunkt bearbeitet. Sie können einen Namen für den Stream durch Aufrufen von [**iwmstreamconfig:: setstreamname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname)festlegen.

Jeder Stream sollte über einen Verbindungs Namen verfügen, der auch als Eingabe Name bezeichnet wird. Wenn Sie das Profil im Writer-Objekt so festlegen, dass eine Datei geschrieben wird, ordnet der Writer jeden Verbindungs Namen einer Eingabe zu. Zum Identifizieren der Eingaben müssen Sie [**iwminputmediarequi:: getConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname) aufrufen, um den Verbindungs Namen abzurufen. Typische Verbindungs Namen sind einfache Beschreibungen der Inhalte, z. b. "Audiodaten". Wenn Ihr Profildaten Ströme enthält, die sich durch die Bitrate gegenseitig ausschließen, muss jeder der sich gegenseitig ausschließenden Datenströme denselben Verbindungs Namen aufweisen. Wenn dies nicht der Fall ist, ist das Profil ungültig und wird vom Writer abgelehnt. Sie können einen Verbindungs Namen durch Aufrufen von [**iwmstreamconfig:: setconnectionname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setconnectionname)festlegen.

Die streamnummer identifiziert den Stream innerhalb der Datei. Im Unterschied zu Eingabe-und Ausgabe Nummern beginnen streamnummern bei 1 und nicht bei 0. Eine streamnummer unterscheidet sich von einem streamindex, den Sie verwenden, wenn Sie Datenströme in einem Profil mithilfe von [**iwmprofile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)erhalten. Der streamindex ist eine Zahl, die dem Stream vom Profil Objekt zugewiesen wird. Streamindexe liegen zwischen 0 und eins kleiner als die Anzahl von Datenströmen, die von [**iwmprofile:: getstreamcount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreamcount)abgerufen werden. Streamnummern müssen nicht sequenziell sein, Sie sind jedoch in der Regel gleich und können zwischen 1 und 63 liegen. Sie können eine streamnummer festlegen, indem Sie [**iwmstreamconfig:: setstreamnumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamnumber)aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konfigurieren von Streams**](configuring-streams.md)
</dt> <dt>

[**Eingaben, Streams und Ausgaben**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




