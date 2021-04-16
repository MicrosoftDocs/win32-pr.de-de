---
description: Allgemeine Aufgaben, die zum Decodieren einer eingeschlossenen Nachricht erforderlich sind.
ms.assetid: cb71ea3a-0edd-4d46-8088-a395fab89d2b
title: Decodieren von eingeschlossenen Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1a0ba12e967f5a0cd56347c0839ce9fca40f02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104557336"
---
# <a name="decoding-enveloped-data"></a><span data-ttu-id="c33a4-103">Decodieren von eingeschlossenen Daten</span><span class="sxs-lookup"><span data-stu-id="c33a4-103">Decoding Enveloped Data</span></span>

<span data-ttu-id="c33a4-104">Die allgemeinen Aufgaben, die zum Decodieren einer eingeschlossenen Nachricht erforderlich sind, werden in der folgenden Abbildung dargestellt und in der folgenden Liste beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c33a4-104">The general tasks required to decode an enveloped message are depicted in the following illustration and described in the list that follows it.</span></span>

![Decodieren von eingeschlossenen Daten](images/decemsg.png)

<span data-ttu-id="c33a4-106">Die Abfolge der Ereignisse für das Decodieren von eingeschlossenen Daten mithilfe der Schlüssel Transport Schlüsselverwaltung, wie in der vorherigen Abbildung dargestellt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c33a4-106">The sequence of events for decoding enveloped data using key transport key management, as depicted in the previous illustration, is as follows:</span></span>

-   <span data-ttu-id="c33a4-107">Ein Zeiger auf die [*Digital eingehüllte*](../secgloss/d-gly.md) Nachricht wird abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c33a4-107">A pointer to the [*digitally enveloped*](../secgloss/d-gly.md) message is retrieved.</span></span>
-   <span data-ttu-id="c33a4-108">Ein [*Zertifikat Speicher*](../secgloss/c-gly.md) wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="c33a4-108">A [*certificate store*](../secgloss/c-gly.md) is opened.</span></span>
-   <span data-ttu-id="c33a4-109">In der Meldung wird die Empfänger-ID (meine ID) abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c33a4-109">From the message, the recipient ID (My ID) is retrieved.</span></span>
-   <span data-ttu-id="c33a4-110">Die Empfänger-ID wird zum Abrufen des Zertifikats verwendet.</span><span class="sxs-lookup"><span data-stu-id="c33a4-110">The recipient ID is used to retrieve the certificate.</span></span>
-   <span data-ttu-id="c33a4-111">Der diesem Zertifikat zugeordnete [*private Schlüssel*](../secgloss/p-gly.md) wird abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c33a4-111">The [*private key*](../secgloss/p-gly.md) associated with that certificate is retrieved.</span></span>
-   <span data-ttu-id="c33a4-112">Der private Schlüssel wird verwendet, um den [*symmetrischen*](../secgloss/s-gly.md) ([*Sitzungs*](../secgloss/s-gly.md)-) Schlüssel zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="c33a4-112">The private key is used to decrypt the [*symmetric*](../secgloss/s-gly.md) ([*session*](../secgloss/s-gly.md)) key.</span></span>
-   <span data-ttu-id="c33a4-113">Der Verschlüsselungsalgorithmus wird aus der Nachricht abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c33a4-113">The encryption algorithm is retrieved from the message.</span></span>
-   <span data-ttu-id="c33a4-114">Mit dem privaten Schlüssel und dem Verschlüsselungsalgorithmus werden die Daten entschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="c33a4-114">Using the private key and encryption algorithm, the data is decrypted.</span></span>

<span data-ttu-id="c33a4-115">Im folgenden Verfahren werden Low-Level-Nachrichten Funktionen verwendet, um die gerade aufgeführten Aufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c33a4-115">The following procedure uses low-level message functions to accomplish the tasks just listed.</span></span>

<span data-ttu-id="c33a4-116">**So decodieren Sie eine eingeschlossene Nachricht**</span><span class="sxs-lookup"><span data-stu-id="c33a4-116">**To decode an enveloped message**</span></span>

1.  <span data-ttu-id="c33a4-117">Einen Zeiger auf das codierte BLOB erhalten.</span><span class="sxs-lookup"><span data-stu-id="c33a4-117">Get a pointer to the encoded BLOB.</span></span>
2.  <span data-ttu-id="c33a4-118">Nennen Sie [**cryptmsgopentodecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), und übergeben Sie die erforderlichen Argumente.</span><span class="sxs-lookup"><span data-stu-id="c33a4-118">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passing the necessary arguments.</span></span>
3.  <span data-ttu-id="c33a4-119">Nennen Sie [**cryptmsgupdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) einmal, und übergeben Sie dabei das in Schritt 2 abgerufene Handle und einen Zeiger auf die Daten, die decodiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c33a4-119">Call [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) once, passing in the handle retrieved in step 2 and a pointer to the data that is to be decoded.</span></span> <span data-ttu-id="c33a4-120">Dies bewirkt, dass die entsprechenden Aktionen für die Nachricht durchgeführt werden, abhängig vom Nachrichtentyp.</span><span class="sxs-lookup"><span data-stu-id="c33a4-120">This causes the appropriate actions to be taken on the message, depending on the message type.</span></span>
4.  <span data-ttu-id="c33a4-121">Nennen Sie [**cryptmsggetparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), und übergeben Sie das in Schritt 2 und CMSG-Typparameter abgerufene handle, \_ \_ um zu überprüfen, ob die Nachricht vom eingeschlossenen Datentyp ist.</span><span class="sxs-lookup"><span data-stu-id="c33a4-121">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in the handle retrieved in step 2 and CMSG\_TYPE\_PARAM to verify that the message is of the enveloped data type.</span></span>
5.  <span data-ttu-id="c33a4-122">Wiederholen Sie den Befehl [**cryptmsggetparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), und übergeben Sie \_ \_ den internen Inhaltstyp CMSG, \_ \_ um den Datentyp des [*inneren Inhalts*](../secgloss/i-gly.md)abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c33a4-122">Again call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in CMSG\_INNER\_CONTENT\_TYPE\_PARAM to get the data type of the [*inner content*](../secgloss/i-gly.md).</span></span>
6.  <span data-ttu-id="c33a4-123">Wenn der Datentyp der inneren Inhalte " **Daten**" ist, können Sie den Inhalt entschlüsseln und decodieren.</span><span class="sxs-lookup"><span data-stu-id="c33a4-123">If the inner content data type is **data**, proceed to decrypt and decode the content.</span></span> <span data-ttu-id="c33a4-124">Andernfalls führen Sie eine für den Inhalts Datentyp geeignete Decodierungs Prozedur aus.</span><span class="sxs-lookup"><span data-stu-id="c33a4-124">Otherwise, run a decoding procedure appropriate for the content data type.</span></span>
7.  <span data-ttu-id="c33a4-125">Angenommen, der innere Inhaltstyp ist "Data", initialisieren Sie die [**CMSG \_ STRG \_ entschlüsseln \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para) -Datenstruktur, und nennen Sie [**cryptmsgcontrol**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), und übergeben Sie CMSG \_ STRG \_ entschlüsseln und die Adresse der-Struktur.</span><span class="sxs-lookup"><span data-stu-id="c33a4-125">Assuming the inner content type is "data", initialize the [**CMSG\_CTRL\_DECRYPT\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para) data structure, and call [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passing in CMSG\_CTRL\_DECRYPT and the address of the structure.</span></span> <span data-ttu-id="c33a4-126">Der Inhalt wird entschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="c33a4-126">The content will be decrypted.</span></span>
8.  <span data-ttu-id="c33a4-127">Nennen Sie [**cryptmsggetparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), und übergeben Sie CMSG \_ Content \_ param, um einen Zeiger auf das decodierte inhaltsdatenblob (**Byte** Zeichenfolge) zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c33a4-127">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in CMSG\_CONTENT\_PARAM to get a pointer to the decoded content data BLOB (**BYTE** string).</span></span>
9.  <span data-ttu-id="c33a4-128">" [**Cryptmsgclose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) " aufrufen, um die Nachricht zu schließen.</span><span class="sxs-lookup"><span data-stu-id="c33a4-128">Call [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) to close the message.</span></span>

<span data-ttu-id="c33a4-129">Das Ergebnis dieser Prozedur ist, dass die Nachricht decodiert und entschlüsselt und ein Zeiger in das inhaltsdatenblob abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c33a4-129">The result of this procedure is that the message is decoded and decrypted and a pointer is retrieved to the content data BLOB.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c33a4-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c33a4-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c33a4-131">Beispiel-C-Programm: Codieren einer eingeschlossenen, signierten Nachricht</span><span class="sxs-lookup"><span data-stu-id="c33a4-131">Example C Program: Encoding an Enveloped, Signed Message</span></span>](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
