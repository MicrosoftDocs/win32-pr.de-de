---
description: Der Codierungsprozess ist das Gegenteil des Decodierungsprozesses, der unter Decodieren einer CERT \_ INFO-Struktur beschrieben wird.
ms.assetid: 5d3311e5-a2fb-46f7-aa76-f232b39b34fd
title: Codieren einer CERT_INFO Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b469ae0bdf02ffd8f30f8b0c2dd44051239a5702ff32704d58de8b60f1ca9701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766785"
---
# <a name="encoding-a-cert_info-structure"></a>Codieren einer CERT \_ INFO-Struktur

Der Codierungsprozess ist das Gegenteil des Decodierungsprozesses, der unter [Decodieren einer CERT \_ INFO-Struktur beschrieben wird.](decoding-a-cert-info-structure.md) Mit dem folgenden Verfahren wird beispielsweise ein codierter **Aussteller zu** einer [**CERT \_ INFO-Struktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) hinzugefügt. Sehen Sie sich auch die Abbildung an, die der Prozedur folgt.

**So fügen Sie einen codierten Aussteller zu einer CERT \_ INFO-Struktur hinzu**

1.  Erstellen Sie eine Zeichenfolge, die den zu verwendenden Ausstellernamen enthält.
2.  Erstellen Sie ein Array [**von CERT \_ RDN \_ ATTR-Strukturen,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) die initialisiert werden, um die richtigen Informationen zur soeben erstellten Ausstellernamenzeichenfolge zu enthalten.
3.  Erstellen Sie ein Array [**von CERT \_ RDN-Strukturen,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) von denen eine über die Informationen zum Array der gerade initialisierten [**CERT \_ RDN \_ ATTR-Strukturen**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) verfügt.
4.  Erstellen Sie [**eine CERT \_ NAME \_ INFO-Struktur,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) die über einen Zeiger auf das Array von [**\_ CERT-RDN-Strukturen**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) verfügt, die gerade erstellt wurden.
5.  Rufen [**Sie CryptEncodeObject auf,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) um die Größe des ausgabecodierten BLOBs zu erhalten, und übergeben Sie ihm die Adresse der soeben erstellten [**CERT NAME \_ \_ INFO-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info)
6.  Ordnen Sie Arbeitsspeicher für das ausgabecodierte BLOB zu.
7.  Rufen [**Sie CryptEncodeObject erneut**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) auf, und übergeben Sie dabei die gleichen Informationen, aber jetzt die Adresse des gerade zugewiesenen Arbeitsspeichers.
8.  Legen Sie **das Issuer.cbData-Element** der [**CERT \_ INFO-Struktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) auf die in Schritt 5 zurückgegebene Größe und das **Issuer.pbData-Element** auf die In Schritt 6 erhaltene Adresse fest. Das codierte **AusstellerBLOB** befindet sich nun dort.

![Hinzufügen eines codierten Ausstellers zu einer \- Zertifikatinformationsstruktur](images/encflow.png)

Um einige Informationen zur Zertifikaterweiterung zu initialisieren und zu codieren, verwenden Sie das folgende Verfahren. Sehen Sie sich auch die Abbildung an, die der Prozedur folgt.

**So fügen Sie einer CERT INFO-Struktur codierte \_ Erweiterungsinformationen hinzu**

1.  Erstellen und Initialisieren einer Erweiterungsinformationsstruktur – in diesem Beispiel handelt es sich um eine [**CERT \_ BASIC CONSTRAINTS \_ \_ INFO-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_basic_constraints_info)
2.  Rufen [**Sie CryptEncodeObject auf,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)und übergeben Sie ihm die Adresse der soeben erstellten Struktur, um die Größe des ausgabecodierten BLOB zu erhalten.
3.  Ordnen Sie Arbeitsspeicher für das ausgabecodierte BLOB zu.
4.  Rufen [**Sie CryptEncodeObject erneut**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) auf, und übergeben Sie dabei die gleichen Informationen, mit der Ausnahme, dass jetzt die Adresse des zugeordneten Arbeitsspeichers übergeben wird.
5.  Erstellen Sie ein Array von [**CERT \_ EXTENSION-Strukturen.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension)
6.  Initialisieren Sie eine der [**CERT \_ EXTENSION-Strukturen,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) sodass **pszObjId** die richtige Zeichenfolge für die in **Value** enthaltenen Daten ist und dass **Value** das verschlüsselte DatenBLOB enthält, das beim Aufruf von [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)ausgegeben wurde.
7.  Initialisieren Sie **das rgExtension-Member** der [**CERT \_ INFO-Struktur,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) um auf das Array von [**CERT \_ EXTENSION-Strukturen zu**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) verweisen.

![Hinzufügen codierter Erweiterungsinformationen zu einer \- Zertifikatinformationsstruktur](images/xtenflow.png)

 

 



