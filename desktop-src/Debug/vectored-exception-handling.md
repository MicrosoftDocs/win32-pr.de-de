---
description: Vektoren von Ausnahme Handlern sind eine Erweiterung der strukturierten Ausnahmebehandlung.
ms.assetid: e4cf8a88-1bdf-4666-8653-fe2e86c4d8ef
title: Behandlung von Vektoren Ausnahmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 011310b46ce8912e03b6481e9b12b986174a3ef0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861127"
---
# <a name="vectored-exception-handling"></a>Behandlung von Vektoren Ausnahmen

Vektoren von Ausnahme Handlern sind eine Erweiterung der strukturierten Ausnahmebehandlung. Eine Anwendung kann eine Funktion registrieren, um alle Ausnahmen für die Anwendung zu überwachen oder zu behandeln. Vektorhandler sind nicht Frame basiert. Daher können Sie einen Handler hinzufügen, der unabhängig davon, wo Sie sich in einem Aufruf Rahmen befinden, aufgerufen wird. Vektorhandler werden in der Reihenfolge aufgerufen, in der Sie hinzugefügt wurden, nachdem der Debugger eine erste Benachrichtigungs Benachrichtigung erhalten hat, aber bevor das System mit dem Entwickeln des Stapels beginnt.

Verwenden Sie die [**addvectoredcontinuehandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler) -Funktion, um einen Vektoren Continue-Handler hinzuzufügen. Verwenden Sie zum Entfernen dieses Handlers die [**removevectoredcontinuehandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler) -Funktion.

Verwenden Sie zum Hinzufügen eines Vektoren Ausnahme Handlers die [**addvectoredexceptionhandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler) -Funktion. Verwenden Sie zum Entfernen dieses Handlers die [**removevectoredexceptionhandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler) -Funktion.

 

 
