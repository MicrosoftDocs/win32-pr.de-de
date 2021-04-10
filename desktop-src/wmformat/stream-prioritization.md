---
title: Streampriorisierung
description: Streampriorisierung
ms.assetid: 6b3e9b03-62ef-422b-97ab-197d1cd15beb
keywords:
- Windows Media-Format-SDK, streampriorisierung
- Advanced Systems Format (ASF), streampriorisierung
- ASF (Advanced Systems Format), streampriorisierung
- Windows Media-Format-SDK, Prioritäts Reihenfolge für Streams
- Advanced Systems Format (ASF), Prioritäts Reihenfolge für Streams
- ASF (Advanced Systems Format), Prioritäts Reihenfolge für Streams
- Streams, Priorisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe1628ef050d393cd2d98e73708d5a9ad6c3be4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038572"
---
# <a name="stream-prioritization"></a>Streampriorisierung

Wenn Sie eine ASF-Datei erstellen, können Sie eine Prioritäts Reihenfolge für die zugehörigen Datenströme angeben. Wenn Sie eine priorisierte Datei streamen und die verfügbare Bandbreite nicht ausreicht, um alle Streams zu übermitteln, löscht der Reader Datenströme in umgekehrter Reihenfolge. Auf diese Weise können Sie sicherstellen, dass die wichtigsten Datenströme in Ihrer Datei aufgrund von Netzwerkproblemen nicht gelöscht werden.

Die streampriorisierung wird mit einem streampriorisierungsobjekt konfiguriert und dem Profil hinzugefügt. Ein Profil kann nur ein Datenstrom Priorisierungs Objekt enthalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktionen der ASF-Datei**](asf-file-features.md)
</dt> <dt>

[**IWMProfile3:: kreatenewstreampriorisierung**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization)
</dt> <dt>

[**IWMProfile3:: getstreamprioritisierung**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)
</dt> <dt>

[**IWMProfile3:: removestreamprioritisierung**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-removestreamprioritization)
</dt> <dt>

[**IWMProfile3:: setstreampriorisierung**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization)
</dt> <dt>

[**Iwmstreampriorisierungsschnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization)
</dt> <dt>

[**Verwenden der streampriorisierung**](using-stream-prioritization.md)
</dt> </dl>

 

 




