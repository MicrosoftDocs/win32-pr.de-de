---
title: Fehler-und Ausnahmebehandlung von ACF-Attributen
description: Verwenden Sie die folgenden Attribute für die Fehlerbehandlung.
ms.assetid: fb00df67-4645-4ef0-9216-618d0af1d9d4
keywords:
- ACF-Mittell, Attribute, Fehler-und Ausnahmebehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7187ab887fa1d09b18385b86065775ca0e656f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340268"
---
# <a name="error-and-exception-handling-acf-attributes"></a><span data-ttu-id="9ddfd-104">Fehler-und Ausnahmebehandlung von ACF-Attributen</span><span class="sxs-lookup"><span data-stu-id="9ddfd-104">Error and Exception Handling ACF Attributes</span></span>

<span data-ttu-id="9ddfd-105">Verwenden Sie die folgenden Attribute für die Fehlerbehandlung.</span><span class="sxs-lookup"><span data-stu-id="9ddfd-105">Use the following attributes for error handling.</span></span>



| <span data-ttu-id="9ddfd-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="9ddfd-106">Attribute</span></span>                                                                | <span data-ttu-id="9ddfd-107">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="9ddfd-107">Usage</span></span>                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ddfd-108">[**\_**](comm-status.md)[**\_ Status Fehlerstatus** von "comm"](fault-status.md)</span><span class="sxs-lookup"><span data-stu-id="9ddfd-108">[**comm\_status**](comm-status.md)[**fault\_status**](fault-status.md)</span></span> | <span data-ttu-id="9ddfd-109">Lassen Sie zu, dass die Client Anwendung Ausnahmen ordnungsgemäß behandelt, indem Sie als Parameterwerte Kommunikations-und Server Fehler an den Client zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9ddfd-109">Let your client application handle exceptions gracefully by causing communication and server errors to be returned to the client as parameter values.</span></span> <span data-ttu-id="9ddfd-110">Die Client Anwendung kann dann die RPC-Lauf Zeitfunktion [**dceerrorinqtext**](/windows/desktop/api/rpcdce/nf-rpcdce-dceerrorinqtext) aufzurufen, um eine Fehlermeldung an den Benutzer weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="9ddfd-110">The client application can then call the RPC run-time function [**DceErrorInqText**](/windows/desktop/api/rpcdce/nf-rpcdce-dceerrorinqtext) to relay an error message to the user.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9ddfd-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9ddfd-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ddfd-112">Importieren von Dateien und Typbibliotheken</span><span class="sxs-lookup"><span data-stu-id="9ddfd-112">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> </dl>

 

 