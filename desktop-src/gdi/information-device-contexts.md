---
description: Mithilfe der Information DC werden Standardgeräte Daten abgerufen.
ms.assetid: 8fd05c17-e8c9-4747-9a66-ce7d958edeb9
title: Informationsgeräte Kontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002e9d5ebb6831f9e2251e76049e586ac3e84056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528325"
---
# <a name="information-device-contexts"></a><span data-ttu-id="b293c-103">Informationsgeräte Kontexte</span><span class="sxs-lookup"><span data-stu-id="b293c-103">Information Device Contexts</span></span>

<span data-ttu-id="b293c-104">Mithilfe der Information DC werden Standardgeräte Daten abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b293c-104">The information DC is used to retrieve default device data.</span></span> <span data-ttu-id="b293c-105">Eine Anwendung kann z. b. die Funktion " [**deeic**](/windows/desktop/api/Wingdi/nf-wingdi-createica) " aufrufen, um einen Informations-DC für ein bestimmtes Drucker Modell zu erstellen, und dann die Funktionen " [**getcurrentobject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) " und " [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) " aufrufen, um die Standard Stift-oder Pinsel Attribute abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b293c-105">For example, an application can call the [**CreateIC**](/windows/desktop/api/Wingdi/nf-wingdi-createica) function to create an information DC for a particular model of printer and then call the [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) and [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) functions to retrieve the default pen or brush attributes.</span></span> <span data-ttu-id="b293c-106">Da das Systemgeräte Informationen abrufen kann, ohne die Strukturen zu erstellen, die normalerweise mit den anderen Typen von Geräte Kontexten verknüpft sind, umfasst ein Informations-DC weitaus weniger Aufwand und wird erheblich schneller erstellt als jeder andere Typ.</span><span class="sxs-lookup"><span data-stu-id="b293c-106">Because the system can retrieve device information without creating the structures normally associated with the other types of device contexts, an information DC involves far less overhead and is created significantly faster than any of the other types.</span></span> <span data-ttu-id="b293c-107">Nachdem eine Anwendung das Abrufen von Daten mithilfe eines Informations-DC abgeschlossen hat, muss Sie die [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b293c-107">After an application finishes retrieving data by using an information DC, it must call the [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) function.</span></span>

 

 



