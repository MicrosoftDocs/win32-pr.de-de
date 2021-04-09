---
description: Die duplikatandle-Funktion erstellt ein doppeltes handle, das von einem anderen angegebenen Prozess verwendet werden kann.
ms.assetid: b79d2b8f-931e-4cab-9bbe-9ead1b102132
title: Objekt Duplizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f8e0948ce55f5d25d7567346ecdec97f04b24a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042594"
---
# <a name="object-duplication"></a><span data-ttu-id="a8f2c-103">Objekt Duplizierung</span><span class="sxs-lookup"><span data-stu-id="a8f2c-103">Object Duplication</span></span>

<span data-ttu-id="a8f2c-104">Die [**duplikatandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) -Funktion erstellt ein doppeltes handle, das von einem anderen angegebenen Prozess verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a8f2c-104">The [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function creates a duplicate handle that can be used by another specified process.</span></span> <span data-ttu-id="a8f2c-105">Diese Methode der Freigabe von Objekt Handles ist komplexer als die Verwendung benannter Objekte oder Vererbung.</span><span class="sxs-lookup"><span data-stu-id="a8f2c-105">This method of sharing object handles is more complex than using named objects or inheritance.</span></span> <span data-ttu-id="a8f2c-106">Hierfür ist eine Kommunikation zwischen dem Erstellungsprozess und dem Prozess erforderlich, in den das Handle dupliziert wird.</span><span class="sxs-lookup"><span data-stu-id="a8f2c-106">It requires communication between the creating process and the process into which the handle is duplicated.</span></span> <span data-ttu-id="a8f2c-107">Die erforderlichen Informationen (der Handle-Wert und die Prozess-ID) können von jeder prozessübergreifenden Kommunikationsmethode (z. b. Named Pipes oder benannte Shared Memory) kommuniziert werden.</span><span class="sxs-lookup"><span data-stu-id="a8f2c-107">The necessary information (the handle value and process identifier) can be communicated by any of the interprocess communication methods, such as named pipes or named shared memory.</span></span>

 

 
