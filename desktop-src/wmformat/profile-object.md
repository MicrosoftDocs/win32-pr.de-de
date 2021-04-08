---
title: Profil Objekt
description: Profil Objekt
ms.assetid: ec42889e-580e-4a65-9fe6-4a5f15c97eb0
keywords:
- Windows Media-Format-SDK, Profil Objekte
- Advanced Systems Format (ASF), Profil Objekte
- ASF (Advanced Systems Format), Profil Objekte
- Objekte, Profil Objekte
- Profile, Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6763d098819bde7d5db404aeffef3cd333d9b1
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103858080"
---
# <a name="profile-object"></a>Profil Objekt

Ein Profil Objekt verwaltet die Einstellungen eines Profils. Profil Objekte können für vorhandene Profildaten erstellt werden, oder Sie können leer erstellt werden, um neue Daten zu empfangen. Ein Profil Objekt wird auch vom Reader-Objekt (und dem synchronen Reader-Objekt) erstellt, wenn eine Datei zum Lesen geladen wird. In diesem Fall wird das Objekt mit den im Header der Datei gespeicherten Profilinformationen aufgefüllt.

Zum Speichern des Inhalts eines Profil Objekts müssen Sie [**iwmprofilemanager:: saveprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile)abrufen.

Ein Profil enthält mehrere Objekte, die verschiedene Aspekte des Profils (z. b. Streams) steuern. Alle diese Objekte sind dem Profil Objekt untergeordnet. Sie erstellen diese Objekte nicht mit Erstellungs Funktionen wie bei den Hauptobjekten dieses SDK. Stattdessen enthalten die Schnittstellen des Profil Objekts Methoden, mit denen die untergeordneten Objekte erstellt werden.

Rufen Sie eine der folgenden Methoden auf, um ein Profil Objekt zu erstellen.



| Methode                                                                                | BESCHREIBUNG                                                                                                                                                     |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iwmprofilemanager:: kreateemptyprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) | Erstellt ein Profil Objekt ohne Profildaten.                                                                                                              |
| [**Iwmprofilemanager:: loadprofilebydata**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebydata)   | Erstellt ein Profil Objekt, das mit Daten aus einem Profil aufgefüllt ist, das als Zeichenfolge gespeichert wurde. Dies ist die einzige Möglichkeit, ein Profil Objekt mit Daten aus einem benutzerdefinierten Profil zu erstellen. |
| [**Iwmprofilemanager:: loadprofilebyid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)       | Erstellt ein Profil Objekt, das mit Daten aus einem Systemprofil aufgefüllt ist. Verwendet die GUID, um das gewünschte Systemprofil zu identifizieren.                                       |
| [**Iwmprofilemanager:: loadsystemprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile)   | Erstellt ein Profil Objekt, das mit Daten aus einem Systemprofil aufgefüllt ist. Verwendet den Profil Index, um das gewünschte Systemprofil zu identifizieren.                              |



 

Alle Methoden in der vorangehenden Tabelle legen einen Zeiger auf eine **iwmprofile** -Schnittstelle fest. Die anderen Schnittstellen des Profil Objekts können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.

Die folgenden Schnittstellen werden von jedem Profil Objekt unterstützt.



| Schnittstelle                                  | BESCHREIBUNG                                                                                                                                       |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iwmlanguagelist**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) | Verwaltet eine Liste der Sprachen, die von einer ASF-Datei unterstützt werden.                                                                                             |
| [**Iwmpacketsize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)     | Steuert die maximale Größe von Paketen in einer Datei.                                                                                                   |
| [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)   | Steuert die minimale Größe von Paketen in einer Datei. Erbt alle Methoden von **iwmpacketsize**.                                                 |
| [**Iwmprofile**](iwmprofile.md)           | Steuert die grundlegenden Einstellungen und Objekte, die in einem Profil enthalten sind.                                                                                    |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)         | Ruft die dem Profil zugeordnete Globally Unique Identifier (GUID) ab. Erbt alle Methoden von **iwmprofile**.                       |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)         | Steuert die Bandbreiten Freigabe und streampriorisierungsinformationen in einem Profil. Erbt alle Methoden von **iwmprofile** und **IWMProfile2**. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Profil-Manager-Objekt**](profile-manager-object.md)
</dt> <dt>

[**Profiles**](profiles.md)
</dt> </dl>

 

 




