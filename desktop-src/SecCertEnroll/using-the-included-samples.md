---
description: Die Zertifikatregistrierungs-API enthält mehrere Beispiele, die Sie beim Erstellen benutzerdefinierter Anwendungen unterstützen. Die meisten Beispiele werden mit C++ geschrieben, aber auch C#- und Visual Basic Scripting Edition-Beispiele (VBScript) sind enthalten.
ms.assetid: 70ac7b75-542c-4d79-85ce-4b1bac414879
title: Verwenden der enthaltenen Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511d9d5424455c1b54c6bd03cc72138b3672b256d535dcbdaf31d2393b2cb5f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127203"
---
# <a name="using-the-included-samples"></a>Verwenden der enthaltenen Beispiele

Die Zertifikatregistrierungs-API enthält mehrere Beispiele, die Sie beim Erstellen benutzerdefinierter Anwendungen unterstützen. Die meisten Beispiele werden mit C++ geschrieben, aber auch C#- und Visual Basic Scripting Edition-Beispiele (VBScript) sind enthalten.

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, werden die folgenden Beispiele standardmäßig im Ordner *%ProgramFiles%* \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ installiert.



| Beispiel                                                                 | Beschreibung                                                                                                                                                                                                                                                                                                                                                | Sprache            |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| [createCNGCustomCMC](createcngcustomcmc.md)                           | Erstellt ein CMC-Anforderungsobjekt aus einer inneren geschachtelten PKCS \# 10-Anforderung.<br/>                                                                                                                                                                                                                                                                            | C++<br/>      |
| [enrollCommon](enrollcommon.md)                                       | Enthält die folgenden Hilfsfunktionen und Makros, die von den enthaltenen Beispielen verwendet werden.<br/>                                                                                                                                                                                                                                                                | C++<br/>      |
| [enrollCustomCMC](enrollcustomcmc.md)                                 | Erstellt eine CMC-Zertifikatanforderung und registriert einen Computer in einer Zertifikathierarchie.<br/>                                                                                                                                                                                                                                                            | C++<br/>      |
| [enrollCustomPKCS10](enrollcustompkcs10.md)                           | Erstellt eine benutzerdefinierte PKCS \# 10-Anforderung, sendet sie an eine eigenständige [*Zertifizierungsstelle*](/windows/desktop/SecGloss/c-gly) und installiert das ausgestellte Zertifikat im [*Zertifikatspeicher.*](/windows/desktop/SecGloss/c-gly)<br/> | C++<br/>      |
| [enrollCustomPKCS10 \_ 2](enrollcustompkcs10-2.md)                      | Erstellt eine benutzerdefinierte PKCS \# 10-Anforderung und versucht, sie bei einer Unternehmenszertifizierungsstelle zu registrieren.<br/>                                                                                                                                                                                                                                                               | C++<br/>      |
| [enrollEOBOCMC](enrolleobocmc.md)                                     | Erstellt eine CMC-Zertifikatanforderung im Namen eines anderen Benutzers und registriert den Benutzer in einer Zertifikathierarchie.<br/>                                                                                                                                                                                                                                    | C++<br/>      |
| [enrollFromPublicKey](enrollfrompublickey.md)                         | Initialisiert ein PKCS \# 10-Zertifikatanforderungsobjekt, umschließt es in einem CMC-Anforderungsobjekt, sendet die CMC-Anforderung an eine Unternehmenszertifizierungsstelle und speichert das von der Zertifizierungsstelle zurückgegebene Zertifikat in einer Datei.<br/>                                                                                                                                                      | C++<br/>      |
| [enrollKeyArchivalCMC](enrollkeyarchivalcmc.md)                       | Erstellt eine CMC-Zertifikatanforderung zum Archivieren eines [*privaten Schlüssels*](/windows/desktop/SecGloss/p-gly) auf einer Zertifizierungsstelle.<br/>                                                                                                                                                                                                     | C++<br/>      |
| [enrollNestedCMC](enrollnestedcmc.md)                                 | Liest eine vorhandene CMC-Zertifikatanforderung aus einer Datei, umschließt sie in einer anderen CMC-Anforderung, signiert diese äußere Anforderung, sendet sie an eine Zertifizierungsstelle und speichert die Zertifikatantwort von der Zertifizierungsstelle in einer Datei.<br/>                                                                                                                                                 | C++<br/>      |
| [enrollPKCS7](enrollpkcs7.md)                                         | Erstellt eine [*PKCS \# 7-Anforderung*](/windows/desktop/SecGloss/p-gly) aus einem vorhandenen Zertifikat, indem der öffentliche und der private Schlüssel und die Zertifikatvorlage geerbt werden. Im Beispiel wird der Benutzer in einer Zertifikathierarchie registriert und die Zertifikatantwort installiert.<br/>                                   | C++<br/>      |
| [enrollRenewalPKCS7](enrollrenewalpkcs7.md)                           | Erstellt ein PKCS \# 7-Anforderungsobjekt, um ein vorhandenes Zertifikat zu erneuern.<br/>                                                                                                                                                                                                                                                                             | C++<br/>      |
| [enrollSimpleMachineCert](enrollsimplemachinecert.md)                 | Registriert einen Computer in einer Zertifikathierarchie mithilfe einer Vorlage, eines Zertifikatanzeigenamens und der Zertifikatbeschreibung.<br/>                                                                                                                                                                                                                 | C++, VBS<br/> |
| [enrollSimpleUserCert](enrollsimpleusercert.md)                       | Registriert einen Endbenutzer mit einer Zertifizierungsstelle mithilfe einer Vorlage, des Antragstellernamens und der Länge des Schlüssels in Bits.<br/>                                                                                                                                                                                                                                       | C++, C #<br/> |
| [enrollWithIX509EnrollmentHelper](enrollwithix509enrollmenthelper.md) | Veranschaulicht die Verwendung des HTTP-Protokolls Windows 7, um ein Zertifikat bei einer Unternehmenszertifizierungsstelle zu registrieren.<br/>                                                                                                                                                                                                                                                | C#<br/>      |
| [installResponseFromPFX](installresponsefrompfx.md)                   | Installiert ein registriertes Zertifikat aus einer PFX-Datei (Personal Information Exchange) im Zertifikatspeicher.<br/>                                                                                                                                                                                                                                      | C++<br/>      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Zertifikatregistrierungs-API](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

