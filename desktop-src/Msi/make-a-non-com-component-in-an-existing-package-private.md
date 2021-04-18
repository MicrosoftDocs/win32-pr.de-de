---
description: Ein Administrator kann erzwingen, dass eine Client Anwendung immer dieselbe Kopie eines nicht-COM-Servers in einem vorhandenen Paket&8212, ohne dass sich dies auf \# andere Anwendungen auswirkt&\# 8212; durch Angeben einer isolierten Komponenten Beziehung zwischen dem Server und dem Client.
ms.assetid: e10d7942-b13c-46a3-a8ca-cb7bc021c76b
title: Erstellen einer nicht-COM-Komponente in einem vorhandenen Paket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d87a74a4f9fe7c3770100f78dd0fcd154772943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343727"
---
# <a name="make-a-non-com-component-in-an-existing-package-private"></a>Erstellen einer nicht-COM-Komponente in einem vorhandenen Paket

Ein Administrator kann erzwingen, dass eine Client Anwendung immer dieselbe Kopie eines nicht-COM-Servers in einem vorhandenen Paket verwendet – ohne Auswirkungen auf andere Anwendungen – indem eine [isolierte Komponenten](isolated-components.md) Beziehung zwischen dem Server und dem Client angegeben wird. Dadurch wird eine private Kopie der Serverkomponente an einem Speicherort installiert, der ausschließlich von der Client Anwendung verwendet wird. Der-Administrator muss mit Transformationen oder einem Paket Erstellungs Tool wie folgt vorgehen:

-   Platzieren Sie die Server-DLL und den exe-Client in separaten Komponenten.
-   Geben Sie einen Datensatz in der [isolatedcomponent-Tabelle](isolatedcomponent-table.md) mit der Client Komponente in der \_ Shared-Spalte der Komponente und der Client Anwendung in der Spalte Komponenten Anwendung ein \_ . Schließen Sie die [isolatecomponents-Aktion](isolatecomponents-action.md) in die Sequenz Tabellen ein.
-   Legen Sie das **msidbcomponentattributesshareddllrefcount** -Bit im [Komponenten Tabellen](component-table.md) Daten Satz für die freigegebene Komponente fest \_ . Das Installationsprogramm erfordert diesen globalen refcount am freigegebenen Speicherort, um die freigegebenen Dateien und die Registrierung in Fällen zu schützen, in denen die Freigabe mit anderen Installationstechnologien erfolgt.

 

 



