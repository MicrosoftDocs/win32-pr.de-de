---
description: Viele Formen der Authentifizierung basieren auf der Idee, dass eine Entität Ihre Identität nachweisen kann, wenn Sie einen Schlüssel (z. b. ein Kennwort) kennt, den nur Sie kennt.
ms.assetid: e17e4eb7-133e-46a0-8247-00a58b88bf61
title: Schlüsselauthentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deaadfdb61340955209ded22b5302e5436271ccc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216340"
---
# <a name="key-authentication"></a><span data-ttu-id="098cd-103">Schlüsselauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="098cd-103">Key Authentication</span></span>

<span data-ttu-id="098cd-104">Viele Formen der Authentifizierung basieren auf der Idee, dass eine Entität Ihre Identität nachweisen kann, wenn Sie einen Schlüssel (z. b. ein Kennwort) kennt, den nur Sie kennt.</span><span class="sxs-lookup"><span data-stu-id="098cd-104">Many forms of authentication are based on the idea that an entity can prove its identity if it can prove it knows a key, such as a password, that only it can know.</span></span>

<span data-ttu-id="098cd-105">Authentifizierungstechniken, die auf einem geheimen Schlüssel basieren (z. b. ein Kennwort), müssen über eine Möglichkeit verfügen, das Geheimnis von öffentlichem wissen zu bewahren.</span><span class="sxs-lookup"><span data-stu-id="098cd-105">Authentication techniques that rely on a secret, such as a password, need to have a way to keep the secret from becoming public knowledge.</span></span> <span data-ttu-id="098cd-106">Ein Kenn Wort Besitzer kann nicht zu einer Tür gehen und das Kennwort angeben.</span><span class="sxs-lookup"><span data-stu-id="098cd-106">A password owner cannot walk up to a door and give the password.</span></span> <span data-ttu-id="098cd-107">Eine Person neben dem doorkeeper könnte lauschen. oder Sie ist möglicherweise die falsche Tür.</span><span class="sxs-lookup"><span data-stu-id="098cd-107">Someone besides the doorkeeper might be listening; or it might be the wrong door.</span></span> <span data-ttu-id="098cd-108">Um einen geheimen Schlüssel beizubehalten, muss ein Benutzer das Kennwort kennen, ohne das Kennwort offenzulegen.</span><span class="sxs-lookup"><span data-stu-id="098cd-108">In order to keep a secret, there must be a way to prove a user knows the password without revealing the password.</span></span> <span data-ttu-id="098cd-109">Das ist die Idee hinter der Authentifizierung mit geheimem Schlüssel, einer Überprüfungs Methode, die im gesamten [*Kerberos-Protokoll*](../secgloss/k-gly.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="098cd-109">That is the idea behind secret key authentication, a method of verification used throughout the [*Kerberos protocol*](../secgloss/k-gly.md).</span></span>

<span data-ttu-id="098cd-110">Beachten Sie, dass das "Geheimnis" bei der Authentifizierung mit geheimem Schlüssel darin besteht, dass der Authentifizierungsprozess "im geheimen Schlüssel" stattfindet, ohne dass der Inhalt des Schlüssels jemals offen geht.</span><span class="sxs-lookup"><span data-stu-id="098cd-110">Notice that the "secret" in secret key authentication is that the authentication process takes place "in secret;" that is, without ever actually revealing the content of the key.</span></span>

<span data-ttu-id="098cd-111">Damit die Authentifizierung mit geheimem Schlüssel funktioniert, müssen die beiden Parteien an eine Transaktion einen [*kryptografiesitzungsschlüssel*](../secgloss/s-gly.md) gemeinsam verwenden, der auch geheim ist, nur für Sie und für andere bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="098cd-111">For secret key authentication to work, the two parties to a transaction must share a cryptographic [*session key*](../secgloss/s-gly.md) which is also secret, known only to them and to no others.</span></span> <span data-ttu-id="098cd-112">Der Schlüssel ist [*symmetrisch*](../secgloss/s-gly.md). Das heißt, es ist ein einzelner Schlüssel, der sowohl für die Verschlüsselung als auch für die Entschlüsselung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="098cd-112">The key is [*symmetric*](../secgloss/s-gly.md); that is, it is a single key used for both encryption and decryption.</span></span> <span data-ttu-id="098cd-113">Eine Partei im Authentifizierungsprozess weist ihr Wissen über den Schlüssel auf, indem Sie eine Nachricht verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="098cd-113">One party in the authentication process proves its knowledge of the key by encrypting a message.</span></span> <span data-ttu-id="098cd-114">Die andere Partei weist ihr Wissen über den Schlüssel auf, indem Sie die Nachricht entschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="098cd-114">The other party proves its knowledge of the key by decrypting the message.</span></span>

 

 
