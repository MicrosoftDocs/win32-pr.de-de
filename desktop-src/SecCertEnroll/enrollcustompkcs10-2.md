---
description: Erstellt eine benutzerdefinierte PKCS \# 10-Anforderung und versucht, Sie in einer Unternehmens Zertifizierungsstelle (Certification Authority, ca) zu registrieren.
ms.assetid: ACBD3CE1-6A2A-47EE-9482-7398ABE15F5C
title: enrollCustomPKCS10_2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d20615826bb72b6282144b72a394cde41e35910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357390"
---
# <a name="enrollcustompkcs10_2"></a>enrollCustomPKCS10 \_ 2

Das \_ Beispiel enrollCustomPKCS10 2 erstellt eine benutzerdefinierte PKCS \# 10-Anforderung und versucht, Sie in einer Unternehmens [*Zertifizierungsstelle (Certification Authority*](/windows/desktop/SecGloss/c-gly) , ca) zu registrieren.

## <a name="location"></a>Standort

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Einschreibung \\ VC \\ enrollCustomPKCS10 2 installiert \_ .

## <a name="discussion"></a>Diskussion

Das \_ Beispiel enrollCustomPKCS10 2:

1.  Verarbeitet die Befehlszeilenargumente. Die Befehlszeile sollte den Namen einer Vorlage und den Namen eines Kryptografieanbieters enthalten.
2.  Erstellt ein [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt und initialisiert es mit dem Namen der Vorlage, die in der Befehlszeile angegeben ist.
3.  Ruft die [*Zertifikat Anforderung*](/windows/desktop/SecGloss/c-gly) aus dem Anmeld ungs Objekt ab.
4.  Ruft die innerste PKCS \# 10-Anforderung aus dem Zertifikat Anforderungs Objekt ab, das in Schritt 3 abgerufen wurde.
5.  Ruft einen [*privaten Schlüssel*](/windows/desktop/SecGloss/p-gly) aus der PKCS \# 10-Anforderung ab.
6.  Erstellt eine [**icspinformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) -Auflistung und fügt der Auflistung die verfügbaren Kryptografieanbieter hinzu und ruft dann ein [**icspstatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) -Objekt für den Anbieter ab, der in der Befehlszeile angegeben ist.
7.  Legt das Status Objekt für den privaten Schlüssel fest.
8.  Versucht, die [*Zertifikat Anforderung*](/windows/desktop/SecGloss/c-gly)zu registrieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PKCS \# 10-Anforderung](pkcs--10-request.md)
</dt> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

 
