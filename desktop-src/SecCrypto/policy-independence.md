---
description: Zertifikate werden gemäß Richtlinien erteilt, die Kriterien definieren, die Anforderer erfüllen muss, um ein Zertifikat zu erhalten.
ms.assetid: ad79dc0d-6457-4459-80e6-ab340436ecac
title: Unabhängigkeit der Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0d99b5babeced0fb87d9e603038e23a40859b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346538"
---
# <a name="policy-independence"></a><span data-ttu-id="1d692-103">Unabhängigkeit der Richtlinie</span><span class="sxs-lookup"><span data-stu-id="1d692-103">Policy Independence</span></span>

<span data-ttu-id="1d692-104">Zertifikate werden gemäß Richtlinien erteilt, die Kriterien definieren, die Anforderer erfüllen muss, um ein Zertifikat zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1d692-104">Certificates are granted according to policies that define criteria that requesters must meet to receive a certificate.</span></span> <span data-ttu-id="1d692-105">Eine Richtlinie kann beispielsweise sein, dass nur kommerzielle Zertifikate erteilt werden sollen, wenn die Antragsteller ihre Identifikation persönlich darstellen.</span><span class="sxs-lookup"><span data-stu-id="1d692-105">For example, one policy may be to grant commercial certificates only if applicants present their identification in person.</span></span> <span data-ttu-id="1d692-106">Eine andere Richtlinie kann [*Anmelde*](../secgloss/c-gly.md) Informationen basierend auf e-Mail-Anforderungen erteilen</span><span class="sxs-lookup"><span data-stu-id="1d692-106">Another policy may grant [*credentials*](../secgloss/c-gly.md) based on email requests.</span></span> <span data-ttu-id="1d692-107">Eine Agentur, bei der Kreditkarten ausgestellt werden, kann sich für eine Datenbank entscheiden und vor der Ausstellung einer Karte telefonisch Fragen stellen.</span><span class="sxs-lookup"><span data-stu-id="1d692-107">An agency that issues credit cards may choose to consult a database and make phone inquiries before issuing a card.</span></span>

<span data-ttu-id="1d692-108">Richtlinien werden in Richtlinien Modulen implementiert, die in C++, C oder Visual Basic geschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="1d692-108">Policies are implemented in policy modules written in C++, C, or Visual Basic.</span></span> <span data-ttu-id="1d692-109">Zertifikat Dienstfunktionen sind von allen Änderungen in der Richtlinie isoliert, die eine Agentur implementieren kann.</span><span class="sxs-lookup"><span data-stu-id="1d692-109">Certificate Services functions are isolated from any changes in policy that an agency might implement.</span></span> <span data-ttu-id="1d692-110">Änderungen an der Richtlinie können im Code des Server Richtlinien Moduls vollständig implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="1d692-110">Changes in policy can be fully implemented in the server policy module code.</span></span> <span data-ttu-id="1d692-111">Eine Unternehmens [*Zertifizierungsstelle (Certification Authority*](../secgloss/c-gly.md) , ca) sollte nur das von Microsoft bereitgestellte Enterprise Policy-Modul verwenden.</span><span class="sxs-lookup"><span data-stu-id="1d692-111">An enterprise [*certification authority*](../secgloss/c-gly.md) (CA) should use only the Microsoft-provided enterprise policy module.</span></span>

 

 
