---
title: Verwenden benutzerdefinierter gegenseitiger Ausschlusstypen
description: Verwenden benutzerdefinierter gegenseitiger Ausschlusstypen
ms.assetid: 9a4d760c-80af-4c67-823d-6da2732671ff
keywords:
- IWMMutualExclusion
- gegenseitiger Ausschluss, IWMMutualExclusion-Schnittstelle
- gegenseitiger Ausschluss, benutzerdefinierte Typen
- Profile, benutzerdefinierte gegenseitige Ausschlusstypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7162b8d0588031e934e55425af03cd0d2e8d0a58524b19251521ec2ab6848094
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845078"
---
# <a name="using-custom-mutual-exclusion-types"></a>Verwenden benutzerdefinierter gegenseitiger Ausschlusstypen

Sie können Objekte für gegenseitigen Ausschluss in einem Profil verwenden, um die Anforderungen benutzerdefinierter Szenarien zu erfüllen. Indem Sie den GUID-Wert CLSID \_ WMMUTEX \_ Unknown an [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype)übergeben, informieren Sie das objekt für gegenseitigen Ausschluss, dass Sie ein benutzerdefiniertes Szenario verwenden.

Sie müssen die Streamauswahl manuell steuern, wenn Sie eine Datei mit einem benutzerdefinierten gegenseitigen Ausschlusswert lesen. Das Readerobjekt verwendet den ersten Stream, den Sie dem gegenseitigen Ausschluss als Standard hinzufügen.

Verwenden Sie die folgenden Schritte, um ein benutzerdefiniertes objekt für gegenseitigen Ausschluss zu erstellen und es einem Profil hinzuzufügen:

1.  Erstellen Sie einen Profil-Manager, indem Sie die [**WMCreateProfileManager-Funktion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) aufrufen.
2.  Beginnen Sie entweder mit einem vorhandenen Profil, oder erstellen Sie ein völlig neues Profil.
    -   Wenn Sie ein vorhandenes Profil verwenden, rufen Sie eine der Lademethoden der [**IWMProfileManager-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) auf. Fahren Sie dann mit Schritt 4 fort.
    -   Wenn Sie ein völlig neues Profil erstellen, rufen [**Sie IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile)auf.
3.  Fügen Sie dem neuen Profil Streams hinzu, indem [**Sie IWMProfile::CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)aufrufen. Konfigurieren Sie die Streams nach Bedarf mithilfe der Methoden von [**IWMStreamConfig.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) Sie können auch **QueryInterface** aufrufen, um auf andere Schnittstellen im Streamkonfigurationsobjekt zuzugreifen.

    **CreateNewStream** erstellt nur ein Streamkonfigurationsobjekt und wirkt sich nicht auf das Profil aus. Nachdem ein Stream ordnungsgemäß konfiguriert wurde, müssen Sie [**IWMProfile::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) aufrufen, um den Stream dem Profil hinzuzufügen.

4.  Erstellen Sie ein objekt für gegenseitigen Ausschluss, indem [**Sie IWMProfile::CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion)aufrufen.
5.  Fügen Sie dem objekt für gegenseitigen Ausschluss die gewünschten Streams hinzu, indem [**Sie IWMStreamList::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream) aufrufen (direkt über [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)verfügbar, das von [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)erbt).
6.  Legen Sie den Typ des gegenseitigen Ausschlusses auf custom fest, indem [**Sie IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype)aufrufen. Übergeben Sie die CLSID \_ WMMUTEX \_ Unknown als Typ-GUID.
7.  Fügen Sie dem Profil das konfigurierte Objekt für gegenseitigen Ausschluss hinzu, indem [**Sie IWMProfile::AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion)aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMMutualExclusion-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[**IWMProfile-Schnittstelle**](iwmprofile.md)
</dt> <dt>

[**IWMProfileManager-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**IWMStreamConfig-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> <dt>

[**IWMStreamList-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)
</dt> <dt>

[**Verwenden des gegenseitigen Ausschlusses**](using-mutual-exclusion.md)
</dt> <dt>

[**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
</dt> </dl>

 

 




