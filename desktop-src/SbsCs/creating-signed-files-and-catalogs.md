---
description: Zum Signieren einer Datei und zum Erstellen eines Katalogs müssen Sie zunächst über einen Prozess zum Signieren von Dateien, ein Zertifikat und einen öffentlichen Schlüssel verfügen.
ms.assetid: 61337ea6-2d6b-4080-9128-5b8527512ce6
title: Erstellen signierter Dateien und Kataloge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1327ed2d64c6f7be9f14acc2c846cf8a887119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216344"
---
# <a name="creating-signed-files-and-catalogs"></a><span data-ttu-id="d31fd-103">Erstellen signierter Dateien und Kataloge</span><span class="sxs-lookup"><span data-stu-id="d31fd-103">Creating Signed Files and Catalogs</span></span>

<span data-ttu-id="d31fd-104">Zum Signieren einer Datei und zum Erstellen eines Katalogs müssen Sie zunächst über einen Prozess zum Signieren von Dateien, ein Zertifikat und einen öffentlichen Schlüssel verfügen.</span><span class="sxs-lookup"><span data-stu-id="d31fd-104">To sign a file and create a catalog for it, you must first have a process for signing files, a certificate, and a public key.</span></span>

<span data-ttu-id="d31fd-105">**So signieren Sie eine Datei und erstellen einen Katalog**</span><span class="sxs-lookup"><span data-stu-id="d31fd-105">**To sign a file and a create a catalog**</span></span>

1.  <span data-ttu-id="d31fd-106">Verwenden Sie [Pktextract.exe](pktextract-exe.md) , um das [*öffentliche Schlüssel Token*](p-sbscs-gly.md) aus der Zertifikatsdatei zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="d31fd-106">Use [Pktextract.exe](pktextract-exe.md) to extract the [*public key token*](p-sbscs-gly.md) from the certificate file.</span></span> <span data-ttu-id="d31fd-107">Die Zertifikatsdatei muss sich im selben Verzeichnis wie das-Hilfsprogramm befinden.</span><span class="sxs-lookup"><span data-stu-id="d31fd-107">The certificate file must be present in the same directory as the utility.</span></span>
2.  <span data-ttu-id="d31fd-108">Verwenden Sie den Wert des öffentlichen Schlüssel Tokens, um das **PublicKeyToken** -Attribut des **assemblyIdentity** -Elements in der Manifest-Datei zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d31fd-108">Use the public key token value to update the **publicKeyToken** attribute of the **assemblyIdentity** element in the manifest file.</span></span>
3.  <span data-ttu-id="d31fd-109">Verwenden Sie [MT.exe](mt-exe.md) , um Hashwerte von Dateien zu generieren, die im Assemblymanifest enthalten sind, und um die Katalog Beschreibungsdatei (CDF) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d31fd-109">Use [MT.exe](mt-exe.md) to generate hashes of files contained in the assembly manifest and to create the catalog description file (.cdf).</span></span>
4.  <span data-ttu-id="d31fd-110">Verwenden Sie Makecat.exe mit der generierten CDF-Datei, um den Sicherheits Katalog für die Assembly zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d31fd-110">Use Makecat.exe with the generated .cdf to create the security catalog for the assembly.</span></span> <span data-ttu-id="d31fd-111">Dieses Tool ist in der CryptoAPI enthalten.</span><span class="sxs-lookup"><span data-stu-id="d31fd-111">This tool is included in the CryptoAPI.</span></span>
5.  <span data-ttu-id="d31fd-112">Verwenden Sie das Hilfsprogramm [SignTool](/windows/desktop/SecCrypto/signtool) zum Signieren des Katalogs, der mit dem in Schritt 1 verwendeten Zertifikat generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d31fd-112">Use the [SignTool](/windows/desktop/SecCrypto/signtool) utility to sign the catalog generated with the certificate used in step 1.</span></span> <span data-ttu-id="d31fd-113">Die CDF aus den Schritten 3 und 4 können gelöscht werden, nachdem der Katalog erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d31fd-113">The .cdf from steps 3 and 4 can be deleted once the catalog is created.</span></span>

<span data-ttu-id="d31fd-114">Siehe auch [Beispiel für Assemblysignierung](assembly-signing-example.md).</span><span class="sxs-lookup"><span data-stu-id="d31fd-114">See also, [Assembly Signing Example](assembly-signing-example.md).</span></span>

 

 
