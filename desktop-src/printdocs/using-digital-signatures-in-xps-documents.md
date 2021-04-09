---
description: In diesem Thema werden Überlegungen zur Verwendung der XPS-API für digitale Signaturen zum Hinzufügen digitaler Signaturen zu einem XPS-Dokument aufgeführt.
ms.assetid: 27c28313-d8db-4c40-9972-cb03bdaa125c
title: Verwenden der XPS Digital-Signatur-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9037a1442a44b082caec21309c94390b3f783e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864955"
---
# <a name="using-xps-digital-signature-api"></a>Verwenden der XPS Digital-Signatur-API

In diesem Thema werden Überlegungen zur Verwendung der XPS-API für digitale Signaturen zum Hinzufügen digitaler Signaturen zu einem XPS-Dokument aufgeführt.

Die XPS Digital Signature-API ermöglicht es Anwendungen, Benutzer aufzufordern, XPS-Dokumente zu signieren und Signaturen zu überprüfen, die in XPS-Dokumenten gefunden werden. Die XPS Digital Signature-API kann auf ein XPS-Dokument angewendet werden, ohne Sie in ein XPS-OM zu laden, und kann für XPS-dokumentstreams verwendet werden, die aus einem XPS-OM serialisiert werden.

Der Abschnitt " [XPS Digital Signature API Programming Tasks](#xps-digital-signature-api-programming-tasks) " enthält Themen, in denen beschrieben wird, wie Sie mit der XPS Digital Signature-API programmieren. In diesem Thema werden die folgenden Überlegungen für die Verwendung der XPS Digital Signature-API beim Hinzufügen von digitaler Signatur Unterstützung zu einer Anwendung aufgeführt.

-   [XPS Digital Signature API-Programmieraufgaben](#xps-digital-signature-api-programming-tasks)
-   [Besondere Hinweise zum Programmieren von XPS Digital Signature API](#special-notes-about-xps-digital-signature-api-programming)
    -   [Überprüfen digitaler Signaturen in einem XPS-Dokument](#verifying-digital-signatures-in-an-xps-document)
    -   [Signatur Richtlinie für digitale Signaturen](#digital-signature-signing-policy)
    -   [Einbetten einer Zertifikat Kette](#embedding-a-certificate-chain)
    -   [Verwenden der CERT- \_ Kontext Struktur](#using-the-cert\_context-structure)
-   [Zugehörige Themen](#related-topics)

## <a name="xps-digital-signature-api-programming-tasks"></a>XPS Digital Signature API-Programmieraufgaben

Dieser Abschnitt enthält Themen, in denen beschrieben wird, wie Programmieraufgaben mithilfe der XPS Digital Signature-API ausgeführt werden.

-   [Allgemeine Programmieraufgaben für digitale Signaturen](basic-digital-signature-programming-tasks.md)<dl>

[Initialisieren des Signatur-Managers](initialize-the-signature-manager.md)  
    [Signieren eines Dokuments](sign-a-document.md)  
    [Hinzufügen einer Signatur Anforderung zu einem XPS-Dokument](add-a-signature-request-to-a-document.md)  
    [Überprüfen von Dokument Signaturen](verify-document-signatures.md)  
    </dl>
-   [Weitere Programmieraufgaben für digitale Signaturen](advanced-digital-signature-programming-tasks.md)<dl>

[Laden eines Zertifikats aus einer Datei](load-a-certificate-from-a-file.md)  
    [Überprüfen, ob ein Zertifikat eine Signatur Methode unterstützt](verify-a-certificate-supports-a-signature-method.md)  
    [Überprüfen, ob das System eine Digest-Methode unterstützt](verify-a-certificate-supports-a-digest-method.md)  
    [Einbinden von Zertifikat Ketten in ein Dokument](embedding-certificate-trust-chains-in-a-document.md)  
    </dl>

## <a name="special-notes-about-xps-digital-signature-api-programming"></a>Besondere Hinweise zum Programmieren von XPS Digital Signature API

Die folgenden Themen erfordern einige besondere Überlegungen, wenn Sie die XPS Digital Signature-API verwenden.

-   [Überprüfen digitaler Signaturen in einem XPS-Dokument](#verifying-digital-signatures-in-an-xps-document)
-   [Signatur Richtlinie für digitale Signaturen](#digital-signature-signing-policy)
-   [Einbetten einer Zertifikat Kette](#embedding-a-certificate-chain)
-   [Verwenden der CERT- \_ Kontext Struktur](#using-the-cert\_context-structure)

### <a name="verifying-digital-signatures-in-an-xps-document"></a>Überprüfen digitaler Signaturen in einem XPS-Dokument

[**Ixpssignature:: Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) überprüft nur den signierten Inhalt, um zu bestimmen, dass er sich seit der Signierung nicht geändert hat. **Ixpssignature:: Verify** überprüft keines der Zertifikate, die zum Signieren des Dokument Inhalts verwendet wurden.

Weitere Informationen zu Zertifikaten und Kryptografie finden Sie unter Informationen [zur Kryptografie](/windows/desktop/SecCrypto/about-cryptography).

Ein Beispiel für die Überprüfung von Dokument Signaturen in einem Programm finden Sie unter [Überprüfen von Dokument Signaturen und Zertifikaten](verify-document-signatures.md).

### <a name="digital-signature-signing-policy"></a>Signatur Richtlinie für digitale Signaturen

Die Signatur Richtlinie für digitale Signaturen bestimmt, welche Teile eines XPS-Dokuments signiert sind. Eine Signatur Richtlinien Option besteht darin, die Signatur Beziehungen zu signieren, die mit dem Signatur Ursprungs Teil beginnen. Da sich die Signatur Beziehungen mit jeder hinzugefügten Signatur ändern, werden Signaturen, die unter dieser Richtlinie vorgenommen werden, beim Hinzufügen neuer Signaturen unterbrechen. Stellen Sie sicher, dass Sie die Auswirkungen und Auswirkungen der Einstellung dieser Richtlinie kennen. Andernfalls kann es zu unerwartetem oder unerwünschtem Verhalten kommen.

Weitere Informationen zum Signieren von Richtlinien finden Sie unter [**XPS \_ Sign \_ Policy**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy).

### <a name="embedding-a-certificate-chain"></a>Einbetten einer Zertifikat Kette

Die Zertifikate, die die Vertrauenskette eines bestimmten Zertifikats bilden, können einem XPS-Dokument hinzugefügt werden. Das Einbetten dieser Zertifikate kann es in Offline Szenarios vereinfachen, dass eine Anwendung die Zertifikate überprüft, die von einer digitalen Signatur verwendet werden.

Weitere Informationen zum Einbetten von Zertifikaten in ein XPS-Dokument finden Sie unter [Einbetten von Zertifikat Ketten in ein Dokument](embedding-certificate-trust-chains-in-a-document.md).

### <a name="using-the-cert_context-structure"></a>Verwenden der CERT- \_ Kontext Struktur

Der [**CERT- \_ Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) und die [**CERT \_ Info**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info) -Strukturen sind die Hauptdaten Strukturen, die Zertifikat Informationen enthalten. Weitere Informationen zur Verwendung dieser Strukturen finden Sie unter [Verwenden einer Zertifikat \_ Info-Datenstruktur](/windows/desktop/SecCrypto/using-a-cert-info-data-structure).

[**Zertifikat \_ Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) Strukturen, die von kryptografieapi-Funktionen zurückgegeben werden, müssen freigegeben werden, wenn Sie nicht mehr benötigt werden. Um eine **CERT- \_ Kontext** Struktur freizugeben, nennen Sie die [**certfreecertifikatecontext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) -Funktion.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Allgemeine Programmieraufgaben für digitale Signaturen](basic-digital-signature-programming-tasks.md)
</dt> <dt>

[Weitere Programmieraufgaben für digitale Signaturen](advanced-digital-signature-programming-tasks.md)
</dt> <dt>

[**CERT- \_ Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**Zertifikat \_ Informationen**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info)
</dt> <dt>

[**Certfreecertififeecontext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[**XPS- \_ Signatur \_ Richtlinie**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
