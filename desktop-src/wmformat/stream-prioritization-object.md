---
title: StreamPriorisierungsobjekt
description: StreamPriorisierungsobjekt
ms.assetid: cb0345ce-6847-435b-8cbb-f8b93856af9f
keywords:
- Windows Medienformat-SDK, Streampriorisierungsobjekte
- Advanced Systems Format (ASF), Streampriorisierungsobjekte
- ASF (Advanced Systems Format), Streampriorisierungsobjekte
- Objekte,Streampriorisierungsobjekte
- Streampriorisierungsobjekte
- Streams, Streampriorisierungsobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a0d8ce386dfa6d3eed64361d77326c515feadb2a6aa05eb697e402d120a55ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699967"
---
# <a name="stream-prioritization-object"></a>StreamPriorisierungsobjekt

Ein Streampriorisierungsobjekt wird verwendet, um eine Wichtigkeitsreihenfolge für die Streams in einem Profil anzugeben. Wenn die vollständige Wiedergabe aufgrund von Bitrateneinschränkungen nicht möglich ist, werden die Streams mit der niedrigsten Priorität zuerst gelöscht.

Streampriorisierungsobjekte können für vorhandene Datenstrompriorisierungsdaten in einem Profil erstellt oder leer erstellt werden, um neue Daten zu empfangen. Streampriorisierungsobjekte können nicht unabhängig von einem Profilobjekt vorhanden sein. Um den Inhalt eines Streampriorisierungsobjekts zu speichern, müssen Sie [**IWMProfile3::SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization)aufrufen. Verwenden Sie eine der folgenden Methoden, um ein Streampriorisierungsobjekt zu erstellen.



| Methode                                                                                          | Beschreibung                                                                  |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**IWMProfile3::CreateNewStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization) | Erstellt ein Streampriorisierungsobjekt ohne Daten.                     |
| [**IWMProfile3::GetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)             | Erstellt ein Streampriorisierungsobjekt, das mit Daten aus dem Profil aufgefüllt wird. |



 

Beide Methoden in der obigen Tabelle legen einen Zeiger auf eine **IWMStreamPrioritization-Schnittstelle** fest. Dies ist die einzige Schnittstelle, die vom Streampriorisierungsobjekt unterstützt wird.



| Schnittstelle                                                  | Beschreibung                                                          |
|------------------------------------------------------------|----------------------------------------------------------------------|
| [**IWMStreamPrioritization**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization) | Verwaltet die Liste der Streams innerhalb des Streampriorisierungsobjekts. |



 

## <a name="remarks"></a>Hinweise

Für ein bestimmtes Profil kann nur eine Streampriorisierung vorhanden sein. Wenn Sie eine neue Streampriorisierung für ein Profil erstellen, das bereits eine Streampriorisierung enthält, wird das alte gelöscht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Profilobjekt**](profile-object.md)
</dt> <dt>

[**Verwenden der Streampriorisierung**](using-stream-prioritization.md)
</dt> </dl>

 

 




