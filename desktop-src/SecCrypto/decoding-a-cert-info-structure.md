---
description: Bei einem Zertifikat besteht der erste Schritt beim Decodieren des Zertifikat-BLOB darin, CertCreateCertificateContext aufzurufen und ihm einen Zeiger auf das codierte Zertifikat (BLOB) zu übergeben.
ms.assetid: b50530e2-15a0-4215-bf18-300cf67d1611
title: Decodieren einer CERT_INFO-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8eab5a75c2a5906ac875f925845f83f3c411c12a31aeea4825efd795b78eaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100880"
---
# <a name="decoding-a-cert_info-structure"></a>Decodieren einer CERT \_ INFO-Struktur

Bei einem Zertifikat besteht der erste Schritt beim Decodieren des [*Zertifikat-BLOB*](../secgloss/b-gly.md) darin, [**CertCreateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext)aufzurufen und ihm einen Zeiger auf das codierte Zertifikat (*BLOB*) zu übergeben. Wenn diese Funktion aufgerufen wird, wird ein Duplikat des codierten Zertifikats erstellt, eine Struktur vom Typ [**CERT \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)und eine Struktur vom Typ [**CERT \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)erstellt. Wie in der folgenden Abbildung gezeigt, enthält ein [*Zertifikatkontext*](../secgloss/c-gly.md) das ursprüngliche *Zertifikat-BLOB, eine C-Struktur* vom Typ **CERT \_ CONTEXT** und eine C-Struktur vom Typ **CERT \_ INFO**. Einer der Member der **CERT \_ CONTEXT-Struktur** verweist auf die **CERT \_ INFO-Struktur** und ein anderer auf das codierte Zertifikat-BLOB.

![Zertifikatkontext](images/certcntx.png)

Das codierte Objekt (Datenmember) wird immer als Eingabe für die [**CryptDecodeObject-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) bereitgestellt, und die Ausgabe ist eine C-Struktur, die möglicherweise codierte Member aufweist, je nachdem, wie weit Sie in den Prozess hinein sind.

Es gibt einen anderen Member, der eine Decodierung erfordert, und das ist der **Erweiterungsmember.** Obwohl sie nicht auf der [**CERT \_ INFO-Ebene**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) codiert ist, enthält sie einige codierte Informationen. Um diese Informationen zu decodieren, fahren Sie wie in der folgenden Abbildung gezeigt fort.

![Decodierungsinformationen](images/xtension.png)

In der [**CERT \_ INFO-Struktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) ist **member rgExtension** ein Zeiger auf ein Array von [**CERT \_ EXTENSION-Strukturen.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) Jede **CERT \_ EXTENSION-Struktur** verfügt über einen **Value-Member,** der codiert ist und decodiert werden muss. Der **Value-Member** wird an die [**CryptDecodeObject-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) übergeben, und die Ausgabe der Funktion hängt dann vom Wert des **pszObjId-Members** ab. Beachten Sie, dass in der Abbildung zwei verschiedene Strukturen erstellt werden, eine vom Typ [**CERT \_ BASIC \_ CONSTRAINTS \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_basic_constraints_info) und eine vom Typ [**CERT \_ AUTHORITY KEY \_ ID \_ \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info), abhängig vom Wert von **pszObjId**.

 

 
