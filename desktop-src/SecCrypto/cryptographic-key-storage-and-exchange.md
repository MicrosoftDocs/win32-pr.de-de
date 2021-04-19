---
description: Es gibt Situationen, in denen Schlüssel aus der sicheren Umgebung des Kryptografiedienstanbieters (kryptografischen Service Provider, CSP) in den Datenbereich einer Anwendung exportiert werden müssen. Schlüssel, die exportiert wurden, werden in verschlüsselten Schlüsselblob-Strukturen gespeichert.
ms.assetid: 859b1bfe-6182-4728-a721-1f34cc98f66f
title: Speicherung von Kryptografieschlüsseln und Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7e789a736f0fcd5208bc16d73b43c6a9232e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346091"
---
# <a name="cryptographic-key-storage-and-exchange"></a><span data-ttu-id="95852-104">Speicherung von Kryptografieschlüsseln und Exchange</span><span class="sxs-lookup"><span data-stu-id="95852-104">Cryptographic Key Storage and Exchange</span></span>

<span data-ttu-id="95852-105">Es gibt Situationen, in denen Schlüssel aus der sicheren Umgebung des [*Kryptografiedienstanbieters (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) in den Datenbereich einer Anwendung exportiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="95852-105">There are situations where keys must be exported from the secure environment of the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) into an application's data space.</span></span> <span data-ttu-id="95852-106">Schlüssel, die exportiert wurden, werden in verschlüsselten [*Schlüsselblob*](../secgloss/k-gly.md) -Strukturen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="95852-106">Keys that have been exported are stored in encrypted [*key BLOB*](../secgloss/k-gly.md) structures.</span></span>

<span data-ttu-id="95852-107">Es gibt zwei Situationen, in denen es erforderlich ist, Schlüssel zu exportieren:</span><span class="sxs-lookup"><span data-stu-id="95852-107">There are two specific situations where it is necessary to export keys:</span></span>

-   <span data-ttu-id="95852-108">Zum Speichern eines [*Sitzungsschlüssels*](../secgloss/s-gly.md) für die spätere Verwendung durch eine Anwendung, z. b. eine Anwendung, die nur eine Datenbankdatei verschlüsselt hat, die zu einem späteren Zeitpunkt entschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="95852-108">To save a [*session key*](../secgloss/s-gly.md) for later use by an application, if, for example, an application has just encrypted a database file to be decrypted at a later time.</span></span> <span data-ttu-id="95852-109">Die Anwendung ist dafür verantwortlich, den Verschlüsselungsschlüssel zu speichern.</span><span class="sxs-lookup"><span data-stu-id="95852-109">The application is responsible for storing the encryption key.</span></span> <span data-ttu-id="95852-110">Dies ist erforderlich, da CSPs keine [*symmetrischen Schlüssel*](../secgloss/s-gly.md) von der Sitzung bis zur Sitzung erhalten.</span><span class="sxs-lookup"><span data-stu-id="95852-110">This is necessary because CSPs do not preserve [*symmetric keys*](../secgloss/s-gly.md) from session to session.</span></span>
-   <span data-ttu-id="95852-111">, Um einen Schlüssel an eine andere Person zu senden.</span><span class="sxs-lookup"><span data-stu-id="95852-111">To send a key to someone else.</span></span> <span data-ttu-id="95852-112">Dies wäre einfacher, wenn die entsprechenden CSPs direkt kommunizieren könnten, dies jedoch nicht möglich ist.</span><span class="sxs-lookup"><span data-stu-id="95852-112">This would be easier if the respective CSPs could communicate directly, but they cannot.</span></span> <span data-ttu-id="95852-113">Da CSPs nicht kommunizieren können, muss der Schlüssel von einem CSP exportiert, an die Zielanwendung übertragen und dann in den Ziel-CSP importiert werden.</span><span class="sxs-lookup"><span data-stu-id="95852-113">Because CSPs cannot communicate, the key has to be exported from one CSP, transmitted to the destination application, and then imported into the destination CSP.</span></span> <span data-ttu-id="95852-114">Dieser Prozess kann komplizierter werden, wenn der Kommunikations Pfad nicht vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="95852-114">This process can become more complicated if the communication path is not trusted.</span></span>

<span data-ttu-id="95852-115">In beiden Fällen muss eine Anwendung einen Sitzungsschlüssel außerhalb des CSP für einen bestimmten Zeitraum speichern.</span><span class="sxs-lookup"><span data-stu-id="95852-115">In either case, an application must store a session key outside the CSP for a period of time.</span></span> <span data-ttu-id="95852-116">Weitere Informationen finden Sie unter [Vorgehensweise zum Speichern eines Sitzungsschlüssels](procedure-for-storing-a-session-key.md).</span><span class="sxs-lookup"><span data-stu-id="95852-116">For more information, see [Procedure for Storing a Session Key](procedure-for-storing-a-session-key.md).</span></span>

 

 
