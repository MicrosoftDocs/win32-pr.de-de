---
description: Um zu erzwingen, dass eine com-Client Anwendung immer dieselbe Kopie eines COM-Servers verwendet, erstellen Sie das Installationspaket der Anwendung, um eine isolierte Komponenten Beziehung zwischen dem com-Server und dem Client anzugeben.
ms.assetid: 387c1c4d-16f5-4f46-b868-c2be7cb3f942
title: Installieren einer COM-Komponente an einem privaten Speicherort
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838b3f40c513fd0998402893543e88526e4a6d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863283"
---
# <a name="installing-a-com-component-to-a-private-location"></a>Installieren einer COM-Komponente an einem privaten Speicherort

Um zu erzwingen, dass eine com-Client Anwendung immer dieselbe Kopie eines COM-Servers verwendet, erstellen Sie das Installationspaket der Anwendung, um eine [isolierte Komponenten](isolated-components.md) Beziehung zwischen dem com-Server und dem Client anzugeben. Dadurch wird eine private Kopie der com-Serverkomponente an einem Speicherort installiert, der ausschließlich von der Client Anwendung verwendet wird. Gehen Sie beim Erstellen des Pakets wie folgt vor:

-   Platzieren Sie die com-Server-DLL und den exe-Client in separaten Komponenten.
-   Geben Sie einen Datensatz in der [isolatedcomponent-Tabelle](isolatedcomponent-table.md) mit der com-Client-Komponente in der frei \_ gegebenen Komponenten Spalte und der Client Anwendung in der \_ Spalte Komponenten Anwendung ein. Schließen Sie die [isolatecomponents-Aktion](isolatecomponents-action.md) in die Sequenz Tabellen ein.
-   Legen Sie das msidbcomponentattributesshareddllrefcount-Bit im [Komponenten Tabellen](component-table.md) Daten Satz für die freigegebene Komponente fest \_ . Das Installationsprogramm erfordert diesen globalen refcount am freigegebenen Speicherort, um die freigegebenen Dateien und die Registrierung in Fällen zu schützen, in denen die Freigabe mit anderen Installationstechnologien erfolgt.

 

 



