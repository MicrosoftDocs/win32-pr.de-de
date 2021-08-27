---
description: Kryptografietools stellen Befehlszeilentools für die Codesignierung, Signaturüberprüfung und andere Kryptografieaufgaben zur Verfügung.
ms.assetid: 21adbcfb-fadd-4818-9dc5-23bfd526b525
title: Kryptografietools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9547ba1d3a13958859c2f0504c60a1a1bbe4a67403c9709bb57900b73ad3a50d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100980"
---
# <a name="cryptography-tools"></a>Kryptografietools

Kryptografietools stellen Befehlszeilentools für die Codesignierung, Signaturüberprüfung und andere Kryptografieaufgaben zur Verfügung.

## <a name="introduction-to-code-signing"></a>Einführung in die Codesignatur

Die Softwarebranche muss Benutzern die Möglichkeit bieten, Code zu vertrauen, einschließlich des im Internet veröffentlichten Codes. Viele Webseiten enthalten nur statische Informationen, die mit geringem Risiko heruntergeladen werden können. Einige Seiten enthalten jedoch Steuerelemente und Anwendungen, die heruntergeladen und auf dem Computer eines Benutzers ausgeführt werden sollen. Das Herunterladen und Ausführen dieser ausführbaren Dateien kann riskant sein.

Gepackte Software verwendet Branding und vertrauenswürdige Verkaufsstellen, um die Integrität der Benutzer sicherzustellen. Diese Garantien sind jedoch nicht verfügbar, wenn Code über das Internet übertragen wird. Darüber hinaus kann das Internet selbst keine Garantie für die Identität des Softwareerstellers bieten. Es kann auch nicht garantiert werden, dass heruntergeladene Software nach der Erstellung nicht geändert wurde. Browser können eine Warnmeldung anzeigen, in der erläutert wird, wie viele Daten heruntergeladen werden können. Browser können jedoch nicht überprüfen, ob es sich bei dem Code um den von ihm beanspruchten Code handelt. Es muss ein aktiverer Ansatz verfolgt werden, um das Internet zu einem zuverlässigen Medium für die Verteilung von Software zu machen.

Ein Ansatz zur Gewährleistung der [](../secgloss/i-gly.md) Authentizität und Integrität von Dateien ist das Anfügen [*digitaler Signaturen*](../secgloss/d-gly.md) an diese Dateien. Eine digitale Signatur, die an eine Datei angefügt ist, identifiziert den Verteiler dieser Datei positiv und stellt sicher, dass der Inhalt der Datei nach dem Erstellen der Signatur nicht geändert wurde.

Digitale Signaturen können mithilfe der Kryptografie-APIs von Microsoft erstellt und überprüft werden. Hintergrundinformationen zur Kryptografie und den [*CryptoAPI-Funktionen*](../secgloss/c-gly.md) finden Sie unter [Cryptography Essentials](cryptography-essentials.md).

Ausführliche Informationen zu digitalen [*Signaturen,*](../secgloss/d-gly.md) [*Zertifikaten*](../secgloss/c-gly.md)und [*Zertifikatspeichern*](../secgloss/c-gly.md)finden Sie in den folgenden Themen:

-   [Hashes und digitale Signaturen](hashes-and-digital-signatures.md)
-   [Digitale Zertifikate](digital-certificates.md)
-   [Verwalten von Zertifikaten mit Zertifikatspeichern](managing-certificates-with-certificate-stores.md)
-   [Überprüfung der Zertifikatvertrauensstellung](certificate-trust-verification.md)

Derzeit unterstützt CryptoAPI Tools die Microsoft Authenticode-Technologie, da Softwarehersteller die folgenden Dateitypen für die Authenticode-Überprüfung signieren können.



| Dateinamenerweiterung                             | Inhalte                                                                                                                                                                                                                              |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| APPX<br/>                                | Installerdateien für eine Windows Store-Geräte-App.<br/>                                                                                                                                                                            |
| CAB<br/>                                 | Eigenständige Dateien, die für die Anwendungsinstallation und -einrichtung verwendet werden. In einer Schränkdatei werden mehrere Dateien in einer Datei komprimiert. Sie befinden sich häufig auf Microsoft-Softwareverteilungsdatenträgern.<br/>                        |
| CAT<br/>                                 | Dateien, die digitale [*Fingerabdruckdateien mehrerer*](../secgloss/t-gly.md) Dateien enthalten. Eine CAT-Datei kann verwendet werden, um die Integrität der Dateien sicherzustellen, deren Fingerabdruck sie enthält.<br/> |
| .dll<br/>                                 | Dateien, die ausführbare Funktionen enthalten.<br/>                                                                                                                                                                                   |
| .exe<br/>                                 | Dateien, die ausführbare Programme enthalten.<br/>                                                                                                                                                                                    |
| .js<br/> .vbs<br/> .wsf<br/>  | Windows Shelldateien für JScript oder Microsoft Visual Basic Scripting Edition (VBScript).<br/>                                                                                                                                    |
| .msi<br/> MSP<br/> MST<br/> | Windows Installerdateien.<br/>                                                                                                                                                                                                   |
| OCX<br/>                                 | Dateien, die Microsoft ActiveX enthalten.<br/>                                                                                                                                                                             |
| PS1<br/>                                 | Dateien, die PowerShell-Skripts enthalten.<br/>                                                                                                                                                                                     |
| .stl<br/>                                 | Dateien, die eine [*Zertifikatvertrauensliste*](../secgloss/c-gly.md) (Certificate Trust List, CTL) enthalten.<br/>                                                                           |
| .sys<br/>                                 | Dateien, die Treiberbinärdateien enthalten.<br/>                                                                                                                                                                                        |



 

Informationen zum digitalen Signieren finden Sie in den folgenden Dokumenten:

-   CCITT, Recommendation X.509, *The Directory-Authentication Framework*,Lecommunications Committee, International Telephone and Soll, International Telecommunications Union, Geneva, 1989.
-   RSA Rsa Rsas, *PKCS \# 7: Kryptografischer Nachrichtensyntaxstandard*. Version 1.5, November 1993.
-   Automatischeier,Ige, *Applied Cryptography*, 2d ed. New York: John Wiley & Sons, 1996.
-   [https://www.rsa.com](https://www.rsa.com/)

> [!Note]  
> Diese Ressourcen sind in einigen Sprachen und Ländern oder Regionen möglicherweise nicht verfügbar.

 

## <a name="microsoft-cryptography-tools"></a>Microsoft Cryptography Tools

Die Veröffentlichungstools und die Signatur-DLL werden im \\ Bin-Verzeichnis Ihrer Microsoft SDK-Installation installiert. Sie enthalten die folgenden Dateien.



| Dateiname                    | Hinweise                                                                                                                                                                                             |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cert2SPC.exe](cert2spc.md) | Erstellt ein [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) nur zu Testzwecken.<br/> |
| [CertMgr.exe](certmgr.md)   | Verwaltet Zertifikate, CTLs und [*Zertifikatsperrlisten*](../secgloss/c-gly.md) (Certificate Revocation Lists, CRLs).<br/>             |
| [MakeCat.exe](makecat.md)   | Erstellt eine nicht signierte Katalogdatei, die die Hashes einer Gruppe von Dateien zusammen mit den zugeordneten Attributen jeder Datei enthält.<br/>                                                               |
| [MakeCert.exe](makecert.md) | Erstellt ein [*X.509-Zertifikat*](../secgloss/x-gly.md) nur zu Testzwecken.<br/>                                                                      |
| Pvk2pfx.exe                  | Konvertiert eine Zertifikatdatei des Softwareherausgebers (.spc) oder eine Datei mit privatem Schlüssel (PVK) in das PFX-Dateiformat (Personal Information Exchange).<br/>                                                   |
| [SetReg.exe](setreg.md)     | Legt Registrierungsschlüssel fest, die die Zertifikatüberprüfung steuern.<br/>                                                                                                                                |
| [SignTool.exe](signtool.md) | Signiert eine Datei und stempelt sie mit einem Zeitstempel. Darüber hinaus überprüft die Signatur einer Datei.<br/>                                                                                                              |



 

 

 
