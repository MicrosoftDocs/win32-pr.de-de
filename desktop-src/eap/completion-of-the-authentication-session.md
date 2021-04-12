---
title: Abschluss der Authentifizierungs Sitzung
description: Nachdem die Authentifizierungs Sitzung abgeschlossen ist, ruft der Authentifizierungsdienst die RasEapEnd-Funktion auf, damit das Authentifizierungsprotokoll seine Arbeits Puffer Freigabe aufhebt.
ms.assetid: 466795ac-fee5-4b82-adc7-af14b6ef3fc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27899ef348630e412b3d52d066f59ea9b5255244
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390207"
---
# <a name="completion-of-the-authentication-session"></a><span data-ttu-id="f3089-103">Abschluss der Authentifizierungs Sitzung</span><span class="sxs-lookup"><span data-stu-id="f3089-103">Completion of the Authentication Session</span></span>

<span data-ttu-id="f3089-104">Nachdem die Authentifizierungs Sitzung abgeschlossen ist, ruft der Authentifizierungsdienst die [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) -Funktion auf, damit das Authentifizierungsprotokoll seine Arbeits Puffer Freigabe aufhebt.</span><span class="sxs-lookup"><span data-stu-id="f3089-104">After the authentication session is completed, the authentication service calls the [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) function to allow the authentication protocol to deallocate its work buffer.</span></span> <span data-ttu-id="f3089-105">Diese Aktion erfolgt unabhängig davon, ob die Authentifizierung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="f3089-105">This action is taken regardless of whether authentication was successful.</span></span> <span data-ttu-id="f3089-106">Durch Aufrufen der **RasEapEnd** -Funktion wird sichergestellt, dass keine weiteren Aufrufe an das Authentifizierungsprotokoll mithilfe dieses bestimmten Benutzers oder Kontexts durchgeführt werden, ohne zuerst [**raseapbegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="f3089-106">Calling the **RasEapEnd** function guarantees that no further calls are made to the authentication protocol using that particular user or context without first calling [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)).</span></span>

 

 