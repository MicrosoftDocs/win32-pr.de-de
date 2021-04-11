---
title: Gegenseitiges Ausschluss Objekt
description: Gegenseitiges Ausschluss Objekt
ms.assetid: dd1f7865-e409-4bf9-9fa0-769a29eaed60
keywords:
- Windows Media-Format-SDK, gegenseitige Ausschluss Objekte
- Advanced Systems Format (ASF), Objekte für gegenseitigen Ausschluss
- ASF (Advanced Systems Format), gegenseitige Ausschluss Objekte
- Objekte, Objekte für gegenseitigen Ausschluss
- gegenseitiger Ausschluss, Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8522b66f82bd88479b8c7b1d0d0b45bd038fdab3
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104101331"
---
# <a name="mutual-exclusion-object"></a>Gegenseitiges Ausschluss Objekt

Ein gegenseitiges Ausschluss Objekt wird verwendet, um eine Anzahl von Streams anzugeben, von denen jeweils nur eine übermittelt werden kann. Dies kann auf verschiedene Weise verwendet werden, wie z. b. das Bereitstellen eines Audiodatenstroms in mehreren Sprachen als Sound für einen Videodaten Strom.

Der gegenseitige Ausschluss ist ein optionaler Teil eines Profils. Gegenseitige Ausschluss Objekte können für vorhandene gegenseitige Ausschluss Informationen in einem Profil erstellt werden, oder Sie können leer erstellt werden, um neue Daten zu empfangen. Gegenseitige Ausschluss Objekte können nicht unabhängig von einem Profil Objekt vorhanden sein. Zum Speichern des Inhalts eines gegenseitigen Ausschluss Objekts müssen Sie [**iwmprofile:: addmutualexclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion)aufrufen.

Verwenden Sie zum Erstellen eines gegenseitigen Ausschluss Objekts eine der folgenden Methoden.



| Methode                                                                              | BESCHREIBUNG                                                                                                                                                 |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iwmprofile:: kreatenewmutualexclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | Erstellt ein gegenseitiges Ausschluss Objekt ohne Daten.                                                                                                         |
| [**Iwmprofile:: getmutualexclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | Erstellt ein gegenseitiges Ausschluss Objekt, das mit Daten aus einem Profil aufgefüllt ist. Verwendet den gegenseitigen Ausschluss Index, um die gewünschten gegenseitigen Ausschluss Informationen zu identifizieren. |



 

Beide Methoden in der vorangehenden Tabelle legen einen Zeiger auf eine **iwmmutualexclusion** -Schnittstelle fest. Die **iwmstreamlist** -Schnittstelle wird von **iwmmutualexclusion** geerbt und muss niemals direkt darauf zugreifen. Die andere Schnittstelle des gegenseitigen Ausschluss Objekts kann durch Aufrufen der **QueryInterface** -Methode abgerufen werden.

Die folgenden Schnittstellen werden von jedem gegenseitigen Ausschluss Objekt unterstützt.



| Schnittstelle                                          | BESCHREIBUNG                                                                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iwmmutualexclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)   | Legt den Typ des zu verwendenden gegenseitigen Ausschlusses fest und ruft ihn ab.                                                                                            |
| [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) | Organisiert Streams in Datensätze, die zum Erstellen komplexer gegenseitiger Ausschluss Szenarien verwendet werden können. Erbt alle Methoden von **iwmmutualexclusion**. |
| [**Iwmstreamlist**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | Verwaltet die Liste von sich gegenseitig ausschließenden Datenströmen.                                                                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Gegenseitiger Ausschluss**](mutual-exclusion.md)
</dt> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Profil-Manager-Objekt**](profile-manager-object.md)
</dt> </dl>

 

 




