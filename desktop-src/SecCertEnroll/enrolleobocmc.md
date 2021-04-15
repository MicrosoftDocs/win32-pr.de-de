---
description: Erstellt eine CMC-Zertifikat Anforderung im Auftrag eines anderen Benutzers und registriert den Benutzer in einer Zertifikatshierarchie.
ms.assetid: 14cc76c9-0e2b-498f-b058-244af6e9111e
title: Einschreibung von "Einschreibung"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca888d949054d695056d42045335f17dfca2f4d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526993"
---
# <a name="enrolleobocmc"></a>Einschreibung von "Einschreibung"

Das Ereignis "" "" "" "" "" "" "" "" Die Registrierung im Namen eines anderen Benutzers erfordert, dass die Zertifikat Anforderung mit einem Registrierungs-Agent-Zertifikat signiert wird.

## <a name="location"></a>Standort

Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Registrierung \\ VC Einschreibung \\ leobocmc installiert.

## <a name="discussion"></a>Diskussion

Das Beispiel "Einschreibung-obocmc":

1.  Verarbeitet die folgenden Befehlszeilenargumente:
    -   Der Name einer Zertifikat Vorlage.
    -   Der Name des Benutzers, der das Zertifikat anfordert.
    -   Der Name einer PFX-Datei (Personal Information Exchange), in der die Anforderung gespeichert werden soll.
    -   Ein Kennwort, das mit der PFX-Datei verwendet werden soll.
    -   Ein optionaler Name des Registrierungs-Agents. Die Vorlage wird verwendet, um ein anmeldungsagentzertifikat zu erstellen, wenn keine im Zertifikat Speicher vorhanden ist.
2.  Erstellt ein [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) -Objekt und initialisiert es mithilfe der Zertifikat Vorlage, die in der Befehlszeile angegeben ist.
3.  Fügt dem Objekt "CMC Request" den Namen des Anforderers hinzu.
4.  Ruft ein vorhandenes Registrierungs-Agent-Zertifikat ab oder erstellt, sofern nicht gefunden, eine Zertifikat Anforderung von der in der Befehlszeile angegebenen anmeldungsagentvorlage und versucht, es zu registrieren.
5.  Überprüft die Zertifikat Kette, die das anmeldungsagentzertifikat enthält.
6.  Erstellt ein [**isignercertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) -Objekt, initialisiert es mit dem Registrierungs-Agent-Zertifikat, ruft die [**isignercertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) -Auflistung aus dem Objekt "CMC Request" ab und fügt das Registrierungs-Agent-Signaturzertifikat der Auflistung hinzu. Das [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt, das im nächsten Schritt erläutert wird, verwendet das Zertifikat zum Signieren der CMC-Anforderung.
7.  Erstellt ein [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt, initialisiert es mithilfe der CMC-Anforderung, versucht, es zu registrieren, und überprüft den Fortschritt des Registrierungsprozesses.
8.  Exportiert das installierte Zertifikat in eine PFX-Datei. Die Datei wird mit dem in der Befehlszeile angegebenen Kennwort geschützt. Die encodedefilew-Funktion ist in der Datei "registricommon. cpp" definiert.
9.  Löscht das Zertifikat aus dem Zertifikat Speicher. Die im folgenden Codebeispiel verwendeten Funktionen finden Sie in der CryptoAPI-Dokumentation.
10. Löscht den privaten Schlüssel vom Computer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CMC eobo-Anforderung](cmc-eobo-request.md)
</dt> <dt>

[PKCS \# 10-Anforderung](pkcs--10-request.md)
</dt> <dt>

[Verwenden der enthaltenen Beispiele](using-the-included-samples.md)
</dt> </dl>

 

 



