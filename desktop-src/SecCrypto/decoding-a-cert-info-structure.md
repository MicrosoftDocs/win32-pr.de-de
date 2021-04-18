---
description: Bei einem Zertifikat ist der erste Schritt beim Decodieren des zertifikatblobs das Aufrufen von "certkreatecertifiertifikatecontext" und das Übergeben eines Zeigers an das codierte Zertifikat (BLOB).
ms.assetid: b50530e2-15a0-4215-bf18-300cf67d1611
title: Decodieren einer CERT_INFO-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7178c9a5bcfc95a8e2945a6e381f0c2c29cf3b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563142"
---
# <a name="decoding-a-cert_info-structure"></a>Decodieren einer Zertifikat \_ Informationsstruktur

Bei einem Zertifikat ist der erste Schritt beim Decodieren des [*zertifikatblobs*](../secgloss/b-gly.md) das Aufrufen von " [**certkreatecertifiertifikatecontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext)" und das Übergeben eines Zeigers an das codierte Zertifikat (*BLOB*). Wenn diese Funktion aufgerufen wird, erstellt Sie ein Duplikat des codierten Zertifikats, erstellt eine Struktur vom Typ [**CERT \_ context**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)und erstellt eine Struktur vom Typ [**CERT \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info). Wie in der folgenden Abbildung dargestellt, enthält ein [*Zertifikat Kontext*](../secgloss/c-gly.md) das ursprüngliche zertifikatblob, eine c-Struktur des Typs **CERT \_ context** und eine c-Struktur des Typs  **CERT \_ Info**. Einer der Member der CERT- **\_ Kontext** Struktur verweist auf die **CERT \_ Info** -Struktur und eine andere auf das codierte zertifikatblob.

![Zertifikat Kontext](images/certcntx.png)

Das codierte Objekt (Datenmember) wird immer als Eingabe für die [**cryptdecodeobject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) -Funktion bereitgestellt, und die Ausgabe ist eine C-Struktur, die ggf. codierte Member hat, abhängig von der Art und Weise, in der Sie sich befinden.

Es gibt einen anderen Member, der Decodierung erfordert, und das ist der **Erweiterungsmember** . Obwohl Sie nicht auf der CERT- [**Informations \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) Ebene codiert ist, enthält Sie einige codierte Informationen. Gehen Sie wie in der folgenden Abbildung gezeigt vor, um diese Informationen zu decodieren.

![Decodieren von Informationen](images/xtension.png)

In der [**CERT \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) -Struktur ist Member **rgextension** ein Zeiger auf ein Array von [**CERT- \_ Erweiterungs**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) Strukturen. Jede Struktur der **Zertifikat \_ Erweiterung** weist einen **Wertmember** auf, der in codierter Form ist und decodiert werden muss. Der **Wertmember** wird an die [**cryptdecodeobject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) -Funktion übergeben, und die Ausgabe der Funktion hängt vom Wert des **pszobjid** -Members ab. Beachten Sie, dass in der Abbildung zwei verschiedene Strukturen erstellt werden, je nach Wert von " **pszobjid**" eine der Typen " [**CERT \_ Basic- \_ \_ Einschränkungen**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_basic_constraints_info) " und eine der Typen " [**CERT \_ Authority \_ Key \_ ID \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info)".

 

 
