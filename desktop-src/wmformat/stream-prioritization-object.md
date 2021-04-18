---
title: Streampriorisierungsobjekt
description: Streampriorisierungsobjekt
ms.assetid: cb0345ce-6847-435b-8cbb-f8b93856af9f
keywords:
- Windows Media-Format-SDK, streampriorisierungsobjekte
- Advanced Systems Format (ASF), streampriorisierungsobjekte
- ASF (Advanced Systems Format), streampriorisierungsobjekte
- Objekte, streampriorisierungsobjekte
- streampriorisierungsobjekte
- Streams, streampriorisierungsobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cce4189f64e85cca4e0d649dbc00409cf9d7c06
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106340683"
---
# <a name="stream-prioritization-object"></a>Streampriorisierungsobjekt

Ein streampriorisierungsobjekt wird verwendet, um eine Wichtigkeits Reihenfolge für die Datenströme in einem Profil anzugeben. Wenn die vollständige Wiedergabe aufgrund von Bitraten Einschränkungen nicht möglich ist, werden die Datenströme mit niedrigster Priorität als erstes gelöscht.

Streampriorisierungsobjekte können für vorhandene Datenstrom Priorisierungs Daten in einem Profil erstellt werden, oder Sie können leer erstellt werden, um neue Daten zu empfangen. Streampriorisierungsobjekte können nicht unabhängig von einem Profil Objekt vorhanden sein. Zum Speichern des Inhalts eines streampriorisierungsobjekts muss [**IWMProfile3:: setstreampriorisierung**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization)aufgerufen werden. Verwenden Sie zum Erstellen eines streampriorisierungsobjekts eine der folgenden Methoden.



| Methode                                                                                          | BESCHREIBUNG                                                                  |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**IWMProfile3:: kreatenewstreampriorisierung**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization) | Erstellt ein streampriorisierungsobjekt ohne Daten.                     |
| [**IWMProfile3:: getstreamprioritisierung**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)             | Erstellt ein Datenstrom Priorisierungs Objekt, das mit Daten aus dem Profil aufgefüllt ist. |



 

Beide Methoden in der vorangehenden Tabelle legen einen Zeiger auf eine **iwmstreampriorisierungsschnittstelle** fest. Dies ist die einzige Schnittstelle, die vom streampriorisierungsobjekt unterstützt wird.



| Schnittstelle                                                  | BESCHREIBUNG                                                          |
|------------------------------------------------------------|----------------------------------------------------------------------|
| [**Iwmstreampriorisierung**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization) | Verwaltet die Liste der Streams im streampriorisierungsobjekt. |



 

## <a name="remarks"></a>Bemerkungen

Für ein bestimmtes Profil kann nur eine streampriorisierung vorhanden sein. Wenn Sie eine neue streampriorisierung für ein Profil erstellen, das bereits eine streampriorisierung enthält, wird das alte gelöscht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Profil Objekt**](profile-object.md)
</dt> <dt>

[**Verwenden der streampriorisierung**](using-stream-prioritization.md)
</dt> </dl>

 

 




