---
description: Registriert einen Endbenutzer mit einer Zertifizierungsstelle (Certification Authority, ca), indem er eine Vorlage, den Antragsteller Namen und die Länge des Schlüssels in Bits verwendet.
ms.assetid: ee290c78-dbfa-4414-8489-aa886360652b
title: Registrierungs simpleusercert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0956455afa814af54cc86661f2d7733a6d16dd8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042486"
---
# <a name="enrollsimpleusercert"></a>Registrierungs simpleusercert

Das Beispiel "anmelsimpleusercert" registriert einen Endbenutzer mit einer Zertifizierungsstelle (Certification Authority, ca), indem er eine Vorlage, den Antragsteller Namen und die Länge des Schlüssels in Bits verwendet.

## <a name="location"></a>Standort

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird eine C++-Version des Beispiels standardmäßig im Ordner *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Registrierung \\ VC \\ registrisimpleusercert installiert. Eine c#-Version ist im Ordner *% Program Files%* \\ Microsoft SDRs \\ Windows \\ v 7.0 \\ Samples \\ X509 Certificate Einschreibung \\ csharp \\ registrisimpleusercert installiert.

## <a name="discussion"></a>Diskussion

Das Beispiel "registrisimpleusercert":

1.  Verarbeitet die Befehlszeilenargumente. Die Befehlszeile muss den Namen der Vorlage, den Antragsteller Namen und die Schlüssellänge enthalten.
2.  Erstellt ein [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt und initialisiert es mithilfe der Vorlage.
3.  Ruft das Objekt der inneren Zertifikat Anforderung aus dem Anmeld-Objekt ab und fragt es nach dem [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Objekt ab. Die innerste Anforderung ist immer eine PKCS \# 10-Anforderung.
4.  Ruft das [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) -Objekt aus der PKCS \# 10-Anforderung ab und legt die in der Befehlszeile angegebene Schlüssellänge fest.
5.  Erstellt ein [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) -Objekt, verwendet es, um den X. 500-Betreffnamen zu codieren, und fügt den Namen der PKCS \# 10-Anforderung hinzu.
6.  Versucht, den Endbenutzer bei der Zertifizierungsstelle zu registrieren und den Fortschritt des Registrierungsvorgangs zu überwachen. Die Funktion "checkenrollstatus" wird in der Datei "registricommon. cpp" definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PKCS \# 10-Anforderung](pkcs--10-request.md)
</dt> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

 



