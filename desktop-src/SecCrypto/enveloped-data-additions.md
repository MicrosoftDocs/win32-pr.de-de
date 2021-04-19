---
description: Listet die Änderungen an den Funktionen für die einumhüllenden Daten auf.
ms.assetid: b025a9c6-d6a3-40b2-9b7f-1e6caa706b59
title: Hinzugefügte Daten Ergänzungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360cc7cb6a65853ae6c23bb995df94566d0adc09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348327"
---
# <a name="enveloped-data-additions"></a><span data-ttu-id="4f6e2-103">Hinzugefügte Daten Ergänzungen</span><span class="sxs-lookup"><span data-stu-id="4f6e2-103">Enveloped Data Additions</span></span>

<span data-ttu-id="4f6e2-104">Die folgenden Änderungen wurden an den Funktionen für eingeschlossene Daten vorgenommen:</span><span class="sxs-lookup"><span data-stu-id="4f6e2-104">The following changes have been made to enveloped data capabilities:</span></span>

-   <span data-ttu-id="4f6e2-105">Die Identifizierung des Empfängers kann nicht nur durch Aussteller und Seriennummer (PKCS \# 7 1,5), sondern auch durch einen Schlüssel Bezeichner erfolgen.</span><span class="sxs-lookup"><span data-stu-id="4f6e2-105">Recipient identification can be done not only by Issuer and Serial Number (PKCS \#7 1.5), but also by Key Identifier.</span></span>
-   <span data-ttu-id="4f6e2-106">Es werden drei Empfänger Schlüsselaustausch Optionen bereitgestellt:</span><span class="sxs-lookup"><span data-stu-id="4f6e2-106">Three recipient key exchange choices are provided:</span></span>
    -   <span data-ttu-id="4f6e2-107">Schlüssel Transport mit RSA-Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="4f6e2-107">Key Transport using RSA keys.</span></span>
    -   <span data-ttu-id="4f6e2-108">Schlüssel Vereinbarung mit Ephemeral-Static Diffie-Hellman algorithmusschlüsseln, die mit 3DES oder RC2 umschließen, oder Ephemeral-Static elliptische Kurve Diffie-Hellman algorithmuschlüsselzeichen, die mit AES umschließt sind</span><span class="sxs-lookup"><span data-stu-id="4f6e2-108">Key Agreement using either Ephemeral-Static Diffie-Hellman algorithm keys wrapped with 3DES or RC2, or Ephemeral-Static Elliptic Curve Diffie-Hellman algorithm keys wrapped with AES.</span></span>
    -   <span data-ttu-id="4f6e2-109">Der Schlüssel Verschlüsselungsschlüssel oder die Schlüssel Übertragung für die e-Mail-Liste, bei dem der Schlüssel zum Verschlüsseln des Inhalts Verschlüsselungsschlüssels bereits an die Empfänger verteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f6e2-109">Key Encryption Key or Mail List key transfer where the key used to encrypt the content encryption key has already been distributed to the recipients.</span></span> <span data-ttu-id="4f6e2-110">RC2, 3DES und AES sind als Schlüssel Wrapping Algorithmen zulässig.</span><span class="sxs-lookup"><span data-stu-id="4f6e2-110">RC2, 3DES and AES are allowed as key-wrapping algorithms.</span></span>
-   <span data-ttu-id="4f6e2-111">Ungeschützte Attribute können in die Nachricht eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="4f6e2-111">Unprotected attributes can be included in the message.</span></span>
-   <span data-ttu-id="4f6e2-112">Ein **originatorinfo** -Feld, das Informationen über den Absender enthält, die Zertifikate und CRLs enthalten können, wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4f6e2-112">An **OriginatorInfo** field that contains information about the originator has been added that can contain certificates and CRLs.</span></span>
-   <span data-ttu-id="4f6e2-113">Auf der Grundlage von ECC-Algorithmen (Elliptic Curve Cryptography) und AES ist Windows Vista oder höher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4f6e2-113">Elliptic Curve Cryptography (ECC) based algorithms and AES require Windows Vista or later.</span></span>

 

 



