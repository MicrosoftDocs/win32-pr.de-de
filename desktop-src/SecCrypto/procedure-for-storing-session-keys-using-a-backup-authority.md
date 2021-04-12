---
description: Eine Anwendung, die eine Sicherungs Stelle zum Speichern von Sitzungs Schlüsseln verwendet, folgt in der Regel den folgenden Schritten.
ms.assetid: 859310ed-6000-44c8-92f7-974326ce0fc9
title: Speichern von Sitzungs Schlüsseln mithilfe einer Sicherungs Stelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59906874f384d4eed9e20d6a781b14e3feba313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345728"
---
# <a name="storing-session-keys-using-a-backup-authority"></a><span data-ttu-id="1de0c-103">Speichern von Sitzungs Schlüsseln mithilfe einer Sicherungs Stelle</span><span class="sxs-lookup"><span data-stu-id="1de0c-103">Storing Session Keys Using a Backup Authority</span></span>

<span data-ttu-id="1de0c-104">Eine Anwendung, die eine [*Sicherungs*](../secgloss/b-gly.md) Stelle zum Speichern von Sitzungs Schlüsseln verwendet, folgt in der Regel den folgenden Schritten.</span><span class="sxs-lookup"><span data-stu-id="1de0c-104">An application using a [*backup authority*](../secgloss/b-gly.md) to store session keys typically follows these steps.</span></span>

<span data-ttu-id="1de0c-105">**So verwenden Sie eine Sicherungs Autorität**</span><span class="sxs-lookup"><span data-stu-id="1de0c-105">**To use a backup authority**</span></span>

1.  <span data-ttu-id="1de0c-106">Verschlüsseln Sie die Datei wie gewohnt.</span><span class="sxs-lookup"><span data-stu-id="1de0c-106">Encrypt the file as usual.</span></span>
2.  <span data-ttu-id="1de0c-107">Exportieren Sie den [*Sitzungsschlüssel*](../secgloss/s-gly.md) , der zum Verschlüsseln der Datei verwendet wird, in ein [*einfaches Schlüsselblob*](../secgloss/s-gly.md), und geben Sie dabei an, dass der [*öffentliche Schlüsselaustausch*](../secgloss/k-gly.md) Schlüssel zum Verschlüsseln des Schlüssel-BLOBs verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="1de0c-107">Export the [*session key*](../secgloss/s-gly.md) used to encrypt the file into a [*simple key BLOB*](../secgloss/s-gly.md), specifying that your own [*key exchange public key*](../secgloss/k-gly.md) be used to encrypt the key BLOB.</span></span> <span data-ttu-id="1de0c-108">Speichern Sie dieses Schlüsselblob mit der verschlüsselten Datei.</span><span class="sxs-lookup"><span data-stu-id="1de0c-108">Store this key BLOB with the encrypted file.</span></span>
3.  <span data-ttu-id="1de0c-109">Exportieren Sie den Sitzungsschlüssel erneut, und geben Sie dabei an, dass der öffentliche Schlüssel der Sicherungs Behörde verwendet werden soll, um das Schlüsselblob zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="1de0c-109">Export the session key again, this time specifying that the backup authority's public key be used to encrypt the key BLOB.</span></span> <span data-ttu-id="1de0c-110">Senden Sie dieses Schlüsselblob zusammen mit der Beschreibung, der Seriennummer usw. des Schlüssels an die Sicherungs Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="1de0c-110">Send this key BLOB to the backup authority, along with the key's description, serial number, and so on.</span></span>

<span data-ttu-id="1de0c-111">Wenn ein [*Schlüsselpaar*](../secgloss/k-gly.md) verloren geht, können die Schlüssel von der [*Sicherungs*](../secgloss/b-gly.md) Zertifizierungsstelle abgerufen werden, wenn die Identität des Besitzers der Schlüssel festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1de0c-111">If a [*key pair*](../secgloss/k-gly.md) is lost, the keys can be retrieved from the [*backup authority*](../secgloss/b-gly.md) if the identity of the keys' owner can be established.</span></span> <span data-ttu-id="1de0c-112">Die Vorgehensweise zum Einrichten der Identität wird durch die Richtlinie der jeweiligen Sicherungs Stelle bestimmt und umfasst keine kryptoapi.</span><span class="sxs-lookup"><span data-stu-id="1de0c-112">The procedure for establishing identity is determined by the policy of the particular backup authority and does not involve CryptoAPI.</span></span>

<span data-ttu-id="1de0c-113">Den Code, der zum Erstellen eines Sitzungsschlüssels und Exportieren des Schlüssels in ein [*einfaches Schlüsselblob*](../secgloss/s-gly.md) erforderlich ist, das in eine Datenträger Datei geschrieben werden kann, finden Sie unter [Beispiel C-Programm: Exportieren eines Sitzungsschlüssels](example-c-program-exporting-a-session-key.md).</span><span class="sxs-lookup"><span data-stu-id="1de0c-113">For the code needed to create a session key and export that key to a [*simple key BLOB*](../secgloss/s-gly.md) that can be written to a disk file, see [Example C Program: Exporting a Session Key](example-c-program-exporting-a-session-key.md).</span></span>

 

 
