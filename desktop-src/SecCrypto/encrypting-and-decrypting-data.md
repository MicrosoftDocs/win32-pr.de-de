---
description: Wenn ein Dokument oder Text durch einen einzelnen Benutzer geschützt werden muss oder wenn das Dokument von einer kleinen Gruppe von Benutzern gemeinsam genutzt werden muss, die alle Zugriff auf das gleiche geheime Kennwort haben, kann eine einfache Verschlüsselung/Entschlüsselung durchgeführt werden.
ms.assetid: 68eefd24-c924-4dd1-8cb3-cc20106f9605
title: Verschlüsseln und Entschlüsseln von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd7123544fb9c8fa59291be2eae2c5bf9a120f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960378"
---
# <a name="encrypting-and-decrypting-data"></a><span data-ttu-id="060f8-103">Verschlüsseln und Entschlüsseln von Daten</span><span class="sxs-lookup"><span data-stu-id="060f8-103">Encrypting and Decrypting Data</span></span>

<span data-ttu-id="060f8-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="060f8-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="060f8-105">Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="060f8-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="060f8-106">Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="060f8-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="060f8-107">Wenn ein Dokument oder Text durch einen einzelnen Benutzer geschützt werden muss oder wenn das Dokument von einer kleinen Gruppe von Benutzern gemeinsam genutzt werden muss, die alle Zugriff auf das gleiche geheime Kennwort haben, kann eine einfache Verschlüsselung/Entschlüsselung durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="060f8-107">When a document or text needs to have privacy protected by a single user or when the document is to be shared among a small group of people who all have access to the same secret password, simple encryption/decryption can be done.</span></span> <span data-ttu-id="060f8-108">CAPICOM unterstützt den PKCS \# 7-Inhaltstyp "verschlüsselteddata" nicht, sondern verwendet eine nicht standardmäßige ASN-Struktur für "verschlüsselteddata".</span><span class="sxs-lookup"><span data-stu-id="060f8-108">CAPICOM does not support the PKCS \#7 EncryptedData content type but uses a non-standard ASN structure for EncryptedData.</span></span> <span data-ttu-id="060f8-109">Daher kann nur CAPICOM ein CAPICOM-Objekt "verschlüsselteddata" entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="060f8-109">Therefore, only CAPICOM can decrypt a CAPICOM EncryptedData object.</span></span>

<span data-ttu-id="060f8-110">In den folgenden Abschnitten werden Beispiele für Verschlüsselungs-und Entschlüsselungs Aufgaben veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="060f8-110">The following sections show examples for encryption and decryption tasks:</span></span>

-   [<span data-ttu-id="060f8-111">Verschlüsseln einer Nachricht in CAPICOM</span><span class="sxs-lookup"><span data-stu-id="060f8-111">Encrypting a Message in CAPICOM</span></span>](encrypting-a-message-in-capicom.md)
-   [<span data-ttu-id="060f8-112">Entschlüsseln einer Nachricht in CAPICOM</span><span class="sxs-lookup"><span data-stu-id="060f8-112">Decrypting a Message in CAPICOM</span></span>](decrypting-a-message-in-capicom.md)

 

 



