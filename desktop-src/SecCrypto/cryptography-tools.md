---
description: Kryptografietools bieten Befehlszeilen Tools für Code Signierung, Signatur Überprüfung und andere Kryptografieaufgaben.
ms.assetid: 21adbcfb-fadd-4818-9dc5-23bfd526b525
title: Kryptografietools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8003bb002bd8d203547779c96bc15491a5418169
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348976"
---
# <a name="cryptography-tools"></a>Kryptografietools

Kryptografietools bieten Befehlszeilen Tools für Code Signierung, Signatur Überprüfung und andere Kryptografieaufgaben.

## <a name="introduction-to-code-signing"></a>Einführung in die Codesignatur

Die Softwarebranche muss den Benutzern die Möglichkeit bieten, Code einschließlich im Internet veröffentlichtem Code zu vertrauen. Viele Webseiten enthalten nur statische Informationen, die mit geringem Risiko heruntergeladen werden können. Einige Seiten enthalten jedoch Steuerelemente und Anwendungen, die heruntergeladen und auf dem Computer eines Benutzers ausgeführt werden. Diese ausführbaren Dateien können riskant heruntergeladen und ausgeführt werden.

Software in Paketen verwendet Branding und vertrauenswürdige Vertriebsniederlassungen, um Benutzer ihrer Integrität zu gewährleisten. diese Garantien sind jedoch nicht verfügbar, wenn Code über das Internet übertragen wird. Darüber hinaus kann das Internet selbst keine Garantie bezüglich der Identität des Software Erstellers bereitstellen. Und es kann nicht garantiert werden, dass Software, die heruntergeladen wurde, nach der Erstellung nicht geändert wurde. Browser können eine Warnmeldung darstellen, in der die möglichen Gefahren beim Herunterladen von Daten in einer beliebigen Art erläutert werden. Browser können jedoch nicht überprüfen, ob der Code für die Ansprüche gilt. Es muss ein aktiveren Ansatz ergriffen werden, damit das Internet für die Software Verteilung ein zuverlässiges Mittel ist.

Eine Möglichkeit, die Authentizität und [*Integrität*](../secgloss/i-gly.md) von Dateien sicherzustellen, ist das Anfügen [*digitaler Signaturen*](../secgloss/d-gly.md) an diese Dateien. Eine digitale Signatur, die an eine Datei angefügt ist, identifiziert den Verteiler dieser Datei positiv und stellt sicher, dass der Inhalt der Datei nach dem Erstellen der Signatur nicht geändert wurde.

Digitale Signaturen können mit den kryptografieapis von Microsoft erstellt und überprüft werden. Hintergrundinformationen zur Kryptografie und den [*CryptoAPI*](../secgloss/c-gly.md) -Funktionen finden Sie unter [Kryptografie Essentials](cryptography-essentials.md).

Ausführliche Informationen zu [*digitalen Signaturen*](../secgloss/d-gly.md), [*Zertifikaten*](../secgloss/c-gly.md)und [*Zertifikat speichern*](../secgloss/c-gly.md)finden Sie in den folgenden Themen:

-   [Hashes und digitale Signaturen](hashes-and-digital-signatures.md)
-   [Digitale Zertifikate](digital-certificates.md)
-   [Verwalten von Zertifikaten mit Zertifikat speichern](managing-certificates-with-certificate-stores.md)
-   [Zertifikat Vertrauensstellungs Überprüfung](certificate-trust-verification.md)

Kryptoapi-Tools unterstützen derzeit die Microsoft Authenticode-Technologie, da Softwarehersteller die folgenden Dateitypen für die Authenticode-Überprüfung signieren können.



| Dateinamenerweiterung                             | Inhalte                                                                                                                                                                                                                              |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| APPX<br/>                                | Installer-Dateien für eine Windows Store-Geräte-app.<br/>                                                                                                                                                                            |
| CAB<br/>                                 | Eigenständige Dateien, die für die Installation und Einrichtung der Anwendung verwendet werden. In einer CAB-Datei werden mehrere Dateien in einer Datei komprimiert. Sie finden Sie im Allgemeinen auf Microsoft-Software Verteilungs Datenträgern.<br/>                        |
| CAT<br/>                                 | Dateien, die digitale Finger [*Abdrücke*](../secgloss/t-gly.md) mehrerer Dateien enthalten. Eine. cat-Datei kann verwendet werden, um die Integrität der Dateien sicherzustellen, deren Fingerabdrücke Sie enthalten.<br/> |
| .dll<br/>                                 | Dateien, die ausführbare Funktionen enthalten.<br/>                                                                                                                                                                                   |
| .exe<br/>                                 | Dateien, die ausführbare Programme enthalten.<br/>                                                                                                                                                                                    |
| .js<br/> .vbs<br/> .wsf<br/>  | Windows Shell-Dateien für JScript oder Microsoft Visual Basic Scripting Edition (VBScript).<br/>                                                                                                                                    |
| .msi<br/> MSP<br/> MST<br/> | Windows Installer-Dateien.<br/>                                                                                                                                                                                                   |
| OCX<br/>                                 | Dateien, die Microsoft ActiveX-Steuerelemente enthalten.<br/>                                                                                                                                                                             |
| PS1<br/>                                 | Dateien, die PowerShell-Skripts enthalten.<br/>                                                                                                                                                                                     |
| STL<br/>                                 | Dateien, die eine [*Zertifikat Vertrauens Liste (Certificate Trust List*](../secgloss/c-gly.md) , CTL) enthalten.<br/>                                                                           |
| .sys<br/>                                 | Dateien, die Treiber Binärdateien enthalten.<br/>                                                                                                                                                                                        |



 

Informationen zu digitalen Signaturen finden Sie in den folgenden Dokumenten:

-   CCITT, Empfehlung X. 509, *das Directory-Authentication Framework*, Consulting Committee, International Telefon und Telegraph, International Telekommunikations Union, Geneva, 1989.
-   RSA-Laboratorien, *PKCS \# 7: kryptografischer Nachrichten Syntax Standard*. Version 1,5, November, 1993.
-   Schneier, Bruce, *angewendete Kryptografie*, 2D Ed. New York: John Wiley & Sons, 1996.
-   [https://www.rsa.com](https://www.rsa.com/)

> [!Note]  
> Diese Ressourcen sind möglicherweise in einigen Sprachen und Ländern oder Regionen nicht verfügbar.

 

## <a name="microsoft-cryptography-tools"></a>Kryptografietools von Microsoft

Die Veröffentlichungs Tools und die Signatur-dll werden im \\ Verzeichnis bin Ihrer Microsoft SDK-Installation installiert. Sie enthalten die folgenden Dateien.



| Dateiname                    | Bemerkungen                                                                                                                                                                                             |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cert2SPC.exe](cert2spc.md) | Erstellt ein [*Software Herausgeber Zertifikat*](../secgloss/s-gly.md) (SPC) nur zu Testzwecken.<br/> |
| [CertMgr.exe](certmgr.md)   | Verwaltet Zertifikate, CTLs und [*Zertifikat Sperr Listen*](../secgloss/c-gly.md) (CRLs).<br/>             |
| [MakeCat.exe](makecat.md)   | Erstellt eine nicht signierte Katalog Datei, die die Hashwerte eines Satzes von Dateien zusammen mit zugeordneten Attributen der einzelnen Dateien enthält.<br/>                                                               |
| [MakeCert.exe](makecert.md) | Erstellt ein [*X. 509*](../secgloss/x-gly.md) -Zertifikat nur zu Testzwecken.<br/>                                                                      |
| Pvk2pfx.exe                  | Konvertiert eine Software Herausgeber Zertifikatsdatei (. SPC) oder eine Datei mit einem privaten Schlüssel (. pvk) in das Dateiformat für den persönlichen Informationsaustausch (PFX).<br/>                                                   |
| [SetReg.exe](setreg.md)     | Legt Registrierungsschlüssel fest, die die Zertifikat Überprüfung steuern.<br/>                                                                                                                                |
| [SignTool.exe](signtool.md) | Signiert und Zeitstempel einer Datei. Außerdem prüft die Signatur einer Datei.<br/>                                                                                                              |



 

 

 
