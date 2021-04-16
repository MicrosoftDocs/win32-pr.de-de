---
description: Beschreibt die Schritte, die zum Verschlüsseln einer Nachricht mit den grundlegenden Kryptografiefunktionen erforderlich sind.
ms.assetid: 34167767-96c5-4a20-b629-07e4d036b4d1
title: Verschlüsseln von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44db44db08268241e399107d8af4088dac3c0c2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104566527"
---
# <a name="encrypting-data"></a><span data-ttu-id="c7cdb-103">Verschlüsseln von Daten</span><span class="sxs-lookup"><span data-stu-id="c7cdb-103">Encrypting Data</span></span>

<span data-ttu-id="c7cdb-104">Im folgenden Verfahren werden die Schritte beschrieben, die zum Verschlüsseln einer Nachricht mit den grundlegenden Kryptografiefunktionen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-104">The following procedure describes steps to take to encrypt a message with the Base Cryptography Functions.</span></span> <span data-ttu-id="c7cdb-105">Informationen zum Verschlüsseln von Nachrichten mit PKCS \# 7-Standards finden Sie unter [Nachrichten Funktionen auf niedriger Ebene](cryptography-functions.md) und [vereinfachte Nachrichten Funktionen](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="c7cdb-105">To encrypt messages using PKCS \#7 standards, see [Low-level Message Functions](cryptography-functions.md) and [Simplified Message Functions](cryptography-functions.md).</span></span>

<span data-ttu-id="c7cdb-106">**So verschlüsseln Sie eine Nachricht**</span><span class="sxs-lookup"><span data-stu-id="c7cdb-106">**To encrypt a message**</span></span>

1.  <span data-ttu-id="c7cdb-107">Generieren Sie einen Sitzungsschlüssel mithilfe der [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-107">Generate a session key by using the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function.</span></span>

    <span data-ttu-id="c7cdb-108">Durch diesen Befehl wird ein zufälliger Schlüssel generiert und ein Handle zurückgegeben, damit der Schlüssel zum Verschlüsseln und Entschlüsseln von Daten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-108">Making this call generates a random key and returns a handle so the key can be used to encrypt and decrypt data.</span></span> <span data-ttu-id="c7cdb-109">Der zu verwendende Verschlüsselungsalgorithmus wird an dieser Stelle ebenfalls angegeben.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-109">The encryption algorithm to use is also specified at this point.</span></span> <span data-ttu-id="c7cdb-110">Da CryptoAPI nicht zulässt, dass Anwendungen öffentliche Schlüssel Algorithmen zum Verschlüsseln von Massendaten verwenden, geben Sie einen symmetrischen Algorithmus wie RC2 oder RC4 mit dem [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) -Aufruf an.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-110">Because CryptoAPI does not permit applications to use public key algorithms to encrypt bulk data, specify a symmetric algorithm such as RC2 or RC4 with the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) call.</span></span>

2.  <span data-ttu-id="c7cdb-111">Verwenden Sie alternativ die [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) -Funktion, um ein Kennwort in einen Schlüssel umzuwandeln, der für die Verschlüsselung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-111">Alternatively, use the [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) function to transform a password into a key suitable for encryption.</span></span>

    <span data-ttu-id="c7cdb-112">Wenn eine Anwendung die Nachricht verschlüsseln muss, damit alle Benutzer mit einem bestimmten Kennwort die Daten entschlüsseln können, verwenden Sie [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) , um das Kennwort in einen Schlüssel zu transformieren, der für die Verschlüsselung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-112">If an application needs to encrypt the message so that anyone with a specified password can decrypt the data, use [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) to transform the password into a key suitable for encryption.</span></span>

    > [!Note]  
    > <span data-ttu-id="c7cdb-113">In diesem Fall wird diese Funktion anstelle der [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) -Funktion aufgerufen, und die nachfolgenden [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) -Aufrufe werden nicht benötigt.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-113">In this case, this function is called instead of the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function and the subsequent [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) calls are not needed.</span></span>

     

3.  <span data-ttu-id="c7cdb-114">Legen Sie bei Bedarf zusätzliche kryptografieeigenschaften des Schlüssels mithilfe der [**cryptsetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) -Funktion fest.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-114">If necessary, set extra cryptographic properties of the key by using the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function</span></span>

    <span data-ttu-id="c7cdb-115">Nachdem der Schlüssel generiert wurde, können zusätzliche kryptografieeigenschaften des Schlüssels mit der [**cryptsetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)-Funktion festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-115">After the key has been generated, extra cryptographic properties of the key can be set with the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)function.</span></span> <span data-ttu-id="c7cdb-116">Diese Funktion ermöglicht, dass verschiedene Abschnitte der Datei mit anderen Schlüssel Salzen verschlüsselt werden und eine Möglichkeit zum Ändern des Verschlüsselungs Modus oder Initialisierungs Vektors des Schlüssels bietet.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-116">This function allows different sections of the file to be encrypted with different key salts and provides a way to change the cipher mode or initialization vector of the key.</span></span> <span data-ttu-id="c7cdb-117">Diese Parameter können verwendet werden, um die Verschlüsselung einem bestimmten Daten Verschlüsselungsstandard zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-117">These parameters can be used to make the encryption conform with a particular data encryption standard.</span></span>

4.  <span data-ttu-id="c7cdb-118">Verschlüsseln Sie die Daten in der Datei mit der [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-118">Encrypt the data in the file with the [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) function.</span></span>

    <span data-ttu-id="c7cdb-119">Die [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) -Funktion nimmt den im vorherigen Schritt generierten Sitzungsschlüssel an und verschlüsselt einen Datenpuffer.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-119">The [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) function takes the session key that was generated in the previous step and encrypts a buffer of data.</span></span>

    > [!Note]  
    > <span data-ttu-id="c7cdb-120">Wenn die Daten verschlüsselt werden, werden die Daten möglicherweise durch den Verschlüsselungsalgorithmus leicht erweitert.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-120">As the data is encrypted, the data may be slightly expanded by the encryption algorithm.</span></span> <span data-ttu-id="c7cdb-121">Die Anwendung ist dafür verantwortlich, die Länge der verschlüsselten Daten zu merken, damit die richtige Länge später für die [**cryptentschlpt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) -Funktion angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-121">The application is responsible for remembering the length of the encrypted data so the proper length can later be specified for the [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) function.</span></span>

     

5.  <span data-ttu-id="c7cdb-122">Verwenden Sie optional die [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) -Funktion, um dem aktuellen Benutzer zu gestatten, die Daten in der Zukunft zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-122">Optionally, use the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function to allow the current user to decrypt the data in the future.</span></span>

    <span data-ttu-id="c7cdb-123">Damit der aktuelle Benutzer die Daten zukünftig entschlüsseln kann, wird die [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) -Funktion verwendet, um den Entschlüsselungsschlüssel in verschlüsselter Form (einem Schlüsselblob) zu speichern, die nur mit dem privaten Schlüssel des Benutzers entschlüsselt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-123">To allow the current user to decrypt the data in the future, the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function is used to save the decryption key in an encrypted form (a key BLOB) that can only be decrypted with the user's private key.</span></span> <span data-ttu-id="c7cdb-124">Diese Funktion erfordert zu diesem Zweck den öffentlichen Schlüsselaustausch Schlüssel des Benutzers, der über die Funktion " [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) " abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-124">This function requires the user's key exchange public key for this purpose, which can be obtained by using the [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) function.</span></span> <span data-ttu-id="c7cdb-125">Die **CryptExportKey** -Funktion gibt ein Schlüssel-BLOB zurück, das von der Anwendung für die Verwendung beim Entschlüsseln der Datei gespeichert werden muss.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-125">The **CryptExportKey** function will return a key BLOB that must be stored by the application for use in decrypting the file</span></span>

> [!Note]  
> <span data-ttu-id="c7cdb-126">Wenn die Anwendung Zertifikate (oder öffentliche Schlüssel) für andere Benutzer aufweist, können andere Benutzer die Datei entschlüsseln, indem Sie [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) -Aufrufe für jeden Benutzer ausführen, der Zugriff erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-126">If the application has certificates (or public keys) for other users, it can permit other users to decrypt the file by performing [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) calls for each user who should receive access.</span></span> <span data-ttu-id="c7cdb-127">Die zurückgegebenen schlüsselblobspeicher müssen von der Anwendung gespeichert werden, wie in Schritt 5.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-127">The returned key BLOBs must be stored by the application, as in step 5.</span></span>

 

## <a name="creating-an-encrypted-message"></a><span data-ttu-id="c7cdb-128">Erstellen einer verschlüsselten Nachricht</span><span class="sxs-lookup"><span data-stu-id="c7cdb-128">Creating an Encrypted Message</span></span>

<span data-ttu-id="c7cdb-129">Die vereinfachten Nachrichten Funktionen erleichtern das Verschlüsseln und Entschlüsseln von Daten.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-129">The simplified message functions make it easier to encrypt and decrypt data.</span></span> <span data-ttu-id="c7cdb-130">Die folgende Abbildung zeigt die einzelnen Aufgaben, die zum Verschlüsseln einer Nachricht durchgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-130">The following illustration depicts the individual tasks that must be accomplished to encrypt a message.</span></span> <span data-ttu-id="c7cdb-131">Die Schritte werden in der folgenden Liste beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-131">The steps are described in the following list.</span></span>

![Verschlüsseln einer Nachricht](images/encmsg.png)

<span data-ttu-id="c7cdb-133">**So verschlüsseln Sie eine Nachricht**</span><span class="sxs-lookup"><span data-stu-id="c7cdb-133">**To encrypt a message**</span></span>

1.  <span data-ttu-id="c7cdb-134">Einen Zeiger auf die Klartext-Nachricht erhalten.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-134">Get a pointer to the plaintext message.</span></span>
2.  <span data-ttu-id="c7cdb-135">Generieren Sie einen symmetrischen (Sitzungs-) Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-135">Generate a symmetric (session) key.</span></span>
3.  <span data-ttu-id="c7cdb-136">Verschlüsseln Sie die Nachrichten Daten mithilfe des symmetrischen Schlüssels und des angegebenen Verschlüsselungsalgorithmus.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-136">Using the symmetric key and specified encryption algorithm, encrypt the message data.</span></span>
4.  <span data-ttu-id="c7cdb-137">Öffnen Sie einen Zertifikat Speicher.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-137">Open a certificate store.</span></span>
5.  <span data-ttu-id="c7cdb-138">Das Zertifikat des Empfängers erhalten.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-138">Get the recipient's certificate.</span></span>
6.  <span data-ttu-id="c7cdb-139">Den öffentlichen Schlüssel aus dem Zertifikat des Empfängers erhalten.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-139">Get the public key from the recipient's certificate.</span></span>
7.  <span data-ttu-id="c7cdb-140">Verschlüsseln Sie den symmetrischen Schlüssel mithilfe des öffentlichen Schlüssels des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-140">Using the recipient's public key, encrypt the symmetric key.</span></span>
8.  <span data-ttu-id="c7cdb-141">Den Bezeichner des Empfängers aus dem Zertifikat des Empfängers erhalten.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-141">Get the recipient's identifier from the recipient's certificate.</span></span>
9.  <span data-ttu-id="c7cdb-142">Fügen Sie Folgendes in die Digital eingeschlossene Nachricht ein: den Daten Verschlüsselungsalgorithmus, die verschlüsselten Daten, den verschlüsselten symmetrischen Schlüssel und den Empfänger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-142">Include the following in the digitally enveloped message: the data encryption algorithm, the encrypted data, the encrypted symmetric key, and the recipient identifier.</span></span>

 

 



