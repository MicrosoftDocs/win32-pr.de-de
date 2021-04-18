---
description: Ab dem X. 509-Zertifikat Format Version 3 kann ein Zertifikat Zertifikat Erweiterungen enthalten.
ms.assetid: fb106cab-8a61-4a83-8fb4-7c045d905575
title: Erweiterungs Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfcf1b47fcc97b87f5956f4584aee07acce04222
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352551"
---
# <a name="extension-handlers"></a>Erweiterungs Handler

Ab dem [*X. 509*](../secgloss/x-gly.md) -Zertifikat Format Version 3 kann ein Zertifikat Zertifikat Erweiterungen enthalten. (Informationen zum Inhalt eines X. 509-Zertifikats finden Sie unter [Zertifikat Eigenschaften](certificate-properties.md).) Diese Erweiterungen geben zusätzliche Informationen an. Eine Erweiterung kann z. b. zusätzliche Informationen zur Identifizierung des Antragstellers angeben oder wichtige Verwendungs Informationen angeben, die die Aufgaben (z. b. Signatur oder Verschlüsselung) angeben, für die ein Schlüssel verwendet werden kann. Ein Satz von Standard Erweiterungen ist für die Anwendungs Verwendung definiert, und Erweiterungen können auch angepasst werden.

Jede Erweiterung verfügt über eine zugeordnete objektbezeichnerzeichenfolge, die den Typ der zusätzlichen Informationen und eine Datenstruktur, die diese Informationen enthält, identifiziert. Beispielsweise ist der Schlüssel Verwendungs Objekt Bezeichner "2.5.29.15", der Informationen zur Schlüssel Verwendung angibt. Die zugehörige Datenstruktur ist ein [**crypt- \_ \_ bitblob**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_bit_blob) (Bitfield), das angibt, wie der Schlüssel verwendet werden kann.

Einem Zertifikat kann eine Erweiterung hinzugefügt werden, bevor es ausgestellt wird. Wenn das Zertifikat ausgestellt wird, sind alle aktivierten Erweiterungen Teil des Zertifikats. Wenn eine Erweiterung als kritisch gekennzeichnet ist, muss Sie von der Anwendung verwendet werden, und die Anwendung muss der Absicht oder dem Wert der Erweiterung entsprechen. Mithilfe der Zertifikat Dienste können Erweiterungen für ein nicht ausgestelltes Zertifikat über die von [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) und [**icertserverpolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy)bereitgestellten Methoden festgelegt werden. Ausführliche Informationen zu Zertifikat Erweiterungen finden Sie in der CryptoAPI-Dokumentation unter [**CERT \_ Extension**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) . Informationen zu allgemeinen Datenstrukturen der Zertifikat Erweiterung finden Sie unter [X. 509-Zertifikat Erweiterungs Strukturen](cryptography-structures.md).

Der Erweiterungs Handler ist ein COM-Objekt, das Routinen für die Codierung komplexer, aber häufig verwendeter Erweiterungen und Datentypen, z. b. IA5String oder PrintableString, bereitstellt.

Erweiterungen mit den Datentypen **Date**, **Long** und **BSTR** benötigen keinen Erweiterungs Handler. Das Richtlinien Modul ruft einfach [**icertserverpolicy:: setcertificateextension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) auf, wobei der *Type* -Parameter auf einen Wert festgelegt ist, der den Erweiterungs Datentyp darstellt: propType \_ Date, propType \_ Long oder propType \_ String. Anschließend übergibt Sie die Erweiterung an die Server-Engine. Die Server-Engine führt seinerseits die Codierung der [*abstrakten Syntax Notation One*](../secgloss/a-gly.md) (ASN. 1) aus, bevor die Erweiterung im Zertifikat gespeichert wird.

Allerdings müssen Erweiterungen, die andere Datentypen als diese Standardtypen aufweisen, ASN. 1 sein, die von einem Erweiterungs Handler codiert werden, bevor das Richtlinien Modul Sie an die Server-Engine übergibt. Wenn das Richtlinien Modul [**icertserverpolicy:: setcertificateextension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) aufruft, um eine ASN. 1-codierte Erweiterung an die Server-Engine zu übergeben, muss der *Typparameter* auf "propType Binary" festgelegt werden \_ . Die Server-Engine speichert dann einfach diese codierte Erweiterung im Zertifikat.

Der standardmäßige Erweiterungs Handler (Certenc.dll) exportiert eine Reihe von **icertencodexxx** -Schnittstellen und kann vom Richtlinien Modul aufgerufen werden. Die erforderlichen Typinformationen sind auch in Certencl.dll enthalten, die im Platform Software Development Kit (SDK) bereitgestellt werden. Jede Schnittstelle stellt eine Codierungs **Methode bereit, die eine** ASN. 1-codierte Zertifikats Erweiterung an das Richtlinien Modul in einem binären Format zurückgibt. Das Richtlinien Modul kann dann die Erweiterung in einem Zertifikat festlegen, indem die [**icertserverpolicy:: setcertificateextension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) -Methode aufgerufen wird.

Weitere Informationen finden Sie unter [Schreiben von benutzerdefinierten Erweiterungs Handlern](writing-custom-extension-handlers.md).

 

 
