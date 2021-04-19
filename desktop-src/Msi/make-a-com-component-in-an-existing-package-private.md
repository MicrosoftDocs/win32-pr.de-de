---
description: Ein Administrator kann erzwingen, dass eine com-Client Anwendung immer dieselbe Kopie eines COM-Servers in einem vorhandenen Paket&8212, ohne dass sich dies auf \# andere Anwendungen auswirkt&\# 8212; durch Angeben einer isolierten Komponenten Beziehung zwischen dem com-Server und dem Client.
ms.assetid: 814eca94-2bb5-4aff-8de3-473da71d4400
title: Erstellen einer COM-Komponente in einem vorhandenen Paket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4935d20c5034af81a52c18d35454553b04cfb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363303"
---
# <a name="make-a-com-component-in-an-existing-package-private"></a>Erstellen einer COM-Komponente in einem vorhandenen Paket

Ein Administrator kann erzwingen, dass eine com-Client Anwendung immer dieselbe Kopie eines COM-Servers in einem vorhandenen Paket verwendet – ohne dass sich dies auf andere Anwendungen auswirkt – indem eine [isolierte Komponenten](isolated-components.md) Beziehung zwischen dem com-Server und dem Client angegeben wird. Dadurch wird eine private Kopie der com-Serverkomponente an einem Speicherort installiert, der ausschließlich von der Client Anwendung verwendet wird. Der-Administrator muss mit Transformationen oder einem Paket Erstellungs Tool wie folgt vorgehen:

-   Platzieren Sie die com-Server-DLL und den exe-Client in separaten Komponenten.
-   Geben Sie einen Datensatz in der [isolatedcomponent-Tabelle](isolatedcomponent-table.md) mit der com-Client-Komponente in der frei \_ gegebenen Komponenten Spalte und der Client Anwendung in der \_ Spalte Komponenten Anwendung ein. Schließen Sie die [isolatecomponents-Aktion](isolatecomponents-action.md) in die Sequenz Tabellen ein.
-   Legen Sie das **msidbcomponentattributesshareddllrefcount** -Bit im [Komponenten Tabellen](component-table.md) Daten Satz für die freigegebene Komponente fest \_ . Das Installationsprogramm erfordert diesen globalen refcount am freigegebenen Speicherort, um die freigegebenen Dateien und die Registrierung in Fällen zu schützen, in denen die Freigabe mit anderen Installationstechnologien erfolgt.

 

 



