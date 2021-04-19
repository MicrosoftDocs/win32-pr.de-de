---
description: Einige Telefon Sätze unterstützen das Konzept des Herunterladens von Daten aus dem oder Hochladen von Daten auf das Telefongerät, sodass das Telefon auf verschiedene Weise programmiert werden kann.
ms.assetid: 5734107d-8104-4d8a-b3f7-3cc2a48f71ca
title: Datenbereiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81376549c63b4fcea92f705246cd58161faeac94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348602"
---
# <a name="data-areas"></a><span data-ttu-id="7612f-103">Datenbereiche</span><span class="sxs-lookup"><span data-stu-id="7612f-103">Data Areas</span></span>

<span data-ttu-id="7612f-104">Einige Telefon Sätze unterstützen das Konzept des Herunterladens von Daten aus dem oder Hochladen von Daten auf das Telefongerät, sodass das Telefon auf verschiedene Weise programmiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7612f-104">Some phone sets support the notion of downloading data from or uploading data to the phone device, which allows the phone set to be programmed in a variety of ways.</span></span> <span data-ttu-id="7612f-105">TAPI modelliert diese Telefon Sätze als einen oder mehrere Download-und Uploadbereiche.</span><span class="sxs-lookup"><span data-stu-id="7612f-105">TAPI models these phone sets as having one or more download or upload areas.</span></span> <span data-ttu-id="7612f-106">Jeder Bereich wird durch eine Zahl zwischen 0 (null) und der Anzahl der auf dem Telefon verfügbaren Datenbereiche (minus 1) identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7612f-106">Each area is identified by a number that ranges from zero to the number of data areas available on the phone minus one.</span></span> <span data-ttu-id="7612f-107">Die Größen der einzelnen Bereiche können variieren.</span><span class="sxs-lookup"><span data-stu-id="7612f-107">Sizes of each area can vary.</span></span> <span data-ttu-id="7612f-108">Das Format der Daten selbst ist gerätespezifisch.</span><span class="sxs-lookup"><span data-stu-id="7612f-108">The format of the data itself is device-specific.</span></span>

<span data-ttu-id="7612f-109">Die TAPI [**phonesetdata**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) -Funktion lädt einen Datenpuffer in einen bestimmten Datenbereich auf dem Telefongerät herunter, und die [**phonegetdata**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) -Funktion lädt den Inhalt eines bestimmten Datenbereichs auf dem Telefongerät in einen Puffer hoch.</span><span class="sxs-lookup"><span data-stu-id="7612f-109">The TAPI [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) function downloads a buffer of data to a given data area in the phone device, and the [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) function uploads the contents of a given data area in the phone device to a buffer.</span></span>

<span data-ttu-id="7612f-110">Wenn ein Datenbereich eines Telefon Geräts geändert wird, wird eine [**Telefon \_ Zustands**](phone-state.md) Meldung an die Anwendung gesendet, um die Anwendung über die Statusänderung zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="7612f-110">When a data area of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application to notify the application about the state change.</span></span> <span data-ttu-id="7612f-111">Die Parameter für diese Nachricht geben Aufschluss über die Änderung.</span><span class="sxs-lookup"><span data-stu-id="7612f-111">Parameters to this message provide an indication of the change.</span></span>

 

 



