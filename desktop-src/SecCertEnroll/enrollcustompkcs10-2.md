---
description: Erstellt eine benutzerdefinierte PKCS \# 10-Anforderung und versucht, sie bei einer Unternehmenszertifizierungsstelle (CA) zu registrieren.
ms.assetid: ACBD3CE1-6A2A-47EE-9482-7398ABE15F5C
title: enrollCustomPKCS10_2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb88a2295217874a12da8b701a46f8dafe3db1cbf53d01273222e607195a789a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780039"
---
# <a name="enrollcustompkcs10_2"></a>enrollCustomPKCS10 \_ 2

Das Beispiel enrollCustomPKCS10 \_ 2 erstellt eine benutzerdefinierte PKCS \# 10-Anforderung und versucht, sie bei einer [*Unternehmenszertifizierungsstelle*](/windows/desktop/SecGloss/c-gly) (CA) zu registrieren.

## <a name="location"></a>Standort

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *%ProgramFiles%* \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollCustomPKCS10 \_ 2 installiert.

## <a name="discussion"></a>Diskussion (Discussion)

Das Beispiel enrollCustomPKCS10 \_ 2:

1.  Verarbeitet die Befehlszeilenargumente. Die Befehlszeile sollte den Namen einer Vorlage und den Namen eines Kryptografieanbieters enthalten.
2.  Erstellt ein [**IX509Enrollment-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) und initialisiert es unter Verwendung des Namens der in der Befehlszeile angegebenen Vorlage.
3.  Ruft die [*Zertifikatanforderung*](/windows/desktop/SecGloss/c-gly) aus dem Registrierungsobjekt ab.
4.  Ruft die innerste PKCS \# 10-Anforderung aus dem In Schritt 3 abgerufenen Zertifikatanforderungsobjekt ab.
5.  Ruft einen [*privaten Schlüssel*](/windows/desktop/SecGloss/p-gly) aus der PKCS \# 10-Anforderung ab.
6.  Erstellt eine [**ICspInformations-Auflistung,**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) fügt der Auflistung die verfügbaren Kryptografieanbieter hinzu und ruft dann ein [**ICspStatus-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) für den in der Befehlszeile angegebenen Anbieter ab.
7.  Legt das Statusobjekt für den privaten Schlüssel fest.
8.  Versucht, die [*Zertifikatanforderung*](/windows/desktop/SecGloss/c-gly)zu registrieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PKCS \# 10-Anforderung](pkcs--10-request.md)
</dt> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

 
