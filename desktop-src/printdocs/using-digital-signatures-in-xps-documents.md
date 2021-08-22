---
description: In diesem Thema werden Überlegungen zur Verwendung der API für digitale XPS-Signaturen zum Hinzufügen digitaler Signaturen zu einem XPS-Dokument aufgeführt.
ms.assetid: 27c28313-d8db-4c40-9972-cb03bdaa125c
title: Verwenden der XPS Digital-Signatur-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ea6e38704efa2a348a90fec247f37b9722857a3838b10233937e63dc37fdbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118469352"
---
# <a name="using-xps-digital-signature-api"></a>Verwenden der XPS Digital-Signatur-API

In diesem Thema werden Überlegungen zur Verwendung der API für digitale XPS-Signaturen zum Hinzufügen digitaler Signaturen zu einem XPS-Dokument aufgeführt.

Mit der XPS Digital Signature-API können Anwendungen Benutzer auffordern, XPS-Dokumente zu signieren und Signaturen in XPS-Dokumenten zu überprüfen. Die XPS Digital Signature-API kann auf ein XPS-Dokument angewendet werden, ohne es in eine XPS OM zu laden, und sie kann in XPS-Dokumentstreams verwendet werden, die von einem XPS OM serialisiert werden.

Der Abschnitt Aufgaben zur Programmierung der [XPS Digital Signature-API](#xps-digital-signature-api-programming-tasks) enthält Themen, in denen beschrieben wird, wie sie mit der XPS Digital Signature-API programmiert werden. In diesem Thema werden die folgenden Überlegungen zur Verwendung der XPS Digital Signature-API beim Hinzufügen der Unterstützung digitaler Signaturen zu einer Anwendung aufgeführt.

-   [Programmiertasks für die API für digitale XPS-Signaturen](#xps-digital-signature-api-programming-tasks)
-   [Besondere Hinweise zur Programmierung der API für digitale XPS-Signaturen](#special-notes-about-xps-digital-signature-api-programming)
    -   [Überprüfen von digitalen Signaturen in einem XPS-Dokument](#verifying-digital-signatures-in-an-xps-document)
    -   [Signaturrichtlinie für digitale Signaturen](#digital-signature-signing-policy)
    -   [Einbetten einer Zertifikatkette](#embedding-a-certificate-chain)
    -   [Verwenden der CERT \_ CONTEXT-Struktur](#using-the-cert\_context-structure)
-   [Zugehörige Themen](#related-topics)

## <a name="xps-digital-signature-api-programming-tasks"></a>Programmiertasks für die API für digitale XPS-Signaturen

Dieser Abschnitt enthält Themen, in denen beschrieben wird, wie Programmieraufgaben mithilfe der XPS Digital Signature-API ausgeführt werden.

-   [Allgemeine Aufgaben zur Programmierung digitaler Signaturen](basic-digital-signature-programming-tasks.md)<dl>

[Initialisieren des Signatur-Managers](initialize-the-signature-manager.md)  
    [Signieren eines Dokuments](sign-a-document.md)  
    [Hinzufügen einer Signaturanforderung zu einem XPS-Dokument](add-a-signature-request-to-a-document.md)  
    [Überprüfen von Dokumentsignaturen](verify-document-signatures.md)  
    </dl>
-   [Zusätzliche Aufgaben zur Programmierung digitaler Signaturen](advanced-digital-signature-programming-tasks.md)<dl>

[Laden eines Zertifikats aus einer Datei](load-a-certificate-from-a-file.md)  
    [Überprüfen, ob ein Zertifikat eine Signaturmethode unterstützt](verify-a-certificate-supports-a-signature-method.md)  
    [Überprüfen, ob das System eine Digestmethode unterstützt](verify-a-certificate-supports-a-digest-method.md)  
    [Einbetten von Zertifikatketten in ein Dokument](embedding-certificate-trust-chains-in-a-document.md)  
    </dl>

## <a name="special-notes-about-xps-digital-signature-api-programming"></a>Besondere Hinweise zur Programmierung der API für digitale XPS-Signaturen

Die folgenden Themen erfordern besondere Überlegungen, wenn Sie die XPS Digital Signature-API verwenden.

-   [Überprüfen von digitalen Signaturen in einem XPS-Dokument](#verifying-digital-signatures-in-an-xps-document)
-   [Signaturrichtlinie für digitale Signaturen](#digital-signature-signing-policy)
-   [Einbetten einer Zertifikatkette](#embedding-a-certificate-chain)
-   [Verwenden der CERT \_ CONTEXT-Struktur](#using-the-cert\_context-structure)

### <a name="verifying-digital-signatures-in-an-xps-document"></a>Überprüfen von digitalen Signaturen in einem XPS-Dokument

[**IXpsSignature::Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) überprüft nur den signierten Inhalt, um festzustellen, ob er sich seit der Signatur nicht geändert hat. **IXpsSignature::Verify** überprüft keines der Zertifikate, die zum Signieren des Dokumentinhalts verwendet wurden.

Weitere Informationen zu Zertifikaten und Kryptografie finden Sie unter [Informationen zur Kryptografie.](/windows/desktop/SecCrypto/about-cryptography)

Ein Beispiel zum Überprüfen von Dokumentsignaturen in einem Programm finden Sie unter Überprüfen von [Dokumentsignaturen und Zertifikaten.](verify-document-signatures.md)

### <a name="digital-signature-signing-policy"></a>Signaturrichtlinie für digitale Signaturen

Die Signaturrichtlinie für digitale Signaturen bestimmt, welche Teile eines XPS-Dokuments signiert werden. Eine Signaturrichtlinienoption besteht darin, die Signaturbeziehungen zu signieren, die vom Signaturursprungsteil beginnen. Da sich die Signaturbeziehungen mit jeder hinzugefügten Signatur ändern, unterbrechen Signaturen, die unter dieser Richtlinie erstellt werden, wenn neue Signaturen hinzugefügt werden. Stellen Sie sicher, dass Sie die Auswirkungen und Auswirkungen der Festlegung dieser Richtlinie klar verstehen. Andernfalls kann unerwartetes oder unerwünschtes Verhalten auftreten.

Weitere Informationen zu Signaturrichtlinien finden Sie unter [**XPS \_ SIGN \_ POLICY**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy).

### <a name="embedding-a-certificate-chain"></a>Einbetten einer Zertifikatkette

Die Zertifikate, aus denen die Vertrauenskette eines bestimmten Zertifikats besteht, können einem XPS-Dokument hinzugefügt werden. Das Einbetten dieser Zertifikate kann es einer Anwendung in Off-Line-Szenarien erleichtern, die von einer digitalen Signatur verwendeten Zertifikate zu überprüfen.

Weitere Informationen zum Einbetten von Zertifikaten in ein XPS-Dokument finden Sie unter [Einbetten von Zertifikatketten in ein Dokument.](embedding-certificate-trust-chains-in-a-document.md)

### <a name="using-the-cert_context-structure"></a>Verwenden der CERT \_ CONTEXT-Struktur

Die [**Strukturen CERT \_ CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) und [**CERT \_ INFO**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info) sind die wichtigsten Datenstrukturen, die Zertifikatinformationen enthalten. Weitere Informationen zur Verwendung dieser Strukturen finden Sie unter [Verwenden einer CERT \_ INFO-Datenstruktur.](/windows/desktop/SecCrypto/using-a-cert-info-data-structure)

[**CERT \_ CONTEXT-Strukturen,**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) die von Kryptografie-API-Funktionen zurückgegeben werden, müssen freigegeben werden, wenn sie nicht mehr benötigt werden. Um eine **CERT \_ CONTEXT-Struktur** freizugeben, rufen Sie die [**CertFreeCertificateContext-Funktion**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Allgemeine Aufgaben zur Programmierung digitaler Signaturen](basic-digital-signature-programming-tasks.md)
</dt> <dt>

[Zusätzliche Aufgaben zur Programmierung digitaler Signaturen](advanced-digital-signature-programming-tasks.md)
</dt> <dt>

[**\_CERT-KONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**CERT \_ INFO**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info)
</dt> <dt>

[**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[**\_ \_ XPS-SIGN-RICHTLINIE**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
