---
title: Storage Modi
description: Asynchroner Speicher unterstützt zwei Speichermodi, die blockieren und nicht blockieren, die ein Client (entweder ein Browser oder das Objekt selbst) angeben kann, indem BINDF ASYNCSTORAGE aus dem Aufruf von \_ IBindStatusCallback GetBindInfo des Monikers zurückgegeben wird.
ms.assetid: df8f9e2c-40d2-4997-b5f9-bdbc524437cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db1a0a4c08daa1663f7513226dc25f4d5c8fd26341a6c8ee7d90a2ec0d1099db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661830"
---
# <a name="storage-modes"></a>Storage Modi

Asynchroner Speicher unterstützt zwei Speichermodi: blockierende und nicht blockierende Modi, die ein Client (entweder ein Browser oder das Objekt selbst) angeben kann, indem BINDF ASYNCSTORAGE aus dem Aufruf von \_ [**IBindStatusCallback::GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85))des Monikers zurückgegeben wird. Wenn ein Client BINDF ASYNCSTORAGE angibt, empfängt er einen Zeiger auf einen nicht \_ blockierenden asynchronen Speicher. Andernfalls wird ein Zeiger auf einen blockierenden asynchronen Speicher empfangen. Auch wenn der Client keinen asynchronen Bindungsvorgang anfordert (indem [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) nicht beim Bindungskontext registriert wird), gibt der Moniker weiterhin einen blockierenden asynchronen Speicher zurück, wodurch das progressive Laden für Legacyanwendungen ermöglicht wird.

Im Nichtblockierungsmodus gibt ein asynchroner Speicher E \_ PENDING zurück, wenn Daten nicht verfügbar sind. Beim Empfang dieser Nachricht wartet der Client auf eine Benachrichtigung, dass zusätzliche Daten verfügbar sind, bevor er erneut versucht, sie herunterzuladen.

Im Blockierungsmodus blockiert der asynchrone Speicher den Aufruf, bis neue Daten verfügbar sind, entsperrt den Aufruf und gibt die \_ neuen Daten zurück. Der Client muss bereit sein, die Daten zu empfangen. Während der Thread blockiert ist, stehen dem Benutzer bereits an den Client übergebene Daten vollständig zur Verfügung.

Der Blockierungsmodus ist erforderlich, da Clients, die den asynchronen Speicher nicht kennen, E PENDING nicht erkennen und davon ausgehen, dass ein nicht behebbarer \_ Fehler aufgetreten ist. Durch das Blockieren von asynchronem Speicher können vorhandene Clients progressives Rendering ausführen.

 

 