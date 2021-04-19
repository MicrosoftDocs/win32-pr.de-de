---
description: Erläutert das Verfahren zum Speichern eines Sitzungsschlüssels.
ms.assetid: 9ab7f747-9c69-40b5-af78-163f3ba315bf
title: Speichern eines Sitzungsschlüssels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b17de657ddba47dd77f68c1ee7a2adfdf93e7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356189"
---
# <a name="storing-a-session-key"></a><span data-ttu-id="481ec-103">Speichern eines Sitzungsschlüssels</span><span class="sxs-lookup"><span data-stu-id="481ec-103">Storing a Session Key</span></span>

> [!Note]  
> <span data-ttu-id="481ec-104">In diesem Abschnitt wird davon ausgegangen, dass Benutzer über einen Satz von [*öffentlichen/privaten Schlüsselpaaren*](../secgloss/p-gly.md)verfügen.</span><span class="sxs-lookup"><span data-stu-id="481ec-104">This section assumes that users possess a set of [*public/private key pairs*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="481ec-105">Anweisungen und ein Beispiel zum Erstellen von Schlüsselpaaren finden Sie im [Beispiel C-Programm: Erstellen eines Schlüssel Containers und](example-c-program-creating-a-key-container-and-generating-keys.md)Erstellen von Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="481ec-105">Instructions and an example for creating key pairs can be found in [Example C Program: Creating a Key Container and Generating Keys](example-c-program-creating-a-key-container-and-generating-keys.md).</span></span>

 

<span data-ttu-id="481ec-106">**So speichern Sie einen Sitzungsschlüssel**</span><span class="sxs-lookup"><span data-stu-id="481ec-106">**To store a session key**</span></span>

1.  <span data-ttu-id="481ec-107">Erstellen Sie ein einfaches [*Schlüsselblob*](../secgloss/k-gly.md) mithilfe der [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="481ec-107">Create a simple [*key BLOB*](../secgloss/k-gly.md) by using the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function.</span></span> <span data-ttu-id="481ec-108">Dadurch wird der Sitzungsschlüssel vom CSP in den Speicherbereich einer Anwendung übertragen.</span><span class="sxs-lookup"><span data-stu-id="481ec-108">This will transfer the session key from the CSP to an application's memory space.</span></span> <span data-ttu-id="481ec-109">Geben Sie an, dass ein öffentlicher Exchange-Schlüssel zum Signieren des Schlüssel-BLOBs verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="481ec-109">Specify that an exchange public key be used to sign the key BLOB.</span></span>
2.  <span data-ttu-id="481ec-110">Speichert das signierte Schlüsselblob auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="481ec-110">Store the signed key BLOB to disk.</span></span> <span data-ttu-id="481ec-111">Es wird davon ausgegangen, dass alle Datenträger nicht sicher sind.</span><span class="sxs-lookup"><span data-stu-id="481ec-111">It is assumed that all disks are nonsecure.</span></span>
3.  <span data-ttu-id="481ec-112">Wenn der Schlüssel benötigt wird, lesen Sie den Schlüssel-BLOB von der Festplatte.</span><span class="sxs-lookup"><span data-stu-id="481ec-112">When the key is needed, read the key BLOB from disk.</span></span>
4.  <span data-ttu-id="481ec-113">Importieren Sie das Schlüsselblob mithilfe der [**cryptimportkey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) -Funktion wieder in den CSP.</span><span class="sxs-lookup"><span data-stu-id="481ec-113">Import the key BLOB back into the CSP by using the [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) function.</span></span>

<span data-ttu-id="481ec-114">Ein Beispiel für das Erstellen eines [*Sitzungsschlüssels*](../secgloss/s-gly.md) und das Exportieren des Schlüssels in ein [*einfaches Schlüsselblob*](../secgloss/s-gly.md) , das in eine Datenträger Datei geschrieben werden kann, finden Sie unter [Beispiel C-Programm: Exportieren eines Sitzungsschlüssels](example-c-program-exporting-a-session-key.md).</span><span class="sxs-lookup"><span data-stu-id="481ec-114">For an example of creating a [*session key*](../secgloss/s-gly.md) and exporting that key to a [*simple key BLOB*](../secgloss/s-gly.md) that can be written to a disk file, see [Example C Program: Exporting a Session Key](example-c-program-exporting-a-session-key.md).</span></span>

<span data-ttu-id="481ec-115">Diese Prozedur bietet nur minimale Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="481ec-115">This procedure provides only minimal security.</span></span> <span data-ttu-id="481ec-116">Wenn der gespeicherte Sitzungsschlüssel verwendet wird, um Daten zu einem späteren Zeitpunkt zu verschlüsseln, bietet das vorherige Verfahren keine angemessene Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="481ec-116">If the stored session key will be used to encrypt data at a later date, the preceding procedure does not provide adequate security.</span></span>

<span data-ttu-id="481ec-117">Signieren Sie das Schlüsselblob mit einem privaten Exchange-Schlüssel, bevor es auf einem Datenträger gespeichert wird, um die Sicherheit zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="481ec-117">To provide greater security, sign the key BLOB with an exchange private key before it is stored to disk.</span></span> <span data-ttu-id="481ec-118">Wenn das Schlüssel-BLOB später von der Festplatte gelesen wird, kann die Signatur überprüft werden, um sicherzustellen, dass das Schlüsselblob intakt ist.</span><span class="sxs-lookup"><span data-stu-id="481ec-118">When the key BLOB is later read from disk, its signature can be validated to ensure that the key BLOB is intact.</span></span>

<span data-ttu-id="481ec-119">Wenn das Schlüsselblob nicht signiert ist, kann jeder Benutzer mit Zugriff auf den Datenträger oder auf ein anderes Medium, auf dem der Schlüssel gespeichert ist, einen neuen Sitzungsschlüssel erstellen.</span><span class="sxs-lookup"><span data-stu-id="481ec-119">If the key BLOB is not signed, anyone with access to the disk or other media where the key is stored can create a new session key.</span></span>

<span data-ttu-id="481ec-120">Der neue Sitzungsschlüssel kann mit dem [*öffentlichen Schlüssel*](../secgloss/p-gly.md) [*Austausch Schlüssel*](../secgloss/e-gly.md)des Benutzers verschlüsselt werden, und dieser neue Schlüssel kann durch den ursprünglichen Schlüssel ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="481ec-120">The new session key can be encrypted with the original user's [*public key*](../secgloss/p-gly.md) [*exchange key*](../secgloss/e-gly.md), and this new key can be substituted for the original.</span></span> <span data-ttu-id="481ec-121">Wenn der Benutzer den ersetzten Sitzungsschlüssel zum Verschlüsseln von Dateien und Nachrichten unwissentlich verwendet hat, kann die Person, die den Ersatzschlüssel erstellt hat, Sie problemlos entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="481ec-121">If the user unknowingly used the substituted session key to encrypt files and messages, the individual who created the substitute key could easily decrypt them.</span></span>

<span data-ttu-id="481ec-122">Digitale Signaturen werden in [Hashes und digitalen Signaturen](hashes-and-digital-signatures.md)ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="481ec-122">Digital signatures are discussed in detail in [Hashes and Digital Signatures](hashes-and-digital-signatures.md).</span></span>

 

 
