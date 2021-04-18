---
description: Prozess zum Decodieren signierter Daten.
ms.assetid: 803220d0-7963-4fc4-8451-a979e54a9cc3
title: Decodieren signierter Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdfd327746c5d0ba8e7089e1c273817b76c16370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340180"
---
# <a name="decoding-signed-data"></a><span data-ttu-id="9c964-103">Decodieren signierter Daten</span><span class="sxs-lookup"><span data-stu-id="9c964-103">Decoding Signed Data</span></span>

<span data-ttu-id="9c964-104">Der folgende allgemeine Prozess decodiert einen [*signierten Datentyp*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="9c964-104">The following general process decodes a [*signed data*](../secgloss/s-gly.md) type.</span></span>

<span data-ttu-id="9c964-105">**Decodieren einer signierten Nachricht**</span><span class="sxs-lookup"><span data-stu-id="9c964-105">**To decode a signed message**</span></span>

1.  <span data-ttu-id="9c964-106">Einen Zeiger auf das codierte BLOB erhalten.</span><span class="sxs-lookup"><span data-stu-id="9c964-106">Get a pointer to the encoded BLOB.</span></span>
2.  <span data-ttu-id="9c964-107">Nennen Sie [**cryptmsgopentodecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), und übergeben Sie die erforderlichen Argumente.</span><span class="sxs-lookup"><span data-stu-id="9c964-107">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passing the necessary arguments.</span></span>
3.  <span data-ttu-id="9c964-108">Nennen Sie [**cryptmsgupdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) einmal, und übergeben Sie dabei das in Schritt 2 abgerufene Handle und einen Zeiger auf die Daten, die decodiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9c964-108">Call [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) once, passing in the handle retrieved in step 2 and a pointer to the data that is to be decoded.</span></span> <span data-ttu-id="9c964-109">Dies bewirkt, dass die entsprechenden Aktionen für die Nachricht durchgeführt werden, abhängig vom Nachrichtentyp.</span><span class="sxs-lookup"><span data-stu-id="9c964-109">This causes the appropriate actions to be taken on the message, depending on the message type.</span></span>
4.  <span data-ttu-id="9c964-110">Aufrufen von [**cryptmsggetparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), übergeben des in Schritt 2 abgerufenen Handles und der entsprechenden Parametertypen für den Zugriff auf die decodierten Daten.</span><span class="sxs-lookup"><span data-stu-id="9c964-110">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in the handle retrieved in step 2 and the appropriate parameter types to access the decoded data.</span></span> <span data-ttu-id="9c964-111">Übergeben Sie z. b. CMSG \_ Content \_ param, um einen Zeiger auf den decodierten Inhalt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9c964-111">For example, pass in CMSG\_CONTENT\_PARAM to get a pointer to the decoded content.</span></span>

<span data-ttu-id="9c964-112">Im folgenden allgemeinen Prozess wird die Signatur einer decodierten, signierten Nachricht überprüft.</span><span class="sxs-lookup"><span data-stu-id="9c964-112">The following general process verifies the signature of a decoded, signed message.</span></span>

<span data-ttu-id="9c964-113">**So überprüfen Sie die Signatur einer decodierten, signierten Nachricht**</span><span class="sxs-lookup"><span data-stu-id="9c964-113">**To verify the signature of a decoded, signed message**</span></span>

1.  <span data-ttu-id="9c964-114">Nennen Sie [**cryptmsggetparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), und übergeben Sie das Nachrichten Handle und CMSG \_ Signer \_ CERT \_ Info \_ param, um die [**Zertifikat \_ Informationen**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) des Signatur Gebers aus der Nachricht abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9c964-114">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in the message handle and CMSG\_SIGNER\_CERT\_INFO\_PARAM to get the signer's [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) from the message.</span></span>
2.  <span data-ttu-id="9c964-115">Zum Öffnen eines temporären Informationsspeicher, der mit den Zertifikaten aus der Nachricht initialisiert wird, wird " [**certopdstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) " aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="9c964-115">Call [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) to open a temporary store that is initialized with the certificates from the message.</span></span>
3.  <span data-ttu-id="9c964-116">Nennen Sie [**certgetsubjetcertificallefromstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) , um die [**Zertifikat \_ Informationen**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) des Signatur Gebers aus den in der Nachricht enthaltenen Zertifikaten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9c964-116">Call [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) to get the signer's [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) from the certificates included in the message.</span></span>
4.  <span data-ttu-id="9c964-117">Nennen Sie [**cryptmsgcontrol**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), und übergeben \_ \_ \_ Sie die Signatur von CMSG STRG Verify, um die Signaturen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9c964-117">Call [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passing in CMSG\_CTRL\_VERIFY\_SIGNATURE to verify the signatures.</span></span>
5.  <span data-ttu-id="9c964-118">" [**Cryptmsgclose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) " aufrufen, um die Nachricht zu schließen.</span><span class="sxs-lookup"><span data-stu-id="9c964-118">Call [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) to close the message.</span></span>

<span data-ttu-id="9c964-119">Das Ergebnis dieser Prozeduren ist, dass die Signatur überprüft und ein Zeiger auf den decodierten Nachrichten Inhalt abgerufen wird, der in Schritt 4 der Prozedur zum Decodieren einer signierten Nachricht abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="9c964-119">The result of these procedures is that the signature is verified and a pointer is retrieved to the decoded message content obtained in step 4 of the procedure for decoding a signed message.</span></span>

<span data-ttu-id="9c964-120">Weitere Informationen zur C-Codierung finden Sie [unter Beispiel c-Programm: Signieren, codieren, decodieren und Überprüfen einer Nachricht](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).</span><span class="sxs-lookup"><span data-stu-id="9c964-120">For C coding details, see [Example C Program: Signing, Encoding, Decoding, and Verifying a Message](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).</span></span>

 

 
