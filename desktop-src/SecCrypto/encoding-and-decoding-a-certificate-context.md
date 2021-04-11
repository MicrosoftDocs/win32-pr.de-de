---
description: Codieren und Decodieren eines Zertifikat Kontexts mithilfe von CryptoAPI.
ms.assetid: 149d1097-5f50-40ba-84f1-b815f54ba33d
title: Codieren und Decodieren eines Zertifikat Kontexts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4168d15ad8db5d4711a18f2042106e7d6d46010
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214946"
---
# <a name="encoding-and-decoding-a-certificate-context"></a>Codieren und Decodieren eines Zertifikat Kontexts

[*CryptoAPI*](../secgloss/c-gly.md) unterstützt das Codieren und Decodieren von [*Zertifikaten*](../secgloss/c-gly.md). CryptoAPI bietet ein umfangreiches, flexibles System von Funktionen und C-Strukturen, die die Codierung und Decodierung auf verschiedene Weise ermöglichen. CryptoAPI unterstützt die standardmäßige [*X. 509*](../secgloss/x-gly.md) -Zertifikat Struktur und die standardmäßige [*abstrakte Syntax Notation One*](../secgloss/a-gly.md) (ASN. 1) Encoding, um die Interoperabilität mit anderen Systemen zu ermöglichen.

Eine Übersicht über codierte Daten finden Sie unter [codierte und decodierte Daten](encoded-and-decoded-data.md).

## <a name="certificate-contexts"></a>Zertifikat Kontexte

Ein [*Zertifikat Kontext*](../secgloss/c-gly.md), [**CERT \_ context**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context), ist eine C-Struktur, die ein codiertes Element, ein Handle für einen [*Zertifikat Speicher*](../secgloss/c-gly.md), einen Zeiger auf das ursprünglich codierte [*zertifikatblob*](../secgloss/c-gly.md)und einen Zeiger auf eine [**CERT \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) C-Struktur enthält.

Die [**CERT \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) -Struktur ist das Herzstück des Zertifikats. Sie enthält in direkter Form und in verschlüsselter Form alle grundlegenden Informationen im Zertifikat. Die folgende Abbildung zeigt die **CERT \_ Info** -Struktur, deren codierte Member als schattiert angezeigt werden.

![CERT \- Info-Struktur](images/certinf2.png)

Die Elemente **IssuerUniqueID** und **subjetuniqueid** sind Teil der [*X. 509*](../secgloss/x-gly.md) Version 2-Zertifikat Implementierung, werden jedoch selten verwendet. Zertifikat Erweiterungen in Version 3 ersetzen die Funktionalität dieser Member.

Wenn die Informationen, die im codierten (schattierten) Element **Aussteller** und Antragsteller enthalten sind, **erforderlich sind,** müssen diese Member decodiert werden. Verwenden Sie [**cryptdecodeobject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) , um diese Member zu decodieren. Die folgende Abbildung zeigt den Prozess der Decodierung eines dieser Member.

![Decodieren mit cryptdecodeobject](images/infoflow.png)

Im veranschaulichten Fall erstellt die [**cryptdecodeobject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) -Funktion eine [**CERT \_ Name \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) -Struktur, ein Array von [**CERT \_ RDN**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) -Strukturen, ein entsprechendes Array von [**\_ RDN-CERT \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) -Strukturen und eine Zeichenfolge, die den Namen enthält. Die Inhalte der Zeichenfolge werden von Mitgliedern der " **CERT \_ RDN \_ attr** "-Struktur bestimmt. Wenn der **pszobjid** -Member z. b. 2.5.4.3 ist, enthält die Zeichenfolge einen allgemeinen Namen. Wenn es 2.5.4.10 ist, würde die Zeichenfolge einen Organisationsnamen enthalten. Eine Liste der [*Objekt*](../secgloss/o-gly.md) -IDs (OIDs) finden Sie unter **CERT \_ RDN \_ attr**.

Der **dwvaluetype** -Member enthält Informationen zum Typ der Zeichenfolge. Wenn es sich um \_ eine druckbare "CERT RDN"-Zeichen \_ \_ Folge handelt, enthält das Wertmember eine Zeichenfolge mit Byte Breite und null terminierten Zeichen Wenn es sich um \_ eine Unicode-RDN-Unicode-Zeichenfolge handelt \_ \_ , ist die Zeichenfolge eine Zeichenfolge mit doppelter Breite (Wort Breite).

Einen ausführlichen Prozess zum Codieren und Decodieren von Zertifikaten finden Sie unter [Codieren einer Zertifikat \_ Informationsstruktur und decodieren](encoding-a-cert-info-structure.md) [einer Zertifikat \_ Informationsstruktur](decoding-a-cert-info-structure.md).

 

 
