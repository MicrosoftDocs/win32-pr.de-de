---
description: TAPI modelliert eine Schaltfläche für Smartphones und Lampen als Schaltflächen-Lamp-Paare.
ms.assetid: e4c50bd6-a256-407f-af3b-b24383a30ea0
title: Telefon Schaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3e65c34096c0cf043b85d80c9c726c6bef982d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755112"
---
# <a name="phone-buttons"></a><span data-ttu-id="41360-103">Telefon Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="41360-103">Phone Buttons</span></span>

<span data-ttu-id="41360-104">TAPI modelliert die Schaltflächen und Lampen eines Telefons als Schaltflächen-Lamp-Paare.</span><span class="sxs-lookup"><span data-stu-id="41360-104">TAPI models a phone's buttons and lamps as button-lamp pairs.</span></span> <span data-ttu-id="41360-105">Eine Schaltfläche, auf der keine Lamp daneben steht, oder eine Lamp ohne Schaltfläche wird mithilfe eines "Dummy"-Indikators für die fehlende Lamp oder Schaltfläche angegeben.</span><span class="sxs-lookup"><span data-stu-id="41360-105">A button with no lamp next to it or a lamp with no button is specified using a "dummy" indicator for the missing lamp or button.</span></span> <span data-ttu-id="41360-106">Eine Schaltfläche mit mehreren Lampen wird mithilfe mehrerer Schaltflächen-Lamp-Paare modelliert.</span><span class="sxs-lookup"><span data-stu-id="41360-106">A button with multiple lamps is modeled by using multiple button-lamp pairs.</span></span>

<span data-ttu-id="41360-107">Die einer Telefon Schaltfläche zugeordneten Informationen können festgelegt und abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="41360-107">Information associated with a phone button can be set and retrieved.</span></span> <span data-ttu-id="41360-108">Wenn eine Schaltfläche gedrückt wird, wird eine [**Telefon- \_ Schalt**](phone-button.md) Flächen Meldung an die Anwendungsfunktion gesendet.</span><span class="sxs-lookup"><span data-stu-id="41360-108">When a button is pressed, a [**PHONE\_BUTTON**](phone-button.md) message is sent to the application function.</span></span> <span data-ttu-id="41360-109">Bei den Parametern dieser Nachricht handelt es sich um ein Handle für das Telefongerät und den Schaltflächen-Lamp-Bezeichner der Schaltfläche, die gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="41360-109">The parameters of this message are a handle to the phone device and the button-lamp identifier of the button that was pressed.</span></span> <span data-ttu-id="41360-110">Die Tastatur-Schaltflächen "0" bis "9", " \* " und " \# " werden den fixierten Schaltflächen-Lamp-IDs 0 bis 11 zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="41360-110">The keypad buttons '0' through '9', '\*', and '\#' are assigned the fixed button-lamp identifiers 0 through 11.</span></span>

<span data-ttu-id="41360-111">Die den Schaltflächen zugeordneten Funktionen sind " [**phonesetbuttoninfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo)", mit dem die mit einer Schaltfläche auf einem Telefongerät verknüpften Informationen festgelegt werden, und [**phonegetbuttoninfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo), das Informationen zurückgibt, die einer Schaltfläche auf einem Telefongerät zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="41360-111">The functions associated with buttons are [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo), which sets the information associated with a button on a phone device, and [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo), which returns information associated with a button on a phone device.</span></span> <span data-ttu-id="41360-112">Die \_ Meldung Telefon Schaltfläche wird an eine Anwendung gesendet, wenn auf dem Telefon eine Schaltfläche gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="41360-112">The PHONE\_BUTTON message is sent to an application when a button on the phone is pressed.</span></span>

<span data-ttu-id="41360-113">Die einer Schaltfläche zugeordneten Informationen enthalten keinerlei semantische Bedeutung, die von TAPI betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="41360-113">The information associated with a button does not carry any semantic meaning as far as TAPI is concerned.</span></span> <span data-ttu-id="41360-114">Dies ist nützlich für gerätespezifische Anwendungen, die die Bedeutung dieser Informationen für ein bestimmtes Telefongerät oder für die Anzeige für den Benutzer verstehen, z. b. die Online Hilfe.</span><span class="sxs-lookup"><span data-stu-id="41360-114">It is useful for device-specific applications that understand the meaning of this information for a given phone device, or for display to the user, such as online help.</span></span>

 

 



