---
description: Mit Hash-und digitalen Signatur Funktionen kann ein Benutzerdaten digital signieren, sodass jeder andere Benutzer überprüfen kann, ob die Daten seit der Signierung geändert wurden. Die Identität des Benutzers, der die Daten signiert hat, kann auch überprüft werden.
ms.assetid: dbe70506-f0d9-4239-a3af-8494fd6d4149
title: Hashes und digitale Signaturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dc2894cbf53834551afef375fb5056df89675a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363648"
---
# <a name="hashes-and-digital-signatures"></a><span data-ttu-id="ee316-104">Hashes und digitale Signaturen</span><span class="sxs-lookup"><span data-stu-id="ee316-104">Hashes and Digital Signatures</span></span>

<span data-ttu-id="ee316-105">Mit [Hash-und digitalen Signatur Funktionen](cryptography-functions.md)kann ein Benutzerdaten digital signieren, sodass jeder andere Benutzer überprüfen kann, ob die Daten seit der Signierung geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="ee316-105">With [Hash and Digital Signature Functions](cryptography-functions.md), a user can digitally sign data so that any other user can verify that the data has not been changed since it was signed.</span></span> <span data-ttu-id="ee316-106">Die Identität des Benutzers, der die Daten signiert hat, kann auch überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="ee316-106">The identity of the user who signed the data can also be verified.</span></span>

<span data-ttu-id="ee316-107">Eine [*digitale Signatur*](../secgloss/d-gly.md) besteht aus einer kleinen Menge an Binärdaten, in der Regel weniger als 256 Bytes.</span><span class="sxs-lookup"><span data-stu-id="ee316-107">A [*digital signature*](../secgloss/d-gly.md) consists of a small amount of binary data, typically less than 256 bytes.</span></span> <span data-ttu-id="ee316-108">Diese Signatur kann mit der signierten Nachricht gebündelt oder separat gespeichert werden, je nachdem, wie eine bestimmte Anwendung implementiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ee316-108">This signature can be bundled with the signed message or stored separately, depending on how a particular application has been implemented.</span></span>

<span data-ttu-id="ee316-109">Der starke Kryptografieanbieter von Microsoft erstellt digitale Signaturen, die den RSA-PKCS ( [*Public Key Cryptography Standards*](../secgloss/p-gly.md) ) \# 1 entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ee316-109">The Microsoft Strong Cryptographic Provider creates digital signatures that conform to the RSA [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \#1.</span></span>

 

 
