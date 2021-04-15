---
description: Zeigt die Schritte zum Entschlüsseln einer verschlüsselten Nachricht an.
ms.assetid: 6af7dd28-325e-431a-9cdb-109d93af6302
title: Entschlüsseln von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970f16862bb8c6693b2ff11f519af3f7c412024b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350158"
---
# <a name="decrypting-data"></a><span data-ttu-id="53cdb-103">Entschlüsseln von Daten</span><span class="sxs-lookup"><span data-stu-id="53cdb-103">Decrypting Data</span></span>

<span data-ttu-id="53cdb-104">Dieser Abschnitt enthält die Schritte zum Entschlüsseln einer verschlüsselten Nachricht.</span><span class="sxs-lookup"><span data-stu-id="53cdb-104">This section presents the steps to decrypt an encrypted message.</span></span>

<span data-ttu-id="53cdb-105">**So entschlüsseln Sie eine verschlüsselte Nachricht**</span><span class="sxs-lookup"><span data-stu-id="53cdb-105">**To decrypt an encrypted message**</span></span>

1.  <span data-ttu-id="53cdb-106">Einen Zeiger auf die Digital eingeschlossene Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="53cdb-106">Get a pointer to the digitally enveloped message.</span></span>
2.  <span data-ttu-id="53cdb-107">Öffnen Sie einen Zertifikat Speicher.</span><span class="sxs-lookup"><span data-stu-id="53cdb-107">Open a certificate store.</span></span>
3.  <span data-ttu-id="53cdb-108">Rufen Sie in der Meldung den Empfänger Bezeichner (meine ID) ab.</span><span class="sxs-lookup"><span data-stu-id="53cdb-108">From the message, retrieve the recipient identifier (My ID).</span></span>
4.  <span data-ttu-id="53cdb-109">Verwenden Sie den Empfänger Bezeichner, um das Zertifikat abzurufen.</span><span class="sxs-lookup"><span data-stu-id="53cdb-109">Use the recipient identifier to retrieve the certificate.</span></span>
5.  <span data-ttu-id="53cdb-110">Den privaten Schlüssel für das Zertifikat erhalten.</span><span class="sxs-lookup"><span data-stu-id="53cdb-110">Get the private key for the certificate.</span></span>
6.  <span data-ttu-id="53cdb-111">Verwenden Sie den privaten Schlüssel, um den symmetrischen (Sitzungs-) Schlüssel zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="53cdb-111">Use the private key to decrypt the symmetric (session) key.</span></span>
7.  <span data-ttu-id="53cdb-112">Rufen Sie den Verschlüsselungsalgorithmus aus der Nachricht ab.</span><span class="sxs-lookup"><span data-stu-id="53cdb-112">Retrieve the encryption algorithm from the message.</span></span>
8.  <span data-ttu-id="53cdb-113">Entschlüsseln Sie die Daten mithilfe des entschlüsselten Sitzungsschlüssels und des Verschlüsselungsalgorithmus.</span><span class="sxs-lookup"><span data-stu-id="53cdb-113">Using the decrypted session key and the encryption algorithm, decrypt the data.</span></span>

<span data-ttu-id="53cdb-114">[**Cryptdecryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) übernimmt alle Aufgaben zum Entschlüsseln einer Nachricht. die Initialisierung von Strukturen und anderen Daten ist jedoch weiterhin erforderlich.</span><span class="sxs-lookup"><span data-stu-id="53cdb-114">[**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) does all of the tasks for decrypting a message; however, initialization of structures and other data is still necessary.</span></span>

<span data-ttu-id="53cdb-115">**So entschlüsseln Sie Daten mithilfe von "cryptdecryptmessage"**</span><span class="sxs-lookup"><span data-stu-id="53cdb-115">**To decrypt data using CryptDecryptMessage**</span></span>

1.  <span data-ttu-id="53cdb-116">Einen Zeiger auf das verschlüsselte Blob erhalten.</span><span class="sxs-lookup"><span data-stu-id="53cdb-116">Get a pointer to the encrypted BLOB.</span></span>
2.  <span data-ttu-id="53cdb-117">Öffnen Sie einen Zertifikat Speicher.</span><span class="sxs-lookup"><span data-stu-id="53cdb-117">Open a certificate store.</span></span>
3.  <span data-ttu-id="53cdb-118">Erstellen Sie ein Zertifikat Speicher Array.</span><span class="sxs-lookup"><span data-stu-id="53cdb-118">Create a certificate store array.</span></span>
4.  <span data-ttu-id="53cdb-119">Initialisieren Sie [**die \_ Meldung "Crypt entschlüsselungsfehlermeldung \_ \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para) ".</span><span class="sxs-lookup"><span data-stu-id="53cdb-119">Initialize the [**CRYPT\_DECRYPT\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para) structure.</span></span>
5.  <span data-ttu-id="53cdb-120">Nennen Sie [**cryptdecryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) , um die in der Nachricht enthaltenen Daten zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="53cdb-120">Call [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to decrypt the data contained in the message.</span></span>

<span data-ttu-id="53cdb-121">[Beispiel für ein C-Programm: die Verwendung von cryptencryptmessage und cryptdecryptmessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) implementiert die soeben vorgestellte Prozedur.</span><span class="sxs-lookup"><span data-stu-id="53cdb-121">[Example C Program: Using CryptEncryptMessage and CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) implements the procedure just presented.</span></span> <span data-ttu-id="53cdb-122">Kommentare zeigen an, welche Code Elemente die einzelnen Schritte in der Prozedur ausführen.</span><span class="sxs-lookup"><span data-stu-id="53cdb-122">Comments show which code elements accomplish each step in the procedure.</span></span> <span data-ttu-id="53cdb-123">Weitere Informationen zur-Funktion finden Sie unter [**cryptdecryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage). Weitere Informationen zur Datenstruktur finden Sie unter [**crypt \_ Entschlüsseln der \_ Nachricht \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para).</span><span class="sxs-lookup"><span data-stu-id="53cdb-123">For details about the function, see [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage), and for details about the data structure, see [**CRYPT\_DECRYPT\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para).</span></span>

 

 



