---
description: Beim Codierungs Vorgang handelt es sich um den umgekehrten Decodierungs Prozess, der unter Decodieren einer Zertifikat \_ Informationsstruktur beschrieben wird
ms.assetid: 5d3311e5-a2fb-46f7-aa76-f232b39b34fd
title: Codieren einer CERT_INFO Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645a1d3054546a7b11c57d4f515dc7d3e26b5fe0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360876"
---
# <a name="encoding-a-cert_info-structure"></a>Codieren einer CERT \_ Info-Struktur

Beim Codierungs Vorgang handelt es sich um den umgekehrten Decodierungs Prozess, der unter [Decodieren einer Zertifikat \_ Informationsstruktur](decoding-a-cert-info-structure.md)beschrieben wird Mit dem folgenden Verfahren wird z. b. ein codierter **Aussteller** zu einer [**CERT \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) -Struktur hinzugefügt. Sehen Sie sich auch die Abbildung an, die auf das Verfahren folgt.

**So fügen Sie einen codierten Aussteller zu einer CERT \_ Info-Struktur hinzu**

1.  Erstellen Sie eine Zeichenfolge, die den zu verwendenden Aussteller Namen enthält.
2.  Erstellen Sie ein Array von [**CERT \_ RDN \_ attr**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) -Strukturen, die so initialisiert werden, dass Sie die richtigen Informationen über die soeben erstellte Zeichenfolge für den Aussteller Namen enthalten.
3.  Erstellen Sie ein Array von [**CERT \_ RDN**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) -Strukturen, von denen eine über die Informationen über das Array der soeben initialisierten [**CERT \_ RDN \_ attr**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) -Strukturen verfügt.
4.  Erstellen Sie eine [**CERT \_ Name \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) -Struktur, die über einen Zeiger auf das Array der soeben erstellten Zertifikat- [**\_ RDN**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) -Strukturen verfügt.
5.  Nennen Sie [**cryptencodeobject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) , um die Größe des Ausgabe codierten BLOBs abzurufen, und übergeben Sie dabei die Adresse der soeben erstellten Struktur von [**CERT \_ Name \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) .
6.  Zuweisen von Arbeitsspeicher für das Ausgabe codierte BLOB.
7.  Nennen Sie " [**cryptencodeobject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) " erneut, und übergeben Sie dabei die gleichen Informationen, aber übergeben Sie nun die Adresse des gerade zugewiesenen Speichers.
8.  Legen Sie den **Aussteller. cbData** -Member der [**CERT \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) -Struktur auf die in Schritt 5 zurückgegebene Größe und den **Aussteller. pbData** -Member auf die in Schritt 6 erhaltene Adresse fest. Das codierte **Ausstellers** -BLOB befindet sich jetzt hier.

![Hinzufügen eines codierten Ausstellers zu einer CERT \- Info-Struktur](images/encflow.png)

Verwenden Sie das folgende Verfahren, um einige Informationen zur Zertifikats Erweiterung zu initialisieren und zu codieren. Sehen Sie sich auch die Abbildung an, die auf das Verfahren folgt.

**So fügen Sie einer CERT Info-Struktur codierte Erweiterungs Informationen hinzu \_**

1.  Erstellen und Initialisieren einer Erweiterungs Informationsstruktur – für dieses Beispiel handelt es sich um eine Informationsstruktur für [**CERT \_ Basic- \_ \_ Einschränkungen**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_basic_constraints_info) .
2.  Nennen Sie [**cryptencodeobject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject), und übergeben Sie dabei die Adresse der soeben erstellten Struktur, um die Größe des Ausgabe codierten BLOB abzurufen.
3.  Zuweisen von Arbeitsspeicher für das Ausgabe codierte BLOB.
4.  Nennen Sie " [**cryptencodeobject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) " erneut, und übergeben Sie die gleichen Informationen, mit dem Unterschied, dass Sie jetzt die Adresse des zugewiesenen Speichers übergeben.
5.  Erstellen Sie ein Array von [**CERT- \_ Erweiterungs**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) Strukturen.
6.  Initialisieren Sie eine der [**CERT- \_ Erweiterungs**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) Strukturen, sodass **die pszobjid** die richtige Zeichenfolge für die in **value** enthaltenen Daten ist, und dieser **Wert** das verschlüsselte datblob enthält, das beim Aufrufen von [**cryptencodeobject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)ausgegeben wurde.
7.  Initialisieren Sie den **rgextension** -Member der [**CERT \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) -Struktur, um auf das Array von [**Zertifikat \_ Erweiterungs**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) Strukturen zu verweisen.

![Hinzufügen von Informationen zu codierten Erweiterungen zu einer CERT \- Info-Struktur](images/xtenflow.png)

 

 



