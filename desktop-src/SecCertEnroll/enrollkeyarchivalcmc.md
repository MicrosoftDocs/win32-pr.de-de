---
description: Erstellt eine CMC-Zertifikatanforderung zum Archivieren eines privaten Schlüssels in einer Zertifizierungsstelle.
ms.assetid: b063989a-fe92-4c2c-9d66-8a14bc830f6b
title: enrollKeyArchivalCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9e2e9856309560e982e7e1dda7ba724fefd0759e6fa10196b321eb66947cf64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882950"
---
# <a name="enrollkeyarchivalcmc"></a>enrollKeyArchivalCMC

Im Beispiel enrollKeyArchivalCMC wird eine CMC-Zertifikatanforderung zum Archivieren eines privaten Schlüssels bei einer Zertifizierungsstelle erstellt. Weitere Informationen finden Sie unter [CMC-Schlüsselarchivierungsanforderung.](cmc-key-archival-request.md)

## <a name="location"></a>Standort

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *%ProgramFiles%* \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollKeyArchivalCMC installiert.

## <a name="discussion"></a>Diskussion (Discussion)

Das beispiel enrollKeyArchivalCMC:

1.  Verarbeitet die Befehlszeilenargumente. Die Befehlszeile sollte den Namen der Zertifikatvorlage enthalten, die für die Registrierung verwendet werden soll.
2.  Erstellt ein [**IX509CertificateRequestCmc-Zertifikatanforderungsobjekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) und initialisiert es für einen Endbenutzerkontext unter Verwendung des Vorlagennamens.
3.  Legt die [**ArchivePrivateKey-Eigenschaft**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey) für die CMC-Anforderung fest.
4.  Erstellt ein [**ICertConfig-Objekt**](/windows/desktop/api/certcli/nn-certcli-icertconfig) und verwendet es, um eine Zeichenfolge abzurufen, die die Zertifizierungsstellenkonfiguration enthält.
5.  Erstellt ein [**CryptoAPI-ICertRequest2-Objekt**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) und verwendet es zum Abrufen des Austauschzertifikats für die Zertifizierungsstelle.
6.  Erstellt ein [**IX509Enrollment-Objekt,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) initialisiert es mithilfe der CMC-Anforderung, erstellt eine Base64-codierte Zeichenfolge, die die Schlüsselarchivierungsanforderung enthält, und sendet es an die Zertifizierungsstelle.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CMC-Schlüsselarchivierungsanforderung](cmc-key-archival-request.md)
</dt> <dt>

[CMC-Anforderung](cmc-request.md)
</dt> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

 
