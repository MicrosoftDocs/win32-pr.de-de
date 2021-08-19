---
description: Ein Administrator kann erzwingen, dass eine Clientanwendung immer dieselbe Kopie eines Nicht-COM-Servers in einem vorhandenen Paket&8212; verwendet, ohne dass sich dies auf andere Anwendungen \#&8212; ausdrungen hat, indem eine isolierte Komponentenbeziehung zwischen Server und Client angegeben \# wird.
ms.assetid: e10d7942-b13c-46a3-a8ca-cb7bc021c76b
title: Privates Verwenden einer Nicht-COM-Komponente in einem vorhandenen Paket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0082d89ca6e921213bb462d1b858154419bef416ffa263b8b63ca6d98660fe7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945614"
---
# <a name="make-a-non-com-component-in-an-existing-package-private"></a>Privates Verwenden einer Nicht-COM-Komponente in einem vorhandenen Paket

Ein Administrator kann erzwingen, dass eine Clientanwendung immer dieselbe Kopie eines Nicht-COM-Servers in [](isolated-components.md) einem vorhandenen Paket verwendet , ohne dass sich dies auf andere Anwendungen ausdrungen hat, indem er eine Isolierte Komponentenbeziehung zwischen server und client anknt. Dadurch wird eine private Kopie der Serverkomponente an einem Speicherort installiert, der ausschließlich von der Clientanwendung verwendet wird. Der Administrator muss Transformationen oder ein Paketerstellungstool verwenden, um Folgendes zu tun:

-   Legen Sie die Server-DLL und den .exe-Client in separaten Komponenten ab.
-   Geben Sie in der [Tabelle IsolatedComponent](isolatedcomponent-table.md) einen Datensatz mit der Clientkomponente in der Spalte Freigegebene Komponente und der Clientanwendung \_ in der Spalte \_ Komponentenanwendung ein. Schließen Sie [die Aktion IsolateComponents](isolatecomponents-action.md) in die Sequenztabellen ein.
-   Legen Sie **das Bit msidbComponentAttributesSharedDllRefCount** im Komponententabellendatensatz für Freigegebene Komponente [](component-table.md) \_ fest. Das Installationsprogramm erfordert diese globale Refcount am freigegebenen Speicherort, um die freigegebenen Dateien und die Registrierung in Fällen zu schützen, in denen die Freigabe mit anderen Installationstechnologien besteht.

 

 



