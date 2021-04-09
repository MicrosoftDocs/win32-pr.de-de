---
description: Um zu erzwingen, dass eine Client Anwendung immer dieselbe Kopie eines nicht-COM-Servers verwendet, erstellen Sie das Installationspaket der Anwendung, um eine isolierte Komponenten Beziehung zwischen dem Server und dem Client anzugeben.
ms.assetid: 3ca9cad7-6848-4483-b5e3-2b7bbdefe605
title: Installieren einer nicht-COM-Komponente an einem privaten Speicherort
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ea4e10e7a08fd008352a36feca537685ee4390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868879"
---
# <a name="installing-a-non-com-component-to-a-private-location"></a>Installieren einer nicht-COM-Komponente an einem privaten Speicherort

Um zu erzwingen, dass eine Client Anwendung immer dieselbe Kopie eines nicht-COM-Servers verwendet, erstellen Sie das Installationspaket der Anwendung, um eine [isolierte Komponenten](isolated-components.md) Beziehung zwischen dem Server und dem Client anzugeben. Dadurch wird eine private Kopie der Serverkomponente an einem Speicherort installiert, der ausschließlich von der Client Anwendung verwendet wird. Gehen Sie beim Erstellen des Pakets wie folgt vor:

-   Platzieren Sie die Server-DLL und den exe-Client in separaten Komponenten.
-   Geben Sie einen Datensatz in der [isolatedcomponent-Tabelle](isolatedcomponent-table.md) mit der Client Komponente in der \_ Shared-Spalte der Komponente und der Client Anwendung in der Spalte Komponenten Anwendung ein \_ . Schließen Sie die [isolatecomponents-Aktion](isolatecomponents-action.md) in die Sequenz Tabellen ein.
-   Legen Sie das msidbcomponentattributesshareddllrefcount-Bit im [Komponenten Tabellen](component-table.md) Daten Satz für die freigegebene Komponente fest \_ . Das Installationsprogramm erfordert diesen globalen refcount am freigegebenen Speicherort, um die freigegebenen Dateien und die Registrierung in Fällen zu schützen, in denen die Freigabe mit anderen Installationstechnologien erfolgt.
-   Vermeiden Sie das Erstellen eines gemeinsam genutzten, registrierten Pfads für Komponenten.

 

 



