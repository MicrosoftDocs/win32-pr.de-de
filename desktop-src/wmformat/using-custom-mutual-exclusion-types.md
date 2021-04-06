---
title: Verwenden benutzerdefinierter gegenseitiger Ausschluss Typen
description: Verwenden benutzerdefinierter gegenseitiger Ausschluss Typen
ms.assetid: 9a4d760c-80af-4c67-823d-6da2732671ff
keywords:
- Iwmmutualexclusion
- gegenseitiger Ausschluss, iwmmutualexclusion-Schnittstelle
- gegenseitiger Ausschluss, benutzerdefinierte Typen
- Profile, benutzerdefinierte gegenseitige Ausschluss Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051e95bfb3f5ef8e39af31368227cf4918b897d2
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101262"
---
# <a name="using-custom-mutual-exclusion-types"></a>Verwenden benutzerdefinierter gegenseitiger Ausschluss Typen

Sie können Objekte mit gegenseitigem Ausschluss in einem Profil verwenden, um die Anforderungen von benutzerdefinierten Szenarios zu erfüllen. Wenn Sie den GUID-Wert CLSID \_ wmmutex \_ Unknown an [**iwmmutualexclusion:: settype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype)übergeben, informieren Sie das gegenseitige Ausschluss Objekt, dass Sie ein benutzerdefiniertes Szenario verwenden.

Sie müssen die Streamauswahl manuell steuern, wenn Sie eine Datei mit einem benutzerdefinierten gegenseitigen Ausschluss Wert lesen. Das Reader-Objekt verwendet den ersten Stream, den Sie dem gegenseitigen Ausschluss als Standardwert hinzufügen.

Verwenden Sie die folgenden Schritte, um ein benutzerdefiniertes gegenseitiges Ausschluss Objekt zu erstellen und es einem Profil hinzuzufügen:

1.  Erstellen Sie einen Profil-Manager, indem Sie die [**wmcreateprofilemanager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) -Funktion aufrufen.
2.  Beginnen Sie mit einem vorhandenen Profil, oder erstellen Sie ein völlig neues Profil.
    -   Wenn Sie ein vorhandenes Profil verwenden, können Sie eine der Load-Methoden der [**iwmprofilemanager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) -Schnittstelle abrufen. Fahren Sie dann mit Schritt 4 fort.
    -   Wenn Sie ein vollständig neues Profil erstellen, nennen Sie [**iwmprofilemanager:: | ateemptyprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).
3.  Fügen Sie dem neuen Profildaten Ströme durch Aufrufen von [**iwmprofile:: createnewstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)hinzu. Konfigurieren Sie die Streams nach Bedarf mithilfe der Methoden von [**iwmstreamconfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig). Sie können auch **QueryInterface** aufrufen, um auf andere Schnittstellen im Datenstrom-Konfigurationsobjekt zuzugreifen.

    " **Kreatenewstream** " erstellt nur ein streamkonfigurationsobjekt und wirkt sich nicht auf das Profil aus. Nachdem ein Stream ordnungsgemäß konfiguriert wurde, müssen Sie [**iwmprofile:: addstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) zum Hinzufügen des Streams zum Profil aufruft.

4.  Erstellen Sie ein gegenseitiges Ausschluss Objekt durch Aufrufen von [**iwmprofile:: createnewmutualexclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion).
5.  Fügen Sie die gewünschten Datenströme dem gegenseitigen Ausschluss Objekt hinzu, indem Sie [**iwmstreamlist:: addstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream) aufrufen (verfügbar direkt von [**iwmmutualexclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion), das von [**iwmstreamlist**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)erbt).
6.  Legen Sie den Typ des gegenseitigen Ausschlusses auf Custom fest, indem Sie [**iwmmutualexclusion:: settype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype)aufrufen. Übergeben Sie die CLSID \_ wmmutex \_ Unknown als GUID-Typ.
7.  Fügen Sie dem Profil das konfigurierte Objekt für den gegenseitigen Ausschluss hinzu, indem Sie [**iwmprofile:: addmutualexclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion)aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmmutualexclusion-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[**Iwmprofile-Schnittstelle**](iwmprofile.md)
</dt> <dt>

[**Iwmprofilemanager-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Iwmstreamconfig-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> <dt>

[**Iwmstreamlist-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)
</dt> <dt>

[**Verwenden von gegenseitigem Ausschluss**](using-mutual-exclusion.md)
</dt> <dt>

[**Wmkreateprofilemanager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
</dt> </dl>

 

 




