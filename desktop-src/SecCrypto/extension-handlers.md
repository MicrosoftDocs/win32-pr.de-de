---
description: Ab Version 3 des X.509-Zertifikatformats kann ein Zertifikat Zertifikaterweiterungen enthalten.
ms.assetid: fb106cab-8a61-4a83-8fb4-7c045d905575
title: Erweiterungshandler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cba61c5896887471038325eba0dbed75f43061cff81452727933a3013c37f8aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006928"
---
# <a name="extension-handlers"></a>Erweiterungshandler

Ab [*Version 3 des X.509-Zertifikatformats*](../secgloss/x-gly.md) kann ein Zertifikat Zertifikaterweiterungen enthalten. (Informationen zum Inhalt eines X.509-Zertifikats finden Sie unter [Zertifikateigenschaften](certificate-properties.md).) Diese Erweiterungen geben zusätzliche Informationen an. Eine Erweiterung kann z. B. zusätzliche Informationen zur Subjektidentifikation oder Schlüsselverwendungsinformationen angeben, die die Aufgaben (z. B. Signatur oder Verschlüsselung) angeben, für die ein Schlüssel verwendet werden kann. Ein Satz von Standarderweiterungen ist für die Anwendungsnutzung definiert, und Erweiterungen können auch angepasst werden.

Jede Erweiterung verfügt über eine zugeordnete Objektbezeichnerzeichenfolge, die den Typ zusätzlicher Informationen identifiziert, und eine Datenstruktur, die diese Informationen enthält. Der Schlüsselverwendungsobjektbezeichner ist beispielsweise "2.5.29.15", der Schlüsselverwendungsinformationen angibt. Die zugeordnete Datenstruktur ist ein [**\_ CRYPT-BIT-BLOB \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_bit_blob) (Bitfeld), das ankündigt, wie der Schlüssel verwendet werden kann.

Eine Erweiterung kann einem Zertifikat hinzugefügt werden, bevor sie ausgestellt wird. Wenn das Zertifikat ausgestellt wird, sind alle aktivierten Erweiterungen Teil des Zertifikats. Wenn eine Erweiterung als kritisch gekennzeichnet ist, muss ihre Verwendung von der verwendenden Anwendung bekannt sein, und die Anwendung muss die Absicht oder den Wert der Erweiterung einhalten. Zertifikatdienste ermöglichen das Festlegen von Erweiterungen für ein nicht ausgestelltes Zertifikat mit methoden, die von [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) und [**ICertServerPolicy bereitgestellt werden.**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) Weitere Informationen zu Zertifikaterweiterungen finden Sie unter [**CERT \_ EXTENSION**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) in der CryptoAPI-Dokumentation. Informationen zu allgemeinen Zertifikaterweiterungsdatenstrukturen finden Sie unter [X.509 Certificate Extension Structures](cryptography-structures.md).

Der Erweiterungshandler ist ein COM-Objekt, das Routinen zum Codieren der komplexeren, aber häufig verwendeten Erweiterungen und Datentypen wie IA5String oder PrintableString bietet.

Erweiterungen mit den Datentypen **DATE,** **LONG** und **BSTR** erfordern keinen Erweiterungshandler. Das Richtlinienmodul ruft einfach [**ICertServerPolicy::SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) auf, während der *Type-Parameter* auf einen Wert festgelegt ist, der den Erweiterungsdatentyp darstellt: PROPTYPE \_ DATE, PROPTYPE LONG oder \_ PROPTYPE \_ STRING. Anschließend wird die Erweiterung an die Server-Engine übermittelt. Die Server-Engine führt wiederum die ASN.1-Codierung [*(Abstract Syntax Notation One)*](../secgloss/a-gly.md) aus, bevor die Erweiterung im Zertifikat gespeichert wird.

Erweiterungen, die andere Datentypen als diese Standardtypen haben, müssen jedoch von einem Erweiterungshandler ASN.1 codiert werden, bevor sie vom Richtlinienmodul an die Server-Engine übergeben werden. Wenn das Richtlinienmodul [**ICertServerPolicy::SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) aufruft, um eine ASN.1-codierte Erweiterung an die Server-Engine zu übergeben, muss der *Type-Parameter* auf PROPTYPE BINARY festgelegt \_ werden. Die Server-Engine speichert diese codierte Erweiterung dann einfach im Zertifikat.

Der Standarderweiterungshandler, Certenc.dll, exportiert eine Reihe von **ICertEncodeXXX-Schnittstellen** und kann vom Richtlinienmodul aufgerufen werden. Die erforderlichen Typinformationen sind auch in der Certencl.dll, die im Platform Software Development Kit (SDK) bereitgestellt wird. Jede Schnittstelle stellt eine **Codierungsmethode** bereit, die eine ASN.1-codierte Zertifikaterweiterung in einem Binärformat an das Richtlinienmodul zurückgibt. Das Richtlinienmodul kann dann die Erweiterung in einem Zertifikat festlegen, indem es die [**ICertServerPolicy::SetCertificateExtension-Methode**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) aufruft.

Weitere Informationen finden Sie unter [Schreiben von benutzerdefinierten Erweiterungshandlern.](writing-custom-extension-handlers.md)

 

 
