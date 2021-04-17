---
title: Speicher Modi
description: Der asynchrone Speicher unterstützt zwei Speicher Modi, die blockieren und nicht blockieren, was ein Client (entweder ein Browser oder das Objekt selbst) angeben kann, indem er bindf \_ asyncstorage aus dem Aufruf von ibindstatuencallback getbindinfo des Monikers zurückgibt.
ms.assetid: df8f9e2c-40d2-4997-b5f9-bdbc524437cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827e893f5077a64485251111837e6b56657756f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390734"
---
# <a name="storage-modes"></a>Speicher Modi

Der asynchrone Speicher unterstützt zwei Speicher Modi: Blockierung und nicht Blockierung, bei denen ein Client (entweder ein Browser oder das Objekt selbst) angeben kann, indem er bindf \_ asyncstorage aus dem Aufruf von [**ibindstatuencallback:: getbindinfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85))des Monikers zurückgibt. Wenn ein Client bindf \_ asyncstorage angibt, empfängt er einen Zeiger auf einen nicht blockierenden asynchronen Speicher. Andernfalls erhält Sie einen Zeiger auf einen blockierenden asynchronen Speicher. Auch wenn der Client keinen asynchronen Bindungs Vorgang anfordert (durch das nicht registrieren von [**ibindstatus-Callback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) beim Bindungs Kontext), gibt der Moniker weiterhin einen blockierenden asynchronen Speicher zurück, der das progressive Laden für ältere Anwendungen ermöglicht.

Im nicht blockierenden Modus gibt ein asynchroner Speicher "E Pending" zurück, \_ Wenn Daten nicht verfügbar sind. Beim Empfang dieser Nachricht wartet der Client auf eine Benachrichtigung, dass zusätzliche Daten verfügbar sind, bevor erneut versucht wird, ihn herunterzuladen.

Im Blockierungs Modus \_ blockiert der asynchrone Speicher den aufzurufenden, bis neue Daten verfügbar sind, und gibt die neuen Daten zurück. Der Client muss bereit sein, die Daten zu empfangen. Während der Thread blockiert wird, sind Daten, die bereits an den Client übermittelt wurden, dem Benutzer vollständig verfügbar.

Der Blockierungs Modus ist erforderlich, da Clients, die den asynchronen Speicher nicht kennen \_ , E ausstehend nicht erkennen und davon ausgehen, dass ein nicht BEHEB barer Fehler aufgetreten ist. Durch das Blockieren des asynchronen Speichers können vorhandene Clients progressives Rendering durchführen.

 

 