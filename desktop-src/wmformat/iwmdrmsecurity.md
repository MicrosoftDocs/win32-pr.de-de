---
title: Iwmdrmsecurity-Schnittstelle
description: Die iwmdrmsecurity-Schnittstelle verwaltet eine Reihe von sicherheitsbezogenen Informationen für das Client Computer-und Digital Rights Management-Subsystem (DRM). Um eine Instanz dieser Schnittstelle zu erhalten, rufen Sie iwmdrmprovider-Erstellungsobjekt auf.
ms.assetid: 9439aedc-359d-4b2c-a88c-7b0e8eacb5a0
keywords:
- Iwmdrmsecurity-Schnittstelle Windows Media-Format
- Iwmdrmsecurity-Schnittstelle Windows Media-Format, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMSecurity
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d8b18e56c24fd0f3d3f86f217f547d626b74ded0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312755"
---
# <a name="iwmdrmsecurity-interface"></a>Iwmdrmsecurity-Schnittstelle

Die **iwmdrmsecurity** -Schnittstelle verwaltet eine Reihe von sicherheitsbezogenen Informationen für das Client Computer-und Digital Rights Management-Subsystem (DRM).

Um eine Instanz dieser Schnittstelle abzurufen, rufen Sie [**iwmdrmprovider:: builateobject**](iwmdrmprovider-createobject.md)auf. Übergeben Sie **IID \_ iwmdrmsecurity** als *riid* -Parameter.

## <a name="members"></a>Member

Die **iwmdrmsecurity** -Schnittstelle erbt von [**iwmdrmeventgenerator**](iwmdrmeventgenerator.md). **Iwmdrmsecurity** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwmdrmsecurity** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                      | BESCHREIBUNG                                                                                                      |
|:--------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**Checkcertforwiderruf**](iwmdrmsecurity-checkcertforrevocation.md)                     | Bestimmt, ob ein Zertifikat widerrufen wurde.<br/>                                                    |
| [**Getcontentenablersforrevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) | Ruft inhaltsenabler-Schnittstellen ab, die das Erneuern von Komponenten basierend auf gesperrten Zertifikaten ermöglichen.<br/> |
| [**Getcontentenablersfromhashes**](iwmdrmsecurity-getcontentenablersfromhashes.md)         | Ruft inhaltsenabler-Schnittstellen ab, die das Erneuern von Komponenten auf der Grundlage von Hash Zertifikaten ermöglichen.<br/>  |
| [**Getmachinecertificate**](iwmdrmsecurity-getmachinecertificate.md)                       | Ruft das Computer Zertifikat des DRM-Subsystems auf dem Client Computer ab.<br/>                        |
| [**Getrevocationdata**](iwmdrmsecurity-getrevocationdata.md)                               | Ruft eine Zertifikat Sperr Liste aus dem lokalen Speicher ab.<br/>                                         |
| [**Getrevocationdataversion**](iwmdrmsecurity-getrevocationdataversion.md)                 | Ruft die Versionsnummer einer Zertifikat Sperr Liste im lokalen Speicher ab.<br/>                     |
| [**Getsecurityversion**](iwmdrmsecurity-getsecurityversion.md)                             | Ruft die Version des DRM-Subsystems auf dem Client Computer ab.<br/>                                    |
| [**Performsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md)                       | Initiiert ein Sicherheitsupdate des DRM-Subsystems auf dem Client Computer.<br/>                              |
| [**"Abtrevocationdata"**](iwmdrmsecurity-setrevocationdata.md)                               | Legt eine Zertifikat Sperr Liste im lokalen Speicher fest.<br/>                                                |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Beispiel für DRM-Individualisierung**](drm-individualization-example.md)
</dt> <dt>

[**Schnittstellen**](drm-interfaces.md)
</dt> <dt>

[**Iwmdrmeventgenerator**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





