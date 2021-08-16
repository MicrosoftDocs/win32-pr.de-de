---
title: Priorisierung von Datenströmen
description: Priorisierung von Datenströmen
ms.assetid: 6b3e9b03-62ef-422b-97ab-197d1cd15beb
keywords:
- Windows Medienformat-SDK, Streampriorisierung
- Advanced Systems Format (ASF), Streampriorisierung
- ASF (Advanced Systems Format), Streampriorisierung
- Windows Medienformat-SDK, Prioritäts reihenfolge für Streams
- Advanced Systems Format (ASF), Prioritäts reihenfolge für Streams
- ASF (Advanced Systems Format), Prioritäts reihenfolge für Streams
- Streams,Priorisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fd34bab6a7957d7cbcdf97a78fc3d8be1f663d43ef1eb1ec8d4c575571ad0a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197276"
---
# <a name="stream-prioritization"></a>Priorisierung von Datenströmen

Wenn Sie eine ASF-Datei erstellen, können Sie eine Prioritäts reihenfolge für ihre konstituierenden Streams angeben. Wenn Sie eine priorisierte Datei streamen und die verfügbare Bandbreite nicht ausreicht, um alle Datenströme zu liefern, gibt der Reader Datenströme in umgekehrter Prioritäts reihenfolge ab. Auf diese Weise können Sie garantieren, dass die wichtigsten Streams in Ihrer Datei aufgrund von Netzwerkproblemen nicht gelöscht werden.

Die Streampriorisierung wird mit einem Streampriorisierungsobjekt konfiguriert und dem Profil hinzugefügt. Ein Profil kann nur ein Streampriorisierungsobjekt enthalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ASF-Dateifeatures**](asf-file-features.md)
</dt> <dt>

[**IWMProfile3::CreateNewStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization)
</dt> <dt>

[**IWMProfile3::GetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)
</dt> <dt>

[**IWMProfile3::RemoveStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-removestreamprioritization)
</dt> <dt>

[**IWMProfile3::SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization)
</dt> <dt>

[**IWMStreamPrioritization-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization)
</dt> <dt>

[**Verwenden der Streampriorisierung**](using-stream-prioritization.md)
</dt> </dl>

 

 




