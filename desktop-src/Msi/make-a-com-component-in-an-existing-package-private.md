---
description: Ein Administrator kann erzwingen, dass eine COM-Clientanwendung immer dieselbe Kopie eines COM-Servers in einem vorhandenen Paket&8212; verwendet, ohne dass sich dies auf andere Anwendungen&8212; ausdrungen hat, indem er eine Isolierte Komponentenbeziehung zwischen dem COM-Server und dem Client \# \# ankämmt.
ms.assetid: 814eca94-2bb5-4aff-8de3-473da71d4400
title: Erstellen einer COM-Komponente in einem vorhandenen Paket als privat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5119e2d9417f51bb815fe9c76cd47be496e4c03cab81e4e0ccd2b7c49c7b8b63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629031"
---
# <a name="make-a-com-component-in-an-existing-package-private"></a>Erstellen einer COM-Komponente in einem vorhandenen Paket als privat

Ein Administrator kann erzwingen, dass eine COM-Clientanwendung immer dieselbe Kopie eines COM-Servers in einem [](isolated-components.md) vorhandenen Paket verwendet – ohne Auswirkungen auf andere Anwendungen – indem er eine Isolierte Komponentenbeziehung zwischen COM-Server und -Client ankämmt. Dadurch wird eine private Kopie der COM-Serverkomponente an einem Speicherort installiert, der ausschließlich von der Clientanwendung verwendet wird. Der Administrator muss Transformationen oder ein Paketerstellungstool verwenden, um Folgendes zu tun:

-   Legen Sie die COM-Server-DLL und den .exe-Client in separaten Komponenten ab.
-   Geben Sie in der [Tabelle IsolatedComponent](isolatedcomponent-table.md) einen Datensatz mit der COM-Clientkomponente in der Spalte Freigegebene Komponente und der Clientanwendung \_ in der Spalte \_ Komponentenanwendung ein. Schließen Sie [die Aktion IsolateComponents](isolatecomponents-action.md) in die Sequenztabellen ein.
-   Legen Sie **das Bit msidbComponentAttributesSharedDllRefCount** im Komponententabellendatensatz für Freigegebene Komponente [](component-table.md) \_ fest. Das Installationsprogramm erfordert diese globale Refcount am freigegebenen Speicherort, um die freigegebenen Dateien und die Registrierung in Fällen zu schützen, in denen die Freigabe mit anderen Installationstechnologien besteht.

 

 



