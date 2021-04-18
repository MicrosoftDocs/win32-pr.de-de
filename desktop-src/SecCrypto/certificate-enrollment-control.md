---
description: Die Zertifikat Registrierungs Steuerung kann von einer Anwendung verwendet werden, die anfordern muss, dass ein Zertifikat für einen benannten Betreff ausgestellt wird.
ms.assetid: ce6661b0-7ed2-452f-a54c-6705d14f3298
title: Zertifikat Registrierungs Steuerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e417a9db7984cbb58b7c2e3b51d828b6d61a97b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340185"
---
# <a name="certificate-enrollment-control"></a>Zertifikat Registrierungs Steuerung

Die Zertifikat Registrierungs Steuerung kann von einer Anwendung verwendet werden, die anfordern muss, dass ein Zertifikat für einen benannten Betreff ausgestellt wird. Es ist so konzipiert, dass Daten in Form einer binären Zeichenfolge (BSTR) akzeptiert werden. Die Daten können von einer Webseite oder von der Benutzeroberfläche des Visual Basic oder Visual C++ Entwicklungssystems stammen. Bei der Ausgabe der Zertifikat Registrierungs Steuerung handelt es sich um eine PKCS \# 10-Zertifikat Anforderung, die an eine [*Zertifizierungsstelle (Certification Authority*](../secgloss/c-gly.md) , ca) gesendet werden kann.

![Zertifikat Registrierungs Steuerung](images/xen-arch.png)

Erforderliche Informationen zum Benutzer, der Zertifikat Antragsteller, werden von der Benutzeroberfläche gesammelt. Diese Informationen werden als BSTR-Eingabe für die Zertifikat Registrierungs Steuerung bereitgestellt. Die Zertifikat Registrierungs Steuerung generiert den entsprechenden Signatur Schlüssel, Schlüsselaustausch Schlüssel oder beide Schlüsselpaare. Das-Steuerelement generiert und signiert dann eine PKCS \# 10- [*Zertifikat Anforderung*](../secgloss/c-gly.md) mit dem generierten [*privaten Schlüssel*](../secgloss/p-gly.md). Die Zertifikat Registrierungs Steuerung verknüpft dann das Schlüsselpaar mit einem temporären Dummy-Zertifikat, das im Anforderungs Speicher gespeichert wird, bis das ausgestellte Zertifikat von einer Zertifizierungsstelle zurückgegeben wird. Schließlich sendet die Anwendung die PKCS \# 10-Zertifikat Anforderung an eine Zertifizierungsstelle.

Wenn die Zertifizierungsstelle die Zertifikat Anforderung genehmigt, erstellt die Zertifizierungsstelle ein Zertifikat, das den öffentlichen Schlüssel enthält. Die Zertifizierungsstelle signiert außerdem das Zertifikat und gibt es zurück.

Wenn das angeforderte Zertifikat von der Zertifizierungsstelle zurückgegeben wird, übergibt die Anwendung die PKCS \# 7-Nachricht an das Zertifikat Registrierungs Steuerelement, in dem das Zertifikat oder die Zertifikatskette aus der PKCS 7-Nachricht extrahiert wird \# . Das Zertifikat und alle anderen Zertifikate in der Vertrauenskette werden in einem [*Zertifikat Speicher*](../secgloss/c-gly.md)gespeichert. Das zurückgegebene Zertifikat wird in keiner Weise geändert. Alle Zertifikat fähigen Anwendungen können nun aus dem Speicher auf dieses Zertifikat zugreifen.

Die Smartcard-Registrierungs Steuerung wird von einem Administrator verwendet, um sich im Auftrag von smartcardbenutzern anzumelden. Der Registrierungsvorgang führt dazu, dass ein Zertifikat ausgestellt wird, das auf der Smartcard eines Benutzers gespeichert wird.

Die Smartcard-Registrierungs Steuerung ist in Scrdenrl.dll enthalten und besteht aus einem Objekt ( **scrdenr**). In Scrdenrl.dll sind keine anderen Objekte enthalten. Dieses Smartcard-Registrierungs Objekt kann mit einer Skriptsprache verwendet werden, z. b. Visual Basic Scripting Edition (VBScript).

Auf dem Computer, auf dem die Smartcard-Registrierungs Steuerung ausgeführt wird, muss ein [*Smartcardleser*](../secgloss/r-gly.md) installiert sein.

Außerdem muss der Smartcard-Aussteller ein Signaturzertifikat erhalten, das auf der Zertifikat Vorlage "anmelmentagent&quot; basiert. Dieses Signaturzertifikat wird verwendet, um die Zertifikat Anforderung zu signieren, die im Auftrag des smartcardempfängers generiert wurde. Standardmäßig werden Domänen Administratoren die Berechtigung zum Anfordern eines Zertifikats auf der Grundlage der Vorlage &quot;Registrierungs-Agent&quot; erteilt. Einem anderen Benutzer kann die Berechtigung erteilt werden, sich für ein anmeldungsagentzertifikat zu registrieren (über das MMC-Snap-in &quot;Active Directory Standorte und Dienste"); Dies ermöglicht es diesem Benutzer jedoch, eine Smartcard mit Domänen Administrator Berechtigungen selbst auszugeben.

 

 
