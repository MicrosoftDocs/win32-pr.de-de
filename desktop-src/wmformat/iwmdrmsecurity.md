---
title: IWMDRMSecurity-Schnittstelle
description: Die IWMDRMSecurity-Schnittstelle verwaltet eine Vielzahl von sicherheitsbezogenen Informationen für den Clientcomputer und das DRM-Subsystem (Digital Rights Management). Um eine Instanz dieser Schnittstelle zu erhalten, rufen Sie IWMDRMProvider CreateObject auf.
ms.assetid: 9439aedc-359d-4b2c-a88c-7b0e8eacb5a0
keywords:
- IWMDRMSicherheitsschnittstelle – Windows-Medienformat
- IWMDRMSecurity interface windows Media Format , beschrieben
topic_type:
- apiref
api_name:
- IWMDRMSecurity
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31593dda35e7fa33540faa3c954f1901e1afa227372b25326c0f36154d443153
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839732"
---
# <a name="iwmdrmsecurity-interface"></a>IWMDRMSecurity-Schnittstelle

Die **IWMDRMSecurity-Schnittstelle** verwaltet eine Vielzahl von sicherheitsbezogenen Informationen für den Clientcomputer und das DRM-Subsystem (Digital Rights Management).

Um eine Instanz dieser Schnittstelle zu erhalten, rufen [**Sie IWMDRMProvider::CreateObject auf.**](iwmdrmprovider-createobject.md) Übergeben **Sie IID \_ IWMDRMSecurity** als *riid-Parameter.*

## <a name="members"></a>Member

Die **IWMDRMSecurity-Schnittstelle** erbt von [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md). **IWMDRMSecurity** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWMDRMSecurity-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                      | Beschreibung                                                                                                      |
|:--------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**CheckCertForRevocation**](iwmdrmsecurity-checkcertforrevocation.md)                     | Bestimmt, ob ein Zertifikat widerrufen wurde.<br/>                                                    |
| [**GetContentEnablersForRevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) | Ruft Schnittstellen für die Inhaltsermöglichung ab, die die Erneuerung von Komponenten basierend auf widerrufenen Zertifikaten ermöglichen.<br/> |
| [**GetContentEnablersFromHashes**](iwmdrmsecurity-getcontentenablersfromhashes.md)         | Ruft Schnittstellen für die Inhaltsermöglichung ab, die die Erneuerung von Komponenten basierend auf Hashzertifikaten ermöglichen.<br/>  |
| [**GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md)                       | Ruft das Computerzertifikat des DRM-Subsystems auf dem Clientcomputer ab.<br/>                        |
| [**GetRevocationData**](iwmdrmsecurity-getrevocationdata.md)                               | Ruft eine Zertifikatsperrliste aus dem lokalen Speicher ab.<br/>                                         |
| [**GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md)                 | Ruft die Versionsnummer einer Zertifikatsperrliste im lokalen Speicher ab.<br/>                     |
| [**GetSecurityVersion**](iwmdrmsecurity-getsecurityversion.md)                             | Ruft die Version des DRM-Subsystems auf dem Clientcomputer ab.<br/>                                    |
| [**PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md)                       | Initiiert ein Sicherheitsupdate für das DRM-Subsystem auf dem Clientcomputer.<br/>                              |
| [**SetRevocationData**](iwmdrmsecurity-setrevocationdata.md)                               | Legt eine Zertifikatsperrliste im lokalen Speicher fest.<br/>                                                |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DRM-Individualisierungsbeispiel**](drm-individualization-example.md)
</dt> <dt>

[**Schnittstellen**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





