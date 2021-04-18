---
description: Zeigt die Beziehung zwischen den Funktionsparametern an, die auf Strukturen oder Arrays und deren initialisierte Daten zeigen.
ms.assetid: 89caf4d3-727f-472b-9a09-e81b4ff4d127
title: Verfahren zum Signieren von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba289928ab39c690e1c44bdbf65c77c18b7edab3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358490"
---
# <a name="procedure-for-signing-data"></a>Verfahren zum Signieren von Daten

Eine einzelne Funktion ( [**cryptsignmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage)) führt alle Aufgaben aus, die unter [Erstellen einer signierten Nachricht](creating-a-signed-message.md)aufgeführt sind. Die Initialisierung von Strukturen und anderen Daten ist jedoch weiterhin erforderlich. Die folgende Abbildung zeigt die Beziehung zwischen den Funktionsparametern, die auf Strukturen oder Arrays und deren initialisierte Daten zeigen. Die Abbildung zeigt nur die Funktionsparameter und Strukturmember, die von anderen Strukturen oder Funktionen abgeleitet werden. Die restlichen Parameter sind einfache Initialisierungen.

![Initialisierungs Zuordnung für einen Rückruf von "cryptsignmessage"](images/crypsign.png)

**So signieren Sie Daten mithilfe von cryptsignmessage**

1.  Einen Zeiger auf die zu Signier enden Daten erhalten.
2.  Weisen Sie den-Zeiger den Daten zu, um 0 (null) des Arrays "zu Signier Ende Daten" zu indizieren.
3.  Erhalten Sie ein Handle für den Kryptografieanbieter.
4.  Öffnen Sie einen [*Zertifikat Speicher*](../secgloss/c-gly.md) , der das Zertifikat des Signatur Gebers enthält.
5.  Erhalten Sie eine Adresse für das Zertifikat des Signatur Gebers.
6.  Weisen Sie die Adresse des Zertifikats dem Index NULL des *msgcert* -Arrays zu.
7.  Weisen Sie die Adressen aller anderen Zertifikate, die in die Nachricht eingeschlossen werden sollen, dem *msgcert* -Array zu.
8.  Initialisieren Sie die Struktur des [**crypt- \_ Algorithmus \_ Bezeichners**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier) , und initialisieren Sie den Member **pszobjid** mit dem gewünschten Hash Algorithmus und den anderen Membern entsprechend.
9.  Initialisieren Sie die Struktur der Crypt-Signierungs [**\_ \_ Nachricht \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para) , und initialisieren Sie das **psigningcert** -Element mit der Adresse des Zertifikats des Signatur Gebers, dem **msgcert** -Arraymember in die Adresse des Signatur Gebers und der anderen Zertifikate, dem **HashAlgorithm** -Member für die Adresse der [**crypt-Algorithmus- \_ \_ bezeichnerstruktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier) und den anderen Membern.
10. Nennen Sie die Funktion [**cryptsignmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage) , und übergeben Sie dabei die [**crypt \_ Sign \_ Message- \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para) -Struktur für den *psignpara* -Parameter, die Adresse des Arrays "zu Signier Ende Daten" für den Parameter " *rgpbtobesigned* ", eine Adresse für den *pbsignedblob* -Ausgabeparameter und Werte für die anderen Parameter nach Bedarf.

 

 
