---
description: Ein Administrator kann erzwingen, dass eine COM-Clientanwendung immer die gleiche Kopie eines COM-Servers in einem vorhandenen Paket&\# 8212 verwendet, ohne dass sich dies auf andere Anwendungen&\# 8212 auswirkt, indem er eine Beziehung zwischen isolierten Komponenten zwischen dem COM-Server und dem Client angibt.
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

Ein Administrator kann erzwingen, dass eine COM-Clientanwendung immer die gleiche Kopie eines COM-Servers in einem vorhandenen Paket verwendet , ohne dass sich dies auf andere Anwendungen auswirkt, indem er eine Beziehung zwischen [isolierten Komponenten](isolated-components.md) zwischen dem COM-Server und dem Client angibt. Dadurch wird eine private Kopie der COM-Serverkomponente an einem Speicherort installiert, der ausschließlich von der Clientanwendung verwendet wird. Der Administrator muss Transformationen oder ein Paketerstellungstool verwenden, um folgende Schritte ausführen zu können:

-   Legen Sie die COM-Server-DLL und den .exe-Client in separate Komponenten ein.
-   Geben Sie in der [Tabelle IsolatedComponent](isolatedcomponent-table.md) einen Datensatz mit der COM-Clientkomponente in der \_ Spalte Komponenten freigegeben und der Clientanwendung in der \_ Spalte Komponentenanwendung ein. Schließen Sie die [IsolateComponents-Aktion](isolatecomponents-action.md) in die Sequenztabellen ein.
-   Legen Sie das Bit **msidbComponentAttributesSharedDllRefCount** im [Komponententabellendatensatz](component-table.md) für Component \_ Shared fest. Das Installationsprogramm erfordert diese globale Refcount-Anzahl am freigegebenen Speicherort, um die freigegebenen Dateien und die Registrierung in Fällen zu schützen, in denen eine Freigabe mit anderen Installationstechnologien erfolgt.

 

 



