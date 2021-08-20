---
description: Vektorierte Ausnahmehandler sind eine Erweiterung der strukturierten Ausnahmebehandlung.
ms.assetid: e4cf8a88-1bdf-4666-8653-fe2e86c4d8ef
title: Behandlung von Vektorausnahmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 926b0499e9399aa77e6835e90c6da016da3f2dc8195a4b4872f7f5119d04978a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405581"
---
# <a name="vectored-exception-handling"></a>Behandlung von Vektorausnahmen

Vektorierte Ausnahmehandler sind eine Erweiterung der strukturierten Ausnahmebehandlung. Eine Anwendung kann eine Funktion registrieren, um alle Ausnahmen für die Anwendung zu beobachten oder zu behandeln. Vektorhandler sind nicht frame-basiert. Daher können Sie einen Handler hinzufügen, der aufgerufen wird, unabhängig davon, wo Sie sich in einem Aufrufframe befinden. Vektorhandler werden in der Reihenfolge aufgerufen, in der sie hinzugefügt wurden, nachdem der Debugger eine Benachrichtigung der ersten Chance erhält, aber bevor das System mit der Entladung des Stapels beginnt.

Um einen vektorierten Continue-Handler hinzuzufügen, verwenden Sie die [**AddVectoredContinueHandler-Funktion.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler) Um diesen Handler zu entfernen, verwenden Sie die [**RemoveVectoredContinueHandler-Funktion.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler)

Um einen vektorierten Ausnahmehandler hinzuzufügen, verwenden Sie die [**AddVectoredExceptionHandler-Funktion.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler) Um diesen Handler zu entfernen, verwenden Sie die [**RemoveVectoredExceptionHandler-Funktion.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler)

 

 
