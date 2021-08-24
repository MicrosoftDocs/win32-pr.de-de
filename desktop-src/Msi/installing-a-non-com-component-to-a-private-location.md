---
description: Um zu erzwingen, dass eine Clientanwendung immer die gleiche Kopie eines Nicht-COM-Servers verwendet, erstellen Sie das Installationspaket der Anwendung, um eine Beziehung zwischen isolierten Komponenten zwischen Server und Client anzugeben.
ms.assetid: 3ca9cad7-6848-4483-b5e3-2b7bbdefe605
title: Installieren einer Nicht-COM-Komponente an einem privaten Speicherort
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d8b835b5b0d734caaf5b5b20d062cd540510776371f72e7019efdc72e12cf7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119295440"
---
# <a name="installing-a-non-com-component-to-a-private-location"></a>Installieren einer Nicht-COM-Komponente an einem privaten Speicherort

Um zu erzwingen, dass eine Clientanwendung immer die gleiche Kopie eines Nicht-COM-Servers verwendet, erstellen Sie das Installationspaket der Anwendung, um eine Beziehung zwischen [isolierten Komponenten](isolated-components.md) zwischen Server und Client anzugeben. Dadurch wird eine private Kopie der Serverkomponente an einem Speicherort installiert, der ausschließlich von der Clientanwendung verwendet wird. Gehen Sie beim Erstellen des Pakets wie folgt vor:

-   Legen Sie die Server-DLL und den .exe-Client in separate Komponenten ab.
-   Geben Sie in der [Tabelle IsolatedComponent](isolatedcomponent-table.md) einen Datensatz mit der Clientkomponente in der \_ Spalte Komponenten freigegeben und der Clientanwendung in der \_ Spalte Komponentenanwendung ein. Schließen Sie die [IsolateComponents-Aktion](isolatecomponents-action.md) in die Sequenztabellen ein.
-   Legen Sie das Bit msidbComponentAttributesSharedDllRefCount im [Komponententabellendatensatz](component-table.md) für Component \_ Shared fest. Das Installationsprogramm erfordert diese globale Refcount-Anzahl am freigegebenen Speicherort, um die freigegebenen Dateien und die Registrierung in Fällen zu schützen, in denen eine Freigabe mit anderen Installationstechnologien erfolgt.
-   Vermeiden Sie das Erstellen eines freigegebenen registrierten Pfads für alle Komponenten.

 

 



