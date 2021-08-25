---
description: Codieren und Decodieren eines Zertifikatkontexts mit cryptoAPI.
ms.assetid: 149d1097-5f50-40ba-84f1-b815f54ba33d
title: Codieren und Decodieren eines Zertifikatkontexts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f640e12034ebf4ec84e0e71013197f043453b62e1102018dcfe9ea887d6ada
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874888"
---
# <a name="encoding-and-decoding-a-certificate-context"></a>Codieren und Decodieren eines Zertifikatkontexts

[*CryptoAPI*](../secgloss/c-gly.md) unterstützt die Codierung und Decodierung von [*Zertifikaten.*](../secgloss/c-gly.md) CryptoAPI umfasst ein umfassendes, flexibles System von Funktionen und C-Strukturen, die die Codierung und Decodierung auf verschiedene Weise ermöglichen. CryptoAPI unterstützt die standardmäßige [*X.509-Zertifikatstruktur*](../secgloss/x-gly.md) und die standardmäßige ASN.1-Codierung [*(Abstract Syntax Notation One),*](../secgloss/a-gly.md) um Interoperabilität mit anderen Systemen bereitzustellen.

Eine Übersicht über codierte Daten finden Sie unter [Codierte und decodierte Daten.](encoded-and-decoded-data.md)

## <a name="certificate-contexts"></a>Zertifikatkontexte

Ein [*Zertifikatkontext*](../secgloss/c-gly.md), [**CERT \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context), ist eine C-Struktur, die einen codierten Member, ein Handle für einen [*Zertifikatspeicher,*](../secgloss/c-gly.md)einen Zeiger auf das ursprüngliche codierte Zertifikat-BLOB und einen Zeiger auf eine [**CERT \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) [*C-Struktur*](../secgloss/c-gly.md)enthält.

Die [**CERT \_ INFO-Struktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) ist das Kernstück des Zertifikats. Sie enthält alle grundlegenden Informationen im Zertifikat in direkter Form und in codierter Form. Die folgende Abbildung zeigt die **CERT \_ INFO-Struktur** mit allen codierten Membern, die als schattiert angezeigt werden.

![Struktur der \- Zertifikatinformationen](images/certinf2.png)

Die Member **IssuerUniqueID** und **SubjectUniqueID** sind Teil der [*X.509*](../secgloss/x-gly.md) Version 2-Zertifikatimplementierungen, werden aber selten verwendet. Zertifikaterweiterungen in Version 3 ersetzen die Funktionalität dieser Member.

Wenn die in den codierten (schattierten) Membern **Issuer** und **Subject** enthaltenen Informationen benötigt werden, müssen diese Member decodiert werden. Verwenden Sie [**CryptDecodeObject,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) um diese Member zu decodieren. Die folgende Abbildung zeigt den Prozess der Decodierung eines dieser Member.

![Decodieren mit cryptdecodeobject](images/infoflow.png)

Im dargestellten Fall erstellt die [**CryptDecodeObject-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) eine [**CERT \_ NAME \_ INFO-Struktur,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) ein Array von [**CERT \_ RDN-Strukturen,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) ein entsprechendes Array von [**CERT \_ RDN \_ ATTR-Strukturen**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) und eine Zeichenfolge, die den Namen enthält. Member der **CERT \_ RDN \_ ATTR-Struktur** bestimmen den Inhalt der Zeichenfolge. Wenn der **pszObjId-Member** beispielsweise 2.5.4.3 ist, enthält die Zeichenfolge einen allgemeinen Namen. Wenn es 2.5.4.10 ist, enthält die Zeichenfolge einen Organisationsnamen. Eine Liste dieser [*Objektbezeichner*](../secgloss/o-gly.md) (OIDs) finden Sie unter **CERT \_ RDN \_ ATTR**.

Der **dwValueType-Member** enthält Informationen zum Typ der Zeichenfolge. Wenn es sich um CERT \_ RDN \_ PRINTABLE \_ STRING handelt, enthält der Wertmember eine Zeichenfolge mit Bytebreite und 0 (null). Wenn es sich um CERT \_ RDN UNICODE STRING handelt, ist die Zeichenfolge eine Zeichenfolge mit \_ \_ doppelter Breite (Wortgröße).

Einen ausführlichen Prozess zum Codieren und Decodieren von Zertifikaten finden Sie unter [Codieren einer CERT \_ INFO-Struktur](encoding-a-cert-info-structure.md) und [Decodieren einer CERT \_ INFO-Struktur.](decoding-a-cert-info-structure.md)

 

 
