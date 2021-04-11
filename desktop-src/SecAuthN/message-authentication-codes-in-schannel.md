---
description: Ein Nachrichtenauthentifizierungscode (Mac) wird verwendet, um Manipulationen und Fälschung von Nachrichten zu erkennen.
ms.assetid: 44f50407-8f55-49c4-9e42-2f1666c9da7c
title: Nachrichten Authentifizierungs Codes in Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93939c0c4b4550ad0c24f8e6ef0e0b8bf9f1b07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217324"
---
# <a name="message-authentication-codes-in-schannel"></a><span data-ttu-id="df55a-103">Nachrichten Authentifizierungs Codes in Schannel</span><span class="sxs-lookup"><span data-stu-id="df55a-103">Message Authentication Codes in Schannel</span></span>

<span data-ttu-id="df55a-104">Ein [*Nachrichtenauthentifizierungscode*](../secgloss/m-gly.md) (Mac) wird verwendet, um Manipulationen und Fälschung von Nachrichten zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="df55a-104">A [*Message Authentication Code*](../secgloss/m-gly.md) (MAC) is used to detect message tampering and forgery.</span></span> <span data-ttu-id="df55a-105">Der Absender einer Nachricht erstellt einen Mac durch Verschlüsseln eines unidirektionalen [*Hashs*](../secgloss/h-gly.md) des Nachrichten Texts mithilfe eines [*Sitzungsschlüssels*](../secgloss/s-gly.md) , der vom Absender und Empfänger gemeinsam genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="df55a-105">The sender of a message creates a MAC by encrypting a one-way [*hash*](../secgloss/h-gly.md) of the message body using a [*session key*](../secgloss/s-gly.md) shared by sender and recipient.</span></span> <span data-ttu-id="df55a-106">Der Mac wird an die Nachricht angehängt, die an den Empfänger gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="df55a-106">The MAC is appended to the message that is sent to the recipient.</span></span> <span data-ttu-id="df55a-107">Der Empfänger der Nachricht generiert den Mac mithilfe des freigegebenen Sitzungsschlüssels und des Nachrichten Texts erneut und vergleicht den generierten Mac mit dem Mac, der vom Absender empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="df55a-107">The message recipient generates the MAC again, using the shared session key and message body, and compares the generated MAC to the MAC received from the sender.</span></span> <span data-ttu-id="df55a-108">Wenn beide identisch sind, muss der Absender über den gemeinsamen Sitzungsschlüssel verfügen, und die Nachricht wurde während der Übertragung nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="df55a-108">If the two are identical, then the sender must have the shared session key, and the message has not been altered in transit.</span></span>

<span data-ttu-id="df55a-109">In Schannel-Protokollen wird der Algorithmus, der verwendet wird, um den Mac zu generieren, durch die Verschlüsselungs [Sammlung](cipher-suites-in-schannel.md) bestimmt, die vom Absender und Empfänger verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="df55a-109">In Schannel protocols, the algorithm used to generate the MAC is determined by the [cipher suite](cipher-suites-in-schannel.md) in use by the sender and recipient.</span></span>

 

 
