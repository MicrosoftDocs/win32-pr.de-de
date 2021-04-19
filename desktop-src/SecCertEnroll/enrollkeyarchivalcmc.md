---
description: Erstellt eine CMC-Zertifikat Anforderung zum Archivieren eines privaten Schlüssels auf einer Zertifizierungsstelle (Certification Authority, ca).
ms.assetid: b063989a-fe92-4c2c-9d66-8a14bc830f6b
title: Registrierungsschlüssel archivalcmc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 144f5f063834c156da5058fbc34f66ebdb76eb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346993"
---
# <a name="enrollkeyarchivalcmc"></a>Registrierungsschlüssel archivalcmc

Das Registrierungs keyarchivalcmc-Beispiel erstellt eine CMC-Zertifikat Anforderung zum Archivieren eines privaten Schlüssels auf einer Zertifizierungsstelle (Certification Authority, ca). Weitere Informationen finden Sie unter [CMC-Schlüssel Archivierungs Anforderung](cmc-key-archival-request.md).

## <a name="location"></a>Standort

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Einschreibung \\ VC \\ registrierungskeyarchivalcmc installiert.

## <a name="discussion"></a>Diskussion

Das Beispiel "registrikeyarchivalcmc":

1.  Verarbeitet die Befehlszeilenargumente. Die Befehlszeile muss den Namen der Zertifikat Vorlage enthalten, die für die Anmeldung verwendet werden soll.
2.  Erstellt ein [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) Certificate Request-Objekt und initialisiert es mit dem Vorlagen Namen für einen Endbenutzer Kontext.
3.  Legt die [**archiveprivatekey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey) -Eigenschaft für die CMC-Anforderung fest.
4.  Erstellt ein [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) -Objekt und verwendet es, um eine Zeichenfolge abzurufen, die die Zertifizierungsstellen Konfiguration enthält.
5.  Erstellt ein CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) -Objekt und verwendet es, um das Exchange-Zertifikat für die Zertifizierungsstelle abzurufen.
6.  Erstellt ein [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt, initialisiert es mithilfe der CMC-Anforderung, erstellt eine Base64-codierte Zeichenfolge, die die Schlüssel Archivierungs Anforderung enthält, und sendet Sie an die Zertifizierungsstelle.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CMC-Schlüssel Archivierungs Anforderung](cmc-key-archival-request.md)
</dt> <dt>

[CMC-Anforderung](cmc-request.md)
</dt> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

 
