---
description: Zeigt die Beziehung zwischen diesen Funktionsparametern, die auf Strukturen oder Arrays verweisen, und ihren initialisierten Daten.
ms.assetid: 89caf4d3-727f-472b-9a09-e81b4ff4d127
title: Verfahren zum Signieren von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10bae09c97fa42086f853d43b2a5a9dc02f0cbdbe2dd946fefe5d39e28a32104
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117977549"
---
# <a name="procedure-for-signing-data"></a>Verfahren zum Signieren von Daten

Eine einzelne Funktion, [**CryptSignMessage,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage)führt alle Aufgaben aus, die unter [Erstellen einer signierten Nachricht](creating-a-signed-message.md)aufgeführt sind. Die Initialisierung von Strukturen und anderen Daten ist jedoch weiterhin erforderlich. Die folgende Abbildung zeigt die Beziehung zwischen diesen Funktionsparametern, die auf Strukturen oder Arrays verweisen, und ihren initialisierten Daten. Die Abbildung zeigt nur die Funktionsparameter und Strukturmember, die von anderen Strukturen oder Funktionen abgeleitet sind. Die restlichen Parameter sind einfache Initialisierungen.

![Initialisierungszuordnung für einen Aufruf von cryptsignmessage](images/crypsign.png)

**So signieren Sie Daten mit CryptSignMessage**

1.  Abrufen eines Zeigers auf die Daten, die signiert werden sollen.
2.  Weisen Sie den Zeiger auf die Daten zu, um 0 (null) eines Arrays vom Datentyp "data to be signed" zu indizieren.
3.  Abrufen eines Handles für den Kryptografieanbieter.
4.  Öffnen Sie einen [*Zertifikatspeicher,*](../secgloss/c-gly.md) der das Zertifikat des Signierers enthält.
5.  Abrufen einer Adresse für das Zertifikat des Signierers.
6.  Weisen Sie die Adresse des Zertifikats dem Nullindex des *MsgCert-Arrays* zu.
7.  Weisen Sie dem *MsgCert-Array* die Adressen aller anderen Zertifikate zu, die in die Nachricht eingeschlossen werden sollen.
8.  Initialisieren Sie die [**CRYPT \_ ALGORITHM \_ IDENTIFIER-Struktur,**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier) und initialisieren Sie den **pszObjId-Member** nach Bedarf mit dem gewünschten Hashalgorithmus und den anderen Membern.
9.  Initialisieren Sie die [**CRYPT \_ SIGN MESSAGE \_ \_ PARA-Struktur,**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para) und initialisieren Sie den **pSigningCert-Member** mit der Adresse des Zertifikats des Signierers, den **MsgCert-Arraymember** mit der Adresse der Zertifikate des Signers und anderer, den **HashAlgorithm-Member** mit der Adresse der [**CRYPT ALGORITHM \_ \_ IDENTIFIER-Struktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier) und die anderen Member nach Bedarf.
10. Rufen Sie die [**CryptSignMessage-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage) auf, und übergeben Sie die [**CRYPT \_ SIGN MESSAGE \_ \_ PARA-Struktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para) für den *pSignPara-Parameter,* die Adresse des Arrays "data to be signed" für den *rgpbToBeSigned-Parameter,* eine Adresse für den *pbSignedBlob-Ausgabeparameter* und ggf. Werte für die anderen Parameter.

 

 
