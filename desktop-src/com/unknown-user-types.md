---
title: Unbekannte Benutzer Typen
description: Unbekannte Benutzer Typen
ms.assetid: c2a4bd83-6eaf-4130-8f86-e99f1e18b63d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4843ca2e19508806bba952403a2211a39f5a5ca
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316575"
---
# <a name="unknown-user-types"></a><span data-ttu-id="51b6b-103">Unbekannte Benutzer Typen</span><span class="sxs-lookup"><span data-stu-id="51b6b-103">Unknown User Types</span></span>

<span data-ttu-id="51b6b-104">Sie können die Produktlokalisierung vereinfachen, indem Sie den folgenden Registrierungsschlüssel hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="51b6b-104">You can ease product localization by adding the following registry key:</span></span>

<span data-ttu-id="51b6b-105">**HKEY \_ LOCAL \_ Machines \\ Software \\ Microsoft \\ OLE2** \\ **unknownusertype**  =  *usertype*</span><span class="sxs-lookup"><span data-stu-id="51b6b-105">**HKEY\_LOCAL\_MACHINES\\SOFTWARE\\Microsoft\\OLE2**\\**UnknownUserType** = *usertype*</span></span>

<span data-ttu-id="51b6b-106">Mit diesem Schlüssel können Funktionen eine angegebene Zeichenfolge anstelle des Standardwerts "unknown" zurückgeben, sodass Lokalisierer einen Benutzertyp einer anderen Sprache angeben können.</span><span class="sxs-lookup"><span data-stu-id="51b6b-106">This key allows functions to return a specified string rather than a default value of "Unknown", enabling localizers to specify a user type of a different language.</span></span>

<span data-ttu-id="51b6b-107">Die Implementierung von [**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) des com-Standard Handlers überprüft die Registrierung durch Aufrufen von [**olereggetusertype**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span><span class="sxs-lookup"><span data-stu-id="51b6b-107">The COM default handler's implementation of [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) examines the registry by calling [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span></span> <span data-ttu-id="51b6b-108">Wenn die Klasse des Objekts in der Registrierung nicht gefunden wird, wird der Benutzertyp aus der [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) -Instanz des Objekts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="51b6b-108">If the object's class is not found in the registry, the user type from the object's [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) instance is returned.</span></span> <span data-ttu-id="51b6b-109">Wenn die Klasse in der **IStorage** -Instanz des Objekts nicht gefunden wird, wird die Zeichenfolge "unknown" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="51b6b-109">If the class is not found in the object's **IStorage** instance, the string "Unknown" is returned.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51b6b-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="51b6b-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51b6b-111">Registrieren von com-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="51b6b-111">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 