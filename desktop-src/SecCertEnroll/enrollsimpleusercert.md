---
description: Registriert einen Endbenutzer bei einer Zertifizierungsstelle mithilfe einer Vorlage, des Betreffnamens und der Länge des Schlüssels in Bits.
ms.assetid: ee290c78-dbfa-4414-8489-aa886360652b
title: enrollSimpleUserCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4763e3ae68404e47207dccdb75c759fc30394e849bee07a71f2c54c649347a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119669910"
---
# <a name="enrollsimpleusercert"></a>enrollSimpleUserCert

Im Beispiel enrollSimpleUserCert wird ein Endbenutzer bei einer Zertifizierungsstelle registriert, indem eine Vorlage, der Name des Betreffs und die Länge des Schlüssels in Bits verwendet werden.

## <a name="location"></a>Standort

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird standardmäßig eine C++-Version des Beispiels im Ordner *%ProgramFiles%* \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollSimpleUserCert installiert. Eine C#-Version wird im Ordner *%ProgramFiles%* \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples \\ X509 Certificate Enrollment \\ CSharp \\ EnrollSimpleUserCert installiert.

## <a name="discussion"></a>Diskussion (Discussion)

Beispiel für enrollSimpleUserCert:

1.  Verarbeitet die Befehlszeilenargumente. Die Befehlszeile sollte den Namen der Vorlage, den Betreffnamen und die Schlüssellänge enthalten.
2.  Erstellt ein [**IX509Enrollment-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) und initialisiert es mithilfe der Vorlage.
3.  Ruft das Anforderungsobjekt des inneren Zertifikats aus dem Registrierungsobjekt ab und fragt es nach dem [**IX509CertificateRequestPkcs10-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) ab. Die innerste Anforderung ist immer eine PKCS \# 10-Anforderung.
4.  Ruft das [**IX509PrivateKey-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) aus der PKCS 10-Anforderung ab und legt die in der \# Befehlszeile angegebene Schlüssellänge fest.
5.  Erstellt ein [**IX500DistinguishedName-Objekt,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) verwendet es zum Codieren des X.500-Betreffnamens und fügt den Namen der PKCS \# 10-Anforderung hinzu.
6.  Versucht, den Endbenutzer bei der Zertifizierungsstelle zu registrieren, und überwacht den Fortschritt des Registrierungsprozesses. Die checkEnrollStatus-Funktion ist in enrollCommon.cpp definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PKCS \# 10-Anforderung](pkcs--10-request.md)
</dt> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

 



