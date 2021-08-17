---
title: Objekt für gegenseitigen Ausschluss
description: Objekt für gegenseitigen Ausschluss
ms.assetid: dd1f7865-e409-4bf9-9fa0-769a29eaed60
keywords:
- Windows Medienformat-SDK, gegenseitige Ausschlussobjekte
- Advanced Systems Format (ASF), gegenseitige Ausschlussobjekte
- ASF (Advanced Systems Format), gegenseitige Ausschlussobjekte
- Objekte,gegenseitige Ausschlussobjekte
- Gegenseitiger Ausschluss,Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32d7e780ac18dcad7ef04f9bb50d3a7389851156866980b21fbe0c231bcb057d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929930"
---
# <a name="mutual-exclusion-object"></a>Objekt für gegenseitigen Ausschluss

Ein objektseitiger Ausschluss wird verwendet, um eine Reihe von Streams anzugeben, von denen immer nur einer übermittelt werden kann. Dies kann auf verschiedene Weise verwendet werden, z. B. das Bereitstellen eines Audiodatenstroms in mehreren Sprachen als Ziel für einen Videostream.

Der gegenseitige Ausschluss ist ein optionaler Teil eines Profils. Gegenseitige Ausschlussobjekte können für vorhandene gegenseitige Ausschlussinformationen in einem Profil erstellt oder leer erstellt werden, um neue Daten zu empfangen. Gegenseitige Ausschlussobjekte können nicht unabhängig von einem Profilobjekt vorhanden sein. Um den Inhalt eines gegenseitigen Ausschlussobjekts zu speichern, müssen Sie [**IWMProfile::AddMutualExclusion aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion)

Verwenden Sie eine der folgenden Methoden, um ein Objekt für gegenseitigen Ausschluss zu erstellen.



| Methode                                                                              | Beschreibung                                                                                                                                                 |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfile::CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | Erstellt ein gegenseitiges Ausschlussobjekt ohne Daten.                                                                                                         |
| [**IWMProfile::GetMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | Erstellt ein Objekt für gegenseitigen Ausschluss, das mit Daten aus einem Profil aufgefüllt wird. Verwendet den Index für gegenseitigen Ausschluss, um die gewünschten Informationen zum gegenseitigen Ausschluss zu identifizieren. |



 

Beide Methoden in der vorangehenden Tabelle legen einen Zeiger auf eine **IWMMutualExclusion-Schnittstelle** fest. Die **IWMStreamList-Schnittstelle** wird von **IWMMutualExclusion** geerbt und muss nie direkt aufgerufen werden. Die andere Schnittstelle des gegenseitigen Ausschlussobjekts kann durch Aufrufen der **QueryInterface-Methode ermittelt** werden.

Die folgenden Schnittstellen werden von jedem gegenseitigen Ausschlussobjekt unterstützt.



| Schnittstelle                                          | BESCHREIBUNG                                                                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)   | Legt den Typ des zu verwendenden gegenseitigen Ausschlusses fest und ruft diesen ab.                                                                                            |
| [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) | Organisiert Streams in Datensätzen, die verwendet werden können, um komplexe Szenarien für gegenseitigen Ausschluss zu erstellen. Erbt alle Methoden von **IWMMutualExclusion.** |
| [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | Verwaltet die Liste der sich gegenseitig ausschließenden Streams.                                                                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Gegenseitiger Ausschluss**](mutual-exclusion.md)
</dt> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Profil-Manager-Objekt**](profile-manager-object.md)
</dt> </dl>

 

 




