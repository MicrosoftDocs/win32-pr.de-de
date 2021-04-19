---
description: 'Vor dem Einfügen von Daten in die Registrierung sollte eine Anwendung die Daten in zwei Kategorien unterteilen: Computer spezifische Daten und benutzerspezifische Daten.'
ms.assetid: 470d00c1-5975-4a58-9a78-fbed7326a60c
title: Datenkategorien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009a3c89d23f713bb2ed08a7f7c53790e08055db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357117"
---
# <a name="categories-of-data"></a><span data-ttu-id="7533c-103">Datenkategorien</span><span class="sxs-lookup"><span data-stu-id="7533c-103">Categories of Data</span></span>

<span data-ttu-id="7533c-104">Vor dem Einfügen von Daten in die Registrierung sollte eine Anwendung die Daten in zwei Kategorien unterteilen: Computer spezifische Daten und benutzerspezifische Daten.</span><span class="sxs-lookup"><span data-stu-id="7533c-104">Before putting data into the registry, an application should divide the data into two categories: computer-specific data and user-specific data.</span></span> <span data-ttu-id="7533c-105">Durch diese Unterscheidung kann eine Anwendung mehrere Benutzer unterstützen und dennoch benutzerspezifische Daten über ein Netzwerk suchen und diese Daten an verschiedenen Speicherorten verwenden, sodass standortunabhängige Benutzerprofil Daten möglich sind.</span><span class="sxs-lookup"><span data-stu-id="7533c-105">By making this distinction, an application can support multiple users, and yet locate user-specific data over a network and use that data in different locations, allowing location-independent user profile data.</span></span> <span data-ttu-id="7533c-106">(Ein Benutzerprofil ist ein Satz von Konfigurationsdaten, die für jeden Benutzer gespeichert werden.)</span><span class="sxs-lookup"><span data-stu-id="7533c-106">(A user profile is a set of configuration data saved for every user.)</span></span>

<span data-ttu-id="7533c-107">Wenn die Anwendung installiert ist, sollten Sie die computerspezifischen Daten unter dem Schlüssel **HKEY \_ local \_ Machine** aufzeichnen.</span><span class="sxs-lookup"><span data-stu-id="7533c-107">When the application is installed, it should record the computer-specific data under the **HKEY\_LOCAL\_MACHINE** key.</span></span> <span data-ttu-id="7533c-108">Insbesondere sollten Schlüssel für den Firmennamen, den Produktnamen und die Versionsnummer erstellt werden, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="7533c-108">In particular, it should create keys for the company name, product name, and version number, as shown in the following example:</span></span>

<span data-ttu-id="7533c-109">**HKEY \_ \_ \\ Software \\ für den lokalen Computer**_MyCompany \\ MyProduct \\ 1,0_</span><span class="sxs-lookup"><span data-stu-id="7533c-109">**HKEY\_LOCAL\_MACHINE\\Software\\**_MyCompany\\MyProduct\\1.0_</span></span>

<span data-ttu-id="7533c-110">Wenn die Anwendung com unterstützt, sollte diese Daten unter **HKEY- \_ \_ \\ Software \\ Klassen für lokale Computer** aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="7533c-110">If the application supports COM, it should record that data under **HKEY\_LOCAL\_MACHINE\\Software\\Classes**.</span></span>

<span data-ttu-id="7533c-111">Eine Anwendung sollte benutzerspezifische Daten mit dem **aktuellen HKEY- \_ \_ Benutzer** Schlüssel aufzeichnen, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="7533c-111">An application should record user-specific data under the **HKEY\_CURRENT\_USER** key, as shown in the following example:</span></span>

<span data-ttu-id="7533c-112">**HKEY \_ Aktuelle \_ Benutzer \\ Software \\**_MyCompany \\ MyProduct \\ 1,0_</span><span class="sxs-lookup"><span data-stu-id="7533c-112">**HKEY\_CURRENT\_USER\\Software\\**_MyCompany\\MyProduct\\1.0_</span></span>

 

 



