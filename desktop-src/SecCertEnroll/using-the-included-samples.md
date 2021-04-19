---
description: Die Zertifikatregistrierungs-API umfasst mehrere Beispiele, die Sie beim Erstellen von benutzerdefinierten Anwendungen unterstützen. Die meisten Beispiele werden mithilfe von C++ geschrieben, aber c#-und Visual Basic Scripting Edition-Beispiele (VBScript) sind ebenfalls enthalten.
ms.assetid: 70ac7b75-542c-4d79-85ce-4b1bac414879
title: Verwenden der enthaltenen Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd3cbf17d35e65ade52e97438d638cbd4f1489e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368939"
---
# <a name="using-the-included-samples"></a>Verwenden der enthaltenen Beispiele

Die Zertifikatregistrierungs-API umfasst mehrere Beispiele, die Sie beim Erstellen von benutzerdefinierten Anwendungen unterstützen. Die meisten Beispiele werden mithilfe von C++ geschrieben, aber c#-und Visual Basic Scripting Edition-Beispiele (VBScript) sind ebenfalls enthalten.

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, werden standardmäßig im Ordner " *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate \\ Registrierungs" die folgenden Beispiele installiert.



| Beispiel                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                | Sprache            |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| ["kreatecngcustomcmc"](createcngcustomcmc.md)                           | Erstellt ein Objekt vom Objekt "CMC Request" aus einer inneren geschachtelten PKCS \# 10-Anforderung.<br/>                                                                                                                                                                                                                                                                            | C++<br/>      |
| [gemeinsame Anmeldung](enrollcommon.md)                                       | Enthält die folgenden Hilfsfunktionen und-Makros, die von den enthaltenen Beispielen verwendet werden.<br/>                                                                                                                                                                                                                                                                | C++<br/>      |
| [Registrier customcmc](enrollcustomcmc.md)                                 | Erstellt eine CMC-Zertifikat Anforderung und registriert einen Computer in einer Zertifikatshierarchie.<br/>                                                                                                                                                                                                                                                            | C++<br/>      |
| [enrollCustomPKCS10](enrollcustompkcs10.md)                           | Erstellt eine benutzerdefinierte PKCS \# 10-Anforderung, übergibt sie an eine eigenständige Zertifizierungsstelle ( [*Certification Authority*](/windows/desktop/SecGloss/c-gly) , ca) und installiert das ausgegebene Zertifikat im [*Zertifikat Speicher*](/windows/desktop/SecGloss/c-gly).<br/> | C++<br/>      |
| [enrollCustomPKCS10 \_ 2](enrollcustompkcs10-2.md)                      | Erstellt eine benutzerdefinierte PKCS \# 10-Anforderung und versucht, Sie in einer Unternehmens Zertifizierungsstelle anzumelden.<br/>                                                                                                                                                                                                                                                               | C++<br/>      |
| [Einschreibung von "Einschreibung"](enrolleobocmc.md)                                     | Erstellt eine CMC-Zertifikat Anforderung im Auftrag eines anderen Benutzers und registriert den Benutzer in einer Zertifikatshierarchie.<br/>                                                                                                                                                                                                                                    | C++<br/>      |
| [Registrierungs frompublickey](enrollfrompublickey.md)                         | Initialisiert ein PKCS \# 10-Zertifikat Anforderungs Objekt, umschließt es in ein Objekt vom Typ "CMC Request", übermittelt die Anforderung "CMC" an eine Unternehmens Zertifizierungsstelle und speichert das von der Zertifizierungsstelle zurückgegebene Zertifikat in einer Datei.<br/>                                                                                                                                                      | C++<br/>      |
| [Registrierungsschlüssel archivalcmc](enrollkeyarchivalcmc.md)                       | Erstellt eine CMC-Zertifikat Anforderung zum Archivieren eines [*privaten Schlüssels*](/windows/desktop/SecGloss/p-gly) auf einer Zertifizierungsstelle.<br/>                                                                                                                                                                                                     | C++<br/>      |
| [registrinetstedcmc](enrollnestedcmc.md)                                 | Liest eine vorhandene CMC-Zertifikat Anforderung aus einer Datei, umschließt Sie in eine andere CMC-Anforderung, signiert diese äußere Anforderung, sendet Sie an eine Zertifizierungsstelle und speichert die Zertifikats Antwort von der Zertifizierungsstelle in einer Datei.<br/>                                                                                                                                                 | C++<br/>      |
| [enrollPKCS7](enrollpkcs7.md)                                         | Erstellt eine [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) -Anforderung von einem vorhandenen Zertifikat, indem die öffentlichen und privaten Schlüssel und die Zertifikat Vorlage geerbt werden. Im Beispiel wird der Benutzer in einer Zertifikat Hierarchie registriert und die Zertifikats Antwort installiert.<br/>                                   | C++<br/>      |
| [enrollRenewalPKCS7](enrollrenewalpkcs7.md)                           | Erstellt ein PKCS \# 7-Anforderungs Objekt, um ein vorhandenes Zertifikat zu erneuern.<br/>                                                                                                                                                                                                                                                                             | C++<br/>      |
| [Registrierungs simplemachinecert](enrollsimplemachinecert.md)                 | Registriert einen Computer in einer Zertifikat Hierarchie mithilfe einer Vorlage, eines Zertifikat anzeigen Amens und der Zertifikat Beschreibung.<br/>                                                                                                                                                                                                                 | C++, VSB<br/> |
| [Registrierungs simpleusercert](enrollsimpleusercert.md)                       | Registriert einen Endbenutzer mit einer Zertifizierungsstelle, indem eine Vorlage, der Antragsteller Name und die Länge des Schlüssels in Bits verwendet werden.<br/>                                                                                                                                                                                                                                       | C++, C #<br/> |
| [enrollWithIX509EnrollmentHelper](enrollwithix509enrollmenthelper.md) | Veranschaulicht, wie Sie das HTTP-Protokoll von Windows 7 zum Registrieren eines Zertifikats in einer Unternehmens Zertifizierungsstelle verwenden.<br/>                                                                                                                                                                                                                                                | C#<br/>      |
| [InstallResponse-frompfx](installresponsefrompfx.md)                   | Installiert ein registriertes Zertifikat aus einer PFX-Datei (Personal Information Exchange) im Zertifikat Speicher.<br/>                                                                                                                                                                                                                                      | C++<br/>      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Zertifikatregistrierungs-API](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

