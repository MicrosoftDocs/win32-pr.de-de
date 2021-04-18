---
description: Das verschlüsselte Dateisystem (EFS) bietet kryptografischen Schutz einzelner Dateien auf NTFS-Dateisystemvolumes mithilfe eines Public-Key-Systems.
ms.assetid: 5f20109f-727d-44a9-90a1-0adc19b00d28
title: Dateiverschlüsselung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55c05d8d746e597fe180feffe25f7f553819e822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352533"
---
# <a name="file-encryption"></a><span data-ttu-id="5c090-103">Dateiverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="5c090-103">File Encryption</span></span>

<span data-ttu-id="5c090-104">Das verschlüsselte Datei System (EFS) bietet eine zusätzliche Sicherheitsebene für Dateien und Verzeichnisse.</span><span class="sxs-lookup"><span data-stu-id="5c090-104">The Encrypted File System, or EFS, provides an additional level of security for files and directories.</span></span> <span data-ttu-id="5c090-105">Es bietet kryptografischen Schutz einzelner Dateien auf NTFS-Dateisystem Volumes mithilfe eines Public-Key-Systems.</span><span class="sxs-lookup"><span data-stu-id="5c090-105">It provides cryptographic protection of individual files on NTFS file system volumes using a public-key system.</span></span>

<span data-ttu-id="5c090-106">Normalerweise ist die Zugriffs Steuerung auf Datei-und Verzeichnisobjekte, die vom Windows-Sicherheitsmodell bereitgestellt werden, ausreichend, um nicht autorisierten Zugriff auf vertrauliche Informationen zu schützen.</span><span class="sxs-lookup"><span data-stu-id="5c090-106">Typically, the access control to file and directory objects provided by the Windows security model is sufficient to protect unauthorized access to sensitive information.</span></span> <span data-ttu-id="5c090-107">Wenn jedoch ein Laptop mit sensiblen Daten verloren geht oder gestohlen wird, kann der Sicherheitsschutz dieser Daten beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="5c090-107">However, if a laptop that contains sensitive data is lost or stolen, the security protection of that data may be compromised.</span></span> <span data-ttu-id="5c090-108">Durch das Verschlüsseln der Dateien wird die Sicherheit erhöht.</span><span class="sxs-lookup"><span data-stu-id="5c090-108">Encrypting the files increases security.</span></span>

<span data-ttu-id="5c090-109">Um zu ermitteln, ob ein Dateisystem Dateiverschlüsselung für Dateien und Verzeichnisse unterstützt, müssen Sie die [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) -Funktion aufrufen und das **FS- \_ \_ Dateiverschlüsselungs** -Bitflag untersuchen.</span><span class="sxs-lookup"><span data-stu-id="5c090-109">To determine whether a file system supports file encryption for files and directories, call the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examine the **FS\_FILE\_ENCRYPTION** bit flag.</span></span> <span data-ttu-id="5c090-110">Beachten Sie, dass die folgenden Elemente nicht verschlüsselt werden können:</span><span class="sxs-lookup"><span data-stu-id="5c090-110">Note that the following items cannot be encrypted:</span></span>

-   <span data-ttu-id="5c090-111">Komprimierte Dateien</span><span class="sxs-lookup"><span data-stu-id="5c090-111">Compressed files</span></span>
-   <span data-ttu-id="5c090-112">Systemdateien</span><span class="sxs-lookup"><span data-stu-id="5c090-112">System files</span></span>
-   <span data-ttu-id="5c090-113">System Verzeichnisse</span><span class="sxs-lookup"><span data-stu-id="5c090-113">System directories</span></span>
-   <span data-ttu-id="5c090-114">Stamm Verzeichnisse</span><span class="sxs-lookup"><span data-stu-id="5c090-114">Root directories</span></span>
-   <span data-ttu-id="5c090-115">Transaktionen</span><span class="sxs-lookup"><span data-stu-id="5c090-115">Transactions</span></span>

<span data-ttu-id="5c090-116">Sparsesdateien können verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="5c090-116">Sparse files can be encrypted.</span></span>

<span data-ttu-id="5c090-117">TxF unterstützt die meisten Vorgänge für EFS-Dateien (verschlüsselte Datei System) nicht.</span><span class="sxs-lookup"><span data-stu-id="5c090-117">TxF does not support most operations on Encrypted File System (EFS) files.</span></span> <span data-ttu-id="5c090-118">Die einzigen Vorgänge, die TxF unterstützt, sind Lesevorgänge wie z. b. " [**leseverschlüsseltedfileraw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)".</span><span class="sxs-lookup"><span data-stu-id="5c090-118">The only operations TxF supports are read operations, such as [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5c090-119">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="5c090-119">In this section</span></span>



| <span data-ttu-id="5c090-120">Thema</span><span class="sxs-lookup"><span data-stu-id="5c090-120">Topic</span></span>                                                                                               | <span data-ttu-id="5c090-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c090-121">Description</span></span>                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c090-122">Behandeln von verschlüsselten Dateien und Verzeichnissen</span><span class="sxs-lookup"><span data-stu-id="5c090-122">Handling Encrypted Files and Directories</span></span>](handling-encrypted-files-and-directories.md)<br/> | <span data-ttu-id="5c090-123">Eine Datei, die als verschlüsselt gekennzeichnet ist, wird vom NTFS-Dateisystem mithilfe des aktuellen Verschlüsselungs Treibers verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="5c090-123">A file marked encrypted is encrypted by the NTFS file system by using the current encryption driver.</span></span><br/>                                                          |
| [<span data-ttu-id="5c090-124">Verschlüsselte Dateien und Benutzerschlüssel</span><span class="sxs-lookup"><span data-stu-id="5c090-124">Encrypted Files and User Keys</span></span>](encrypted-files-and-user-keys.md)<br/>                       | <span data-ttu-id="5c090-125">Listet die Funktionen auf, die zum Erstellen eines neuen Schlüssels, zum Hinzufügen eines Schlüssels zu einer verschlüsselten Datei, zum Abfragen der Schlüssel für eine verschlüsselte Datei und zum Entfernen von Schlüsseln aus einer verschlüsselten Datei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5c090-125">Lists the functions to use to create a new key, add a key to an encrypted file, query the keys for an encrypted file, and remove keys from an encrypted file.</span></span><br/> |
| [<span data-ttu-id="5c090-126">Sichern und Wiederherstellen verschlüsselter Dateien</span><span class="sxs-lookup"><span data-stu-id="5c090-126">Backup and Restore of Encrypted Files</span></span>](backup-and-restore-of-encrypted-files.md)<br/>       | <span data-ttu-id="5c090-127">Die unformatierten Verschlüsselungsfunktionen ermöglichen die Sicherung verschlüsselter Dateien.</span><span class="sxs-lookup"><span data-stu-id="5c090-127">The raw encryption functions enable backup of encrypted files.</span></span><br/>                                                                                                |



 

<span data-ttu-id="5c090-128">Weitere Informationen zur Verschlüsselung finden Sie unter [Hinzufügen von Benutzern zu einer verschlüsselten Datei](adding-users-to-an-encrypted-file.md).</span><span class="sxs-lookup"><span data-stu-id="5c090-128">For more information about encryption, see [Adding Users to an Encrypted File](adding-users-to-an-encrypted-file.md).</span></span>

<span data-ttu-id="5c090-129">Weitere Informationen zur Kryptografie finden Sie unter [Cryptography](/windows/desktop/SecCrypto/cryptography-portal).</span><span class="sxs-lookup"><span data-stu-id="5c090-129">For more information about cryptography, see [Cryptography](/windows/desktop/SecCrypto/cryptography-portal).</span></span>

 

